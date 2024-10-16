<!--
author:   Sebastian Zug, Karl Fessel & Andrè Dietrich
email:    sebastian.zug@informatik.tu-freiberg.de

version:  1.0.2
language: de
narrator: Deutsch Female

import:  https://raw.githubusercontent.com/liascript-templates/plantUML/master/README.md
         https://github.com/LiaTemplates/AVR8js/main/README.md
         https://github.com/LiaTemplates/Pyodide

icon: https://upload.wikimedia.org/wikipedia/commons/d/de/Logo_TU_Bergakademie_Freiberg.svg

link:    https://fonts.googleapis.com
         https://fonts.gstatic.com
         https://fonts.googleapis.com/css2?family=Noto+Sans+Cuneiform&display=swap
-->


[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://github.com/TUBAF-IfI-LiaScript/VL_DigitaleSysteme/main/lectures/07_RTOS_Konzepte.md#1)


# Scheduling

| Parameter                | Kursinformationen                                                                                                                                                                                    |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Veranstaltung:**       | `Vorlesung Digitale Systeme`                                                                                                                                                                         |
| **Semester**             | `Sommersemester 2022`                                                                                                                                                                                |
| **Hochschule:**          | `Technische Universität Freiberg`                                                                                                                                                                    |
| **Inhalte:**             | `Konzepte eingebetteter Betriebssysteme`                                                                                                                                                             |
| **Link auf den GitHub:** | [https://github.com/TUBAF-IfI-LiaScript/VL_DigitaleSysteme/blob/main/lectures/07_RTOS_Konzepte.md](https://github.com/TUBAF-IfI-LiaScript/VL_DigitaleSysteme/blob/main/lectures/07_RTOS_Konzepte.md) |
| **Autoren**              | @author                                                                                                                                                                                              |

![](https://media.giphy.com/media/26gR2qGRnxxXAvhBu/giphy.gif)

---

## Ausgangspunkt und Begriffe

Nehmen wir an, dass wir ein autonom fahrendes Fahrzeug allein mit einem zentralen Rechner betreiben wollen. Welche Aufgaben müssen dabei abgedeckt werden und welche zeitlichen Eigenschaften sind dabei zu berücksichtigen?

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
                                          zeitliche Toleranz
                        gering                                            hoch
                        "$\mu s$                                            _s_
                        +-----------------------------------------------------+
aperiodische Aufgaben   ||        x                x                   x     ||
                        ||      Notfall-         Automatisches       Klima-  ||
                        ||      bremsasisstent   Fernlicht           anlage  ||
                        ||                                                   ||
periodische Aufgaben    ||   x                  x                      X     ||
                        || Motorsteuerung     Abstands-              GNSS    ||
                        ||                    regelung               messung ||
                        +-----------------------------------------------------+   .
```

Entsprechend gilt es eine beschränkte Zahl von Ressourcen auf eine Vielzahl von Aufgaben unterschiedlicher Priorität abzubilden.

> **Merke:**  Echtzeitbetrieb nach DIN 44300 … Ein Betrieb eines Rechensystems, bei dem Programme zur Verarbeitung anfallender Daten ständig betriebsbereit sind, derart, dass die Verarbeitungsergebnisse innerhalb einer vorgegebenen Zeitspanne verfügbar sind. Die Daten können je nach Anwendungsfall nach einer zeitlich zufälligen Verteilung oder zu vorherbestimmten Zeitpunkten anfallen.


$$
r + \Delta e \leq d
$$


Die Endzeit $d$ wird durch die Bereitzeit $r$ und die Zeitdauer der Ausführung $\Delta e$ unterschritten.

+ _Harte Echtzeit_ (Rechtzeitigkeit - timeliness) 	= die Abarbeitung einer Anwendung wird innerhalb eines bestimmten Zeithorizontes umgesetzt

+ _Weiche Echtzeit_ = es genügt, die Zeitbedingungen für den überwiegenden Teil der Fälle zu erfüllen, geringfügige Überschreitungen der Zeitbedingungen sind erlaubt

## Intuitive Lösung - Nanokernel

Echtzeitimplementierung als „nanokernel“

+ Ausrichtung an einer minimalen festen Periode $p$
+ Evaluation des Laufzeitverhaltens aller Tasks zwingend notwendig
+ keine Schutzfunktionen des Speichers
+ Polling als einzige Zugriffsfunktion auf die Hardware

```c
switch off interrupts
setup timer
c = 0;
while (1) {
   suspend until timer expires
   c++;
   Task0();    //do tasks due every cycle
   if (((c+0) % 2) == 0)
      Task1(); //do tasks due every 2nd cycle
   if (((c+1) % 3) == 0)
      Task2(); //do tasks due every 3rd cycle, with phase 1
...
}
```

         {{1-2}}
| Vorteile                                     | Nachteile                                     |
| -------------------------------------------- | --------------------------------------------- |
| + Einfache Umsetzbarkeit auf Mikrocontroller | - keine Prioritäten                           |
| + Vereinfachter Hardwarezugriff              | - keine Adaption zur Laufzeit                 |
|                                              | - keine Interrupts / Unterbrechung            |
|                                              | -  beschränkte Wiederverwendbarkeit des Codes |
|                                              | - implizite Zeitannahmen                      |

         {{1-2}}
> **Wir benötigen ein systematisches Scheduling, dass eine variable Auswahl der Tasks zulässt!**

## Scheduling Grundlagen

![alt-text](https://media.giphy.com/media/USgYEZKM6NqIZlW8vE/giphy.gif)

### Taskmodel

Eine Task ist die Ausführung eines sequentiellen Programms auf einem Prozessor in seiner spezifischen Umgebung (Kontext). Eine Task...

+ erfüllt eine von Programm spezifizierte Aufgabe
+ ist Träger der Aktivität = Abstraktion der Rechenzeit die kleinste planbare Einheit

```text @plantUML.png
@startuml
hide empty description
[*] -[#0000FF]-> ready : generate
waiting --> ready : release
ready --> running : start
running --> ready  : preempt
running --> waiting  : wait
running --> suspended  : terminate
suspended --> ready  : activate
suspended --> [*]  : deleted
@enduml
```


| Zustand     | Bedeutung                                                                                                                                                                                            |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _waiting_   |                                                                                                                                                                                                      |
| _ready_     | Der Scheduler wählt aus der Liste der Tasks denjenigen lauffähigen Prozess als nächstes zur Bearbeitung aus, der die höchste Priorität hat. Mehrere Tasks können sich im Zustand _ready_ befinden. |
| _running_   |    In einem Ein-Prozessorsystem kann immer nur ein Task aktiv sein. Er bekommt die die CPU zugeteilt und wird ausgeführt, bis er entweder (1) sich selbst beendet (in den Zustand _suspended_) versetzt, (2) auf ein Betriebsmittel warten muss (z.B. auf das Ende eine I/O-Aufrufes), oder (3) nicht mehr die höchste Priorität hat, da beispielsweise die Wartebedingung eines höherprioren Prozesses erfüllt wurde.                                                                                                                                                                                                 |
| _suspended_ |         Ein Task wird in den Zustand _suspended_ versetzt, wenn nicht mehr alle Bedingungen zur direkten Ausführung erfüllt sind. Ein Task kann dabei auf unterschiedliche Bedingungen warten, beispielsweise auf das Ende von I/O-Aufrufen, auf den Ablauf einer definierten Zeitspanne oder auf das Freiwerden sonstiger Betriebsmittel.                                                                                                                                                                                               |

> **Aufgabe:** Grenzen Sie den Taskbegriff von Prozessen und Threads ab.

### Charakterisierung von Tasks

1. **Zeitverhalten**

_Periodische Tasks_ ... werden mit einer bestimmten Frequenz $f$ regelmäßig aktiviert.

- Durchlaufen einer Regelschleife
- Pollendes Abfragen eines Sensors

_Aperiodische Tasks_ ... lassen sich  nicht auf ein zeitlich wiederkehrendes Muster abbilden.

- Tastendruck auf einem Bedienfeld
- Freefall-Detektion

_Sporadische Tasks_ ... treten nicht regulär auf. Man nimmt aber eine obere Schranke bzgl. der Häufigkeit ihres Aufrufs an.

- Fahrradtacho (obere Schranke = Geschwindigkeit)
- Anfragen auf einer Kommunikationsschnittstelle


---

          {{1-3}}
*****************************************************************************

2. **Abhängigkeiten**

_unabhängige Tasks_  ... können in jeder beliebigen Reihenfolge ausgeführt werden
_abhängige Tasks_ ... werden durch Vorgänger-Relationen beschrieben und in einem Precedencegraphen dargestellt

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
                           Auslesen des
                             Sensors
                                |
              +-----------------+-----------------+
              |                 |                 |     
              v                 v                 v
          Ausreißer           Offset          Rauschen
         detektieren         erkennen         filtern
              |                 |                 |
              +--------+--------+                 |
                       |                          |
                       v                          v
               Validitätsberechnung           Messungen
         .        realisieren               linearisieren
                       |                          |
                       +--------------+-----------+
                                      |
                                      v
                                  Datenset
                                kommmunizieren                                 .
```

*****************************************************************************


---

          {{2-3}}
*****************************************************************************

3. **Unterbrechbarkeit**

![alt-text](../images/07_Scheduling/PreemptiveTaskScheduling.png "Unterbrechung einer Taskausführung beim Bereitwerden höherpriorer Tasks")

*****************************************************************************

###  Taskparameter

**Singuläre Tasks**

| Parameter    | Bedeutung                                |
| ------------ | ---------------------------------------- |
| $T$          | Tasktyp (Abfragen des Temperaturfühlers) |
| $T_i$        | i-te Instanz des Tasktyp (Taskobjekt)    |
| $r_i$        | Bereitzeit (ready time)                  |
| $\Delta e_i$ | Ausführungszeit (execution time)         |
| $s_i$        | Startzeit (starting time)                |
| $c_i$        | Abschlusszeit (completion time)          |
| $d_i$        | First (deadline)                         |


  <!--
  style="width: 80%; min-width: 420px; max-width: 720px;"
  -->
```ascii

   "$r_i$"    "$s_i$"      "$c_i$"   "$d_i$"
               +-------------+
  ----|--------|             |---------|------>
               +-------------+                       
                    "$\Delta e_i$"      

      |<--------------------->|
            "$\Delta t_i$"                                                     .
```

**Periodische Tasks**

| Parameter      | Bedeutung                                                  |
| -------------- | ---------------------------------------------------------- |
| $T_{ij}$       | j-te Ausführung der i-ten Instanz des Tasktyp (Taskobjekt) |
| $r^j_i$        | Bereitzeit (ready time)                                    |
| $\Delta e_i$   | Ausführungszeit (execution time)                           |
| $s^j_i$        | Startzeit (starting time)                                  |
| $c^j_i$        | Abschlusszeit (completion time)                            |
| $d^j_i$        | First (deadline)                                           |
| $\Delta p^j_i$ | Zeitspanne zwischen den Startzeiten (Jitter)               |

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
                      "$p^j_i$"                            "$p^{j+1}_i$"
    |<------------------------------------------>|<-----------------------

 "$r^j_i$" "$s^j_i$"      "$c^j_i$" "$d^j_i$"    "$r^{j+1}_i$" "$s^{j+1}_i$"
             +-------------+                                     +------        
----|--------|             |---------|-----------|---------------|
             +-------------+                                     +------      
                  "$\Delta e_i$"             
                                "$\Delta p^j_i$"                 
             <-------------------------------------------------->              .
```

###  Herausforderung Ausführungsdauer  $\Delta e_i$

Die Ausführungsdauer einer Programmsequenz wird durch

- die Programmlogik (Kontrollflussgraph),
- die Eingabedaten (Auswirkungen auf Schleifendurchlaufzahlen etc.),
- den Compiler (Optimierungsstufe) und
- die Architektur und Taktfrequenz des Ausführungsrechners (Cache- und Pipelining-Effekten)

bestimmt. Da einzelne Aspekte stochastisch verteilt sind, können keine präzisen Aussagen zur Verarbeitungsdauer getroffen werden.

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
                        beobachtete Schwankung
  "$s_i$"                der Ausführungszeit
     +---------------------+-------------+
-----|                     |XXXXXXXXXXXXX|------------>
     +---------------------+-------------+                              

                  BCET   |<--------------------->|   WCET
                               tatsächliche
                            Ausführungsbandbreite                              .   
```

Der Lösungsansatz besteht darin mit Hilfe eines entsprechenden Puffers eine untere und obere Schranke zu definieren, die das maximal mögliche Laufverhalten erfasst.

> _BCET_ ... Best Case Execution Time
>
> _WCET_ ... Worst Case Execution Time


Mögliche Messverfahren sind:

- die Erfassung von oszillierenden Pins
- das automatische Abzählen im Assembler Code  
- die Schätzung auf höherabstrakter Codeebene (grafische Modellierungstools)

![alt-text](../images/07_Scheduling/AblaufMasterarbeitWolf.png "Ablauf der Vorhersage des Laufzeitverhaltens von Simulink Modellen (Quelle Masterarbeit Markus Wolf)")

Ergebnis im Vergleich der Periodendauer von unterschiedlichen Modellen auf einem [PPC750GL](http://datasheets.chipdb.org/IBM/PowerPC/7xx/PowerPC-740-750.pdf)

| Modellgröße | Schätzung | Laufzeitmessung | Differenz |
| ----------- | --------- | --------------- | --------- |
| 160         | 10818     | 9816            | 10,2%     |
| 366         | 1762      | 1583            | 11,4%     |
| 756         | 13721     | 14946           | -8,2%     |


### Scheduling als NP Vollständiges Problem

Allgemeine Formulierung des Schedulingproblems:

Gegeben seien:

- eine Menge von Tasks 		$T= {T_1, T_2, ..., T_n }$
- eine Menge von Prozessoren 	$P= {P_1, P_2, ..., P_m }$
- eine Menge von Ressourcen	$R= {R_1, R_2, ..., R_s }$

Scheduling bedeutet die Zuordnung von Prozessoren und Ressourcen zu Tasks, so dass alle  für individuelle Tasks definierten Beschränkungen eingehalten werden.

> **Merke:** In seiner allgemeinen Form ist das Scheduling-Problem NP-vollständig. Dabei gelten folgende Annahmen:
>
> - gleiche Bereitzeiten aller Tasks,
> - keine Abhängigkeiten,
> - nur feste Prioritäten, ...

Dafür lassen sich unterschiedliche Optimierungskriterien definieren:

- Mittlere Antwortzeit $t_r = 1/n \sum_{(i=1, ..., n)} (c_i -r_i )$
- Maximale Zeit bis zum Abschluss $t_c =max(c_i - r_i)$
- Maximale Auslastung des Systems $r = \sum_{(i=1, ..., n)} \Delta e_i / t$
- ...

Diese Metriken sind auf Nicht-Echtzeitscheduling ausgerichtet und können nicht übernommen werden weil:

- keine Deadlines und
- keine unterschiedlichen Prioritäten der Tasks (Fairness) berücksichtigt werden
- Kurze Reaktionszeiten genügen nicht, Zeiten müssen garantiert sein
- keine weiteren Parameter wie Periodizität oder Abhängigkeiten abgebildet werden

> **Merke:** Echtzeit braucht die Evaluation der Deadlines. Entsprechend muss für die Latency gelten $L_{max} = 0$

Weiche Echtzeitkriterien lassen eine Abweichung von dieser Vorgabe zu:

> Maximale Zahl von verspäteten Tasks

> Maximale Verspätung $L_{max} = max(c_i-d_i)$

Bereitzeit für alle Tasks $T_1 - T_5$ = 0

**Optimierung hinsichtlich der maximalen Verzögerung**

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
Task 5                                                  ####~~~~~~~
     4                                   ########~~~~~~~
     3                           ####~~~~
     2                   ####~~~~              ## Ausführung innerhalb Deadline
     1   ########--------                      ~~ Ausführung nach Deadline

        |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|>         .
        0   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15  
               "$d_1$"     "$d_2$" "$d_1$"    "$d_4$"      "$d_5$"
```

$L_{max} = L_1 = L_4 = L_5 = 2$, $N_{late} = 5$

**Optimierung hinsichtlich der Zahl der verzögerten Tasks**

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
Task 5                                  ############
     4                   ###############
     3           ########
     2   ########
     1          ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~###############

        |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|>
        0   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15  
               "$d_1$"     "$d_2$" "$d_1$"    "$d_4$"      "$d_5$"

                <------------------ "$N_{late}$" ------------------>           .
```

$L_{max} = L_1 = 13$, $N_{late} = 1$

### Einplanbarkeitsanalyse

1. **Korrekte Konfiguration der Tasks**

   Überlegung: Die Deadline muss hinreichend weit von der Startzeit entfernt sein

   $\Delta e_i \leq (d_i - r_i) \leq p_i$

   <!--
   style="width: 80%; min-width: 420px; max-width: 720px;"
   -->
   ```ascii
   "$r_2$"         "$r_1$" "$d_1$"                         "$d_2$"
    |---|---|---|---|---|---|---|---|---|---|---|---|---|---|-->                

    |-------------------|
           "$\Delta e_2$"
                     |--------------|
                          "$\Delta e_1$"                                         .
   ```


2. **Verfügbare (Prozessor-) Zeit**

Überlegung: Wir können nicht mehr Performance abfordern, als überhaupt vorhanden ist.

$\sum \Delta e_i \cdot f_i \leq P_{CPU}$

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii

   <------------------------- "$t$"---------------------->

  |---|---|---|---|---|---|---|---|---|---|---|---|---|---|-->                

  |---------------|-----------|    .....    |-------------|     
       "$\Delta e_2$" "$\Delta e_1$"             "$\Delta e_3$"      
```

3. **Überlappende Tasks**

Überlegung: Die letztmögliche Ausführungszeit zweier Tasks überlappt nicht.

$d_i \leq d_j - \Delta e_j$

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii


           "$\Delta e_m$"   "$\Delta e_l$"             "$\Delta e_k$"     

                      |---------------|               
      |-------------------|                           |-------|
"$r_m$"              "$r_l$"             "$r_k$"
  |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|-->        
                         "$d_m$"     "$d_l$"                 "$d_k$"
```

> Achtung: Das Scheitern des Tests schließt die Existenz eines gültigen Schedules nicht aus! In beiden nachfolgenden Fällen scheitert das Kriterium!

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
"$e_1=4, r_1=0, d_1= 6$"                                                      |-------|   
"$e_2=6, r_2=4, d_2=10$"                  |-----------------------|  
"$e_3=2, r_3=13, d_3=15$" |---------------|  

                          |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|-->      
                          0   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15      
                                                 "$d_1$"        "$d_2$"             "$d_3$"
```

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii
"$e_1=5, r_1=0, d_1= 6$"                                                      |-------|
"$e_2=6, r_2=4, d_2=10$"                  |-----------------------|  
"$e_3=2, r_3=13, d_3=15$" |-------------------|

                          |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|-->      
                          0   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15      
                                                 "$d_1$"        "$d_2$"             "$d_3$"
```


| Kriterium                                | Bedeutung                   | Aussage     |
| ---------------------------------------- | --------------------------- | ----------- |
| $e_i \leq (d_i - r_i) \leq p_i$          | notwendige Ausführungsdauer | notwendig   |
| $\sum \Delta e_i \cdot f_i \leq P_{CPU}$ | verfügbare Rechenzeit       | notwendig   |
| $d_i \leq d_j - e_j$                     | Überlappung                 | hinreichend |

Wann findet die Prüfung dieser Kriterien statt? Innerhalb unseres Taskmodell werden die Parametersets unmittelbar nach der Erzeugung untersucht.

```text @plantUML.png
@startuml
hide empty description
[*] -[#0000FF]-> ready : generate -> Evaluation
waiting --> ready : release
ready --> running : start
running --> ready  : preempt
running --> waiting  : wait
running --> suspended  : terminate
suspended --> ready  : activate
suspended --> [*]  : deleted
@enduml
```

### Klassifikation Scheduling Verfahren

𒀭𒆗𒀳𒀭𒁇𒀀𒈾𒀭𒀜𒋾𒀀𒇉𒈦𒄘𒃼𒀭𒅎𒀭𒀀𒇉𒀀𒌑𒋛𒀪𒀉𒁍𒁕𒀜𒋫𒀀𒈝𒀊𒁍𒀸𒅗𒇻𒈾𒀫𒀀𒈾𒆪𒀠𒁍𒌝𒀀𒇉𒌓𒄒𒉣𒀉𒋾𒀀𒊏𒀭𒌓𒀝𒆪𒌋𒀭𒆷𒈦𒇻𒀭𒆘𒀀𒁺𒀭𒀫𒌓𒀭𒈾𒀭𒇸𒀀𒉿𒈝𒀸 𒀭𒆗𒀳𒀭𒁇𒀀𒈾𒀭𒀜𒋾𒀀𒇉𒈦𒄘𒃼𒀭𒅎𒀭𒀀𒇉𒀀𒌑𒋛𒀪𒀉𒁍𒁕𒀜𒋫𒀀𒈝𒀊𒁍𒀸𒅗𒇻𒈾𒀫𒀀𒈾𒆪𒀠𒁍𒌝𒀀𒇉𒌓𒄒𒉣𒀉𒋾𒀀𒊏𒀭𒌓𒀝𒆪𒌋𒀭𒆷𒈦𒇻𒀭𒆘𒀀𒁺𒀭𒀫𒌓𒀭𒈾𒀭𒇸𒀀𒉿𒈝𒀸 𒀭𒆗𒀳𒀭𒁇𒀀𒈾𒀭𒀜𒋾𒀀𒇉𒈦𒄘𒃼𒀭𒅎𒀭𒀀𒇉𒀀𒌑𒋛𒀪𒀉𒁍𒁕𒀜𒋫𒀀𒈝𒀊𒁍𒀸𒅗𒇻𒈾𒀫𒀀𒈾𒆪𒀠𒁍𒌝𒀀𒇉𒌓𒄒𒉣𒀉𒋾𒀀𒊏𒀭𒌓𒀝𒆪𒌋𒀭𒆷𒈦𒇻𒀭𒆘𒀀𒁺𒀭𒀫𒌓𒀭𒈾𒀭𒇸𒀀𒉿𒈝𒀸 𒀭𒆗𒀳𒀭𒁇𒀀𒈾𒀭𒀜𒋾𒀀𒇉𒈦𒄘𒃼𒀭𒅎𒀭𒀀𒇉𒀀𒌑𒋛𒀪𒀉𒁍𒁕𒀜𒋫𒀀𒈝𒀊𒁍𒀸𒅗𒇻𒈾𒀫𒀀𒈾𒆪𒀠𒁍𒌝𒀀𒇉𒌓𒄒𒉣𒀉𒋾𒀀𒊏𒀭𒌓𒀝𒆪𒌋𒀭𒆷𒈦𒇻𒀭𒆘𒀀𒁺𒀭𒀫𒌓𒀭𒈾𒀭𒇸𒀀𒉿𒈝𒀸 

Statische Verfahren (offline-scheduling):

- Analyse der Durchführbarkeit zur Entwicklungszeit
- Fester Plan, wann welche Task beginnt (Task-Beschreibungs-Liste, TDL)
- Planung für periodische Tasks basierend auf Superperiode
- unflexibel gegenüber Änderungen
- maximale Auslastung stets erreichbar
- kaum Aufwand zur Laufzeit

<!-- data-type="none" -->
| Zeit | Aktion    | WCET |
| ---- | --------- | ---- |
| 10   | starte T1 | 16   |
| 15   | sende M5  |      |
| 26   | stoppe T1 |      |
| 33   | starte T2 | 37   |
| ...  |           |      |

Nicht adaptive Verfahren

- Offline Analyse der Task-Laufzeit
- Online Berechnung von Scheduling-Plänen mit festen Prioritäten

Adaptive Verfahren

-  Online Analyse der Task-Laufzeit; Schätzung der Ausführungszeit
-  Online Erstellung des Plans unter variabler Priorisierung
-  Fehlertoleranz notwendig, da keine Garantie gegeben werden kann

## Zusammenfassung
<!--
@harte_Echtzeit: [harte Echtzeit](https://de.wikipedia.org/wiki/Echtzeit)
-->

<!--
style="width: 80%; min-width: 420px; max-width: 720px;"
-->
```ascii

                      +------------------+--------------------+
Anforderungen der     | "@harte_Echtzeit"| weiche Echtzeit    |
Anwendungen           +------------------+--------------------+

                      +---------------------------------------+
                      | synchron bereit  | asynchron bereit   |
                      +---------------------------------------+
                      | periodisch | aperiodisch | sporadisch |
Taskmodell            +---------------------------------------+
                      | präemptiv        | nicht-präemtiv     |
                      +---------------------------------------+
                      | unabhängig       | abhängig           |
                      +---------------------------------------+

                      +---------------------------------------+
Scheduler             |statisch          | dynamisch          |
                      +---------------------------------------+
```

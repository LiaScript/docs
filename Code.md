# Language Mappings

This document contains a list of mappings for language identifiers for
[`highlight.js`](https://highlightjs.org), which is mostly used in Markdown
parsers, and [`ace`](https://ace.c9.io), which is applied by LiaScript. Since
both projects do not contain all languages and the names of the language
identfiers might vary, we provide a mapping.


> All language identifiers and alias marked as `code` can be used within
> LiaScript code-blocks. If you want to apply another language not yet supported,
> then `plaintext` will be used as a default.

This mapping is applied by LiaScript at:

https://github.com/LiaScript/LiaScript/blob/development/src/typescript/webcomponents/editor-modes.ts

... and will be updated in accordace with this document. Feel free to make
comments/issues or to add other mappings.



| highlight.js        | alias                                                                      | language                                                                                       | category   | cloud9/ace           |
| ------------------- | -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------- | -------------------- |
| 1c                  |                                                                            | 1C:Enterprise                                                                                  | enterprise |                      |
| 4d                  |                                                                            |                                                                                                |            |                      |
| `abap`              | `sap-abap`                                                                 | [ABAB (Advanced Business Application Programming)](https://en.wikipedia.org/wiki/ABAP)         | enterprise | `abap`               |
|                     |                                                                            | [ABC](https://homepages.cwi.nl/~steven/abc/programmers/handbook.html)                          | common     | `abc`                |
| abnf                |                                                                            | [Augmented Backus-Naur Form](https://tools.ietf.org/html/rfc5234)                              |            |                      |
| accesslog           |                                                                            | [Apache Access Log](https://httpd.apache.org/docs/2.4/logs.html#accesslog)                     | logs       |                      |
| `actionscript`      | `as`                                                                       | ActionScript                                                                                   | scripting  | `actionscript`       |
| `ada`               |                                                                            | Ada                                                                                            |            | `ada`                |
| `alan`              | `i`, `ln`                                                                  | Alan IF                                                                                        |            |                      |
|                     |                                                                            | [Alda](https://alda.io)                                                                        | music      | `alda`               |
| `angelscript`       | `asc`                                                                      | [AngelScript](https://www.angelcode.com/angelscript)                                           | scripting  | `c_cpp`              |
| `apache`            | `apacheconf`                                                               | [Apache config](https://httpd.apache.org)                                                      | config     | `apache_conf`        |
|                     |                                                                            | [APEX](https://www.guru99.com/apex-tutorial.html)                                              | enterprise | `apex`               |
| `applescript`       | `osascript`                                                                | [AppleScript](https://en.wikipedia.org/wiki/AppleScript)                                       | scripting  | `applescript`        |
|                     |                                                                            | [AQL (ArangoDB Query Language)](https://www.arangodb.com/docs/stable/aql)                      |            | `aql`                |
| arcade              |                                                                            | [ArcGIS Arcade](https://developers.arcgis.com/arcade)                                          | scripting  |                      |
| `arduino`           | `ino`                                                                      | [Arduino](https://www.arduino.cc)                                                              |            | `c_cpp`              |
| `armasm`            | `arm`                                                                      | ARM Assembly                                                                                   | assembler  | `assembly_x86`       |
|                     |                                                                            | [ASL (ACPI Source Language)](https://acpica.org/sites/acpica/files/asl_tutorial_v20190625.pdf) |            | `asl`                |
| `asciidoc`          | `adoc`                                                                     | [AsciiDoc](http://asciidoc.org)                                                                | markup     | `asciidoc`           |
| `aspectj`           |                                                                            | [AspectJ](https://www.eclipse.org/aspectj)                                                     |            | `java`               |
| `autohotkey`        | `ahk`                                                                      | AutoHotkey                                                                                     | scripting  | `autohotkey`         |
| autoit              |                                                                            | AutoIt                                                                                         | scripting  |                      |
| `avrasm`            | `asm`                                                                      | AVR Assembly                                                                                   | assembler  | `assembly_x86`       |
| awk                 | `mawk`, `nawk`, `gawk`                                                     | [Awk](https://www.gnu.org/software/gawk/manual/gawk.html)                                      |            |                      |
| axapta              |                                                                            | [Microsoft X++](https://dynamics.microsoft.com/en-us/ax-overview/)                             | enterprise |                      |
| `bash`              | `sh`, `zsh`                                                                | [Bash](https://www.gnu.org/software/bash)                                                      | common     | `sh`                 |
| `basic`             |                                                                            | [BASIC](https://en.wikipedia.org/wiki/Tandy_1000)                                              |            | `vbscript`           |
| `bbcode`            |                                                                            | BBCode                                                                                         |            |                      |
| bnf                 |                                                                            | [Backus–Naur Form](https://en.wikipedia.org/wiki/Backus–Naur_form)                             |            |                      |
| brainfuck           | bf                                                                         | [Brainfuck](https://esolangs.org/wiki/Brainfuck)                                               | esoteric   |                      |
| `c`                 | `h`                                                                        | C                                                                                              | system     | `c_cpp`              |
|                     |                                                                            |                                                                                                |            | `c9search`           |
| cal                 |                                                                            | [C/AL](https://docs.microsoft.com/en-us/dynamics-nav/programming-in-c-al)                      |            |                      |
| capnproto           | capnp                                                                      | [Cap’n Proto](https://capnproto.org/capnp-tool.html)                                           | protocols  |                      |
| ceylon              |                                                                            | [Ceylon](https://ceylon-lang.org)                                                              |            |                      |
|                     |                                                                            | [Cirru](http://text.cirru.org)                                                                 |            | `cirru`              |
| `cisco`             |                                                                            | Cisco CLI                                                                                      |            |                      |
| clean               | dcl, icl                                                                   | [Clean](http://clean.cs.ru.nl)                                                                 | functional |                      |
| clojure-repl        |                                                                            | [Clojure REPL](https://clojure.org)                                                            | lisp       |                      |
| `clojure`           | `clj`, `edn`                                                               | [Clojure](https://clojure.org)                                                                 | lisp       | `clojure`            |
| `cmake`             | `cmake.in`                                                                 | [CMake](https://cmake.org)                                                                     |            | `makefile`           |
|                     |                                                                            | [Cobol](https://en.wikipedia.org/wiki/COBOL)                                                   | enterprise | `cobol`              |
| `coffeescript`      | `coffee`, `cson`, `iced`                                                   | [CoffeeScript](https://coffeescript.org)                                                       | scripting  | `coffee`             |
|                     |                                                                            | [ColdFusion](https://en.wikipedia.org/wiki/Adobe_ColdFusion)                                   |            | `coldfusion`         |
| coq                 |                                                                            | [Coq](https://coq.inria.f)                                                                     | functional |                      |
| cos                 | `cls`                                                                      | Caché Object Script                                                                            | enterprise |                      |
| `cpc`               |                                                                            | CpcdosC+                                                                                       |            |                      |
| `cpp`               | `cc`, `c++`, `h++`, `hpp`, `hh`, `hxx`, `cxx`                              | [C++](https://isocpp.org)                                                                      | system     | `c_cpp`              |
| `crmsh`             | `crm`, `pcmk`                                                              | [crmsh](http://crmsh.github.io)                                                                | config     | `sh`                 |
| `crystal`           | `cr`                                                                       | [Crystal](https://crystal-lang.org)                                                            | scripting  | `crystal`            |
| `csharp`            | `cs`, `c#`                                                                 | [C\#](https://docs.microsoft.com/en-us/dotnet/csharp)                                          | common     | `csharp`             |
|                     |                                                                            | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_document`    |
|                     |                                                                            | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_orchestra`   |
|                     |                                                                            | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_score`       |
| `csp`               |                                                                            | [CSP (ContentSecurityPolicy)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)           |            | `csp`                |
| `css`               |                                                                            | [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)                                        | web        | `css`                |
| `curl`              |                                                                            | cURL                                                                                           |            |                      |
|                     |                                                                            | [Curly](https://9seconds.github.io/curly)                                                      | template   | `curly`              |
| `cypher`            |                                                                            | Cypher (Neo4j)                                                                                 |            |                      |
| `d`                 |                                                                            | [D](https://dlang.org)                                                                         |            | `d`                  |
| `dafny`             |                                                                            | Dafny                                                                                          |            |                      |
| `dart`              |                                                                            | [Dart](https://dart.dev)                                                                       | scripting  | `dart`               |
| `delphi`            | `dpr`, `dfm`, `pas`, `pascal`                                              | [Delphi](https://www.embarcadero.com/products/delphi)                                          | common     | `pascal`             |
| `diff`              | `patch`                                                                    | [Diff](https://www.gnu.org/software/diffutils)                                                 | common     | `diff`               |
| `django`            | `jinja`                                                                    | [Django](https://www.djangoproject.com)                                                        | template   | `django`             |
| dns                 | bind, zone                                                                 | [DNS Zone](https://en.wikipedia.org/wiki/Zone_file)                                            | config     |                      |
| `dockerfile`        | `docker`                                                                   | [Dockerfile](https://docs.docker.com/engine/reference/builder/)                                | config     | `dockerfile`         |
| `dos`               | `bat`, `cmd`                                                               | [Batch file (DOS)](https://en.wikipedia.org/wiki/Batch_file)                                   |            | `batchfile`          |
| dsconfig            |                                                                            | dsconfig                                                                                       | config     |                      |
|                     |                                                                            | [Drolls](https://en.wikipedia.org/wiki/Drools)                                                 | enterprise | `drools`             |
| dts                 |                                                                            | [Device Tree](https://elinux.org/Device_Tree_Reference)                                        | config     |                      |
|                     |                                                                            | [DOT (graph description language)](https://graphviz.org/doc/info/lang.html)                    | graphical  | `dot`                |
| dust                | dst                                                                        | [Dust](https://www.dustjs.com)                                                                 | template   |                      |
| `dylan`             |                                                                            | Dylan                                                                                          |            |                      |
| ebnf                |                                                                            | [Extended Backus-Naur Form](https://en.wikipedia.org/wiki/Extended_Backus–Naur_form)           |            |                      |
|                     |                                                                            | [UN/EDIFACT](https://en.wikipedia.org/wiki/EDIFACT)                                            | protocol   | `edifact`            |
|                     |                                                                            | [Eiffel](https://www.eiffel.org)                                                               |            | `eiffel`             |
|                     |                                                                            | [EJS (Embedded JavaScript teplating)](https://ejs.co)                                          | template   | `ejs`                |
| `elixir`            | `ex`, `exs`                                                                | [Elixir](https://elixir-lang.org)                                                              | functional | `elixir`             |
| `elm`               |                                                                            | [Elm](https://elm-lang.org)                                                                    | functional | `elm`                |
| erb                 |                                                                            | [ERB (Embedded Ruby)](https://ruby-doc.org/stdlib-2.6.5/libdoc/erb/rdoc/ERB.html)              | template   |                      |
| erlang-repl         |                                                                            | [Erlang REPL]( https://www.erlang.org)                                                         | functional |                      |
| `erlang`            | `erl`                                                                      | [Erlang]( https://www.erlang.org)                                                              | functional | `erlang`             |
| excel               | xls, xlsx                                                                  | [Excel formulae](https://products.office.com/en-us/excel)                                      |            |                      |
| `extempore`         | `xtlang`, `xtm`                                                            | Extempore                                                                                      |            |                      |
| fix                 |                                                                            | FIX                                                                                            |            |                      |
| flix                |                                                                            | [Flix](https://flix.dev)                                                                       |            |                      |
|                     |                                                                            | [Forth](https://www.forth.com/forth)                                                           |            | `forth`              |
| `fortran`           | `f90`, `f95`                                                               | [Fortran](https://en.wikipedia.org/wiki/Fortran)                                               | scientific | `fortran`            |
| `fsharp`            | `fs`, `f#`                                                                 | [F#](https://docs.microsoft.com/en-us/dotnet/fsharp)                                           | functional | `fsharp`             |
|                     |                                                                            | [FSL (FEMAG script language)](https://script.profemag.ch/content/FSL/intro.html)               | scientific | `fsl`                |
|                     |                                                                            |                                                                                                |            | `ftl`                |
| gams                | gms                                                                        | [GAMS](https://www.gams.com)                                                                   | scientific |                      |
| gauss               | gss                                                                        | [GAUSS](https://www.aptech.com)                                                                | scientific |                      |
| `gcode`             | `nc`                                                                       | [G-code](https://www.sis.se/api/document/preview/911952)                                       |            | `gcode`              |
| `gherkin`           | `feature`                                                                  | [Gherkin](https://cucumber.io/docs/gherkin)                                                    |            | `gherkin`            |
|                     |                                                                            |                                                                                                |            | `gitignore`          |
| `glsl`              |                                                                            | [GLSL (OpenGL Shading Language)](https://en.wikipedia.org/wiki/OpenGL_Shading_Language)        | graphics   | `glsl`               |
| gml                 |                                                                            | [GML (Game Maker Language)](https://docs2.yoyogames.com)                                       | scripting  |                      |
|                     |                                                                            | [Gobstones](https://es.wikipedia.org/wiki/Gobstones)                                           |            | `gobstones`          |
| `go`                | `golang`                                                                   | [Go](http://golang.org)                                                                        | common     | `golang`             |
| golo                |                                                                            | [Golo](http://golo-lang.org)                                                                   |            |                      |
| gradle              |                                                                            | [Gradle](https://gradle.org)                                                                   |            |                      |
|                     |                                                                            |                                                                                                |            | `graphqlschema`      |
| `groovy`            |                                                                            | [Groovy](https://groovy-lang.org)                                                              |            | `groovy`             |
| `haml`              |                                                                            | [HAML](http://haml.info)                                                                       | template   | `haml`               |
| `handlebars`        | `hbs`, `html.hbs`, `html.handlebars`, `htmlbars`                           | [Handlebars](https://handlebarsjs.com)                                                         | template   | `handlebars`         |
| `haskell`           | `hs`                                                                       | [Haskell](https://www.haskell.org)                                                             | functional | `haskell`            |
|                     |                                                                            | [Haskell Cabal](https://www.haskell.org/cabal)                                                 |            | `haskell_cabal`      |
| `haxe`              | `hx`                                                                       | [Haxe]( https://haxe.org)                                                                      |            | `haxe`               |
|                     |                                                                            | [Hjson, a user interface for JSON](https://hjson.github.io)                                    | config     | `hjson`              |
| hsp                 |                                                                            | [HSP (Hot Soup Processor)](https://en.wikipedia.org/wiki/Hot_Soup_Processor)                   | scripting  |                      |
|                     |                                                                            |                                                                                                |            | `html_elixir`        |
|                     |                                                                            |                                                                                                |            | `html_ruby`          |
| http                | https                                                                      | [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)                             | protocol   |                      |
| `hy`                | `hylang`                                                                   | [Hy](http://docs.hylang.org/en/stable)                                                         | lisp       | `lisp`               |
| inform7             | i7                                                                         | [Inform 7](http://inform7.com)                                                                 | markup     |                      |
| `ini`               | `toml`                                                                     | [TOML, also INI](https://github.com/toml-lang/toml)                                            | config     | `ini`, `toml`        |
|                     |                                                                            | [io](https://iolanguage.org)                                                                   |            | `io`                 |
|                     |                                                                            | [ion](https://github.com/ion-lang/ion)                                                         | ion        | `ion`                |
| irpf90              |                                                                            | [IRPF90](http://irpf90.ups-tlse.fr)                                                            | scientific |                      |
| isbl                |                                                                            | ISBL                                                                                           | enterprise |                      |
|                     |                                                                            | [Jack](https://classes.engineering.wustl.edu/cse365/jack.php)                                  |            | `jack`               |
|                     |                                                                            |                                                                                                |            | `jade`               |
| `java`              | `jsp`                                                                      | [Java](https://www.java.com)                                                                   | common     | `java`, `jsp`        |
| `javascript`        | `js`, `jsx`, `mjs`, `cjs`                                                  | [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)                          | scripting  | `javascript`, `jsx`  |
| jboss-cli           | wildfly-cli                                                                | [JBoss CLI](https://docs.jboss.org/author/display/WFLY/Command+Line+Interface)                 | config     |                      |
| `json`              |                                                                            | [JSON (JavaScript Object Notation)](http://www.json.org)                                       | config     | `json`, `json5`      |
|                     |                                                                            | [JSONiq](http://www.jsoniq.org)                                                                |            | `jsoniq`             |
|                     |                                                                            | JSSM (JavaScript State Machine)                                                                |            | `jssm`               |
| julia-repl          | `jldoctest`                                                                | [Julia REPL](https://julialang.org)                                                            |            |                      |
| `julia`             |                                                                            | [Julia](https://julialang.org)                                                                 | common     | `julia`              |
| `kotlin`            | `kot`,`kt`, `kts`                                                          | [Kotlin](https://kotlinlang.org)                                                               | common     | `kotlin`             |
| lasso               | ls, lassoscript                                                            | [Lasso](http://www.lassosoft.com/What-Is-Lasso)                                                |            |                      |
| `latex`             | `tex`                                                                      | [LaTeX](https://www.latex-project.org)                                                         | markup     | `latex`, `tex`       |
|                     |                                                                            | [Latte](https://latte-lang.org)                                                                |            | `latte`              |
| ldif                |                                                                            | [LDIF](https://en.wikipedia.org/wiki/LDAP_Data_Interchange_Format)                             | config     |                      |
| leaf                |                                                                            | [Leaf](https://vapor.github.io/documentation/guide/leaf.html)                                  |            |                      |
| `less`              |                                                                            | [Less](http://lesscss.org)                                                                     | web        | `less`               |
|                     |                                                                            | [Liquid](https://shopify.github.io/liquid/basics/introduction)                                 | template   | `liquid`             |
| `lisp`              |                                                                            | Lisp                                                                                           | lisp       | `lisp`               |
| livecodeserver      |                                                                            | LiveCode                                                                                       | enterprise |                      |
| `livescript`        | `ls`                                                                       | [LiveScript](https://livescript.net)                                                           | scripting  | `livescript`         |
| llvm                |                                                                            | [LLVM IR](https://llvm.org/docs/LangRef.html)                                                  | assembler  |                      |
|                     |                                                                            |                                                                                                |            | `logiql`             |
|                     |                                                                            |                                                                                                |            | `logtalk`            |
| `lsl`               |                                                                            | [LSL (Linden Scripting Language)](http://wiki.secondlife.com/wiki/LSL_Portal)                  | scripting  | `lsl`                |
| `lua`               |                                                                            | [Lua](https://www.lua.org)                                                                     | scripting  | `lua`                |
|                     |                                                                            |                                                                                                |            | `luapage`            |
|                     |                                                                            |                                                                                                |            | `lucene`             |
| `makefile`          | `mk`, `mak`, `make`,                                                       | [Makefile](https://www.gnu.org/software/make/manual/html_node/Introduction.html)               | common     | `makefile`           |
| `markdown`          | `md`, `mkd`, `mkdown`                                                      | [Markdown](https://daringfireball.net/projects/markdown)                                       | markup     | `markdown`           |
|                     |                                                                            |                                                                                                |            | `mask`               |
| mathematica         | mma, wl                                                                    | [Wolfram Language](https://www.wolfram.com/mathematica)                                        | scientific |                      |
| `matlab`            |                                                                            | [Matlab](https://www.mathworks.com/products/matlab.html)                                       | scientific | `matlab`             |
| maxima              |                                                                            | [Maxima](http://maxima.sourceforge.net)                                                        | scientific |                      |
|                     |                                                                            |                                                                                                |            | `maze`               |
|                     |                                                                            |                                                                                                |            | `mediawiki`          |
| `mel`               |                                                                            | [MEL (Maya Embedded Language)](http://www.autodesk.com/products/autodesk-maya/overview)        | graphics   | `mel`                |
| `mercury`           | `m`, `moo`                                                                 | [Mercury](https://www.mercurylang.org)                                                         | functional |                      |
| `mipsasm`           | `mips`                                                                     | [MIPS Assembly](https://en.wikipedia.org/wiki/MIPS_architecture)                               | assembler  | `mips`               |
|                     |                                                                            |                                                                                                |            | `mixal`              |
| mizar               |                                                                            | [Mizar](http://mizar.org/language)                                                             | scientific |                      |
| mojolicious         |                                                                            | [Mojolicious](https://mojolicious.org)                                                         | template   |                      |
| monkey              |                                                                            | [Monkey](https://blitzresearch.itch.io/monkey2)                                                |            |                      |
| moonscript          | moon                                                                       | [MoonScript](http://moonscript.org)                                                            | scripting  |                      |
|                     |                                                                            |                                                                                                |            | `mushcode`           |
|                     |                                                                            |                                                                                                |            | `mysql`              |
| n1ql                |                                                                            | [N1QL (Couchbase query language)](https://www.couchbase.com/products/n1ql)                     |            |                      |
| nestedtext          | nt                                                                         | [NestedText](https://nestedtext.org)                                                           | config     |                      |
| `nginx`             | `nginxconf`                                                                | [Nginx config](https://www.nginx.com)                                                          | config     | `nginx`              |
| `nim`               |                                                                            | [Nim](https://nim-lang.org)                                                                    | system     | `nim`                |
| `nix`               | `nixos`                                                                    | [Nix](http://nixos.org/nix)                                                                    |            | `nix`                |
| node-repl           |                                                                            | Node REPL                                                                                      | scripting  |                      |
| `nsis`              |                                                                            | [NSIS (Nullsoft Scriptable Install System)](https://nsis.sourceforge.io/Main_Page)             |            | `nsis`               |
|                     |                                                                            |                                                                                                |            | `nunjacks`           |
| `objectivec`        | `mm`, `objc`, `obj-c`, `obj-c++`, `objective-c++`                          | [Objective-C](https://developer.apple.com/documentation/objectivec)                            | common     | `objectivec`         |
| `ocaml`             | `ml`                                                                       | [OCaml]( https://ocaml.org)                                                                    | functional | `ocaml`              |
| `openscad`          | `scad`                                                                     | [OpenSCAD](https://www.openscad.org)                                                           | scientific | `scad`               |
| oxygene             |                                                                            | [Oxygene](https://www.elementscompiler.com/elements/default.aspx)                              |            |                      |
| parser3             |                                                                            | [Parser3](https://www.parser.ru/en)                                                            | template   |                      |
|                     |                                                                            | [PartiQL](https://partiql.org)                                                                 |            | `partiql`            |
| `perl`              | `pl`, `pm`                                                                 | [Perl](https://www.perl.org)                                                                   | common     | `perl`               |
| pf                  | pf.conf                                                                    | [Packet Filter config](http://man.openbsd.org/pf.conf)                                         | config     |                      |
| `pgsql`             | `postgres`, `postgresql`                                                   | [PostgreSQL and PL/pgSQL](https://www.postgresql.org/docs/11/sql.html)                         |            | `pgsql`              |
| php-template        |                                                                            | [PHP Template](https://www.php.net)                                                            | common     |                      |
| `php`               |                                                                            | [PHP](https://www.php.net)                                                                     | common     | `php`                |
|                     |                                                                            |                                                                                                |            | `php_laravel_blade`  |
|                     |                                                                            | [Apache Pig](https://pig.apache.org)                                                           |            | `pig`                |
| `plaintext`         | `text`, `txt`                                                              | Plain text without any highlighting                                                            |            | `plaintext`, `text`  |
| pony                |                                                                            | [Pony](https://www.ponylang.io)                                                                |            |                      |
| `powershell`        | `pwsh`, `ps`, `ps1`                                                        | [PowerShell](https://docs.microsoft.com/en-us/powershell)                                      |            | `powershell`         |
|                     |                                                                            |                                                                                                |            | `praat`              |
|                     |                                                                            |                                                                                                |            | `prisma`             |
| `processing`        | `pde`                                                                      | [Processing](https://processing.org)                                                           | graphics   | `c_cpp`              |
| profile             |                                                                            | Python profiler                                                                                |            |                      |
| `prolog`            |                                                                            | [Prolog](https://en.wikipedia.org/wiki/Prolog)                                                 | logic      | `prolog`             |
| `properties`        |                                                                            | .properties                                                                                    | config     | `properties`         |
| `protobuf`          |                                                                            | [Protocol Buffers](https://developers.google.com/protocol-buffers/docs/proto3)                 | protocols  | `protobuf`           |
| `puppet`            | `pp`                                                                       | [Puppet](https://puppet.com/docs)                                                              | config     | `puppet`             |
| `purebasic`         | `pb`, `pbi`                                                                | [PureBASIC](https://www.purebasic.com)                                                         |            | `vbscript`           |
| python-repl         | pycon                                                                      | Python REPL                                                                                    | common     |                      |
| `python`            | `py`, `gyp`, `ipython`                                                     | [Python](https://www.python.org)                                                               | common     | `python`             |
| q                   | k, kdb                                                                     | [Q](https://kx.com/connect-with-us/developers)                                                 |            |                      |
| `qml`               | `qt`                                                                       | [QML](https://doc.qt.io/qt-5/qmlapplications.html)                                             | scripting  | `qml`                |
| `qsharp`            |                                                                            | Q#                                                                                             |            |                      |
| `r`                 |                                                                            | [R](https://www.r-project.org)                                                                 | scientific | `r`                  |
|                     |                                                                            |                                                                                                |            | `raku`               |
|                     |                                                                            |                                                                                                |            | `razor`              |
|                     |                                                                            |                                                                                                |            | `rdoc`               |
| reasonml            | re                                                                         | [ReasonML](https://reasonml.github.io)                                                         | functional |                      |
|                     |                                                                            |                                                                                                |            | `red`                |
|                     |                                                                            |                                                                                                |            | `redshift`           |
|                     |                                                                            |                                                                                                |            | `rhtml`              |
| rib                 |                                                                            | [RenderMan RIB](https://renderman.pixar.com/resources/RenderMan_20/ribBinding.html)            | graphics   |                      |
| roboconf            | graph, instances                                                           | [Roboconf](http://roboconf.net)                                                                | config     |                      |
| routeros            |                                                                            | [Microtik RouterOS script](https://wiki.mikrotik.com/wiki/Manual:Scripting)                    |            |                      |
| rsl                 |                                                                            | [RenderMan RSL](https://renderman.pixar.com/resources/RenderMan_20/shadingLanguage.html)       | graphics   |                      |
|                     | `rest`                                                                     | [reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText)                             |            | `rst`                |
| `ruby`              | `gemspec`, `irb`, `podspec`, `rb`, `thor`                                  | [Ruby](https://www.ruby-lang.org)                                                              | common     | `ruby`               |
| ruleslanguage       |                                                                            | [Oracle Rules Language](https://docs.oracle.com/cd/E17904_01/dev.1111/e10227/rlref.htm)        | enterprise |                      |
| `rust`              | `rs`                                                                       | [Rust](https://www.rust-lang.org)                                                              | common     | `rust`               |
|                     |                                                                            | [SAC](https://en.wikipedia.org/wiki/SAC_programming_language)                                  |            | `sac`                |
| sas                 |                                                                            | SAS                                                                                            |            |                      |
|                     |                                                                            |                                                                                                |            | `sass`               |
| `scala`             |                                                                            | [Scala](https://www.scala-lang.org)                                                            | functional | `scala`              |
| `scheme`            |                                                                            | [Scheme](http://community.schemewiki.org/?what-is-scheme)                                      | lisp       | `scheme`             |
| scilab              | sci                                                                        | [Scilab](https://www.scilab.org)                                                               | scientific |                      |
| `scss`              |                                                                            | [SCSS](https://sass-lang.com)                                                                  | web        | `scss`               |
| `shell`             | `console`, `shellsession`                                                  | Shell Session                                                                                  | common     | `sh`                 |
|                     |                                                                            |                                                                                                |            | `sjs`                |
|                     |                                                                            |                                                                                                |            | `slim`               |
| smali               |                                                                            | [Smali](https://github.com/JesusFreke/smali)                                                   |            |                      |
| smalltalk           | st                                                                         | [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk)                                           |            |                      |
|                     |                                                                            |                                                                                                |            | `smarty`             |
|                     |                                                                            |                                                                                                |            | `smithy`             |
| sml                 | ml                                                                         | [SML (Standard ML)](https://www.smlnj.org)                                                     | functional |                      |
| `solidity`          | `sol`                                                                      | Solidity                                                                                       |            |                      |
|                     |                                                                            |                                                                                                |            | `soy`                |
|                     |                                                                            |                                                                                                |            | `space`              |
|                     |                                                                            |                                                                                                |            | `sparql`             |
| `spl`               |                                                                            | Slunk SPL                                                                                      |            |                      |
| sqf                 |                                                                            | [SQF](https://community.bistudio.com/wiki/SQF_syntax)                                          | scripting  |                      |
| `sql`               |                                                                            | [SQL](https://en.wikipedia.org/wiki/SQL)                                                       | database   | `sql`                |
|                     |                                                                            |                                                                                                |            | `sqlserver`          |
| stan                | stanfuncs                                                                  | [Stan probabilistic programming language](http://mc-stan.org)                                  | scientific |                      |
| stata               | ado, do                                                                    | [Stata](https://en.wikipedia.org/wiki/Stata)                                                   | scientific |                      |
| step21              | p21, step, stp                                                             | [STEP Part 21](https://en.wikipedia.org/wiki/ISO_10303-21)                                     |            |                      |
| `structured-text`   | `iecst`, `scl`, `stl`                                                      | Structured Text                                                                                |            |                      |
| `stylus`            | `styl`                                                                     | [Stylus](https://github.com/stylus/stylus)                                                     | web        | `stylus`             |
| subunit             |                                                                            | [SubUnit](https://pypi.org/project/python-subunit)                                             |            |                      |
| `supercollider`     | `sc`                                                                       | Supercollider                                                                                  |            |                      |
| `svelte`            |                                                                            |                                                                                                |            |                      |
| `swift`             |                                                                            | [Swift](https://swift.org)                                                                     | common     | `swift`              |
| `taggerscript`      |                                                                            | [Tagger Script](https://picard.musicbrainz.org)                                                |            |                      |
| tap                 |                                                                            | [Test Anything Protocol](https://testanything.org)                                             |            |                      |
| `tcl`               | `tk`                                                                       | [Tcl](https://www.tcl.tk/about/language.html)                                                  |            | `tcl`                |
|                     |                                                                            |                                                                                                |            | `terraform`          |
|                     |                                                                            |                                                                                                |            | `textile`            |
| thrift              |                                                                            | [Thrift](https://thrift.apache.org)                                                            | protocols  |                      |
| `toit`              |                                                                            | Toit                                                                                           |            |                      |
| tp                  |                                                                            | TP                                                                                             |            |                      |
|                     |                                                                            |                                                                                                |            | `turtle`             |
| `twig`              | `craftcms`                                                                 | [Twig](https://twig.symfony.com)                                                               | template   | `twig`               |
| `typescript`        | `ts`, `tsx`                                                                | [TypeScript](https://www.typescriptlang.org)                                                   | common     | `typescript`, `tsx`  |
| `unicorn-rails-log` |                                                                            | Unicorn Rails log                                                                              |            | `                    |
| `vala`              |                                                                            | [Vala](https://wiki.gnome.org/Projects/Vala)                                                   |            | `vala`               |
| `vbnet`             | `vb`                                                                       | [Visual Basic .NET](https://docs.microsoft.com/dotnet/visual-basic/getting-started)            | common     | `vbscript`           |
| vbscript-html       |                                                                            | [VBScript in HTML](https://en.wikipedia.org/wiki/VBScript)                                     | scripting  |                      |
| `vbscript`          | `vbs`                                                                      | [VBScript](https://en.wikipedia.org/wiki/VBScript)                                             | scripting  | `vbscript`           |
|                     |                                                                            |                                                                                                |            | `velocity`           |
| `verilog`           | `sv`, `svh`, `v`                                                           | [Verilog](http://www.verilog.com)                                                              |            | `verilog`            |
| `vhdl`              |                                                                            | [VHDL](https://en.wikipedia.org/wiki/VHDL)                                                     |            | `vhdl`               |
| vim                 |                                                                            | [Vim Script](https://www.vim.org)                                                              | scripting  |                      |
|                     |                                                                            |                                                                                                |            | `visualforce`        |
| wasm                |                                                                            | [WebAssembly](https://webassembly.org)                                                         | web        |                      |
|                     |                                                                            | [Wollok](https://github.com/uqbar-project/wollok)                                              |            | `wollok`             |
| wren                |                                                                            | [Wren](https://wren.io)                                                                        | scripting  |                      |
| `x++`               | `axapta`                                                                   | X++                                                                                            |            |                      |
| `x86asm`            |                                                                            | [Intel x86 Assembly](https://en.wikipedia.org/wiki/X86_assembly_language)                      | assembler  | `assembly_x86`       |
| `xsharp`            | `xs`, `prg`                                                                | X#                                                                                             |            |                      |
| xl                  | tao                                                                        | [XL](http://xlr.sf.net)                                                                        |            |                      |
| `xml`               | `atom`, `html`, `plist`, `rss`, `svg`, `wsf`, `xhtml`, `xjb`, `xsd`, `xsl` | [HTML, XML](https://www.w3.org/XML)                                                            |            | `html`, `svg`, `xml` |
| `xquery`            | `xpath`, `xq`                                                              | [XQuery](https://www.w3.org/XML/Query)                                                         | functional | `xquery`             |
| `yaml`              | `yml`                                                                      | [YAML](https://yaml.org)                                                                       | config     | `yaml`               |
|                     |                                                                            |                                                                                                |            | `zeek`               |
| zenscript           | zs                                                                         | ZenScript                                                                                      |            |                      |
| zephir              | zep                                                                        | [Zephir](https://zephir-lang.com/en)                                                           |            |                      |


## Short List

Complete overview on all supported languages and the applied syntax highlighting
scheme of `ace`.


| short-code          | syntax-highlighting |
| ------------------- | ------------------- |
| `abap`              | `abap`              |
| `sap-abap`          | `abap`              |
| `abc`               | `abc`               |
| `actionscript`      | `actionscript`      |
| `as`                | `actionscript`      |
| `ada`               | `ada`               |
| `alda`              | `alda`              |
| `angelscript`       | `c_cpp`             |
| `asc`               | `c_cpp`             |
| `apache`            | `apache_conf`       |
| `apacheconf`        | `apache_conf`       |
| `apache_conf`       | `apache_conf`       |
| `apex`              | `apex`              |
| `applescript`       | `applescript`       |
| `osascript`         | `applescript`       |
| `aql`               | `aql`               |
| `arduino`           | `c_cpp`             |
| `ino`               | `c_cpp`             |
| `armasm`            | `assembly_x86`      |
| `arm`               | `assembly_x86`      |
| `asl`               | `asl`               |
| `asciidoc`          | `asciidoc`          |
| `adoc`              | `asciidoc`          |
| `aspectj`           | `java`              |
| `autohotkey`        | `autohotkey`        |
| `ahk`               | `autohotkey`        |
| `avrasm`            | `assembly_x86`      |
| `asm`               | `assembly_x86`      |
| `bash`              | `sh`                |
| `sh`                | `sh`                |
| `basic`             | `vbscript`          |
| `c`                 | `c_cpp`             |
| `h`                 | `c_cpp`             |
| `c9search`          | `c9search`          |
| `cirru`             | `cirru`             |
| `clojure`           | `clojure`           |
| `clj`               | `clojure`           |
| `edn`               | `clojure`           |
| `cmake`             | `makefile`          |
| `cmake.in`          | `makefile`          |
| `cobol`             | `cobol`             |
| `coffeescript`      | `coffee`            |
| `coffee`            | `coffee`            |
| `cson`              | `coffee`            |
| `iced`              | `coffee`            |
| `coldfusion`        | `coldfusion`        |
| `cpp`               | `c_cpp`             |
| `cc`                | `c_cpp`             |
| `c++`               | `c_cpp`             |
| `h++`               | `c_cpp`             |
| `hpp`               | `c_cpp`             |
| `hh`                | `c_cpp`             |
| `hxx`               | `c_cpp`             |
| `cxx`               | `c_cpp`             |
| `crmsh`             | `sh`                |
| `crm`               | `sh`                |
| `pcmk`              | `sh`                |
| `crystal`           | `crystal`           |
| `cr`                | `crystal`           |
| `csharp`            | `csharp`            |
| `cs`                | `csharp`            |
| `c#`                | `csharp`            |
| `csound_document`   | `csound_document`   |
| `csound_orchestra`  | `csound_orchestra`  |
| `csound_score`      | `csound_score`      |
| `csp`               | `csp`               |
| `css`               | `css`               |
| `curly`             | `curly`             |
| `d`                 | `d`                 |
| `dart`              | `dart`              |
| `delphi`            | `pascal`            |
| `dpr`               | `pascal`            |
| `dfm`               | `pascal`            |
| `pas`               | `pascal`            |
| `pascal`            | `pascal`            |
| `diff`              | `diff`              |
| `patch`             | `diff`              |
| `django`            | `django`            |
| `jinja`             | `django`            |
| `dockerfile`        | `dockerfile`        |
| `docker`            | `dockerfile`        |
| `dos`               | `batchfile`         |
| `bat`               | `batchfile`         |
| `cmd`               | `batchfile`         |
| `batchfile`         | `batchfile`         |
| `drools`            | `drools`            |
| `dot`               | `dot`               |
| `edifact`           | `edifact`           |
| `eiffel`            | `eiffel`            |
| `ejs`               | `ejs`               |
| `elixir`            | `elixir`            |
| `ex`                | `elixir`            |
| `exs`               | `elixir`            |
| `elm`               | `elm`               |
| `erlang`            | `erlang`            |
| `erl`               | `erlang`            |
| `forth`             | `forth`             |
| `fortran`           | `fortran`           |
| `f90`               | `fortran`           |
| `f95`               | `fortran`           |
| `fsharp`            | `fsharp`            |
| `fs`                | `fsharp`            |
| `f#`                | `fsharp`            |
| `fsl`               | `fsl`               |
| `ftl`               | `ftl`               |
| `gcode`             | `gcode`             |
| `nc`                | `gcode`             |
| `gherkin`           | `gherkin`           |
| `feature`           | `gherkin`           |
| `gitignore`         | `gitignore`         |
| `glsl`              | `glsl`              |
| `gobstones`         | `gobstones`         |
| `go`                | `golang`            |
| `golang`            | `golang`            |
| `graphqlschema`     | `graphqlschema`     |
| `groovy`            | `groovy`            |
| `haml`              | `haml`              |
| `handlebars`        | `handlebars`        |
| `hbs`               | `handlebars`        |
| `html.hbs`          | `handlebars`        |
| `html.handlebars`   | `handlebars`        |
| `htmlbars`          | `handlebars`        |
| `haskell`           | `haskell`           |
| `hs`                | `haskell`           |
| `haskell_cabal`     | `haskell_cabal`     |
| `haxe`              | `haxe`              |
| `hx`                | `haxe`              |
| `hjson`             | `hjson`             |
| `html_elixir`       | `html_elixir`       |
| `html_ruby`         | `html_ruby`         |
| `hy`                | `lisp`              |
| `hylang`            | `lisp`              |
| `ini`               | `ini`               |
| `toml`              | `toml`              |
| `io`                | `io`                |
| `ion`               | `ion`               |
| `jack`              | `jack`              |
| `jade`              | `jade`              |
| `java`              | `java`              |
| `jsp`               | `jsp`               |
| `javascript`        | `javascript`        |
| `js`                | `javascript`        |
| `mjs`               | `javascript`        |
| `cjs`               | `javascript`        |
| `jsx`               | `jsx`               |
| `json`              | `json`              |
| `json5`             | `json5`             |
| `jsoniq`            | `jsoniq`            |
| `jssm`              | `jssm`              |
| `julia`             | `julia`             |
| `kotlin`            | `kotlin`            |
| `kot`               | `kotlin`            |
| `kt`                | `kotlin`            |
| `kts`               | `kotlin`            |
| `latex`             | `latex`             |
| `tex`               | `tex`               |
| `latte`             | `latte`             |
| `less`              | `less`              |
| `liquid`            | `liquid`            |
| `lisp`              | `lisp`              |
| `livescript`        | `livescript`        |
| `ls`                | `livescript`        |
| `logiql`            | `logiql`            |
| `logtalk`           | `logtalk`           |
| `lsl`               | `lsl`               |
| `lua`               | `lua`               |
| `luapage`           | `luapage`           |
| `lucene`            | `lucene`            |
| `makefile`          | `makefile`          |
| `mk`                | `makefile`          |
| `mak`               | `makefile`          |
| `make`              | `makefile`          |
| `markdown`          | `markdown`          |
| `md`                | `markdown`          |
| `mkd`               | `markdown`          |
| `mkdown`            | `markdown`          |
| `mask`              | `mask`              |
| `matlab`            | `matlab`            |
| `maze`              | `maze`              |
| `mediawiki`         | `mediawiki`         |
| `mel`               | `mel`               |
| `mipsasm`           | `mips`              |
| `mips`              | `mips`              |
| `mixal`             | `mixal`             |
| `mushcode`          | `mushcode`          |
| `mysql`             | `mysql`             |
| `nginx`             | `nginx`             |
| `nginxconf`         | `nginx`             |
| `nim`               | `nim`               |
| `nix`               | `nix`               |
| `nixos`             | `nix`               |
| `nsis`              | `nsis`              |
| `nunjacks`          | `nunjacks`          |
| `objectivec`        | `objectivec`        |
| `mm`                | `objectivec`        |
| `objc`              | `objectivec`        |
| `obj-c`             | `objectivec`        |
| `obj-c++`           | `objectivec`        |
| `objective-c++`     | `objectivec`        |
| `ocaml`             | `ocaml`             |
| `ml`                | `ocaml`             |
| `openscad`          | `scad`              |
| `scad`              | `scad`              |
| `perl`              | `perl`              |
| `pl`                | `perl`              |
| `pm`                | `perl`              |
| `pgsql`             | `pgsql`             |
| `postgres`          | `pgsql`             |
| `postgresql`        | `pgsql`             |
| `php`               | `php`               |
| `php_laravel_blade` | `php_laravel_blade` |
| `pig`               | `pig`               |
| `plaintext`         | `plaintext`         |
| `text`              | `text`              |
| `txt`               | `text`              |
| `partiql`           | `partiql`           |
| `powershell`        | `powershell`        |
| `pwsh`              | `powershell`        |
| `ps`                | `powershell`        |
| `ps1`               | `powershell`        |
| `praat`             | `praat`             |
| `prisma`            | `prisma`            |
| `processing`        | `c_cpp`             |
| `pde`               | `c_cpp`             |
| `prolog`            | `prolog`            |
| `properties`        | `properties`        |
| `protobuf`          | `protobuf`          |
| `puppet`            | `puppet`            |
| `pp`                | `puppet`            |
| `purebasic`         | `vbscript`          |
| `pb`                | `vbscript`          |
| `pbi`               | `vbscript`          |
| `python`            | `python`            |
| `py`                | `python`            |
| `gyp`               | `python`            |
| `ipython`           | `python`            |
| `qml`               | `qml`               |
| `qt`                | `qml`               |
| `r`                 | `r`                 |
| `raku`              | `raku`              |
| `razor`             | `razor`             |
| `rdoc`              | `rdoc`              |
| `red`               | `red`               |
| `redshift`          | `redshift`          |
| `rhtml`             | `rhtml`             |
| `rst`               | `rst`               |
| `rest`              | `rst`               |
| `ruby`              | `ruby`              |
| `gemspec`           | `ruby`              |
| `irb`               | `ruby`              |
| `podspec`           | `ruby`              |
| `rb`                | `ruby`              |
| `thor`              | `ruby`              |
| `rust`              | `rust`              |
| `rs`                | `rust`              |
| `sac`               | `sac`               |
| `sass`              | `sass`              |
| `scala`             | `scala`             |
| `scheme`            | `scheme`            |
| `scss`              | `scss`              |
| `shell`             | `sh`                |
| `console`           | `sh`                |
| `shellsession`      | `sh`                |
| `sjs`               | `sjs`               |
| `slim`              | `slim`              |
| `smarty`            | `smarty`            |
| `smithy`            | `smithy`            |
| `soy`               | `soy`               |
| `space`             | `space`             |
| `sparql`            | `sparql`            |
| `sql`               | `sql`               |
| `sqlserver`         | `sqlserver`         |
| `stylus`            | `stylus`            |
| `styl`              | `stylus`            |
| `swift`             | `swift`             |
| `tcl`               | `tcl`               |
| `tk`                | `tcl`               |
| `terraform`         | `terraform`         |
| `textile`           | `textile`           |
| `turtle`            | `turtle`            |
| `twig`              | `twig`              |
| `craftcms`          | `twig`              |
| `typescript`        | `typescript`        |
| `ts`                | `typescript`        |
| `tsx`               | `tsx`               |
| `vala`              | `vala`              |
| `vbnet`             | `vbscript`          |
| `vb`                | `vbscript`          |
| `vbscript`          | `vbscript`          |
| `vbs`               | `vbscript`          |
| `velocity`          | `velocity`          |
| `verilog`           | `verilog`           |
| `vhdl`              | `vhdl`              |
| `visualforce`       | `visualforce`       |
| `wollok`            | `wollok`            |
| `x86asm`            | `assembly_x86`      |
| `xml`               | `xml`               |
| `atom`              | `xml`               |
| `html`              | `html`              |
| `plist`             | `xml`               |
| `rss`               | `xml`               |
| `svg`               | `svg`               |
| `wsf`               | `xml`               |
| `xhtml`             | `xml`               |
| `xjb`               | `xml`               |
| `xsd`               | `xml`               |
| `xsl`               | `xml`               |
| `xquery`            | `xquery`            |
| `xpath`             | `xquery`            |
| `xq`                | `xquery`            |
| `yaml`              | `yaml`              |
| `yml`               | `yaml`              |
| `zeek`              | `zeek`              |

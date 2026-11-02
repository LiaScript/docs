# Language Mappings

This document contains a list of mappings for language identifiers for
[`highlight.js`](https://highlightjs.org), which is mostly used in Markdown
parsers, and [`ace`](https://ace.c9.io), which is applied by LiaScript. Since
both projects do not contain all languages and the names of the language
identifiers might vary, we provide a mapping.


> All language identifiers and aliases marked as `code` get syntax
> highlighting within LiaScript code-blocks. All other identifiers, as well as
> languages that are not listed at all, are shown as plain text without any
> highlighting.

This mapping is applied by LiaScript at:

https://github.com/LiaScript/LiaScript/blob/development/src/typescript/webcomponents/editor-modes.ts

The [Short List](#short-list) at the end contains all identifiers that are
defined there (state of LiaScript 2.6.0), including additional file endings
that are not part of `highlight.js`. Feel free to make comments/issues or to
add other mappings.



| highlight.js        | alias                                                               | language                                                                                       | category   | cloud9/ace           |
| ------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------- | -------------------- |
| 1c                  |                                                                     | 1C:Enterprise                                                                                  | enterprise |                      |
| 4d                  |                                                                     |                                                                                                |            |                      |
| `abap`              | `sap-abap`                                                          | [ABAB (Advanced Business Application Programming)](https://en.wikipedia.org/wiki/ABAP)         | enterprise | `abap`               |
|                     | `abc`                                                               | [ABC](https://homepages.cwi.nl/~steven/abc/programmers/handbook.html)                          | common     | `abc`                |
| abnf                |                                                                     | [Augmented Backus-Naur Form](https://tools.ietf.org/html/rfc5234)                              |            |                      |
| accesslog           |                                                                     | [Apache Access Log](https://httpd.apache.org/docs/2.4/logs.html#accesslog)                     | logs       |                      |
| `actionscript`      | `as`                                                                | ActionScript                                                                                   | scripting  | `actionscript`       |
| `ada`               |                                                                     | Ada                                                                                            |            | `ada`                |
| alan                | i, ln                                                               | Alan IF                                                                                        |            |                      |
|                     | `alda`                                                              | [Alda](https://alda.io)                                                                        | music      | `alda`               |
| angelscript         | asc                                                                 | [AngelScript](https://www.angelcode.com/angelscript)                                           | scripting  |                      |
| `apache`            | `apacheconf`                                                        | [Apache config](https://httpd.apache.org)                                                      | config     | `apache_conf`        |
|                     | `apex`, `cls`, `trigger`, `tgr`                                     | [APEX](https://www.guru99.com/apex-tutorial.html)                                              | enterprise | `apex`               |
| `applescript`       | osascript                                                           | [AppleScript](https://en.wikipedia.org/wiki/AppleScript)                                       | scripting  | `applescript`        |
|                     | `aql`                                                               | [AQL (ArangoDB Query Language)](https://www.arangodb.com/docs/stable/aql)                      |            | `aql`                |
| arcade              |                                                                     | [ArcGIS Arcade](https://developers.arcgis.com/arcade)                                          | scripting  |                      |
| `arduino`           | `ino`                                                               | [Arduino](https://www.arduino.cc)                                                              |            | `c_cpp`              |
| `armasm`            | `arm`                                                               | ARM Assembly                                                                                   | assembler  | `assembly_arm32`     |
|                     | `asl`, `dsl`, `asl.json`                                            | [ASL (ACPI Source Language)](https://acpica.org/sites/acpica/files/asl_tutorial_v20190625.pdf) |            | `asl`                |
| `asciidoc`          | `adoc`                                                              | [AsciiDoc](http://asciidoc.org)                                                                | markup     | `asciidoc`           |
| `aspectj`           |                                                                     | [AspectJ](https://www.eclipse.org/aspectj)                                                     |            | `java`               |
|                     | `astro`                                                             | [Astro](https://github.com/astrolang/astro)                                                    | functional | `astro`              |
| `autohotkey`        | `ahk`                                                               | AutoHotkey                                                                                     | scripting  | `autohotkey`         |
| autoit              |                                                                     | AutoIt                                                                                         | scripting  |                      |
| `avrasm`            | `asm`                                                               | AVR Assembly                                                                                   | assembler  | `assembly_x86`       |
| awk                 | mawk, nawk, gawk                                                    | [Awk](https://www.gnu.org/software/gawk/manual/gawk.html)                                      |            |                      |
| axapta              |                                                                     | [Microsoft X++](https://dynamics.microsoft.com/en-us/ax-overview/)                             | enterprise |                      |
| `bash`              | `sh`, zsh                                                           | [Bash](https://www.gnu.org/software/bash)                                                      | common     | `sh`                 |
| `basic`             | `bas`                                                               | [BASIC](https://en.wikipedia.org/wiki/Tandy_1000)                                              |            | `basic`              |
| bbcode              |                                                                     | BBCode                                                                                         |            |                      |
|                     | `bibtex`, `bib`                                                     | [BibTeX](http://www.bibtex.org)                                                                | markup     | `bibtex`             |
| bnf                 |                                                                     | [Backus–Naur Form](https://en.wikipedia.org/wiki/Backus–Naur_form)                             |            |                      |
| brainfuck           | bf                                                                  | [Brainfuck](https://esolangs.org/wiki/Brainfuck)                                               | esoteric   |                      |
| `c`                 | `h`                                                                 | C                                                                                              | system     | `c_cpp`              |
|                     | `c9search`, `c9search_results`                                      | Cloud9 search results                                                                          |            | `c9search`           |
| cal                 |                                                                     | [C/AL](https://docs.microsoft.com/en-us/dynamics-nav/programming-in-c-al)                      |            |                      |
| capnproto           | capnp                                                               | [Cap’n Proto](https://capnproto.org/capnp-tool.html)                                           | protocols  |                      |
|                     | `cedar`                                                             | [Cedar policy language](https://www.cedarpolicy.com)                                           |            | `cedar`              |
|                     | `cedarschema`                                                       | [Cedar schema](https://www.cedarpolicy.com)                                                    |            | `cedarschema`        |
| ceylon              |                                                                     | [Ceylon](https://ceylon-lang.org)                                                              |            |                      |
|                     | `cirru`                                                             | [Cirru](http://text.cirru.org)                                                                 |            | `cirru`              |
| cisco               |                                                                     | Cisco CLI                                                                                      |            |                      |
| clean               | dcl, icl                                                            | [Clean](http://clean.cs.ru.nl)                                                                 | functional |                      |
| clojure-repl        |                                                                     | [Clojure REPL](https://clojure.org)                                                            | lisp       |                      |
| `clojure`           | `clj`, `edn`                                                        | [Clojure](https://clojure.org)                                                                 | lisp       | `clojure`            |
| `clue`              |                                                                     | [Clue](https://crates.io/crates/clue)                                                          | system     | `clue`               |
| `cmake`             | `cmake.in`                                                          | [CMake](https://cmake.org)                                                                     |            | `makefile`           |
|                     | `cobol`, `cbl`, `cob`                                               | [Cobol](https://en.wikipedia.org/wiki/COBOL)                                                   | enterprise | `cobol`              |
| `coffeescript`      | `coffee`, `cson`, `iced`                                            | [CoffeeScript](https://coffeescript.org)                                                       | scripting  | `coffee`             |
|                     | `coldfusion`, `cfm`, `cfc`                                          | [ColdFusion](https://en.wikipedia.org/wiki/Adobe_ColdFusion)                                   |            | `coldfusion`         |
| coq                 |                                                                     | [Coq](https://coq.inria.f)                                                                     | functional |                      |
| cos                 | cls                                                                 | Caché Object Script                                                                            | enterprise |                      |
| cpc                 |                                                                     | CpcdosC+                                                                                       |            |                      |
| `cpp`               | `cc`, `c++`, `h++`, `hpp`, `hh`, `hxx`, `cxx`                       | [C++](https://isocpp.org)                                                                      | system     | `c_cpp`              |
| `crmsh`             | `crm`, `pcmk`                                                       | [crmsh](http://crmsh.github.io)                                                                | config     | `sh`                 |
| `crystal`           | `cr`                                                                | [Crystal](https://crystal-lang.org)                                                            | scripting  | `crystal`            |
| `csharp`            | `cs`, `c#`                                                          | [C\#](https://docs.microsoft.com/en-us/dotnet/csharp)                                          | common     | `csharp`             |
|                     | `csound_document`, `csd`                                            | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_document`    |
|                     | `csound_orchestra`, `orc`                                           | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_orchestra`   |
|                     | `csound_score`, `sco`                                               | [Csound](https://csound.com/get-started.html#what-is-csound)                                   |            | `csound_score`       |
| `csp`               |                                                                     | [CSP (ContentSecurityPolicy)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)           |            | `csp`                |
| `css`               |                                                                     | [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)                                        | web        | `css`                |
|                     | `csv`                                                               | [Comma-Separated Values](https://en.wikipedia.org/wiki/Comma-separated_values)                 | data       | `csv`                |
| curl                |                                                                     | cURL                                                                                           |            |                      |
|                     | `curly`                                                             | [Curly](https://9seconds.github.io/curly)                                                      | template   | `curly`              |
|                     | `cuttlefish`                                                        | Cuttlefish config                                                                              | config     | `cuttlefish`         |
| cypher              |                                                                     | Cypher (Neo4j)                                                                                 |            |                      |
| `d`                 |                                                                     | [D](https://dlang.org)                                                                         |            | `d`                  |
| dafny               |                                                                     | Dafny                                                                                          |            |                      |
| `dart`              |                                                                     | [Dart](https://dart.dev)                                                                       | scripting  | `dart`               |
| `delphi`            | `dpr`, `dfm`, `pas`, `pascal`                                       | [Delphi](https://www.embarcadero.com/products/delphi)                                          | common     | `pascal`             |
| `diff`              | `patch`                                                             | [Diff](https://www.gnu.org/software/diffutils)                                                 | common     | `diff`               |
| `django`            | `jinja`                                                             | [Django](https://www.djangoproject.com)                                                        | template   | `django`             |
| dns                 | bind, zone                                                          | [DNS Zone](https://en.wikipedia.org/wiki/Zone_file)                                            | config     |                      |
| `dockerfile`        | `docker`                                                            | [Dockerfile](https://docs.docker.com/engine/reference/builder/)                                | config     | `dockerfile`         |
| `dos`               | `bat`, `cmd`                                                        | [Batch file (DOS)](https://en.wikipedia.org/wiki/Batch_file)                                   |            | `batchfile`          |
| dsconfig            |                                                                     | dsconfig                                                                                       | config     |                      |
|                     | `drools`, `drl`                                                     | [Drools](https://en.wikipedia.org/wiki/Drools)                                                 | enterprise | `drools`             |
| dts                 |                                                                     | [Device Tree](https://elinux.org/Device_Tree_Reference)                                        | config     |                      |
|                     | `dot`                                                               | [DOT (graph description language)](https://graphviz.org/doc/info/lang.html)                    | graphical  | `dot`                |
| dust                | dst                                                                 | [Dust](https://www.dustjs.com)                                                                 | template   |                      |
| dylan               |                                                                     | Dylan                                                                                          |            |                      |
| ebnf                |                                                                     | [Extended Backus-Naur Form](https://en.wikipedia.org/wiki/Extended_Backus–Naur_form)           |            |                      |
|                     | `edifact`, `edi`                                                    | [UN/EDIFACT](https://en.wikipedia.org/wiki/EDIFACT)                                            | protocol   | `edifact`            |
|                     | `eiffel`, `e`, `ge`                                                 | [Eiffel](https://www.eiffel.org)                                                               |            | `eiffel`             |
|                     | `ejs`                                                               | [EJS (Embedded JavaScript templating)](https://ejs.co)                                         | template   | `ejs`                |
| `elixir`            | `ex`, `exs`                                                         | [Elixir](https://elixir-lang.org)                                                              | functional | `elixir`             |
| `elm`               |                                                                     | [Elm](https://elm-lang.org)                                                                    | functional | `elm`                |
| `erb`               |                                                                     | [ERB (Embedded Ruby)](https://ruby-doc.org/stdlib-2.6.5/libdoc/erb/rdoc/ERB.html)              | template   | `html_ruby`          |
| erlang-repl         |                                                                     | [Erlang REPL]( https://www.erlang.org)                                                         | functional |                      |
| `erlang`            | `erl`                                                               | [Erlang]( https://www.erlang.org)                                                              | functional | `erlang`             |
| excel               | xls, xlsx                                                           | [Excel formulae](https://products.office.com/en-us/excel)                                      |            |                      |
| extempore           | xtlang, xtm                                                         | Extempore                                                                                      |            |                      |
| fix                 |                                                                     | FIX                                                                                            |            |                      |
| `flix`              |                                                                     | [Flix](https://flix.dev)                                                                       | common     | `flix`               |
|                     | `forth`, `frt`, `ldr`, `fth`, `4th`                                 | [Forth](https://www.forth.com/forth)                                                           |            | `forth`              |
| `fortran`           | `f90`, `f95`                                                        | [Fortran](https://en.wikipedia.org/wiki/Fortran)                                               | scientific | `fortran`            |
| `fsharp`            | `fs`, `f#`                                                          | [F#](https://docs.microsoft.com/en-us/dotnet/fsharp)                                           | functional | `fsharp`             |
|                     | `fsl`                                                               | [FSL (FEMAG script language)](https://script.profemag.ch/content/FSL/intro.html)               | scientific | `fsl`                |
|                     | `ftl`                                                               | [FreeMarker Template Language](https://freemarker.apache.org)                                  | template   | `ftl`                |
| gams                | gms                                                                 | [GAMS](https://www.gams.com)                                                                   | scientific |                      |
| gauss               | gss                                                                 | [GAUSS](https://www.aptech.com)                                                                | scientific |                      |
| `gdscript`          | `gd`                                                                | [GDScript (Godot)](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/index.html) | scripting  | `gdscript`           |
| `gdshader`          | `gdshaderinc`                                                       | [Godot Shading Language](https://docs.godotengine.org/en/stable/tutorials/shaders/shader_reference/shading_language.html) | graphics   | `gdshader`           |
| `gdresource`        | `tres`, `tscn`                                                      | [Godot Resource/Scene](https://docs.godotengine.org/en/stable/contributing/development/file_formats/tscn.html) | config     | `gdresource`         |
| `gcode`             | `nc`                                                                | [G-code](https://www.sis.se/api/document/preview/911952)                                       |            | `gcode`              |
| `gherkin`           | `feature`                                                           | [Gherkin](https://cucumber.io/docs/gherkin)                                                    |            | `gherkin`            |
|                     | `gitignore`, `.gitignore`                                           | [.gitignore](https://git-scm.com/docs/gitignore)                                               | config     | `gitignore`          |
| `glsl`              |                                                                     | [GLSL (OpenGL Shading Language)](https://en.wikipedia.org/wiki/OpenGL_Shading_Language)        | graphics   | `glsl`               |
| gml                 |                                                                     | [GML (Game Maker Language)](https://docs2.yoyogames.com)                                       | scripting  |                      |
|                     | `gobstones`, `gbs`                                                  | [Gobstones](https://es.wikipedia.org/wiki/Gobstones)                                           |            | `gobstones`          |
| `go`                | `golang`                                                            | [Go](http://golang.org)                                                                        | common     | `golang`             |
| golo                |                                                                     | [Golo](http://golo-lang.org)                                                                   |            |                      |
| gradle              |                                                                     | [Gradle](https://gradle.org)                                                                   |            |                      |
|                     | `graphqlschema`, `gql`                                              | [GraphQL schema](https://graphql.org)                                                          | query      | `graphqlschema`      |
| `groovy`            |                                                                     | [Groovy](https://groovy-lang.org)                                                              |            | `groovy`             |
|                     | `groq`                                                              | [GROQ](https://www.sanity.io/docs/groq)                                                        | query      | `groq`               |
| `haml`              |                                                                     | [HAML](http://haml.info)                                                                       | template   | `haml`               |
| `handlebars`        | `hbs`, `html.hbs`, `html.handlebars`, `htmlbars`                    | [Handlebars](https://handlebarsjs.com)                                                         | template   | `handlebars`         |
| `haskell`           | `hs`                                                                | [Haskell](https://www.haskell.org)                                                             | functional | `haskell`            |
|                     | `haskell_cabal`, `cabal`                                            | [Haskell Cabal](https://www.haskell.org/cabal)                                                 |            | `haskell_cabal`      |
| `haxe`              | `hx`                                                                | [Haxe]( https://haxe.org)                                                                      |            | `haxe`               |
|                     | `hjson`                                                             | [Hjson, a user interface for JSON](https://hjson.github.io)                                    | config     | `hjson`              |
| hsp                 |                                                                     | [HSP (Hot Soup Processor)](https://en.wikipedia.org/wiki/Hot_Soup_Processor)                   | scripting  |                      |
|                     | `eex`, `html_elixir`, `html.eex`                                    | HTML with Embedded Elixir (EEx)                                                                | template   | `html_elixir`        |
|                     | `html_ruby`, `erb`, `html.erb`                                      | HTML with Embedded Ruby (ERB)                                                                  | template   | `html_ruby`          |
| http                | https                                                               | [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)                             | protocol   |                      |
| `hy`                | `hylang`                                                            | [Hy](http://docs.hylang.org/en/stable)                                                         | lisp       | `lisp`               |
| inform7             | i7                                                                  | [Inform 7](http://inform7.com)                                                                 | markup     |                      |
| `ini`               | `toml`                                                              | [TOML, also INI](https://github.com/toml-lang/toml)                                            | config     | `ini`, `toml`        |
|                     | `io`                                                                | [io](https://iolanguage.org)                                                                   |            | `io`                 |
|                     | `ion`                                                               | [ion](https://github.com/ion-lang/ion)                                                         | ion        | `ion`                |
| irpf90              |                                                                     | [IRPF90](http://irpf90.ups-tlse.fr)                                                            | scientific |                      |
| isbl                |                                                                     | ISBL                                                                                           | enterprise |                      |
|                     | `jack`                                                              | [Jack](https://classes.engineering.wustl.edu/cse365/jack.php)                                  |            | `jack`               |
|                     | `jade`, `pug`                                                       | [Pug (formerly Jade)](https://pugjs.org)                                                       | template   | `jade`               |
| `java`              | `jsp`                                                               | [Java](https://www.java.com)                                                                   | common     | `java`, `jsp`        |
| `javascript`        | `js`, `jsx`, `mjs`, `cjs`                                           | [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)                          | scripting  | `javascript`, `jsx`  |
|                     | `jexl`                                                              | [JEXL](https://github.com/TomFrost/Jexl)                                                       | scripting  | `jexl`               |
| `jsdoc`             | `jsdoc_comment`                                                     | [JSDoc](https://jsdoc.app)                                                                     |            | `javascript`         |
| jboss-cli           | wildfly-cli                                                         | [JBoss CLI](https://docs.jboss.org/author/display/WFLY/Command+Line+Interface)                 | config     |                      |
| `json`              |                                                                     | [JSON (JavaScript Object Notation)](http://www.json.org)                                       | config     | `json`               |
|                     | `json5`                                                             | [JSON5](https://json5.org)                                                                     | config     | `json5`              |
|                     | `jsoniq`, `jq`                                                      | [JSONiq](http://www.jsoniq.org)                                                                |            | `jsoniq`             |
|                     | `jssm`, `jssm_state`                                                | JSSM (JavaScript State Machine)                                                                |            | `jssm`               |
| julia-repl          | jldoctest                                                           | [Julia REPL](https://julialang.org)                                                            |            |                      |
| `julia`             |                                                                     | [Julia](https://julialang.org)                                                                 | common     | `julia`              |
| `kotlin`            | `kot`, `kt`, `kts`                                                  | [Kotlin](https://kotlinlang.org)                                                               | common     | `kotlin`             |
| lasso               | ls, lassoscript                                                     | [Lasso](http://www.lassosoft.com/What-Is-Lasso)                                                |            |                      |
| `latex`             | `tex`                                                               | [LaTeX](https://www.latex-project.org)                                                         | markup     | `latex`, `tex`       |
|                     | `latte`                                                             | [Latte](https://latte-lang.org)                                                                |            | `latte`              |
| ldif                |                                                                     | [LDIF](https://en.wikipedia.org/wiki/LDAP_Data_Interchange_Format)                             | config     |                      |
| leaf                |                                                                     | [Leaf](https://vapor.github.io/documentation/guide/leaf.html)                                  |            |                      |
| `less`              |                                                                     | [Less](http://lesscss.org)                                                                     | web        | `less`               |
|                     | `liquid`                                                            | [Liquid](https://shopify.github.io/liquid/basics/introduction)                                 | template   | `liquid`             |
| `lisp`              |                                                                     | Lisp                                                                                           | lisp       | `lisp`               |
| livecodeserver      |                                                                     | LiveCode                                                                                       | enterprise |                      |
| `livescript`        | `ls`                                                                | [LiveScript](https://livescript.net)                                                           | scripting  | `livescript`         |
| llvm                |                                                                     | [LLVM IR](https://llvm.org/docs/LangRef.html)                                                  | assembler  |                      |
|                     | `logiql`, `lql`, `logic`                                            | LogiQL (LogicBlox)                                                                             | database   | `logiql`             |
|                     | `logtalk`, `lgt`                                                    | [Logtalk](https://logtalk.org)                                                                 |            | `logtalk`            |
| `lsl`               |                                                                     | [LSL (Linden Scripting Language)](http://wiki.secondlife.com/wiki/LSL_Portal)                  | scripting  | `lsl`                |
| `lua`               |                                                                     | [Lua](https://www.lua.org)                                                                     | scripting  | `lua`                |
|                     | `luapage`, `lp`                                                     | Lua Pages                                                                                      | template   | `luapage`            |
|                     | `lucene`                                                            | [Apache Lucene query syntax](https://lucene.apache.org)                                        | query      | `lucene`             |
| `makefile`          | `mk`, `mak`, `make`                                                 | [Makefile](https://www.gnu.org/software/make/manual/html_node/Introduction.html)               | common     | `makefile`           |
|                     | `mariadb`                                                           | [MariaDB](https://mariadb.org)                                                                 | database   | `mariadb`            |
| `markdown`          | `md`, `mkd`, `mkdown`                                               | [Markdown](https://daringfireball.net/projects/markdown)                                       | markup     | `markdown`           |
|                     | `mask`                                                              | [MaskJS](https://github.com/atmajs/MaskJS)                                                     | template   | `mask`               |
| mathematica         | mma, wl                                                             | [Wolfram Language](https://www.wolfram.com/mathematica)                                        | scientific |                      |
| `matlab`            |                                                                     | [Matlab](https://www.mathworks.com/products/matlab.html)                                       | scientific | `matlab`             |
| maxima              |                                                                     | [Maxima](http://maxima.sourceforge.net)                                                        | scientific |                      |
|                     | `maze`, `mz`                                                        | Maze (esoteric language)                                                                       |            | `maze`               |
|                     | `mediawiki`, `wiki`                                                 | [MediaWiki markup](https://www.mediawiki.org/wiki/Help:Formatting)                             | markup     | `mediawiki`          |
| `mel`               |                                                                     | [MEL (Maya Embedded Language)](http://www.autodesk.com/products/autodesk-maya/overview)        | graphics   | `mel`                |
| mercury             | m, moo                                                              | [Mercury](https://www.mercurylang.org)                                                         | functional |                      |
| `mipsasm`           | `mips`                                                              | [MIPS Assembly](https://en.wikipedia.org/wiki/MIPS_architecture)                               | assembler  | `mips`               |
|                     | `mixal`                                                             | [MIXAL (MIX assembly)](https://en.wikipedia.org/wiki/MIX_(abstract_machine))                   | assembler  | `mixal`              |
| mizar               |                                                                     | [Mizar](http://mizar.org/language)                                                             | scientific |                      |
| mojolicious         |                                                                     | [Mojolicious](https://mojolicious.org)                                                         | template   |                      |
| monkey              |                                                                     | [Monkey](https://blitzresearch.itch.io/monkey2)                                                |            |                      |
| moonscript          | moon                                                                | [MoonScript](http://moonscript.org)                                                            | scripting  |                      |
|                     | `mushcode`, `mc`, `mush`                                            | [MUSHcode](https://en.wikipedia.org/wiki/Softcode)                                             | scripting  | `mushcode`           |
|                     | `mysql`                                                             | [MySQL](https://www.mysql.com)                                                                 | database   | `mysql`              |
| n1ql                |                                                                     | [N1QL (Couchbase query language)](https://www.couchbase.com/products/n1ql)                     |            |                      |
|                     | `nasal`, `nas`                                                      | [Not Another Scripting LAnguage](https://mathieugouin.github.io/nasal)                         | scripting  | `nasal`              |
| nestedtext          | nt                                                                  | [NestedText](https://nestedtext.org)                                                           | config     |                      |
| `nginx`             | `nginxconf`                                                         | [Nginx config](https://www.nginx.com)                                                          | config     | `nginx`              |
| `nim`               |                                                                     | [Nim](https://nim-lang.org)                                                                    | system     | `nim`                |
| `nix`               | `nixos`                                                             | [Nix](http://nixos.org/nix)                                                                    |            | `nix`                |
| node-repl           |                                                                     | Node REPL                                                                                      | scripting  |                      |
| `nsis`              |                                                                     | [NSIS (Nullsoft Scriptable Install System)](https://nsis.sourceforge.io/Main_Page)             |            | `nsis`               |
|                     | `nunjucks`, `nunjs`, `nj`, `njk`                                    | [Nunjucks](https://mozilla.github.io/nunjucks)                                                 | template   | `nunjucks`           |
| `objectivec`        | `mm`, `objc`, `obj-c`, `obj-c++`, `objective-c++`                   | [Objective-C](https://developer.apple.com/documentation/objectivec)                            | common     | `objectivec`         |
| `ocaml`             | `ml`                                                                | [OCaml]( https://ocaml.org)                                                                    | functional | `ocaml`              |
| `odin`              |                                                                     | [Odin](https://odin-lang.org)                                                                  | system     | `odin`               |
| `openscad`          | `scad`                                                              | [OpenSCAD](https://www.openscad.org)                                                           | scientific | `scad`               |
| oxygene             |                                                                     | [Oxygene](https://www.elementscompiler.com/elements/default.aspx)                              |            |                      |
| parser3             |                                                                     | [Parser3](https://www.parser.ru/en)                                                            | template   |                      |
|                     | `partiql`, `pql`                                                    | [PartiQL](https://partiql.org)                                                                 |            | `partiql`            |
| `perl`              | `pl`, `pm`                                                          | [Perl](https://www.perl.org)                                                                   | common     | `perl`               |
| pf                  | pf.conf                                                             | [Packet Filter config](http://man.openbsd.org/pf.conf)                                         | config     |                      |
| `pgsql`             | `postgres`, `postgresql`                                            | [PostgreSQL and PL/pgSQL](https://www.postgresql.org/docs/11/sql.html)                         |            | `pgsql`              |
| php-template        |                                                                     | [PHP Template](https://www.php.net)                                                            | common     |                      |
| `php`               |                                                                     | [PHP](https://www.php.net)                                                                     | common     | `php`                |
|                     | `php_laravel_blade`, `blade.php`                                    | [Laravel Blade](https://laravel.com/docs/blade)                                                | template   | `php_laravel_blade`  |
|                     | `pig`                                                               | [Apache Pig](https://pig.apache.org)                                                           |            | `pig`                |
| `plaintext`         | `text`, `txt`, `plain_text`                                         | Plain text without any highlighting                                                            |            | `text`, `plain_text` |
|                     | `plsql`                                                             | [PL/SQL](https://en.wikipedia.org/wiki/PL/SQL)                                                 | database   | `plsql`              |
| pony                |                                                                     | [Pony](https://www.ponylang.io)                                                                |            |                      |
| `powershell`        | `pwsh`, `ps`, `ps1`                                                 | [PowerShell](https://docs.microsoft.com/en-us/powershell)                                      |            | `powershell`         |
|                     | `praat`, `praatscript`, `psc`, `proc`                               | [Praat scripts](https://www.fon.hum.uva.nl/praat)                                              | scientific | `praat`              |
|                     | `prisma`                                                            | [Prisma schema](https://www.prisma.io)                                                         | database   | `prisma`             |
| `processing`        | `pde`                                                               | [Processing](https://processing.org)                                                           | graphics   | `c_cpp`              |
| profile             |                                                                     | Python profiler                                                                                |            |                      |
| `prolog`            |                                                                     | [Prolog](https://en.wikipedia.org/wiki/Prolog)                                                 | logic      | `prolog`             |
| `properties`        |                                                                     | .properties                                                                                    | config     | `properties`         |
| `protobuf`          |                                                                     | [Protocol Buffers](https://developers.google.com/protocol-buffers/docs/proto3)                 | protocols  | `protobuf`           |
|                     | `prql`                                                              | [PRQL](https://prql-lang.org)                                                                  | query      | `prql`               |
| `puppet`            | `pp`                                                                | [Puppet](https://puppet.com/docs)                                                              | config     | `puppet`             |
| `purebasic`         | `pb`, `pbi`                                                         | [PureBASIC](https://www.purebasic.com)                                                         |            | `vbscript`           |
| python-repl         | pycon                                                               | Python REPL                                                                                    | common     |                      |
| `python`            | `py`, `gyp`, `ipython`                                              | [Python](https://www.python.org)                                                               | common     | `python`             |
| q                   | k, kdb                                                              | [Q](https://kx.com/connect-with-us/developers)                                                 |            |                      |
| `qml`               | `qt`                                                                | [QML](https://doc.qt.io/qt-5/qmlapplications.html)                                             | scripting  | `qml`                |
| qsharp              |                                                                     | Q#                                                                                             |            |                      |
| `r`                 |                                                                     | [R](https://www.r-project.org)                                                                 | scientific | `r`                  |
|                     | `raku`, `rakumod`, `rakutest`, `p6`, `pl6`, `pm6`                   | [Raku (formerly Perl 6)](https://raku.org)                                                     | common     | `raku`               |
|                     | `razor`, `cshtml`                                                   | Razor (ASP.NET)                                                                                | template   | `razor`              |
|                     | `rdoc`, `rd`                                                        | [RDoc](https://ruby.github.io/rdoc)                                                            | markup     | `rdoc`               |
| reasonml            | re                                                                  | [ReasonML](https://reasonml.github.io)                                                         | functional |                      |
|                     | `red`, `reds`                                                       | [Red](https://www.red-lang.org)                                                                |            | `red`                |
|                     | `redshift`                                                          | Amazon Redshift SQL                                                                            | database   | `redshift`           |
|                     | `rhtml`                                                             | R HTML (knitr)                                                                                 | template   | `rhtml`              |
| rib                 |                                                                     | [RenderMan RIB](https://renderman.pixar.com/resources/RenderMan_20/ribBinding.html)            | graphics   |                      |
| roboconf            | graph, instances                                                    | [Roboconf](http://roboconf.net)                                                                | config     |                      |
|                     | `robot`, `resource`                                                 | [Robot Framework](https://robotframework.org)                                                  |            | `robot`              |
| routeros            |                                                                     | [Microtik RouterOS script](https://wiki.mikrotik.com/wiki/Manual:Scripting)                    |            |                      |
| rsl                 |                                                                     | [RenderMan RSL](https://renderman.pixar.com/resources/RenderMan_20/shadingLanguage.html)       | graphics   |                      |
|                     | `rst`, `rest`                                                       | [reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText)                             |            | `rst`                |
| `ruby`              | `gemspec`, `irb`, `podspec`, `rb`, `thor`                           | [Ruby](https://www.ruby-lang.org)                                                              | common     | `ruby`               |
| ruleslanguage       |                                                                     | [Oracle Rules Language](https://docs.oracle.com/cd/E17904_01/dev.1111/e10227/rlref.htm)        | enterprise |                      |
| `rust`              | `rs`                                                                | [Rust](https://www.rust-lang.org)                                                              | common     | `rust`               |
|                     | `sac`                                                               | [SAC](https://en.wikipedia.org/wiki/SAC_programming_language)                                  |            | `sac`                |
| sas                 |                                                                     | SAS                                                                                            |            |                      |
|                     | `sass`                                                              | [Sass (indented syntax)](https://sass-lang.com)                                                | web        | `sass`               |
| `scala`             |                                                                     | [Scala](https://www.scala-lang.org)                                                            | functional | `scala`              |
| `scheme`            |                                                                     | [Scheme](http://community.schemewiki.org/?what-is-scheme)                                      | lisp       | `scheme`             |
| scilab              | sci                                                                 | [Scilab](https://www.scilab.org)                                                               | scientific |                      |
|                     | `scrypt`                                                            | [sCrypt](https://scrypt.io)                                                                    |            | `scrypt`             |
| `scss`              |                                                                     | [SCSS](https://sass-lang.com)                                                                  | web        | `scss`               |
| `shell`             | `console`, `shellsession`                                           | Shell Session                                                                                  | common     | `sh`                 |
|                     | `sjs`                                                               | StratifiedJS                                                                                   | scripting  | `sjs`                |
|                     | `slim`, `skim`                                                      | [Slim](https://slim-template.github.io)                                                        | template   | `slim`               |
| smali               |                                                                     | [Smali](https://github.com/JesusFreke/smali)                                                   |            |                      |
| smalltalk           | st                                                                  | [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk)                                           |            |                      |
|                     | `smarty`                                                            | [Smarty](https://www.smarty.net)                                                               | template   | `smarty`             |
|                     | `smithy`                                                            | [Smithy](https://smithy.io)                                                                    |            | `smithy`             |
| sml                 | ml                                                                  | [SML (Standard ML)](https://www.smlnj.org)                                                     | functional |                      |
|                     | `snippets`                                                          | Ace snippets                                                                                   |            | `snippets`           |
| solidity            | sol                                                                 | Solidity                                                                                       |            |                      |
|                     | `soy`, `soy_template`                                               | [Closure Templates (Soy)](https://github.com/google/closure-templates)                         | template   | `soy_template`       |
|                     | `space`                                                             | Space (Tree Notation)                                                                          |            | `space`              |
|                     | `sparql`, `rq`                                                      | [SPARQL](https://www.w3.org/TR/sparql11-query)                                                 | query      | `sparql`             |
| spl                 |                                                                     | Splunk SPL                                                                                     |            |                      |
| sqf                 |                                                                     | [SQF](https://community.bistudio.com/wiki/SQF_syntax)                                          | scripting  |                      |
| `sql`               |                                                                     | [SQL](https://en.wikipedia.org/wiki/SQL)                                                       | database   | `sql`                |
|                     | `sqlserver`                                                         | Microsoft SQL Server (T-SQL)                                                                   | database   | `sqlserver`          |
| stan                | stanfuncs                                                           | [Stan probabilistic programming language](http://mc-stan.org)                                  | scientific |                      |
| stata               | ado, do                                                             | [Stata](https://en.wikipedia.org/wiki/Stata)                                                   | scientific |                      |
| step21              | p21, step, stp                                                      | [STEP Part 21](https://en.wikipedia.org/wiki/ISO_10303-21)                                     |            |                      |
| structured-text     | iecst, scl, stl                                                     | Structured Text                                                                                |            |                      |
| `stylus`            | `styl`                                                              | [Stylus](https://github.com/stylus/stylus)                                                     | web        | `stylus`             |
| subunit             |                                                                     | [SubUnit](https://pypi.org/project/python-subunit)                                             |            |                      |
| supercollider       | sc                                                                  | Supercollider                                                                                  |            |                      |
| svelte              |                                                                     |                                                                                                |            |                      |
|                     | `svg`                                                               | [SVG](https://developer.mozilla.org/docs/Web/SVG)                                              | web        | `svg`                |
| `swift`             |                                                                     | [Swift](https://swift.org)                                                                     | common     | `swift`              |
| taggerscript        |                                                                     | [Tagger Script](https://picard.musicbrainz.org)                                                |            |                      |
| tap                 |                                                                     | [Test Anything Protocol](https://testanything.org)                                             |            |                      |
| `tcl`               | `tk`                                                                | [Tcl](https://www.tcl.tk/about/language.html)                                                  |            | `tcl`                |
|                     | `terraform`, `tf`, `tfvars`, `terragrunt`                           | [Terraform (HCL)](https://www.terraform.io)                                                    | config     | `terraform`          |
|                     | `textile`                                                           | [Textile](https://textile-lang.com)                                                            | markup     | `textile`            |
| thrift              |                                                                     | [Thrift](https://thrift.apache.org)                                                            | protocols  |                      |
| toit                |                                                                     | [Toit](https://toitware.com)                                                                   |            |                      |
| tp                  |                                                                     | TP                                                                                             |            |                      |
|                     | `turtle`, `ttl`                                                     | [Turtle (RDF)](https://www.w3.org/TR/turtle)                                                   | data       | `turtle`             |
| `twig`              | `craftcms`                                                          | [Twig](https://twig.symfony.com)                                                               | template   | `twig`               |
| `typescript`        | `ts`, `tsx`                                                         | [TypeScript](https://www.typescriptlang.org)                                                   | common     | `typescript`, `tsx`  |
| `tsv`               |                                                                     | [Tab-Separated Values](https://en.wikipedia.org/wiki/Tab-separated_values)                     | data       | `tsv`                |
| unicorn-rails-log   |                                                                     | Unicorn Rails log                                                                              |            |                      |
| `vala`              |                                                                     | [Vala](https://wiki.gnome.org/Projects/Vala)                                                   |            | `vala`               |
| `vbnet`             | `vb`                                                                | [Visual Basic .NET](https://docs.microsoft.com/dotnet/visual-basic/getting-started)            | common     | `vbscript`           |
| vbscript-html       |                                                                     | [VBScript in HTML](https://en.wikipedia.org/wiki/VBScript)                                     | scripting  |                      |
| `vbscript`          | `vbs`                                                               | [VBScript](https://en.wikipedia.org/wiki/VBScript)                                             | scripting  | `vbscript`           |
|                     | `velocity`, `vm`                                                    | [Apache Velocity](https://velocity.apache.org)                                                 | template   | `velocity`           |
| `verilog`           | `sv`, `svh`, `v`                                                    | [Verilog](http://www.verilog.com)                                                              |            | `verilog`            |
| `vhdl`              |                                                                     | [VHDL](https://en.wikipedia.org/wiki/VHDL)                                                     |            | `vhdl`               |
| vim                 |                                                                     | [Vim Script](https://www.vim.org)                                                              | scripting  |                      |
|                     | `visualforce`, `vfp`, `component`, `page`                           | Visualforce (Salesforce)                                                                       | enterprise | `visualforce`        |
|                     | `vue`                                                               | [Vue single-file components](https://vuejs.org)                                                | web        | `vue`                |
| wasm                |                                                                     | [WebAssembly](https://webassembly.org)                                                         | web        |                      |
|                     | `wollok`, `wlk`, `wpgm`, `wtest`                                    | [Wollok](https://github.com/uqbar-project/wollok)                                              |            | `wollok`             |
| wren                |                                                                     | [Wren](https://wren.io)                                                                        | scripting  |                      |
| x++                 | axapta                                                              | X++                                                                                            |            |                      |
| `x86asm`            |                                                                     | [Intel x86 Assembly](https://en.wikipedia.org/wiki/X86_assembly_language)                      | assembler  | `assembly_x86`       |
| xsharp              | xs, prg                                                             | X#                                                                                             |            |                      |
| xl                  | tao                                                                 | [XL](http://xlr.sf.net)                                                                        |            |                      |
| `xml`               | `atom`, `html`, `plist`, `rss`, `wsf`, `xhtml`, `xjb`, `xsd`, `xsl` | [HTML, XML](https://www.w3.org/XML)                                                            |            | `xml`, `html`        |
| `xquery`            | `xpath`, `xq`                                                       | [XQuery](https://www.w3.org/XML/Query)                                                         | functional | `xquery`             |
| `yaml`              | `yml`                                                               | [YAML](https://yaml.org)                                                                       | config     | `yaml`               |
|                     | `zeek`, `bro`                                                       | [Zeek](https://zeek.org)                                                                       | scripting  | `zeek`               |
| zenscript           | zs                                                                  | ZenScript                                                                                      |            |                      |
| zephir              | zep                                                                 | [Zephir](https://zephir-lang.com/en)                                                           |            |                      |
|                     | `zig`                                                               | [Zig](https://ziglang.org)                                                                     | common     | `zig`                |


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
| `adb`               | `ada`               |
| `alda`              | `alda`              |
| `apache`            | `apache_conf`       |
| `apacheconf`        | `apache_conf`       |
| `apache_conf`       | `apache_conf`       |
| `htaccess`          | `apache_conf`       |
| `htgroups`          | `apache_conf`       |
| `htpasswd`          | `apache_conf`       |
| `apex`              | `apex`              |
| `cls`               | `apex`              |
| `trigger`           | `apex`              |
| `tgr`               | `apex`              |
| `applescript`       | `applescript`       |
| `oascript`          | `applescript`       |
| `astro`             | `astro`             |
| `aql`               | `aql`               |
| `arduino`           | `c_cpp`             |
| `ino`               | `c_cpp`             |
| `armasm`            | `assembly_arm32`    |
| `arm`               | `assembly_arm32`    |
| `assembly_arm32`    | `assembly_arm32`    |
| `arm32`             | `assembly_arm32`    |
| `asl`               | `asl`               |
| `dsl`               | `asl`               |
| `asl.json`          | `asl`               |
| `asciidoc`          | `asciidoc`          |
| `adoc`              | `asciidoc`          |
| `aspectj`           | `java`              |
| `autohotkey`        | `autohotkey`        |
| `ahk`               | `autohotkey`        |
| `avrasm`            | `assembly_x86`      |
| `asm`               | `assembly_x86`      |
| `a`                 | `assembly_x86`      |
| `bash`              | `sh`                |
| `sh`                | `sh`                |
| `basic`             | `basic`             |
| `bas`               | `basic`             |
| `bibtex`            | `bibtex`            |
| `bib`               | `bibtex`            |
| `c`                 | `c_cpp`             |
| `h`                 | `c_cpp`             |
| `c9search`          | `c9search`          |
| `c9search_results`  | `c9search`          |
| `cedar`             | `cedar`             |
| `cedarschema`       | `cedarschema`       |
| `cirru`             | `cirru`             |
| `clojure`           | `clojure`           |
| `clj`               | `clojure`           |
| `cljs`              | `clojure`           |
| `edn`               | `clojure`           |
| `clue`              | `clue`              |
| `cmake`             | `makefile`          |
| `cmake.in`          | `makefile`          |
| `cobol`             | `cobol`             |
| `cbl`               | `cobol`             |
| `cob`               | `cobol`             |
| `coffeescript`      | `coffee`            |
| `coffee`            | `coffee`            |
| `cakefile`          | `coffee`            |
| `cf`                | `coffee`            |
| `cson`              | `coffee`            |
| `iced`              | `coffee`            |
| `coldfusion`        | `coldfusion`        |
| `cfm`               | `coldfusion`        |
| `cfc`               | `coldfusion`        |
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
| `csd`               | `csound_document`   |
| `csound_orchestra`  | `csound_orchestra`  |
| `orc`               | `csound_orchestra`  |
| `csound_score`      | `csound_score`      |
| `sco`               | `csound_score`      |
| `csp`               | `csp`               |
| `css`               | `css`               |
| `csv`               | `csv`               |
| `curly`             | `curly`             |
| `cuttlefish`        | `cuttlefish`        |
| `d`                 | `d`                 |
| `di`                | `d`                 |
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
| `djt`               | `django`            |
| `dockerfile`        | `dockerfile`        |
| `docker`            | `dockerfile`        |
| `dos`               | `batchfile`         |
| `bat`               | `batchfile`         |
| `cmd`               | `batchfile`         |
| `batchfile`         | `batchfile`         |
| `prql`              | `prql`              |
| `drools`            | `drools`            |
| `drl`               | `drools`            |
| `dot`               | `dot`               |
| `edifact`           | `edifact`           |
| `edi`               | `edifact`           |
| `eiffel`            | `eiffel`            |
| `e`                 | `eiffel`            |
| `ge`                | `eiffel`            |
| `ejs`               | `ejs`               |
| `elixir`            | `elixir`            |
| `ex`                | `elixir`            |
| `exs`               | `elixir`            |
| `elm`               | `elm`               |
| `erlang`            | `erlang`            |
| `erl`               | `erlang`            |
| `hrl`               | `erlang`            |
| `eex`               | `html_elixir`       |
| `flix`              | `flix`              |
| `forth`             | `forth`             |
| `frt`               | `forth`             |
| `ldr`               | `forth`             |
| `fth`               | `forth`             |
| `4th`               | `forth`             |
| `fortran`           | `fortran`           |
| `f90`               | `fortran`           |
| `f95`               | `fortran`           |
| `f`                 | `fortran`           |
| `fsharp`            | `fsharp`            |
| `fsi`               | `fsharp`            |
| `fs`                | `fsharp`            |
| `fsx`               | `fsharp`            |
| `fsscript`          | `fsharp`            |
| `f#`                | `fsharp`            |
| `fsl`               | `fsl`               |
| `ftl`               | `ftl`               |
| `gdscript`          | `gdscript`          |
| `gd`                | `gdscript`          |
| `gdshader`          | `gdshader`          |
| `gdshaderinc`       | `gdshader`          |
| `gdresource`        | `gdresource`        |
| `tres`              | `gdresource`        |
| `tscn`              | `gdresource`        |
| `gcode`             | `gcode`             |
| `nc`                | `gcode`             |
| `gherkin`           | `gherkin`           |
| `feature`           | `gherkin`           |
| `gitignore`         | `gitignore`         |
| `.gitignore`        | `gitignore`         |
| `glsl`              | `glsl`              |
| `frag`              | `glsl`              |
| `vert`              | `glsl`              |
| `gobstones`         | `gobstones`         |
| `gbs`               | `gobstones`         |
| `go`                | `golang`            |
| `golang`            | `golang`            |
| `graphqlschema`     | `graphqlschema`     |
| `gql`               | `graphqlschema`     |
| `groq`              | `groq`              |
| `groovy`            | `groovy`            |
| `haml`              | `haml`              |
| `handlebars`        | `handlebars`        |
| `hbs`               | `handlebars`        |
| `html.hbs`          | `handlebars`        |
| `html.handlebars`   | `handlebars`        |
| `htmlbars`          | `handlebars`        |
| `tpl`               | `handlebars`        |
| `mustache`          | `handlebars`        |
| `haskell`           | `haskell`           |
| `hs`                | `haskell`           |
| `haskell_cabal`     | `haskell_cabal`     |
| `cabal`             | `haskell_cabal`     |
| `haxe`              | `haxe`              |
| `hx`                | `haxe`              |
| `hjson`             | `hjson`             |
| `html_elixir`       | `html_elixir`       |
| `html.eex`          | `html_elixir`       |
| `html_ruby`         | `html_ruby`         |
| `erb`               | `html_ruby`         |
| `html.erb`          | `html_ruby`         |
| `hy`                | `lisp`              |
| `hylang`            | `lisp`              |
| `ini`               | `ini`               |
| `conf`              | `ini`               |
| `cfg`               | `ini`               |
| `prefs`             | `ini`               |
| `io`                | `io`                |
| `ion`               | `ion`               |
| `jack`              | `jack`              |
| `jade`              | `jade`              |
| `pug`               | `jade`              |
| `java`              | `java`              |
| `jsp`               | `jsp`               |
| `javascript`        | `javascript`        |
| `js`                | `javascript`        |
| `jsm`               | `javascript`        |
| `jsx`               | `jsx`               |
| `cjs`               | `javascript`        |
| `mjs`               | `javascript`        |
| `mts`               | `typescript`        |
| `cts`               | `typescript`        |
| `str`               | `typescript`        |
| `jexl`              | `jexl`              |
| `jsdoc`             | `javascript`        |
| `jsdoc_comment`     | `javascript`        |
| `json`              | `json`              |
| `json5`             | `json5`             |
| `jsoniq`            | `jsoniq`            |
| `jq`                | `jsoniq`            |
| `jssm`              | `jssm`              |
| `jssm_state`        | `jssm`              |
| `julia`             | `julia`             |
| `jl`                | `julia`             |
| `kotlin`            | `kotlin`            |
| `kot`               | `kotlin`            |
| `kt`                | `kotlin`            |
| `kts`               | `kotlin`            |
| `latex`             | `latex`             |
| `ltx`               | `latex`             |
| `tex`               | `tex`               |
| `latte`             | `latte`             |
| `less`              | `less`              |
| `liquid`            | `liquid`            |
| `lisp`              | `lisp`              |
| `livescript`        | `livescript`        |
| `ls`                | `livescript`        |
| `logiql`            | `logiql`            |
| `lql`               | `logiql`            |
| `logtalk`           | `logtalk`           |
| `lgt`               | `logtalk`           |
| `lsl`               | `lsl`               |
| `lua`               | `lua`               |
| `luapage`           | `luapage`           |
| `lp`                | `luapage`           |
| `lucene`            | `lucene`            |
| `makefile`          | `makefile`          |
| `make`              | `makefile`          |
| `mak`               | `makefile`          |
| `mk`                | `makefile`          |
| `gnumakefile`       | `makefile`          |
| `ocamlmakefile`     | `makefile`          |
| `mariadb`           | `mariadb`           |
| `markdown`          | `markdown`          |
| `md`                | `markdown`          |
| `mkd`               | `markdown`          |
| `mkdown`            | `markdown`          |
| `mask`              | `mask`              |
| `matlab`            | `matlab`            |
| `maze`              | `maze`              |
| `mz`                | `maze`              |
| `mediawiki`         | `mediawiki`         |
| `wiki`              | `mediawiki`         |
| `mel`               | `mel`               |
| `mipsasm`           | `mips`              |
| `mips`              | `mips`              |
| `mixal`             | `mixal`             |
| `mushcode`          | `mushcode`          |
| `mc`                | `mushcode`          |
| `mush`              | `mushcode`          |
| `mysql`             | `mysql`             |
| `nasal`             | `nasal`             |
| `nginx`             | `nginx`             |
| `nginxconf`         | `nginx`             |
| `nas`               | `nasal`             |
| `nim`               | `nim`               |
| `nix`               | `nix`               |
| `nixos`             | `nix`               |
| `nsis`              | `nsis`              |
| `nsh`               | `nsis`              |
| `nsi`               | `nsis`              |
| `nunjucks`          | `nunjucks`          |
| `nunjs`             | `nunjucks`          |
| `nj`                | `nunjucks`          |
| `njk`               | `nunjucks`          |
| `objectivec`        | `objectivec`        |
| `mm`                | `objectivec`        |
| `objc`              | `objectivec`        |
| `obj-c`             | `objectivec`        |
| `obj-c++`           | `objectivec`        |
| `objective-c++`     | `objectivec`        |
| `ocaml`             | `ocaml`             |
| `ml`                | `ocaml`             |
| `mli`               | `ocaml`             |
| `odin`              | `odin`              |
| `openscad`          | `scad`              |
| `scad`              | `scad`              |
| `partiql`           | `partiql`           |
| `pql`               | `partiql`           |
| `perl`              | `perl`              |
| `pl`                | `perl`              |
| `pm`                | `perl`              |
| `pgsql`             | `pgsql`             |
| `postgres`          | `pgsql`             |
| `postgresql`        | `pgsql`             |
| `php`               | `php`               |
| `inc`               | `php`               |
| `phtml`             | `php`               |
| `shtml`             | `php`               |
| `php3`              | `php`               |
| `php4`              | `php`               |
| `php5`              | `php`               |
| `phps`              | `php`               |
| `phpt`              | `php`               |
| `aw`                | `php`               |
| `ctp`               | `php`               |
| `module`            | `php`               |
| `php_laravel_blade` | `php_laravel_blade` |
| `blade.php`         | `php_laravel_blade` |
| `pig`               | `pig`               |
| `plain_text`        | `plain_text`        |
| `text`              | `text`              |
| `txt`               | `text`              |
| `plsql`             | `plsql`             |
| `powershell`        | `powershell`        |
| `pwsh`              | `powershell`        |
| `ps`                | `powershell`        |
| `ps1`               | `powershell`        |
| `praat`             | `praat`             |
| `praatscript`       | `praat`             |
| `psc`               | `praat`             |
| `proc`              | `praat`             |
| `prisma`            | `prisma`            |
| `processing`        | `c_cpp`             |
| `pde`               | `c_cpp`             |
| `prolog`            | `prolog`            |
| `plg`               | `prolog`            |
| `properties`        | `properties`        |
| `protobuf`          | `protobuf`          |
| `proto`             | `protobuf`          |
| `puppet`            | `puppet`            |
| `pp`                | `puppet`            |
| `epp`               | `puppet`            |
| `purebasic`         | `vbscript`          |
| `pb`                | `vbscript`          |
| `pbi`               | `vbscript`          |
| `python`            | `python`            |
| `py`                | `python`            |
| `gyp`               | `python`            |
| `ipython`           | `python`            |
| `pyi`               | `python`            |
| `qml`               | `qml`               |
| `qt`                | `qml`               |
| `r`                 | `r`                 |
| `raku`              | `raku`              |
| `rakumod`           | `raku`              |
| `rakutest`          | `raku`              |
| `p6`                | `raku`              |
| `pl6`               | `raku`              |
| `pm6`               | `raku`              |
| `razor`             | `razor`             |
| `cshtml`            | `razor`             |
| `rdoc`              | `rdoc`              |
| `rd`                | `rdoc`              |
| `red`               | `red`               |
| `reds`              | `red`               |
| `redshift`          | `redshift`          |
| `rhtml`             | `rhtml`             |
| `robot`             | `robot`             |
| `resource`          | `robot`             |
| `rst`               | `rst`               |
| `rest`              | `rst`               |
| `ruby`              | `ruby`              |
| `gemspec`           | `ruby`              |
| `irb`               | `ruby`              |
| `podspec`           | `ruby`              |
| `guardfile`         | `ruby`              |
| `rakefile`          | `ruby`              |
| `gemfile`           | `ruby`              |
| `rb`                | `ruby`              |
| `rake`              | `ruby`              |
| `thor`              | `ruby`              |
| `rust`              | `rust`              |
| `rs`                | `rust`              |
| `sac`               | `sac`               |
| `sass`              | `sass`              |
| `scala`             | `scala`             |
| `sbt`               | `scala`             |
| `scheme`            | `scheme`            |
| `scm`               | `scheme`            |
| `sm`                | `scheme`            |
| `rkt`               | `scheme`            |
| `oak`               | `scheme`            |
| `logic`             | `logiql`            |
| `scrypt`            | `scrypt`            |
| `scss`              | `scss`              |
| `shell`             | `sh`                |
| `console`           | `sh`                |
| `shellsession`      | `sh`                |
| `sjs`               | `sjs`               |
| `slim`              | `slim`              |
| `skim`              | `slim`              |
| `smarty`            | `smarty`            |
| `smithy`            | `smithy`            |
| `soy`               | `soy_template`      |
| `soy_template`      | `soy_template`      |
| `space`             | `space`             |
| `sparql`            | `sparql`            |
| `rq`                | `sparql`            |
| `sql`               | `sql`               |
| `sqlserver`         | `sqlserver`         |
| `stylus`            | `stylus`            |
| `styl`              | `stylus`            |
| `swift`             | `swift`             |
| `snippets`          | `snippets`          |
| `tcl`               | `tcl`               |
| `tk`                | `tcl`               |
| `terraform`         | `terraform`         |
| `tf`                | `terraform`         |
| `tfvars`            | `terraform`         |
| `terragrunt`        | `terraform`         |
| `toml`              | `toml`              |
| `textile`           | `textile`           |
| `turtle`            | `turtle`            |
| `ttl`               | `turtle`            |
| `twig`              | `twig`              |
| `swig`              | `twig`              |
| `craftcms`          | `twig`              |
| `typescript`        | `typescript`        |
| `ts`                | `typescript`        |
| `tsv`               | `tsv`               |
| `tsx`               | `tsx`               |
| `vala`              | `vala`              |
| `vbnet`             | `vbscript`          |
| `vb`                | `vbscript`          |
| `vbscript`          | `vbscript`          |
| `vbs`               | `vbscript`          |
| `velocity`          | `velocity`          |
| `vm`                | `velocity`          |
| `verilog`           | `verilog`           |
| `sv`                | `verilog`           |
| `svh`               | `verilog`           |
| `v`                 | `verilog`           |
| `vh`                | `verilog`           |
| `vhdl`              | `vhdl`              |
| `vhd`               | `vhdl`              |
| `visualforce`       | `visualforce`       |
| `vfp`               | `visualforce`       |
| `component`         | `visualforce`       |
| `page`              | `visualforce`       |
| `vue`               | `vue`               |
| `wollok`            | `wollok`            |
| `wlk`               | `wollok`            |
| `wpgm`              | `wollok`            |
| `wtest`             | `wollok`            |
| `x86asm`            | `assembly_x86`      |
| `xml`               | `xml`               |
| `atom`              | `xml`               |
| `html`              | `html`              |
| `plist`             | `xml`               |
| `rss`               | `xml`               |
| `wsdl`              | `xml`               |
| `xslt`              | `xml`               |
| `svg`               | `svg`               |
| `wsf`               | `xml`               |
| `xbl`               | `xml`               |
| `xhtml`             | `html`              |
| `xjb`               | `xml`               |
| `xsd`               | `xml`               |
| `xsl`               | `xml`               |
| `htm`               | `html`              |
| `we`                | `html`              |
| `wpy`               | `html`              |
| `mathml`            | `xml`               |
| `mml`               | `xml`               |
| `rdf`               | `xml`               |
| `xaml`              | `xml`               |
| `xul`               | `xml`               |
| `xquery`            | `xquery`            |
| `xpath`             | `xquery`            |
| `xq`                | `xquery`            |
| `yaml`              | `yaml`              |
| `yml`               | `yaml`              |
| `zeek`              | `zeek`              |
| `bro`               | `zeek`              |
| `zig`               | `zig`               |

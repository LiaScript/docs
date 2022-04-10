<!--

author:   André Dietrich
email:    LiaScript@web.de
version:  19.0.9
language: en
narrator: UK English Female

logo:     https://liascript.github.io/img/bg-showcase-1.jpg

comment:  This document shall provide an entire compendium and course on the
          development of Open-courSes with [LiaScript](https://LiaScript.github.io).
          As the language and the systems grows, also this document will be updated.
          Feel free to fork or copy it, translations are very welcome...

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

link: https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

link: https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css

-->


# LiaScript

> To see this document as an interactive LiaScript rendered version, click on the
> following link/badge:
>
> [![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md)
>
> If you need help, feel free to ask us any questions in the chat:
>
> [![Gitter](https://badges.gitter.im/LiaScript/community.svg)](https://gitter.im/LiaScript/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


                            --{{0}}--
With LiaScript, we tried to implement an extended
[Markdown](https://en.wikipedia.org/wiki/Markdown) format that should enable
everyone to create, share, adapt, translate or correct online courses without
the need of being a web-developer. We believe that a language-based approach,
instead of a tooling-centered one, provides more flexibility, freedom of
creativity, and sustainability. Therefor we tried to develop a simplistic syntax
that extends the static Markdown with quizzes, animations, spoken text,
automated visualization [ASCII-art](https://en.wikipedia.org/wiki/ASCII_art) and
much more. Everything has been woven around Markdown, so that the content can
still be read and interpreted with any kind of editor or Markdown-interpreter.


**What is LiaScript?**

* a Markdown dialect for interactive courses and data-driven publishing,
* everything is implemented in Elm/JavaScript and runs directly within the
  browser (online),
* the interpreter itself is also a reader, which allows for storing documents as
  well as the progress,
* courses can also be taken offline, since the interpreter is also a progressive
  web app (PWA), that allows to store documents and progress directly within
  the browser (locally),
* everything is private, we do not store any data about the courses nor the
  users and their progress


                            --{{1}}--
There are a couple of problems that we currently see in the creation of
[Open educational resources (OER)](https://en.wikipedia.org/wiki/Open_educational_resources).
One of them is isolation, that means people, who want to create content, are
seldomly connected via the applied technologies, instead, they are separated by
platforms, authoring tools and used core technologies (programming languages).
Furthermore, it is not possible to simply grab an educational website/project
and to adapt its content for another audience. Additionally, it seems to be
nearly impossible for people without a technical background to simply set up a
small course. Thus, they stuck with Word, PowerPoint, and PDF, since they
provide a simple continuation of the static formats people have used before the
computer-era.
"_If I want to publish content for the computer, I want my audience to dive in, experiment, simulate, play with the content... but not only read._"

                              {{1}}
********************************************************************************

**Goals**

* Simplicity: with a human-centered markup-language, anyone should be enabled to
  create and modify content.
* Interactive: the browser is the next operating systems and although content
  with LiaScript is developed within a "static" markup-language it should not be
  presented that way.
* Extendability: everything that is not part of LiaScript shall be embeddable
  and importable.
* Durability: platforms go down, the development of proprietary software/formats
  is discontinued, but LiaScript is not hosted on one platform (it can be
  hosted everywhere) and even without the LiaScript interpreter the content is
  still readable and interpretable with every editor; you could even print or
  engrave it on stone or clay. Furthermore, if you use some kind of versioning
  system (e.g. [git](https://en.wikipedia.org/wiki/Git)) you can refer to any
  previous version of your course.

********************************************************************************

                           --{{2}}--
Imagine a world where everyone would have the same access to high quality
educational content for free. Imagine all kind of schoolbooks, technical or
scientific literature could become open-courSe projects and more interactive,
with collaborating teachers and students. Everything that is required is a
simple text-editor and a web-browser.

                             {{2}}
![OER logo](https://upload.wikimedia.org/wikipedia/commons/2/20/Global_Open_Educational_Resources_Logo.svg)


## Tools

                           --{{0}}--
As already mentioned all you need to work with LiaScript is an text-editor, but
it can be usefull to apply one of the following tools. At least we apply them to
see the result of a change within the course document immediately. You will see,
that the development of online-courses will speed up, especially if there is no
need for memorizing complex point and click sequences.

> "_Let the editor be your canvas and the keyboard your brush._"

### Editing

**Atom:**

                           --{{0}}--
There are currently 2 plugins for the [Atom Editor](https://atom.io/) available,
which are intended to ease and simplify the development of online courses with
LiaScript.

![Atom with liascript-plugins](https://raw.githubusercontent.com/andre-dietrich/liascript-preview/master/preview.gif "Screencast of the Atom-editor with the liascript-preview and liascript-snippts installed.")

0. [Atom](https://atom.io): This is the free and open and official
   [GitHub](https://github.com) editor, with lots of plugins for various use
   cases.
1. [liascript-preview](https://atom.io/packages/liascript-preview): Is a tiny
   previewer that, if it was toggled ( `Alt+L` ), updates the view on your
   course each time you save your document.
2. [liascript-snippets](https://atom.io/packages/liascript-snippets): If you
   start typing `lia` in your Markdown document you switch on a fuzzy search,
   that contains a lot of LiaScript help, examples, and snippets.



                             {{1}}
********************************************************************************

**LiaScript-DevServer:**

                           --{{1}}--
If you are used to another editor, you can also start a LiaScript development
server locally. It works like the plugin for Atom and updates your course within
your browser on every save, but this can also be used to monitor multiple
projects. And you can also use it for testing purposes, as if you would deploy
your projects.

![liascript-devserver](https://raw.githubusercontent.com/liascript/liascript-devserver/main/pics/navigation.gif "Screencast of the liascript-devserver while navigating through a folder-structure.")

Get the project from:

* npmjs: https://www.npmjs.com/package/@liascript/devserver
* GitHub: https://github.com/LiaScript/LiaScript-DevServer

********************************************************************************


                             {{2}}
********************************************************************************

**CodiLIA:**

                           --{{2}}--
If you prefer to work with multiple authors simultaneously, then you should give
[CodiLIA](https://github.com/liascript/codilia) a try. It is a fork of the
collaborative editor
[CodiMD/Hedgehoc](https://github.com/hedgedoc/hedgedoc/tree/master), but instead
of a Markdown preview, you will have a LiaScript preview, and you can
immediately publish your courses.

Project: https://github.com/liascript/codilia

!?[CodiLIA deploy to Heroku](https://www.youtube.com/watch?v=AERiykLvcoQ "**Movie:** A HowTo deploy CodiLIA server to Heroku for free.")

********************************************************************************

### Projects

                           --{{0}}--
The easiest way of importing a LiaScript into another website or
[Learning Management System (LMS)](https://en.wikipedia.org/wiki/Learning_management_system)
such as
[Moodle](https://en.wikipedia.org/wiki/Moodle),
[ILIAS](https://en.wikipedia.org/wiki/ILIAS), or
[OPAL](https://de.wikipedia.org/wiki/OPAL_%28Lernplattform%29), is via importing
an external website or if possible via an
[`iframe`](https://en.wikipedia.org/wiki/HTML_element#Frames).

!?[LiaScript embed into OPAL](https://www.youtube.com/watch?v=c97m2guiAeA "Movie: Screencast of a LiaScript course that is hosted via CodiLIA and imported as an external resource into OPAL.")


                             {{1}}
********************************************************************************

**LiaScript-Exporter:**

                           --{{1}}--
However, there might be cases where you want to store the progress within the
LMS. We therefor have developed an experimental exporter, which allows to bundle
your entire project as an
[SCORM](https://en.wikipedia.org/wiki/Sharable_Content_Object_Reference_Model)
compliant zip-file that can be imported into most common LMS. Other formats than
SCORM can be added too, simply write us a mail or create an issue, if you
require another one.

* npmjs: https://www.npmjs.com/package/@liascript/exporter
* GitHub: https://github.com/liascript/liascript-exporter

********************************************************************************


                             {{2}}
********************************************************************************

**Preview-Lia:**

                           --{{2}}--
If you want to refer to your own courses or to foreign ones on your personal
website or blog, you can make use of our "preview web component". This creates
preview cards, which are updated at client-side, so that there is no need to
manually update all information whenever there is a change in the course. Simply
add the `script` tag as depicted in the code-snippet and link to your courses
via the tag `preview-lia`.

``` html
<html>
  <head>
    <script type="text/javascript" src="https://liascript.github.io/course/preview-lia.js"></script>
  </head>
  <body>
    ...
    <preview-lia src="https://raw.githubusercontent.com/liaScript/docs/master/README.md">
    </preview-lia>

    <preview-lia src="https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md">
    </preview-lia>

    ...
  </body>
</html>
```

> For more information visit the blog entry:
> [Markdown just got a new preview tag](https://aizac.herokuapp.com/markdown-just-got-a-new-preview-tag)
>
> _However, you can also use this to refer to your personal GitHub projects._

********************************************************************************


                           --{{3}}--
LiaScript was originally developed for supporting programming courses for
embedded systems. You can see an example of the previous eLab remote laboratory
installation.

                             {{3}}
!?[eLab demonstrator](https://www.youtube.com/watch?v=bICfKRyKTwE "**Movie:** A review on the historical eLab system, the predecessor to LiaScript.")

                           --{{4}}--
Now it is the opposite, our main focus lays in the development of the Markup
language, but parts of the old systems can still be used. Especially if you want
to teach programming in (_Java_, _C_, _C++_, _C#_, _Mono_, _Go_ and _Python_).
The CodeRunner is an open-source project that enables remote compiling and
execution of code. We apply it to teach procedural and object-oriented
programming. You can either host your own server or use our free herokuapp:

       {{4}}
> **CodeRunner:**
>
> * GitHub: https://github.com/liascript/CodeRunner
>
> * Try the interactive LiaScript version at:
>
>   https://liascript.github.io/course/?https://github.com/liascript/CodeRunner
>
> * Or if you want to import this functionality into your course, then add the
>   following statement into the main header of your LiaScript course:
>
>   `import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md`


### Publishing

                           --{{0}}--
By now you should have a basic idea of what you can do with LiaScript, but
probably not how you can publish your courses. The best way is actually to use
[GitHub](https://github.com), this way no prior versions of your course get
lost, and you give others (you can even invite them) the opportunity to
contribute to your project.

                           --{{1}}--
No further hosting is required, no further compilation step, the JavaScript
interpreter of LiaScript does everything else directly within the browser at
client-side.

                           --{{2}}--
As you can see from the _example_, it is also possible to refer to a specific
slide. You only have to add a `#` with the number of the slide, or you can add
the name of the specific slide as well.

                           --{{3}}--
You can also add additional tags to your project to make it discoverable. We
currently use three distict categories: `liascript` to mark it to be related to
the projects, while the others `liascript-course` and `liascript-template` are
used to distinguish the projects into courses or extension, which can be added
to courses.

                           --{{4}}--
The same way you can also refer to courses that you have put into your
[DropBox](https://en.wikipedia.org/wiki/Dropbox_%28service%29),
[ownCloud](https://en.wikipedia.org/wiki/OwnCloud),
[NextCloud](https://en.wikipedia.org/wiki/Nextcloud), or if you have access to
some old-fashioned webspace then you can also store all of your files there. You
only have to make them publically available and to refer to the raw or in other
words, the text document. All other sources are loaded relative to this URL.

0. Create a free account at https://github.com
1. Refer to your projects as via a URL parameter:

   `https://LiaScript.github.io/course/?YOUR_RAW_COURSE_URL.md`

2. Example with reference to a specific slide:

   https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md#5

3. Make your document discoverable by adding the tags `liascript` and or
   `liascript-course`, `liascript-template` to make it appear in one of the
   following GitHub topics:

   - general: https://github.com/topics/liascript
   - free courses: https://github.com/topics/liascript-course
   - extensions: https://github.com/topics/liascript-template

   _More information on tagging projects can be found [here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)._

4. Use other ways of hosting repositories as well (e.g.
   [DropBox](https://en.wikipedia.org/wiki/Dropbox_%28service%29),
   [ownCloud](https://en.wikipedia.org/wiki/OwnCloud),
   [NextCloud](https://en.wikipedia.org/wiki/Nextcloud)).

#### LiaBooks

                           --{{0}}--
However, we have no idea who is using LiaScript elsewhere, so it might be hard
to find some resources online. From time to time we translate open-books into
LiaScript and make them more interactive. You can see some of our the
experiments at the following URL and use them as a source of inspiration:

https://github.com/LiaBooks

![screenshot of the LiaBooks repository](img/screenshot_liabooks.png)

> __Full overview on courses via the topic `liascript-course`:__
>
> https://github.com/topics/liascript-course


#### LiaTemplates

                           --{{0}}--
If you tried out CodeRunner, you will have probably noticed that you can reuse
functionality from different courses, simply by using the keyword `import:`
within the main definition of your LiaScript document. Such a functionality is
defined with the help of macros. We will dive deeper into this feature at the
end of this document, but if you are interested you can inspect some of our
templates, which shall provide self-explaining courses of how to embed and use
the implemented macros.

https://github.com/LiaTemplates

![screenshot of the LiaTemplates repository](img/screenshot_liatemplates.png)

> __Full overview on extensions via the topic `liascript-template`:__
>
> https://github.com/topics/liascript-template

## Markdown-Syntax

                          --{{0}}--
This section is intended to give a brief overview on the basic Markdown syntax
elements. The only difference to common Markdown at this point is, that you can
define meta-information such as author, language, voice, etc. within a
HTML-comment at the beginning of every document. We will describe all of these
elements in more detail in [section: Macros](#macros). All of these `macros`
start with a single word, which is followed by a colon. If you require more
space, like for `comment:` or `link:` you can use multiple lines, but every
following line has to start with an indentation.

Initial LIA-comment-tag for basic definitions:

``` XML
<!--

author:   Andre Dietrich

email:    LiaScript@web.de

version:  0.0.1

language: en

narrator: US English Female

comment:  Write a short abstract of your course, that
          might contain multiple lines and sentences.

script:   https://javascript_resourse_url

script:   https://another_javascript_resourse_url

link:     https://some_css_stuff
          https://and_some_more_css
-->
```


                          --{{1}}--
The meta-information from your document is later shown within the
information-section as well as within the home-section.

                            {{1}}
![Screencast of meta-information usage](img/meta-information.gif)



                          --{{2}}--
If you already know Markdown, then you can skip most of the content in this
section. However, there are some slight differences that will be marked with a
trailing star at the section title.

            {{2}}
<!-- style="font-size: 2em" -->
> Something might be different 💫


### Structuring

                          --{{0}}--
A course is structured as any other Markdown document with starting hash-tags,
whereby the number of hash-tags is used to define the hierarchy of your
document.

<!-- class="translate"-->
```markdown
# Main Title

 ...

## Section Title 1

 ...

### Subsection Title

 ...
## Section Title 2
```

                          --{{1}}--
Every section is presented separately. In contrast to most Markdown-parsers,
LiaScript applies a two step-approach. Sections are parsed at first, which means
that the parsers searches for patterns as depicted below. Parsing the content of
a section is quite time-consuming, that is why the section-content gets only
analyzed, if this specific section should be displayed to the user. However,
this happens only at the first appearance, afterwards the resulting view is
restored from a local cache.

                            {{1}}
**Preprocessing pattern:** `## foo bar`


#### Sub-Titles 💫

                          --{{0}}--
There might be some cases, where you want to add further headings. We therefor
apply the following syntax with underlining "equal signs" or "dashes". In
common Markdown, this alternative syntax is applied to define level-1 and
level-2 headings. We use it to create headings that are one level `=` or two
levels `-` below the main heading. However, these subsections will not be part
of the table of contents, and since their interpretation is slightly different
to common Markdown, it should be avoided.

<!-- class="translate"-->
```markdown
...

## Section Title

Local Subsection
================

Local Sub-SubSection
--------------------
```

### Content blocks

                          --{{0}}--
How would you separate paragraphs or other content elements from each other, if
you only have a type-writer? The easiest way is a spatial separation, and in
Markdown this is done via an empty line. Thus, whenever you have blocks such as
paragraphs, enumerations, or tables, it is common practice to separate them via
a newline. This makes it easier for you to edit and structure your course, and
it prevents the interpreter from too much work.

<!-- class="translate"-->
``` markdown
This is a paragraph that consist only of one line.

Here comes another paragraph
with multiple lines.
And multiple sentences.
```

### Text-Formatting 💫


                            --{{0}}--
How does text-highlighting work in a text file and thus within a paragraph?
Well, Markdown defines some basic characters that can be used to surround a word
or a collection of words. We tried to use the GitHub flavored Markdown style for
simple formatting, thus simply use multiple asterisks or underscores to mark
certain parts of a text.

* `*italic*` -> *italic*<!-- class="notranslate"-->
* `**bold**` -> **bold**<!-- class="notranslate"-->
* `***bold and italic ***` -> ***bold and italic ***<!-- class="notranslate"-->
* `_also italic_` -> _also italic_<!-- class="notranslate"-->
* `__also bold__` -> __also bold__<!-- class="notranslate"-->
* `___also bold and italic___` -> ___also bold and italic___<!-- class="notranslate"-->
* `~strike~` -> ~strike~<!-- class="notranslate"-->


                          --{{1}}--
We define some additions to common Markdown, such as underline and superscript,
which can be defined with the following syntax:

                            {{1}}
* `~~underline~~` -> ~~underline~~<!-- class="notranslate"-->
* `~~~strike and underline~~~` -> ~~~strike and underline~~~<!-- class="notranslate"-->
* `^superscript^` -> ^superscript^<!-- class="notranslate"-->


#### Combinations

                          --{{0}}--
As you can see from the examples, you can combine and nest all elements freely.


* `**bold _bold italic_**` -> **bold _bold italic_**<!-- class="notranslate"-->
* `**~bold strike~ ~~bold underline~~**` -> **~bold strike~ ~~bold underline~~**<!-- class="notranslate"-->
* `*~italic strike~ ~~italic underline~~*` -> *~italic strike~ ~~italic underline~~*<!-- class="notranslate"-->

#### Escape Characters

                          --{{0}}--
If you want to use asterisks, hash-tags, or other syntax elements within your
document without applying their functionality, then you can escape or in other
words indicate them with a starting backslash. If you want to escape a
backslash, you will have to write two subsequent backslashes. But you do not
have to use it, if there is only one asterisk within a line, this will be
interpreted as a single character. So you will have to apply this kind of
escaping only to prevent misunderstandings between you and the interpreter.


``` markdown
\*, \~, \_, \#, \{, \}, \[, \], \|, \`, \$, \@, \\
```

**Result:** \*, \~, \_, \#, \{, \}, \[, \], \|, \`, \$, \@, \\

### Symbols & Unicode 💫

                          --{{0}}--
One thing that we missed in standard Markdown, was an implementation for arrows.
The verbatim text shows, how arrows are defined in our Markdown implementation with
their result on the right.

`->` ->, `->>` ->>, `>->` >->, `<-` <-, `<-<` <-<,
`<<-` <<-, `<->` <->, `=>` =>, `<=` <=, `<=>` <=>

`-->` -->, `<--` <--, `<-->` <-->, `==>` ==>, `<==` <==, `<==>` <==>

`~>` ~>, `<~` <~

                          --{{1}}--
But you can also use some basic smileys. We will try to extend this partial
support in the future.

                            {{1}}
`:-)` :-), `;-)` ;-), `:-D` :-D, `:-O` :-O, `:-(` :-(, `:-|` :-|,
`:-/` :-/, `:-P` :-P, `:-*` :-*, `:')` :'), `:'(` :'(

                          --{{2}}--
However, since LiaScript accepts
[Unicode](https://en.wikipedia.org/wiki/Unicode), you can also copy and paste
any kind of character including [emojis](https://emojipedia.org).


### References

> The next section shows how external resources can be referenced and integrated.


#### Simple Links

                          --{{0}}--
There are two ways of adding links to a Markdown document, either by inlining
the URL directly or you can name it (as shown in listing 2), by applying the
typical brackets and parenthesis notation, the optional information is put in
double quotes at the end of the URL. This optional information is used as a
title attribute, and it is shown, when the user hovers the link with the mouse.


1. Example of an URL-link -> http://goo.gl/fGXNvu

   text-formatting can be applied also `*** http://goo.gl/fGXNvu ***` ->
   *** http://goo.gl/fGXNvu ***

2. Naming the link (`[title](http://goo.gl/fGXNvu "optional info")`) ->
   [title](http://goo.gl/fGXNvu "optional info")

3. For internal navigation you can refer to the slide number or to title with
   a starting `#`

   * `[next slide](#18)` -> [next slide](#18)
   * `[next slide](#preview-lia-💫)` -> [next slide](#preview-lia-💫)
   * If your internal link includes parentheses or other characters, your can
     also use percent-encoding. An opening parentheses would then be written as
     `%28` and a closing one as `%29`.

     For more information visit:
     https://developer.mozilla.org/en-US/docs/Glossary/percent-encoding

##### Preview-Lia 💫

                          --{{0}}--
LiaScript has an advanced preview link, that will load the remote course and
parse the meta-information such as title, version, comment, logo, email, tags,
form your main HTML-comment at the top of your document. To do this, you will
have to use `[preview-lia]` as the title of your link, which is followed by the
raw URL of your course document.


`[preview-lia](https://raw.githubusercontent.com/LiaScript/docs/master/README.md)`

[preview-lia](https://raw.githubusercontent.com/LiaScript/docs/master/README.md)


                          --{{1}}--
You can use this technique also to create previews for other courses on your
personal website or for other GitHub projects, as it was described in section
[Projects](#projects). For more information follow the link:

{{1}} https://aizac.herokuapp.com/markdown-just-got-a-new-preview-tag/


##### QR-Codes 💫

                          --{{0}}--
Sometimes it might be required to have both, a link and a visual representation
of it as an __QR-Codes__. Similar to previews, you simply name your link
`qr-code`:


* Syntax: `[qr-code](https://LiaScript.github.io)`
* Example:

  [qr-code](https://LiaScript.github.io)

                          --{{1}}--
You can add further information to your link by adding a title. Markdown is also
allowed within the link title. In case of an image or media link, the title will
be used as a subtitle and displayed accordingly.

                            {{1}}
* Syntax: `[qr-code](https://LiaScript.github.io "Checkout the LiaScript website or the __[blog at heroku](https://aizac.herokuapp.com)__")`
* Example:

  [qr-code](https://LiaScript.github.io "Checkout the LiaScript website or the __[blog at heroku](https://aizac.herokuapp.com)__")


#### Images 💫

                          --{{0}}--
Images are defined similar to links, but they are indicated with a starting
exclamation mark.

                          --{{1}}--
The name of the link or the alt-text is not wasted, since it is not displayed
anymore. Instead, it is displayed, if the image cannot be loaded for some
reasons, and it is used by screen readers to give visually impaired people a
hint, of what will be visible on the image. So please, don't leave it empty.

                          --{{2}}--
The URL can be either relative to your Markdown document or it can be absolute,
which means it is pointing to an external resource.

                          --{{3}}--
The optional title in LiaScript is not only used as a title attribute, instead
it is used as a real sub-title for all media links.

<!-- style="font-size: 1.4em" -->
**Image-notation: !\[{1}{`alt-text`}\]({2}{url} {3}{"optional sub-title"})**

                            {{2}}
* relative URL: `![Beautiful Lenna](img/lenna.jpg)`

  ![Beautiful Lenna](img/lenna.jpg)

* absolute URL: `![Annunciation of ...](https://upload.wiki...jpg)`

  ![Annunciation of the brith of Christ](https://upload.wikimedia.org/wikipedia/commons/5/51/Leonardo_da_Vinci_Annunciation.jpg "{3}{*Annunciation c. 1472–1476*: is thought to be Leonardo's earliest complete work}")


                          --{{4}}--
Note, that LiaScript is smart enough to scale your images to the optimal size.
If your image is smaller than the current maximal applicable width, it is shown
in full size. If it is larger, than it is scaled to fit in width and also in
height. You can further click on all images to open them as modal and if the
image is quite large, such as Leonardo's painting, then you can also zoom and
inspect it, by hovering with the mouse or thumb.

                         --{{5}}--
Additionally, if you start a paragraph with an image, LiaScript expects it to be
a floating object, which is depicted with a maximal size of 50% of your
view-port, if it is not smaller than that.

                           {{5}}
********************************************************************************

``` markdown
![Beautiful Lenna](img/lenna.jpg "subtitles are allowed too")
Lorem ipsum dolor sit amet, consectetur adipisicing elit, ...

```

---

![Beautiful Lenna](img/lenna.jpg "subtitles are allowed too") Lorem ipsum dolor
sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut
labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa
qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet,
consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et
dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
laboris nisi ut aliquip ex ea commodo consequat.


********************************************************************************

##### Galleries 💫

                          --{{0}}--
How would you interpret a paragraph full of images? We thought that the only
reasonable depiction of this could be a gallery.

``` markdown
![img1](url) ![img2](url) ![img3](url)
![img4](url)
![img5](url)
```

                          --{{1}}--
And we like this idea... You can click on every image and inspect it also with
the zooming feature.

                            {{1}}
![Portrait of a lady](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg/723px-Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg "La Belle Ferronnière, c. 1490–1498")
![Lady with an Ermine](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Lady_with_an_Ermine_-_Leonardo_da_Vinci_-_Google_Art_Project.jpg/761px-Lady_with_an_Ermine_-_Leonardo_da_Vinci_-_Google_Art_Project.jpg "Lady with an Ermine, c. 1489–1491, Czartoryski Museum, Kraków, Poland")
![Mona Lisa](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg/687px-Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg "Mona Lisa or La Gioconda c. 1503–1516, Louvre, Paris")
![Virgin and Child ](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Leonardo_da_Vinci_-_Virgin_and_Child_with_St_Anne_C2RMF_retouched.jpg/764px-Leonardo_da_Vinci_-_Virgin_and_Child_with_St_Anne_C2RMF_retouched.jpg "The Virgin and Child with Saint Anne, c. 1501–1519, Louvre, Paris")
![The Death of Leonardo da Vinci](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Francois_Ier_Leonard_de_Vinci-Jean_Auguste_Dominique_Ingres.jpg/1276px-Francois_Ier_Leonard_de_Vinci-Jean_Auguste_Dominique_Ingres.jpg "The Death of Leonardo da Vinci, by Ingres, 1818")


#### Audio 💫

                          --{{0}}--
If an exclamation mark indicates visual content, why not using a question mark
to indicate auditive content. (From our perspective it resembles an ear.)
Everything is similar to images and the URLs can be either relative or absolute.

* Syntax: `?[a horse](https://www.w3schools.com/html/horse.mp3 "hear a horse")`
* Example:

  ?[a horse](https://www.w3schools.com/html/horse.mp3 "hear a horse")


                          --{{1}}--
Additionally, you can also directly reference music from the
[SoundCloud](https://Soundcloud.com) website or from
[Music.YouTube](https://music.youtube.com). The associated song will be
automatically embedded for you.

                            {{1}}
* Syntax: `?[soundcloud](https://soundcloud.com/glennmorrison/beethoven-moonlight-sonata)`
* Example:

  ?[soundcloud](https://soundcloud.com/glennmorrison/beethoven-moonlight-sonata)


#### Movies 💫

                          --{{0}}--
Images are marked with a starting exclamation mark before the link, audio by a
starting question mark and movies are made of images and sound, that is why you
combine both marks `!?`. Defining resources this way shows at least the links
correctly in other Markdown parsers or on GitHub. There is baked-in support for
[YouTube](https://YouTube.com), [Vimeo](https://Vimeo.com),
[PeerTube](https://peertube.tv), [DailyMotion](https://www.dailymotion.com) and
[TeacherTube](https://TeacherTube.com), which means that you only have to
include the link and the resource will be embedded appropriately.

**Movie-notation: `!?[alt-text](movie-url)`**

- YouTube: `!?[The Future of Programming](https://www.youtube.com/watch?v=8pTEmbeENF4)`

  !?[The Future of Programming](https://www.youtube.com/watch?v=8pTEmbeENF4)

- relative path: `!?[Something about math](vid/math.mp4)`

  !?[Something about math](vid/math.mp4)

- > # List of supported Video Platforms
  >
  > * [DailyMotion](https://www.dailymotion.com)
  > * [PeerTube](https://peertube.tv)
  > * [TeacherTube](https://TeacherTube.com)
  > * [Video TU-Freiberg](https://video.tu-freiberg.de)
  > * [Vimeo](https://Vimeo.com)
  > * [YouTube](https://YouTube.com)

                          --{{1}}--
If you required more control over your video, such as autoplay, muted,
start-time, and probably also size and colors, the you can also apply custom
styling rules, then you should take a look at the following section:

                            {{1}}
[Customizing-Multimedia](#Customizing-Multimedia)

#### So what is left?? 💫

                          --{{0}}--
If it is something else that you want to embed something else from another
website, then you should try out the link syntax with two starting question
marks. This means, LiaScript will try to use the [oEmbed](https://oembed.com)
service, which is offered by a couple of websites. If this succeeds, this will
embed only a specific part. If it fails, then LiaScript will at least try to
embed the website via an `iframe`.

Examples:

* [SketchFab](https://sketchfab.com): `??[ear model](https://sketchfab.com/3d-models/ear-anatomy-468e2039bde34a3fabb9e90bff9cd56b)`

  ??[ear model](https://sketchfab.com/3d-models/ear-anatomy-468e2039bde34a3fabb9e90bff9cd56b)

* [StoryMaps](https://storymaps.arcgis.com): `??[presentation](https://storymaps.arcgis.com/stories/583f8b48a857442cb8d27411c93a9664)`

  ??[presentation](https://storymaps.arcgis.com/stories/583f8b48a857442cb8d27411c93a9664)

* [CirquitJS](https://www.falstad.com/circuit): `  ??[Simulation: Noninverting Amplifier](https://www.falstad.com/circuit/circuitjs.html?startCircuit=amp-noninvert.txt)`

  ??[Simulation: Noninverting Amplifier](https://www.falstad.com/circuit/circuitjs.html?startCircuit=amp-noninvert.txt)


##### Galleries \#2 💫

                          --{{0}}--
What you have seen previously with images is also possible with any kind of
multimedia link. Simply put everything into one paragraph and LiaScript will
automatically generate a gallery for you:

``` markdown
![img](url) ?[audio](url) !?[movie](url)
??[something else](url)
??[something else](url)
```

![Photo of Jupiter](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Latest_NASA_photo_of_Jupiter_taken_this_Sunday_by_the_Juno_probe.png/1280px-Latest_NASA_photo_of_Jupiter_taken_this_Sunday_by_the_Juno_probe.png)
?[a horse](https://www.w3schools.com/html/horse.mp3 "hear a horse")
!?[Fun with Tables](https://www.youtube.com/watch?v=Y_7q9T5jYHo)
??[VTK VolumeContour](https://kitware.github.io/vtk-js/examples/VolumeContour/index.html)
??[Circuit simulation](https://www.falstad.com/circuit/circuitjs.html?startCircuit=majority.txt)
??[Bust of Nefertiti](https://sketchfab.com/3d-models/bust-of-nefertiti-foia-results-8c60faca6152405e9d35784efa8b9aa1)


## Markdown-Blocks

                          --{{0}}--
So far we had introduced Markdown only on a tiny level, which means, by now you
should know how to emphasize words and phrases within a paragraph, how to add
images and how you can use references to point to internal or external
resources. But, all we did so far is to work with **paragraphs**. But as pointed
out in the quote below, Markdown can do even more.

> ... Markdown’s syntax is comprised entirely of punctuation characters, which
> punctuation characters have been carefully chosen so as to look like what
> they mean. E.g., asterisks around a word actually look like \*emphasis\*.
> Markdown lists look like, well, lists. Even blockquotes look like quoted
> passages of text, assuming you’ve ever used email.
>
> -- Markdown philosophy by
> [John Gruber](https://daringfireball.net/projects/markdown/syntax#philosophy)

                          --{{1}}--
Within the following part we will learn how to deal with Markdown blocks and
how to format your content to define the following elements:

<!-- --{{1}}--
list, blockquotes, tables, custom HTML, horizontal rules and dealing with
code-blocks.
 -->

       {{1}}
1. Lists
2. Blockquotes
3. Tables
4. HTML
5. Code-Snippets
6. Horizontal rules

### Lists

                          --{{0}}--
The GitHub-flavored Markdown supports two types of lists, ordered and unordered
ones, and so does LiaScript. If you every used a typewriter then the following
syntax for lists would look natural to you. The only thing that matters here is
the correct indentation.

> **Use spaces for correct indentation!** Tabs are allowed too, but might be
> confusing, since editors tend to use varying lengths from 2 to 4 spaces to
> display them...

#### Unordered Lists

                          --{{0}}--
To define an unordered list, starting asterisks `*`, pluses `+`, and dashes `-`
can be used and mixed. If one point has more than one line, you can also use
multiple lines to define paragraphs. All other Markdown elements, you will get
to know, can be included in the same way.

**Markdown-Syntax:**

<!-- class="translate"-->
``` markdown
* alpha
+ **beta**
- gamma
  and delta

  new Paragraph

  - and another
  - important list

- epsilon
```

                          --{{1}}--
As you can see from the result, you can apply all Markdown styling elements
freely. The starting characters will be interpreted equally, thus it makes no
difference, if you use asterisks, pluses and dashes. To improve the readability
of your document, we would recommend to stick with one format for every level.
Starting with asterisks on the first level and dashes within the second level,
etc.

                            {{1}}
********************************************************************************

**Result:**

* alpha
+ **beta**
- gamma
  and delta

  new Paragraph

  - and another
  - important list

- epsilon

********************************************************************************

#### Ordered Lists 💫

                          --{{0}}--

Ordered lists start with a number and a dot. As you can see from the example,
the numbering is important. In contrast to the GitHub flavored Markdown or the
original Markdown, where the list below would result in **two** separate lists,
and the numbering for every list would start at 1, ignoring your numbering
order. With the LiaScript interpretation you can separate your lists, add more
explanations in between, or use animations to make certain parts appear or
disappear.


**Markdown-Syntax:**

<!-- class="translate"-->
``` markdown
0. alpha
1. **beta**

Something else ...

3. * gamma
   * delta
   * and epsilon
2. probably zeta
```

**Result:**

0. alpha
1. **beta**

Something else ...

3. * gamma
   * delta
   * and epsilon
2. probably zeta


### Blockquotes

                          --{{0}}--
If you, from time to time, reply to emails, than the following notation will
look quite familiar to you. To make use of quoted text, simply start a line with
a `>` greater than character.

**Markdown-Syntax:**

<!-- class="translate"-->
``` md
> This was said some time ago ...
>
>> This was said even longer ago,
> > I guess ...
>
> * aleph
> * beth
```

                          --{{1}}--
As you can see from the example, all Markdown elements can be used within a
blockquote and vice versa. Everything you have learned so far can be easily
combined, it could also be a gallery or an embedded object...


                            {{1}}
********************************************************************************

**Result:**

> This was said some time ago ...
>
>> This was said even longer ago,
> > I guess ...
>
> * aleph
> * beth

********************************************************************************

#### Citations 💫

                          --{{0}}--
Blockquotes are often used for citations, and so do we. You can use the
following pattern to mark a blockquote as a citation. Simply use two paragraphs
within a blockquote and start the second one with two dashes `--`.

**LiaScript-Syntax:**

<!-- class="translate"-->
```
> “Live as if you were to die tomorrow.
> Learn as if you were to live forever.”
>
> -- Mahatma Gandhi
```

                          --{{1}}--
The resulting blockquote looks slightly different. Furthermore, the paragraph
followed by dashes is put into and HTML `cite`-tag.

             {{1}}
> “Live as if you were to die tomorrow.
> Learn as if you were to live forever.”
>
> -- Mahatma Gandhi


                          --{{2}}--
You can use this syntax, with starting dashes, everywhere within a LiaScript
document and your corresponding paragraph it will be rendered within a
`cite`-tag. But, at this time it will only affect the representation of
blockquotes. We are not sure yet, how this can also be applied to images,
tables, lists, etc.

             {{2}}
<!-- class="translate"-->
``` md
lorem ipsum ....

-- Some more citations
```

### Tables

                          --{{0}}--
Tables, _as we hope_, are easy to interpret and to create. Simply use horizontal
rules to separate cells. The header is always defined by the first line, while
the second line is used to separate the table header from the body visually and
to define the column alignment.


**Markdown-format:**

<!-- class="translate"-->
``` markdown
| Tables               |      Are      |  Cool |
| -------------------- |:-------------:| -----:|
| *** columns 3 is *** | right-aligned | $1600 |
| ** column 2 is **    |   centered    |   $12 |
| * zebra stripes *    |   are neat    |    $1 |
```

                          --{{1}}--
As you can see in the result, you can sort tables, by clicking onto the icon
that appears on the right of every header cell. A table will then be either
sorted ascending, descending, or not sorted, which means your initial row order
will be restored.

                            {{1}}
********************************************************************************

**Result:**

| Tables               |      Are      |  Cool |
| -------------------- |:-------------:| -----:|
| *** columns 3 is *** | right-aligned | $1600 |
| ** column 2 is **    |   centered    |   $12 |
| * zebra stripes *    |   are neat    |    $1 |

********************************************************************************

                          --{{2}}--
The position of the colon defines whether a column should be centered, aligned
to the left or to the right. By default, if you do not use colons, all columns
are aligned to the left.


          {{2}}
* centered --> `:---:`
* right --> `---:`
* left --> `:---` or `---` (default)


#### Tables <--> Data (Demo) 💫

                          --{{0}}--
But why stopping here? A table, in many cases, is just a representation of a
dataset. If so, why not simply visualizing it accordingly and plot a graph,
display a chart or a map, or whatever fits the most for your data. At the moment
we apply simple rules to identify the nature of your dataset and thus choose a
visual representation.

> For more details have a look at section [Fun With Tables](#fun-with-tables),
> which provides and extensive overview onto all supported representation
> schemes.

                          --{{1}}--
The easiest and probably most obvious representation of a simple plot, would be
the following. A header with some names and columns that contain numbers. The
first column is interpreted as the main column and thus defines the <var>x</var>
values, the rest is up to you. A cell is then only associated with a number, if
the first "word", _sequence of characters separated by a space_, can be parsed
as a number. The `0km` within this example gets ignored. So if you want certain
values to be ignored, simply attach something directly to the number, or add a
character in front of it.


          {{1}}
``` md
| x's |  some y's  |                  dist |
| --- |:----------:| ---------------------:|
| 1   |    1 \$    |                 16 km |
| 2.2 |    2 \$    |                 12 km |
| 3.3 |    5 \$    |                  1 km |
| 4   | -12.333 \$ | 0km _will be ignored_ |
```

                          --{{2}}--
LiaScript identifies this pattern and automatically adds a button above the
table, which allows to switch between the table and the "line chart"
representation. You can modify the chart interactively and even download the
resulting image.

          {{2}}
<!-- class="notranslate"-->
| x's |  some y's  |                  dist |
| --- |:----------:| ---------------------:|
| 1   |    1 \$    |                 16 km |
| 2.2 |    2 \$    |                 12 km |
| 3.3 |    5 \$    |                  1 km |
| 4   | -12.333 \$ | 0km _will be ignored_ |


                            --{{3}}--
A function cannot possess different <var>y</var>-values for one
<var>x</var>-value, thus, if you have two or more equal <var>x</var>-values, the
resulting plot will be a scatter plot.

           {{3}}
``` markdown
| x's |  some y's  |  dist |
| --- |:----------:| -----:|
| 1   |    1 \$    | 16 km |
| 2.2 |    2 \$    | 12 km |
| 3.3 |    5 \$    |  1 km |
| 4   | -12.333 \$ | -5 km |
| 4   |            |     1 |
```

           {{3}}
<!-- class="notranslate"-->
| x's |  some y's  |  dist |
| --- |:----------:| -----:|
| 1   |    1 \$    | 16 km |
| 2.2 |    2 \$    | 12 km |
| 3.3 |    5 \$    |  1 km |
| 4   | -12.333 \$ | -5 km |
| 4   |            |     1 |


                                   --{{4}}--
Last but not least _bar-charts_. If the first column contains at least one cell,
that cannot be parsed as a number while the others do have, then this table gets
interpreted as a bar-chart. The first column thus defines your set of groups. It
is now also possible to sort your table according to different columns, and to
see this ordering also within the bar-chart representation.


                               {{4}}
```markdown
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |
```

                               {{4}}
<!-- class="notranslate"-->
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


                          --{{5}}--
As mentioned earlier, this is only a brief introduction into this topic. So
check out section [Fun With Tables](#fun-with-tables) for a complete overview.

#### Editing

                          --{{0}}--
Editing tables might seem tedious, but actually it is not. There is a huge
number of plugins for different editors that you can use, which do the
formatting for you. You can use them to quickly navigate through your cells, and
some even allow sorting.

![Demo of a table editor](img/table-editing.gif)

**Editors: Plugins**

* Atom: [markdown-table-editor](https://atom.io/packages/markdown-table-editor)
* VS-Code: [Markdown Table](https://marketplace.visualstudio.com/items?itemName=TakumiI.markdowntable)
* Obsidion: [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian)


### HTML

                          --{{0}}--
You can also use plain HTML in your Markdown, if you miss something. It will
mostly work pretty good, but it should be used with caution, since some
interpreters apply different rules. Some interpret everything within an HTML tag
as HTML, while others allow mixing. Thus, HTML can contain Markdown, which
contains HTML, which contains... By the way, LiaScript allows mixing. Thus, keep
in mind that newlines and indentation are still relevant.

**Markdown-Syntax:**

<!-- class="translate"-->
``` html
<div style="color: green">

Test <q>**bold**</q> and <b>HTML bold</b> works also inline

![Beautiful Lenna](img/lenna.jpg "Image of Lenna with a hat")

</div>
```

                          --{{1}}--
The result shows how the inline-CSS is applied to all nested Markdown elements.
However, if you want to apply some styling to your document, LiaScript supports
another minimal invasive way of doing that. We will describe this in detail in
section [Styling](#styling).

                            {{1}}
********************************************************************************

**Result:**

<div style="color: green">

Test <q>**bold**</q> and <b>HTML bold</b> works also inline

![Beautiful Lenna](img/lenna.jpg "Image of Lenna with a hat")

</div>

> See the following list for an complete overview onto all HTML elements:
>
> [HTML Element Reference](https://www.w3schools.com/tags/default.asp)

********************************************************************************



                          --{{2}}--
If you use custom HTML instead of Markdown, then no styling will be applied. You
can of course create more complex content or tables, this way you can apply your
own styling to all elements.

                            {{2}}
[CSS-Reference](https://www.w3schools.com/CSSref/default.asp)

                          --{{3}}--
If you want to, you can also copy the generated LiaScript structure and use our
classes. Most Browsers include an inspector, which can be used to interactively
inspect the entire DOM-tree.

                            {{3}}
Open Inspector: <kdb>Ctrl+Shift+i</kdb> or <kdb>Ctrl+Shift+k</kdb>

                            {{3}}
!?[Inspecting the DOM](https://www.youtube.com/watch?v=Gk6BljF60RI)

                          --{{4}}--
But, you can also import your own styles within the main document comment by
using the `link` definition. We will explain this in more details within the
macro section [link](#link).

                            {{4}}
``` md
<!--
...
link: file.css
...
-->

# Main Title
```

#### Details & Summary

                          --{{0}}--
The `details` and `summary` tags are standard HTML tags and GitHub also supports
their usage with Markdown. These tags offer a neat way to define something what
is nowadays called accordion. Thus, your user can click on the summary text to
make the body of the `details`-tag appear.

**Syntax:**

<!-- class="notranslate"-->
``` md
<details>

<summary>**Honest Textbook ads (click to enlarge)**</summary>

!?[If High School and College Textbooks Were Honest - Honest Ads](https://www.youtube.com/watch?v=lhSjYT7pWkw)

</details>
```

**Result:**

<details>

<summary>**Honest Textbook ads (click to enlarge)**</summary>

!?[If High School and College Textbooks Were Honest - Honest Ads](https://www.youtube.com/watch?v=lhSjYT7pWkw)

</details>

#### `<lia-keep>` 💫

                          --{{0}}--
If you want to embed more complex HTML, and only HTML, without taking care about
indentation and formatting, then should use the `lia-keep` tag to surround your
code.

``` html
<lia-keep>
  <style>
    table, th, td {
      border: 1px solid black;
      width: 250px; height: 40px;
      text-align: center;
    }
  </style>

  <table style="margin: 1em">
    <tr>
      <th>**Header 1**</th>
      <th>**Header 2**</th>
    </tr>
    <tr>
      <td>Cell 1</td>
      <td rowspan="2">Cell 2</td>
    </tr>
    <tr>
      <td>Cell 3</td>
    </tr>
  </table>
</lia-keep>
```

                          --{{1}}--
As it is demonstrated in the result, everything within this tag will be treated
as HTML only, no Markdown parsing will be applied and indentation will be
checked.

                            {{1}}
********************************************************************************

**Result:**

<lia-keep>
  <style>
    table, th, td {
      border: 1px solid black;
      width: 250px;
      height: 40px;
      text-align: center;
    }
  </style>

  <table style="margin: 1em">
    <tr>
      <th>**Header 1**</th>
      <th>**Header 2**</th>
    </tr>
    <tr>
      <td>Cell 1</td>
      <td rowspan="2">Cell 2</td>
    </tr>
    <tr>
      <td>Cell 3</td>
    </tr>
  </table>

</lia-keep>


********************************************************************************

                          --{{2}}--

This way, you could for example also import even more complex HTML-tables,
pictures with multiple sources for different screen-sizes, and more.
_With great power comes great responsibility._  Thus, you will also be
responsibile for your styling.


### Code

                          --{{0}}--
In Markdown, you can use a sequence of at least three subsequent backticks `\``
to indicate a code-block that should not be treated as Markdown, but instead
contains some kind of code for which syntax-highlighting should be used, if
possible. The first word after the backticks is used as an indicator, for which
kind of syntax-highlighting should be applied.

```` md
``` python
import time
# Quick, count to ten!
for i in range(10):
    # (but not *too* quick)
    time.sleep(0.5)
    print(i)
```
````

                          --{{1}}--
In case you are wondering, how to embed a code-block into a code-block with
backticks? Three backticks are the minimum, thus you can surround your Markdown
code-block example with a sequence of 4 or more backticks. If you start with
four backticks, LiaScript will parse everything as code until it reaches a
matching number of backticks.

        {{1}}
``` python
import time
# Quick, count to ten!
for i in range(10):
  # (but not *too* quick)
  time.sleep(0.5)
  print(i)
```

                          --{{2}}--
However, we are still in the Markdown world with static code visualization.
LiaScript has also support for interactive programming, thus all of your
code-snippet can be made executable and editable. This will be described in more
detail in section [Interactive Coding](#interactive-coding).

#### Differences to Markdown 💫

                          --{{0}}--
Markdown also supports adding code by using tilde `~` characters instead of
backticks. This is at the moment not supported by LiaScript, but might be added
in the future.

``` md
~~~ javascript
var a = "b"
~~~
```

                          --{{1}}--
Additionally, it is also possible in standard Markdown to use indentation with
at least 4 spaces to mark a block or a line as code. In LiaScript this is
treated differently. You can use indentation to keep your document readable. The
two indicators for text-to-speech in the example are treated equally by
LiaScript, but another Markdown interpreter will interpret the second example as
a single paragraph, while the indicator in the first example will be treated as
code, and thus be easier to read with any other Markdown interpreter (including
the representation on GitHub).


                            {{1}}
<!-- class="translate"-->
``` md
This is not code ...

    Any kind of text with a 4 space
    indentation will be treated as code
    in Markdown ...

                --{{1}}--
This text will be spoken out loud in LiaScript.

--{{2}}--
This text will be spoken out loud too.
```


#### Projects 💫

                          --{{0}}--
If you want to bundle a couple of code-blocks into something that mirrors a
project, you can achieve this with the following syntax. All code-blocks are
simply attached to each other, in order to indicate a grouping. If you separate
them at least by one newline, they will be treated separately. This will be
pretty neat, if we introduce the concept of interactive code-blocks.


```` md
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
````

                          --{{1}}--
You can define optional names within the head of your code-block. The starting
plus `+` and minus `-` symbols are used to indicate, if the resulting
code-blocks should be visible or hidden. However, you can change this, by
clicking onto the resulting title-bar to either maximize or minimize the
code-block.

                            {{1}}
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```

                          --{{2}}--
If you do not add a plus or a minus as a prefix to your file, the plus is used
as default.


#### Supported Languages 💫

                          --{{0}}--
In most cases you can simply add the name of the language or the common filename
ending into the head of a code snippet. Most Markdown interpreters will use
[highlight.js](https://highlightjs.org) for language rendering, since we require
also an editor with syntax highlighting capabilities, we use
[ace](https://ace.c9.io). Thus, the language support might differ to other
systems. We therefor apply a mapping, so that you can still use all
[highlight.js](https://highlightjs.org) short-codes but also those of
[ace](https://ace.c9.io).

Overview: https://github.com/LiaScript/docs/blob/master/Code.md


### Horizontal rules 💫

                          --{{0}}--
At the moment it is possible to insert horizontal rules by adding lines with at
least 3 dashes, longer sequences of dashes are allowed too. Common Markdown also
allows to define such rules with asterisks `*`, but this is used in LiaScript to
group blocks, as we will described later...

**Markdown-Syntax:**

<!-- class="translate"-->
``` markdown
some paragraph

---

something else

----------------
```

**Result:**

some paragraph

---

something else

----------------


## Custom Styling


                 <!-- style="color: red" -->
                          --{{0}}--
In order to support a nearly equal experience for all Markdown interpreters you
should stick with the basic Markdown notation or use simple HTML-tags as much as
possible, for example if you want to change the color of a sentence or a word.

                          --{{1}}--
However, LiaScript allows you also to inject attributes into all Markdown blocks
and inline elements by attaching an HTML-comment to that specific object. If the
content of this HTML-comment can be parsed as HTML-attributes, then these
settings will be applied to the element attached.

                           {{1-2}}
``` markdown
<!--
style="color: red;" id = "elementID" class="foo bar"
-->
```



                            {{2}}
********************************************************************************

**Further resources:**

                         --{{2}}--
The following resources will give you a full overview onto the most common HTML
attributes and onto styling elements. It might be pretty overwhelming at first
glance, what is possible, but you will see, that with some basic elements you
can already achieve a lot. And when it comes to HTML and styling, you can find
examples for pretty much everything on your prefered search-engine, e.g.
[ecosia](https://www.ecosia.org).


* **HTML attributes:**

  > Checkout the following link to get a full overview onto all HTML attributes,
  > which you can also apply in LiaScript:
  > [w3schools: HTML Attribute Reference](https://www.w3schools.com/tags/ref_attributes.asp)

* **Styling with CSS:**

  > In most cases inline-styling will be applied, the following website covers
  > all CSS-Syntax elements, which then can be used simply by attaching comments
  > in the following way:
  >
  > `<!-- style="color: red; font-size: 20px;" -->`
  >
  > [w3schools CSS-Tutorial](https://www.w3schools.com/Css/css_syntax.asp)
  >
  > !?[Basic Inline Styling - CSS](https://www.youtube.com/watch?v=jH_WY-sQ8Lg)

********************************************************************************


### Block-Styling

                            --{{0}}--
So what is actually a block in LiaScript or Markdown? Basically it is everything
that is separated by a newline, such as a paragraph, a table, a code-block or a
list. But it can also be a block of multiple blocks, such as a list, which may
consist of different bullet points, where every bullet point can be a list of
multiple blocks by itself.

* **Blocks:**

  * [tables](#Tables)
  * [paragraphs](#content-blocks)
  * [lists (ordered/unordered)](#lists)
  * [blockquotes](#blockquotes)
  * [horizontal rules](#horizontal-rules-💫)
  * [HTML-blocks](#HTML) (if standing alone)

* **LiaScript-Extensions:**

  * [comments](#narrator)
  * [citations](#citations-💫)
  * [effects](#effects)
  * [quizzes](#quizzes)
  * [surveys](#surveys)
  * [tables](#fun-with-tables)
  * [ASCII-Art](#ascii-art-#2) & [Charts](#charts)
  * [executable code-blocks and projects](#Syntax-highlighting)



                          --{{1}}--
Settings for entire blocks can be set with a **starting** comment that includes
all required HTML-attributes and can even contain animation settings. This can
also be used to highlight specific elements of your slides.

                            {{1}}
********************************************************************************

**LiaScript-Syntax:**

``` markdown
<!-- class = "animated rollIn" style = "animation-delay: 3s; color: purple" -->
The whole text-block should appear in purple color and with a wobbling effect.
Which is a **bad** example, please use it with caution ...

```

**Result: (be patient)**

<!-- class = "animated rollIn" style = "animation-delay: 3s; color: purple" -->
The whole text-block should appear in purple color and with a wobbling effect.
Which is a **bad** example, please use it with caution ...

********************************************************************************


                          --{{2}}--
Additionally, this method can be used to overwrite some aspects of all Markdown
element. The example shows how you can change the background color for a certain
element. This comes quite handy, if you want to emphasize further some parts of
your document.

                            {{2}}
********************************************************************************

``` markdown
<!-- style="background-color: tomato;"-->
> **Warning**
>
> You have to be aware, that this does not affect the
> font-color (dark/light mode). Try to use  pastel
> colors, or overwrite the color manually with:
>
>  `color: white;`
```

<!-- style="background-color: tomato;"-->
> **Warning**
>
> You have to be aware, that this does not affect the
> font-color (dark/light mode). Try to use  pastel
> colors, or overwrite the color manually with:
>
>  `color: white;`

********************************************************************************

                          --{{3}}--
The following example depicts the interconnection of nested block-elements. For
the entire table and also for all other blocks, it is possible to set the
properties for width, font-color and font size, which will be applied onto every
cell. And every cell can overwrite these values simply by adding a style-comment
as the first element. These settings are even preserved, if you reorder the
table.

                            {{3}}
********************************************************************************

``` markdown
               <!-- style="width: 50%; min-width: 400px; color: red; font-size:20px" -->
| <!-- style="background: azure"--> Header 1 | <!-- style="background: brown"--> Header 2        |
|:------------------------------------------ |:------------------------------------------------- |
| <!-- style="background: coral"--> Item 1   | <!-- style="background: rgb(12,12,111)"--> Item 2 |
| <!-- style="background: cyan" --> Item 3   | <!-- style="background: #b88608"--> Item 4        |
```

**Result**

                <!-- style="width: 50%; min-width: 400px; color: red; font-size:20px" -->
| <!-- style="background: azure"--> Header 1 | <!-- style="background: brown"--> Header 2        |
|:------------------------------------------ |:------------------------------------------------- |
| <!-- style="background: coral"--> Item 1   | <!-- style="background: rgb(12,12,111)"--> Item 2 |
| <!-- style="background: cyan" --> Item 3   | <!-- style="background: #b88608"--> Item 4        |

********************************************************************************


                          --{{4}}--
There are some special (internal) formats for changing the appearance of
code-blocks and how to deal with tables. These topics will be handled
separately.


### Inline-Styling

                          --{{0}}--
So what are inline elements? These are basically all the tiny parts, such as
single words, bold-text, links, inline-code, but also images and videos. In
contrast to blocks where you attach the comment to front, inline elements can be
modified by attaching a comment to the end. That's it ...

**LiaScript-Syntax:**

``` markdown
This **is an important**<!-- style="color: red" --> part
of the text<!-- style="color: green; font-size: 10rem;" -->.


![image](...Creative-Tail-Animal-lion.svg)<!--
style = "width: 300px;
         border: 10px solid;"
class = "animated infinite bounce"
-->

Some blurry and black-and-white video:

!?[movie](https://www.youtube.com/watch?v=8pTEmbeENF4)<!--
style = "filter: blur(2px); grayscale(80%);"
-->
```

                          --{{1}}--
As you can see from the results, the entire bold text is treated as one block,
whereby in the second case only the single word "text" gets modified.

                            {{1}}
********************************************************************************

**Result:**

This **is an important**<!-- style="color: red" --> part
of the text<!-- style="color: green; font-size: 10rem;" -->.

![image](https://upload.wikimedia.org/wikipedia/commons/d/d0/Creative-Tail-Animal-lion.svg)<!--
style = "width: 300px;
         border: 10px solid;"
class = "animated infinite bounce"
-->

Some blurry and black-and-white video:

!?[movie](https://www.youtube.com/watch?v=8pTEmbeENF4)<!--
style = "filter: blur(2px) grayscale(80%);"
-->

********************************************************************************

                          --{{2}}--
CSS is a pretty powerful tool and by using HTML-comments to tweak your Markdown,
you can still read the document with any ordinary Markdown interpreter that
simply ignores these comments.

### Images and Styling

                          --{{0}}--
Styling images might happen quite often. However, you have to be aware of the
fact, that the modal view functionality is only possible if LiaScript is in
total control of the image. Thus, it will handle the optimal scaling for you and
adds a click-event to switch to the modal view.

```markdown
![The Wave](...ave_off_Kanagawa_%28Kanagawa_oki_nami.jpg "without attribute injection")

![Workplace](https://www.w3schools.com/htmL/workplace.jpg "with attribute are added")<!-- usemap="#workmap" -->

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" title="Computer" onclick="alert('You clicked the Computer')" >
  <area shape="rect" coords="290,172,333,250" title="Phone" href="#12">
  <area shape="circle" coords="337,300,44" title="Cup of coffee" href="#Projects">
</map>
```

                          --{{1}}--
Thus, if you click onto the first image, you will be able to inspect it in more
detail. If you click onto the second image, then a map associated with this
image  is in charge of it, which handles click-events differently.

                            {{1}}
********************************************************************************

**Result**

![Workplace](https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/1952.343_-_Under_the_Wave_off_Kanagawa_%28Kanagawa_oki_nami.jpg/2560px-1952.343_-_Under_the_Wave_off_Kanagawa_%28Kanagawa_oki_nami.jpg "without attribute injection")

![Workplace](https://www.w3schools.com/htmL/workplace.jpg "with attribute are added")<!-- usemap="#workmap" -->

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" title="Computer" onclick="alert('Cmputer')" >
  <area shape="rect" coords="290,172,333,250" title="Phone" href="#12">
  <area shape="circle" coords="337,300,44" title="Cup of coffee" href="#Projects">
</map>

> -- The example for the map was taken from
> [w3schools](https://www.w3schools.com/tags/tag_map.asp).

********************************************************************************

### What else can you do

                         --{{0}}--
The following examples present some useful application of combining attribute
injection into LiaScript components.


#### Hiding Content

                          --{{0}}--
There might be use cases where you either want to show some parts only on GitHub
and provide and alternative view at LiaScript. As it was shortly introduced in
the sections before, you can add comments to the start of every block to add
additional attributes. These attributes can also be used as a trigger to hide or
show content.

``` markdown
<!-- style="display:block" -->
<div style="display:none">

Visible only in LiaScript, but not on GitHub.

</div>

-----------------------------------------------

<!-- style="display:none" -->
<div style="display:block" id="fooBar">

Not visible in LiaScript, but on GitHub!

</div>
```

                          --{{1}}--
The attributes within the comment will overwrite the attributes within the
block. Thus, if there would be more stuff within style, this will be overwritten
too, but other attributes like `id` that are not contained within the comment
won't be affected...

#### Customizing Multimedia

                          --{{0}}--
As you have seen previously sizing videos and applying CSS filters is easy.
However, there might also be the case that you want to start a video from some
special point or to play it automatically, when it appears.


                          --{{1}}--
If the video is yours, then you can use the following attributes `àutoplay` and
`muted` to control the behavior and the additional fragment `#t=4,12` attached
to the URL of the video, will tell the browser where to start and where to stop
the video. The stop-parameter should be optional.


                            {{1}}
``` markdown
!?[Something about math](vid/math.mp4#t=4,12)<!--
autoplay="true"
muted="true"
-->
```


                          --{{2}}--
The resulting video starts immediately at second 4 and stops at second 10, and
of course it will be muted.

                 {{2}}
!?[Something about math](vid/math.mp4#t=4,10)<!--
autoplay="true"
muted="true" -->


##### Platform Diversity

                          --{{0}}--
However, if you are referencing other resource on platforms such as
[YouTube](https://youtube.com), [Vimeo](https://vimeo.com),
[DailyMotion](https://dailymotion.com), [PeerTube](https://peertube.tv) or
[TeacherTube](https://teachertube.com) you can achieve something similar, but in
a slightly different way. These settings have to be added to the URL of your
resource and different platforms might have different capabilities.


                          --{{1}}--
In most cases, you can use something like `&autoplay=1`, `&muted=true` or
`&mute=false` as it is depicted below:

                            {{1}}
`!?[Multimedia](url/...?autoplay=1&mute=1&start=1895&end=1905)`


                          --{{2}}--
But, different platforms support different functionalities. Here is a link list
of the different possible settings. For [PeerTube](https://peertube.tv) and
[TeacherTube](https://teachertube.com) we could not find any settings so far.


                            {{2}}
********************************************************************************

**URL Parameters:**

* [DailyMotion](http://embedcodedailymotion.blogspot.com/2016/05/dailymotion-embed-generator-tdborder.html)
* [Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/360001494447-Using-Player-Parameters)
* [YouTube](https://developers.google.com/youtube/player_parameters)
* PeerTube
* TeacherTube

********************************************************************************


## Math & Formulas

                 --{{0}}--
The following will not work on [GitHub](https://github.com), but most
Markdown-interpreters do support formulas with a
[LaTeX](https://en.wikipedia.org/wiki/LaTeX)-like syntax. As it is common in
many Markdown dialects, such as in
[Pandoc-Markdown](https://pandoc.org/MANUAL.html#math), you can apply dollar
signs to surround a "math"-environment. Everything within the dollar signs
belongs to the formula only, there is currently no nesting of other HTML or
LiaScript/Markdown allowed.


              --{{1}}--
Use single dollar signs to define an inline formula, which will be treated as an
ordinary text element.

                          {{1}}
Inline math-mode `$ \frac{a}{\sum{b+i}} $` -> $ \frac{a}{\sum{b+i}} $<!-- class="notranslate"-->


             --{{2}}--
Use double dollar signs to indicate a formula-block. This way you can also use
multiple lines to define a formula or a set of formulas that will furthermore
be displayed larger.


                          {{2}}
Multi-line math-mode can be applied by double dollars `$$ formula $$`
$$
  \frac{a}{\sum{b+i}}
$$<!-- class="notranslate"-->

                           --{{3}}--
Currently, we apply the [KaTeX](http://katex.org) library for typesetting. If you
are already familiar with [LaTeX](https://en.wikipedia.org/wiki/LaTeX) or
[MathJAX](https://www.mathjax.org), as another alternative library, then you can
start immediately to define formulas. If not, then check out some of the
following resources.

         {{3}}
* via KaTeX: http://katex.org

* Supported functions:

  https://katex.org/docs/supported.html

* Alphabetically sorted features:

  https://katex.org/docs/support_table.html

* Detexify: get the appropriate command by drawing symbols

  http://detexify.kirelabs.org/classify.html


                 --{{4}}--
Sometimes it might be tedious to find the right, command for the intended
symbol, if you can draw it, then you should give
[detexify](http://detexify.kirelabs.org/classify.html) a try.



### Formula Playground
<!--
@formula: <script>console.html(`<lia-formula formula="@'input" displayMode="true"></lia-formula>`);"LIA: stop"</script>

-->

                          --{{0}}--
Alignment is a typical use case for formulas. The code below, shows how this can
be achieved by using ampersands, which are used as an anchor for the center of a
formula.

<!-- class="notranslate"-->
```latex
\begin{split}
  a &=b+c \\
    &=e+f \\
    &=g+h+i+j\\
a+b+&c+d=12\\
\end{split}
```
@formula


                          --{{1}}--
If you want to number your formulas, we recommend using the `\tag` command to
add or overwrite the reference number. Automatic numbering does not work well at
the moment, since the formulas are rendered within a
[web component](https://en.wikipedia.org/wiki/Web_Components), and it does
conflict with the LiaScript idea of animation, which we describe in a later part
of this series.


      {{1}}
<!-- class="notranslate"-->
```latex
\tag{33}
\begin{equation}
 a =b+c
\end{equation}
```
@formula


                          --{{2}}--
And finally it is possible to add some styling, but with
[KaTeX](https://katex.org/docs/supported.html#html)-functionalities, this
includes some basic styling, with the same inline CSS, as we had described it in
section [Custom Styling](#custom-styling). (Can you spot the strange looking
german character [_Eszett_](https://en.wikipedia.org/wiki/%C3%9F).) And you can
mark elements as links with `\href` and add images with the command
`\includegraphics`.


      {{2}}
<!-- class="notranslate"-->
```latex
\begin{Bmatrix}
   a & b & c & d & e & f \\
   g & h & i & j & k & l \\
   m & n & o & p & q & r \\
   s & t & u & v & w & x \\
   y & z & ä & ö & ü &
   \htmlStyle{color: red; font-size: 26px}{ß}
\end{Bmatrix}
\\
\href{https://katex.org/docs/supported.html#html}{\KaTeX HTML support}
\\
\includegraphics[height=0.8em, totalheight=0.9em, width=0.9em, alt=KA logo]{https://katex.org/img/khan-academy.png}
```
@formula

## Footnotes

                            --{{0}}--
Before moving on to the LiaScript specific features, such as quizzes, surveys,
animations, ASCII-art, etc., we would like present a last feature that is common
to many Markdown dialects and these are footnotes. So, what are footnotes in
general and when to use them.

                            {{0-1}}
>     {{|> UK English Male}}
> Footnotes are notes at the foot of the page while endnotes are collected under
> a separate heading at the end of a chapter, volume, or entire work. Unlike
> footnotes, endnotes have the advantage of not affecting the layout of the main
> text, but may cause inconvenience to readers who have to move back and forth
> between the main text and the endnotes.
>
> -- [Wikipedia](https://en.wikipedia.org/wiki/Note_%28typography%29)


                          --{{1}}--
In LiaScript a "section", which is defined by a header and a body, resembles a
page. Thus, the body might contain a couple of footnote-marks, while the actual
footnotes have to be defined at the end of the body. Other Markdown interpreters
might define a more "wide-spread" usage of footnotes, but in LiaScript this is
not possible at the moment. We parse/interpret only one section at a time and
not the entire document. So keep this in mind when using footnotes.


                            {{1}}
``` markdown
### header 3

body

body

body

footnotes

## ...
```

### Standard-Footnotes

                          --{{0}}--
The standard way of creating footnotes is to attach a marker to important
elements within your sections. A marker is defined by brackets with a starting
`^`. Then you can insert numbers, symbols and words.

               <!-- class="translate"-->
``` markdown
Something[^1] important[^2] about[^🦶] notes.
```

                          --{{1}}--
At the end of your body, you simply add a list with all indented remarks you
want to add. This list starts with your markers, that are followed by a colon.
Your notes or footnote-bodies can consist of multiple paragraphs and all other
block-elements that you have mentioned so far, but they have to be indented with
at least 2 spaces.

                            {{1}}
                <!-- class="translate"-->
``` markdown
[^1]: **Something** and **anything** are concepts of existence in ontology,
  contrasting with the concept of nothing. Both are used to describe the
  understanding that what exists is not nothing without needing to address the
  existence of everything. The philosopher, David Lewis, has pointed out that
  these are necessarily vague terms, asserting that "ontological ...

  -- [Wikipedia](https://en.wikipedia.org/wiki/Something_%28concept%29)

[^2]:> It is **important** to mention that anything can be added to a footnote
  > also some piece of code, images, videos, etc.
  >
  > ??[How to Use Footnotes](https://www.youtube.com/watch?v=Gg6vXoHO95I)

[^🦶]: Actually you are not forced to use numbers, you can use any kind of
       symbol or even words too.

       _But, please be consise._
```

                          --{{2}}--
By clicking onto the footnote, all of your comments will be shown in a modal
view in all view-modes. If you are in "textbook" mode, then these footnotes
are additionally displayed at the very end of the current "page".


                            {{2}}
********************************************************************************

**Result:**

Something[^1] important[^2] about[^🦶] notes.

********************************************************************************

[^1]: **Something** and **anything** are concepts of existence in ontology,
  contrasting with the concept of nothing. Both are used to describe the
  understanding that what exists is not nothing without needing to address the
  existence of everything. The philosopher, David Lewis, has pointed out that
  these are necessarily vague terms, asserting that "ontological ...

  -- [Wikipedia](https://en.wikipedia.org/wiki/Something_%28concept%29)

[^2]:> It is **important** to mention that anything can be added to a footnote
  > also some piece of code, images, videos, etc.
  >
  > ??[How to Use Footnotes](https://www.youtube.com/watch?v=Gg6vXoHO95I)

[^🦶]: Actually you are not forced to use numbers, you can use any kind of
       symbol or even words too.

       _But, please stick to one explicit format._

### Inline-Footnotes

                          --{{0}}--
The following idea of defining inline-footnotes was borrowed from LaTeX. If you
want to add only some text without further Markdown-syntax then you can add this
in parentheses to your footnote-mark. In this case it is not necessary to add a
more sophisticated explanation to the end of the sections.


`Inline Footnote [^x](__explanation__ in one line)` => Inline Footnote[^x](__explanation__ in one line)

## State

                          --{{0}}--
Some words about state. The LiaScript runtime-environment preserves the internal
state of the following elements, depending on where you execute your courses and
depending on the version.

* [Tasks](#tasks)
* [Quizzes](#quizzes)
* [Surveys](#surveys)
* Code
* `(<script>)`


                          --{{1}}--
LiaScript currently runs in three different environments. You can either share
and read courses via the [project website](https://LiaScript.github.io/course/),
generate
[SCORM-packages](https://en.wikipedia.org/wiki/Sharable_Content_Object_Reference_Model),
which can be uploaded to an LMS, or create self-containing websites.


                            {{1}}
1. **LiaScript PWA**

                          --{{2}}--
   If you share your course via the website, then all the courses and the
   current course states are preserved within the Browser database
   [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
   locally. **All of the states?** Well ... the internal state of the previous
   components is only preserved, if your course has a version greater than or
   equal to `1.0.0`. The default version is `0.0.1`, which means that the course
   is in _development mode_, and thus the structure of your course might change
   every time. If a user reloads the course, then all states are cleared.

   - Where: https://LiaScript.github.io/course/
   - Source: [liascript/src/typescript/connectors/Browser](https://github.com/LiaScript/LiaScript/tree/development/src/typescript/connectors/Browser)

2. **SCORM 1.2**

                          --{{3}}--
   [SCORM](https://en.wikipedia.org/wiki/Sharable_Content_Object_Reference_Model)
   stands for Sharable Content Object Reference Model and allows you to store
   the course state directly within every LMS that has support for SCORM 1.2.
   For this case you have to use our
   [exporter](https://github.com/LiaScript/LiaScript-Exporter), which translates
   your course into a "SCORM-compliant" zip-file. You can check if your LMS has
   support for SCORM, by visiting our LMS-overview.

   - Where: https://github.com/LiaScript/LiaScript-Exporter#scorm12
   - Source: [liascript/src/typescript/connectors/SCORM1.2](https://github.com/LiaScript/LiaScript/tree/development/src/typescript/connectors/SCORM1.2)
   - Does your LMS support SCORM 1.2:
     [LMS-Overview](https://github.com/LiaScript/LiaScript-Exporter#lms-support-list)

3. **Base**

                          --{{4}}--
   You can also use our
   [exporter-tool](https://github.com/LiaScript/LiaScript-Exporter) to create
   single websites of your course. But, this "base" does only support to store
   user-settings, such as style, mode, etc. This "base-connector" is also used
   for the live-server and editors. If you are a developer and want to extend
   the LiaScript support to store state within your backend, then this is the
   right place to look at. This module provides an abstract class, to which all
   statefull data is sent. You can simply inherit from this class and implement
   the access to your system.

   - Where: https://github.com/LiaScript/LiaScript-Exporter#web
   - Source: [liascript/src/typescript/connectors/Base](https://github.com/LiaScript/LiaScript/tree/development/src/typescript/connectors/Base)

                          --{{5}}--
For more information on versioning and how to use it, check out section
[`version`](#version) within the [macros](#macros) section. But for now, it is
okay to know, that you can adapt, restructure and share your courses freely, if
you are in dev-mode. If your course is ready to be launched, use versioning to
preserve the state of your users.

## Tasks

                          --{{0}}--
Before we show you how to create quizzes, we would like to introduce **tasks**,
which were also a source of inspiration for us, for developing a similar syntax
for quizzes and surveys. The GitHub flavored Markdown offers a very intuitive
way of creating check-lists or task-lists.

<!-- class="translate" -->
``` markdown
**Which topics did you master so far?**

- [ ] Biology
- [ ] Chemistry
- [ ] Computer Science
- [X] Something about LiaScript
```

                          --{{1}}--
It is basically a list where the brackets are used to symbolize check-boxes and
by using an upper- or lowercase x, it is possible to mark a checkbox as checked.
In LiaScript however, it is possible for the user to manipulate these states,
and they will be preserved if your document is in version 1 or greater.

                            {{1}}
********************************************************************************

**Which topics did you master so far?**

- [ ] Biology
- [ ] Chemistry
- [ ] Computer Science
- [X] Something about LiaScript

********************************************************************************

### Tasks and Scripting

                          --{{0}}--
In case you are wondering where the **"Script"** in LiaScript comes from? We
wanted to make documents more interactive, by embedding native support for
scripting. Coding will become an essential skill in the future so why not using
it to directly extend the native capabilities of static documents and its
elements. Scripts can either be executed separately or they can be attached to
tasks, quizzes, surveys, and code-snippets.

                          --{{1}}--
The example might look a bit weird for the moment, but it is only meant as a
demonstration. You can use scripting in LiaScript, if you want to, but it is not
required. Thus, whenever you change the state of the task-list, then the script
below gets executed and the `@input`-macro will be substituted by current input.
`output="tasks"` says, that the result is published under the topic "tasks",
thus, every script that contains an `@input(\`tasks\`)` will be executed
afterwards as well with the changed input. Task-lists simply produces and array
with boolean values.

                            {{1}}
<!-- class="translate" -->
``` markdown
**What do you want to learn today?**

- [X] Biology
- [ ] Chemistry
<script output="tasks">"@input"</script>

<script style="width: 100%">
try {
  let task = @input(`tasks`) // interpret the output="tasks"

  if(task[0]) {
    send.liascript(`## Biology

Hey, great, you want to learn something about Biology.

* resource 1
* resource 2

The input from the tasks above was: \`[${task}]\``)
  } else send.clear()
} catch(e) { }
</script>
```

                          --{{2}}--
Depending on the input scripts can generate different results, it is even
possible to return LiaScript code, which will be analyzed and rendered
dynamically. If an empty string or undefined gets returned, then the script will
not be visible to the user. We will describe all Lia-Scripting capabilities and
features in more detail in a later [chapter](#javaScript-or-js-components).


                            {{2}}
********************************************************************************

**What do you want to learn today?**

- [X] Biology
- [ ] Chemistry
<script output="tasks">"@input"</script>


<script style="width: 100%">
try {
  let task = JSON.parse("@input(`tasks`)")

  if(task[0]) {
    send.liascript(`## Biology

Hey, great, you want to learn something about Biology.

* resource 1
* resource 2

The input from the tasks above was: \`[${task}]\``
    )
  } else send.clear()
} catch(e) { }
</script>


<script style="width: 100%">
try {
  let task = @input(`tasks`)

  if(task[1]) {
    send.liascript(`## Chemistry

Hey, great, you want to learn something about Chemistry.

The input from the tasks above was: \`[${task}]\`

...`)
  } else send.clear()
} catch(e) { }
</script>

********************************************************************************


                          --{{3}}--
If we are talking about embedding scripts, that perform some kind of
calculation, data analysis, etc. Why shouldn't this be visible to the user as
well? We all know what can happen when you cannot get access to primary data and
the code that was used to analyze it. In LiaScript you can inspect these
highlighted elements with rounded corners, which represent the result of a
script, simply by double-clicking or double-tabbing. The user can manipulate
them and observe the results, simply by changing the code. If the editor is
closed, then the code gets reevaluated.

                            {{3}}
> Europe's entire austerity policy after the debt crisis was based on wrong
> conclusions drawn from incorrect data and false calculations from a
> **single Excel spreadsheet**.
>
> https://en.wikipedia.org/wiki/Growth_in_a_Time_of_Debt

                          --{{4}}--
But, this is enough for the moment, let us continue with quizzes...

## Quizzes

                          --{{0}}--
Quizzes are an essential element of every online course, which allow students to
reflect and test their knowledge. As mentioned before, we used the
GitHub-flavored Markdown notation for tasks as an inspiration for quizzes.

                          --{{1}}--
Long story short, everything that is related to quizzes is defined as a
combination of brackets with brackets or parentheses.

    {{1-2}}
- `[[   ]]`
- `[(   )]`

                          --{{2}}--
LiaScript currently supports 5 different types of quizzes and one, so-called
generic type, which can be used to created custom quizzes of any kind.


                            {{2-3}}
1. Multiple-Choice: `[[X|x| ]] ...`
2. Single-Choice:   `[(X|x| )] ...`
3. Matrix: as a combination of multiple- and single-choice quizzes
3. Text-Quiz: `[[solution]]`
4. Selection-Quiz: `[[ opt. 1 | opt. 2 | (solution opt.) ]]`
0. "Generic": `[[!]]`


                          --{{3}}--
Additionally, it is possible to tweak every quiz with additional features, such
as hints, a resolution that is presented if the users solves the quiz by their
own or clicks onto the "show solution" button. And finally, as you have seen it
with tasks, you can attach scripts to each quiz in order to implement more
sophisticated quizzes or simply to log the output.

                            {{3}}
1. Hints: `[[?]]`
2. Solutions: some arbitrary Markdown content
3. Associated scripts: to be executed, when the user clicks onto the
   "check"-button

### Quiz Types

                          --{{0}}--
Within the following section we will introduce the 5 types of quizzes, which are
currently supported by LiaScript. Additionally, you have to know that users
cannot fail, by default it is possible to retry a quiz until it is solved, or
the user clicks onto the resolve button. The only thing that is counted is the
number of trials.


<div style="width:100%;height:0;padding-bottom:68%;position:relative;"><iframe src="https://giphy.com/embed/pKEufUXBqsLi8" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/the-simpsons-poochie-pKEufUXBqsLi8">via GIPHY</a></p>


                          --{{1}}--
If testing knowledge becomes something deeply personal, without any limitation
on the number of trials, why should anyone cheat at all. In this sense,
LiaScript is meant to be a language for learning and education instead of
assessment. But, if you want to, you can also tweak this by using scripts 😉.


#### 1. Multiple-Choice

                           --{{0}}--
A multiple-choice quiz can also be interpreted as a task list with a predefined
solution. Thus, the only thing that has to be done, is to surround your "ASCII"
checkboxes with additional brackets, which are followed by a line of
Markdown/LiaScript.

<!-- class="translate"-->
``` markdown
- [[ ]] Empty means not checked
- [[X]] Uppercase `X` means checked ...
- [[x]] ... and lowercase `x` too ...
- [[ ]] **as defined in the first line** ...
```

                          --{{1}}--
As you can see from the example it does not matter, whether you use lowercase or
uppercase `X` to mark a checked element.

                            {{1}}
********************************************************************************

**Result:**

- [[ ]] Empty means not checked
- [[X]] Uppercase `X` means checked ...
- [[x]] ... and lowercase `x` too ...
- [[ ]] **as defined in the first line** ...

********************************************************************************

                          --{{2}}--
The starting dashes for quizzes are also optional, you can omit them and GitHub
and other Markdown renderer will present a single paragraph. Or, you can also
use an indentation of at least 4 spaces, which will be presented by other
interpreters as code. However, all the following representations will be
interpreted by LiaScript as the same quiz.


                            {{2}}
<!-- class="translate"-->
``` markdown
Without starting dashes (paragraph):

[[ ]] Empty means not checked
[[X]] Uppercase `X` means checked ...
[[x]] ... and lowercase `x` too ...
[[ ]] **as defined in the first line** ...

With indentation of at least 4 spaces (code):

    [[ ]] Empty means not checked
    [[X]] Uppercase `X` means checked ...
    [[x]] ... and lowercase `x` too ...
    [[ ]] **as defined in the first line** ...
```

#### 2. Single-Choice

                          --{{0}}--
If brackets are used to define checkboxes, why not using parentheses to indicate
radio-buttons. In contrast to multiple-choice quizzes only one option can be
selected.

<!-- class="translate"-->
``` markdown
- [( )] Not selected
- [(X)] **This one has to be selected**
- [( )] ~~Do not select this one ...~~
```

                          --{{1}}--
You can also omit the starting dashes and/or use indentation as with
multiple-choice quizzes and use upper- or lowercase `X` to indicate the
solution.

                            {{1}}
********************************************************************************

**Result:**

- [( )] Not selected
- [(X)] **This one has to be selected**
- [( )] ~~Do not select this one ...~~

********************************************************************************

                          --{{2}}--
However, you can also define multiple possible solutions a user might select
only one option, but multiple might be correct.

                            {{2}}
<!-- class="translate"-->
``` markdown
What is the correct spelling of H(D)D?

    [(X)] hard (**disk**) drive
    [( )] hard (**desk**) drive
    [(x)] hard (**disc**) drive
```

                            {{3}}
********************************************************************************

**Result:**

What is the correct spelling of H(D)D?

    [(X)] hard (**disk**) drive
    [( )] hard (**desk**) drive
    [(x)] hard (**disc**) drive

********************************************************************************

                          --{{3}}--
Thus, if the user selects the first or the last option, the quiz will be marked
as solved, or if the user clicks onto the "show solution" button, both options
will be presented.



                            {{4}}
> ## How to create a true/false quiz?
>
>                        --{{4}}--
> Using single-choice quizzes, it is also possible to define something simple as
> a True or False quiz.
>
> <!-- class="translate"-->
> ``` markdown
> Do you know an easier way of creating quizzes?
>
>     [( )] Yes
>     [(X)] No
> ```
>
> **Result:**
>
> Do you know an easier way of creating quizzes?
>
>     [( )] Yes
>     [(X)] No


#### 3. Matrix-Quiz

                          --{{0}}--
You can also combine multiple single- and multiple-choice quizzes into one
larger matrix-quiz. The "vector" quizzes are now simply defined as rows, whereby
you have to define a custom header, which represent the solution options. It
makes no real difference if you use parentheses or brackets within the header
line, use brackets if you want to insert parenthesis and vice versa.


                            {{0}}
<!-- class="translate"-->
``` markdown
- [[male (der)] (female [die]) [neuter (das)]]
- [    [X]           [ ]             [ ]     ]  Mann - German for man
- [    ( )           (X)             ( )     ]  Frau - German for woman
```

                          --{{1}}--
However, within the quiz-body, which is contains the quiz-vectors as rows, the
brackets and parenthesis make a difference. The first row gets presented as
multiple-choice with checkboxes, while the second line defines a single-choice
with radio buttons.

                            {{1}}
********************************************************************************

Man or woman is obvious, but you guess the remaining German grammatical genders?

    [[male (der<!-- class="notranslate"-->)]   (female [die<!-- class="notranslate"-->])   [neuter (das<!-- class="notranslate"-->)]]
    [    [X]           [ ]             [ ]     ]  Mann<!-- class="notranslate"--> - German for man
    [    ( )           (X)             ( )     ]  Frau<!-- class="notranslate"--> - German for woman
    [    [X]           [ ]             [ ]     ]  Junge<!-- class="notranslate"--> - German for boy
    [    ( )           ( )             (X)     ]  Mädchen<!-- class="notranslate"--> - German for girl
    [    [X]           [X]             [ ]     ]  Paprika<!-- class="notranslate"--> - German for bell pepper
    [    (X)           (X)             (X)     ]  Joghurt<!-- class="notranslate"--> - German for yogurt

********************************************************************************

                            {{2}}
> **Fun fact:**
>
>                         --{{2}}--
> The number of elements within a row does not necessarily have to match the
> number of elements within the head. Although it might be rendered strangely,
> this does not cause an error. You as a course designer can see, that there
> might have a mistake occurred, but maybe you use it with a purpose.
>
> <!-- class="translate"-->
> ``` markdown
> [[option 1] [option 2]]
> [   [X]                     ] only with option 1
> [   [ ]        [X]          ] with two options
> [   [X]        [ ]       [X]] with three options
> ```
>
> [[option 1] [option 2]]
> [   [X]                     ] only with option 1
> [   [ ]        [X]          ] with two options
> [   [X]        [ ]       [X]] with three options

#### 4. Text-Quiz

                          --{{0}}--
A simple text-input quiz is defined only by two brackets that contain the
solution string. For these simple kind of quizzes, it is currently not allowed
to add a starting dash, but you can use optional indentation. The reason for
this is, that in the future we would like to extend the usage of text- and
selection-quizzes to be used everywhere, within paragraphs or tables to from
clozes.

<!-- class="translate"-->
``` markdown
What did the fish say when he swam into the wall?

    [[dam]]
```

                            {{1}}
********************************************************************************
**Result:**

What did the fish say when he swam into the wall?

    [[dam]]

********************************************************************************

                          --{{1}}--
The user input will be compared with your solution-string, and if and only if
they are equal the quiz will be labelled as solved. For different reasons it
might  be necessary to clean up the input, in order to deal with different types
of spelling, uppercase and lowercase, etc. Fort this purpose scripts can be
associated to a quiz, see therefor section
[Associated Scripts](#associated-scripts).


#### 5. Selection-Quiz

                          --{{0}}--
Finally, a selection-quiz is a collection of LiaScript/Markdown options that are
separated by vertical bars `|`. The solution is defined by the option or options
that are surrounded by parenthesis. An option can be any kind of LiaScript
inline element and since vertical bars `|` are used as separators, you can
simplify the readability by using newlines.

<!-- class="translate"-->
``` markdown
What is the derivative function of $f(x) = x^6$?

[[ $f'(x) = 6$ | ( $f'(x) = 6x^5$ ) | $f'(x) = 5x^6$ ]]

Can be also written as:

    [[  $f'(x) = 6$
    | ( $f'(x) = 6x^5$ )
    |   $f'(x) = 5x^6$
    | ( **This will be counted as correct too...** )
    ]]
```

                          --{{1}}--
This type of quiz allows you to have multiple correct options and starting
dashes are not supported yet, due to their future usage as native input elements
for clozes. And you can use indentation, such as it is possible for all quizzes.


                            {{1}}
********************************************************************************

**Result:**

What is the derivative function of $f(x) = x^6$?

[[ $f'(x) = 6$<!-- class="notranslate"-->
| ( $f'(x) = 6x^5$<!-- class="notranslate"--> )
| $f'(x) = 5x^6$<!-- class="notranslate"--> ]]


Can be also written as:

    [[  $f'(x) = 6$<!-- class="notranslate"-->
    | ( $f'(x) = 6x^5$<!-- class="notranslate"-->  )
    |   $f'(x) = 5x^6$<!-- class="notranslate"-->
    | ( **This will be counted as correct too...** )
    ]]

********************************************************************************


#### 0. Generic Quizzes

                          --{{0}}--
Generic quizzes can be used to define any kind of quiz. The course-developer can
define own types of quizzes, whereby the following combination of brackets with
an additional exclamation mark has to be associated with a script.

``` markdown
[[!]]
<script>
  const random = Math.random()

  alert("random value: "+ random)

  random < 0.2
</script>
```

                          --{{1}}--
This script does only generate a random number, outputs the result in an `alert`
and checks if the random value is less than 0.2. And if so, the quiz will be
marked as solved otherwise not. Thus, the last statement has to be `true` in
order to mark a quiz as solved, any other value will be accounted as `false`.

                            {{1}}
    [[!]]
    <script>
      const random = Math.random()

      alert("random value:"+ random)

      random < 0.2
    </script>

                          --{{2}}--
The usage of associated scripts for quizzes will be described in detail in
section [Associated Scripts](#associated-scripts).

#### Notes about Questions

                          --{{0}}--
Not all of the previous examples we have shown were perfect in the sense of
accessibility. Although these quizzes look good "for us", they might not be
perfectly for people that require a screen-reader to go through a course.
However, you can improve your quizzes by asking your question as a paragraph,
which is followed by your quiz. This way LiaScript will associate or label the
quiz with your question.

<!-- class="translate"-->
``` markdown
Ask a question as an ordinary Markdown paragraph,
which is followed by what?

    [[quiz]]
```

                          --{{1}}--
If your question requires more elements, then it is also possible to group it
with supplemental elements by putting it into a single HTML-element such as a
`div`. The `div` will get a unique ID and the question will be labeled with this
ID by using the
[aria-labelledby](https://www.w3.org/TR/wai-aria/#aria-labelledby) attribute.

                            {{1}}
<!-- class="translate"-->
``` markdown
<div>

Ask a question as an ordinary Markdown paragraph,
which is followed by what?

1. important
2. also relevant ...
3. [an image](http://...)

</div>

    [[quiz]]
```

### Tweaks

                          --{{0}}--
All of the following elements can be added to any type of quiz that you have
seen before. This includes and arbitrary number of hints, a more detailed
solution or a custom script that handles the user input.

<div style="width:100%;height:0;padding-bottom:63%;position:relative;"><iframe src="https://giphy.com/embed/qUDenOaWmXImQ" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/scott-pilgrim-michael-cera-level-up-qUDenOaWmXImQ">via GIPHY</a></p>

#### Hints

                          --{{0}}--
To any type of quiz you can add as many hints as you want, the pattern is simply
two brackets with an additional question mark. If you want to, you can also add
starting dashes to the hints.

<!-- class="translate"-->
``` markdown
What is $37 + 15$?

    [[52]]
    [[?]] the solution is larger than 50
    [[?]] it is less than 55
    [[?]] it should be an even number

This is also a valid quiz ...

[[52]]
- [[?]] the solution is larger than 50
- [[?]] it is less than 55
- [[?]] it should be an even number
```

                          --{{1}}--
The user can reveal these hints, step by step by clicking onto the light bulb or
"show hint" button.

                            {{1}}
********************************************************************************

What is $37 + 15$?

    [[52]]
    [[?]] the solution is larger than 50
    [[?]] it is less than 55
    [[?]] it should be an even number

********************************************************************************


#### Solution


                                   --{{0}}--
And finally, some quizzes might require some more explanations, if they are
solved or not. Therefor, simply use two "lines" that are defined by at least
three asterisks to group your solution. The solution explanation can contain
an arbitrary number of LiaScript elements.

<!-- class="translate"-->
```` markdown
What is $37 + 15$?

[[52]]
[[?]] the solution is larger than 50
[[?]] it is less than 55
[[?]] it should be an even number
***********************************************************************

52 is the correct solution, you get this by adding:

``` ascii
                        .------.
                        |      |
                        |      v
                        |
                        |     (1)
  37           3(7)     |     (3)x          37
+ 15         + 1(5)     |   + (1)x        + 15
---- -->     ------ --> |   ------ -->    ----
  ??           (12)     |     (5)2          52
                |       |                 ====
                '-------'
                  carry
```

??[MS-DOS Math Game](https://archive.org/embed/msdos_Super_Solvers_Teasure_MathStorm_1992)

***********************************************************************
````

                          --{{1}}--
In this case the solution contains an ASCII-art drawing, but it can be anything,
such as a an image, a video, or even something like a small game

                            {{1}}
********************************************************************************
What is $37 + 15$?

[[52]]
[[?]] the solution is larger than 50
[[?]] it is less than 55
[[?]] it should be an even number
******************************************************

52 is the correct solution, you get this by adding:

``` ascii
                        .------.
                        |      |
                        |      v
                        |
                        |     (1)
  37           3(7)     |     (3)x          37
+ 15         + 1(5)     |   + (1)x        + 15
---- -->     ------ --> |   ------ -->    ----
  ??           (12)     |     (5)2          52
                |       |                 ====
                '-------'
                  carry
```

??[MS-DOS Math Game](https://archive.org/embed/msdos_Super_Solvers_Teasure_MathStorm_1992)

*******************************************************

********************************************************************************



#### Associated Scripts

                          --{{0}}--
The following section contains a list of use-cases and ideas how to use quizzes
and scripts in association to generate a more complex user experience.

<div style="width:100%;height:0;padding-bottom:100%;position:relative;"><iframe src="https://giphy.com/embed/4GaHBQh3f4jBEpbQvP" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/shecodesio-swipe-up-computer-congratulations-4GaHBQh3f4jBEpbQvP">via GIPHY</a></p>

##### Cleaning up

                          --{{0}}--
If you are using for example the text-quiz, and you want to react to different
ways of spelling or to clean starting and trailing white-spaces. Then you can
attach a script to your quiz. The `@input` is marker that will be substituted by
the current user input. `trim` and `toLowerCase` are  JavaScript
functions/methods that are used to clean the input string. The last statement of
your quiz-script defines if the quiz is marked as solved or not. Only if the
last statement evaluates to `true` it is marked as solved, for any other value
it is simply a failed trial.


``` markdown
What did the fish say when he swam into the wall?

[[dam]]
<script>
let input = "@input".trim().toLowerCase()

input == "dam" || input == "damn"
</script>
```

                          --{{1}}--
Try out the following quiz. You can now enter "damn" or "dam" in different ways,
surrounded by spaces.

                            {{1}}
********************************************************************************

<!-- class="notranslate"-->
What did the fish say when he swam into the wall?

[[dam]]
<script>
let input = "@input".trim().toLowerCase()

input == "dam" || input == "damn"
</script>

********************************************************************************


##### Quiz `@input`s

                          --{{0}}--
`@input` will be replaced by the current state of the quiz that should be
checked. If you are not sure, how the input might look like, you can always
experiment with a simple `alert` that shows the current input.

                            {{1}}
********************************************************************************

---

**Text-quiz:**

                          --{{1}}--
The output or in LiaScript terms the `@input` gets substituted by a string,
without apostrophes. This might look strange since you have to add apostrophes
within the code, but all inputs are substituted without any additional type
formatting, this way they can be used in different ways and even contain peaces
of code.

``` markdown
[[text]]
<script> alert("@input") </script>
```

**Result:**

[[text]]
<script> alert("@input") </script>

********************************************************************************



                            {{2}}
********************************************************************************

---

**Selection-quiz:**

                          --{{2}}--
A selection quiz is defined by a number that represents the current input,
starting from `0`. The initial state is marked with `-1` to indicate that
nothing has been selected so far. In this example `A` would be represented by
`0`, `B` by `1`, `C` by `2` and so on.


``` markdown
[[A|B|C|(D)]]
<script> alert(@input) </script>
```

**Result:**

[[A|B|C|(D)]]
<script> alert(@input) </script>

********************************************************************************



                            {{3}}
********************************************************************************

---

**Multiple-choice:**

                          --{{3}}--
A multiple-choice quiz is represented by an array of ones and zeros, whereby a
`1` means checked and `0` the opposite.

``` markdown
[[X]] A
[[ ]] B
[[X]] C
<script> alert("@input") </script>
```

**Result:**

[[X]] A
[[ ]] B
[[X]] C
<script> alert("@input") </script>

********************************************************************************



                            {{4}}
********************************************************************************

---

**Single-choice:**

                          --{{4}}--
A single-choice quizzes behave similar as selections, the state is represented
by a number, starting from `0`, which represents the first option. A quiz that
has been not touched by the user will return `-1` as input value.

``` markdown
[(X)] 0
[( )] 1
[(X)] 2
<script> alert("@input") </script>
```

**Result:**

[(X)] 0
[( )] 1
[(X)] 2
<script> alert("@input") </script>

********************************************************************************



                            {{5}}
********************************************************************************

---

**Matrix:**

                          --{{5}}--
As matrices are arrays of "vector" quizzes, their input state is represented as
an array of multiple-choice and single-choice states. Thus, a list of lists with
zeros and ones as well as numbers.

``` markdown
Weird, isn't it ;-)

[[male (der)]   (female [die])   [neuter (das)]]
[    [X]           [ ]             [ ]     ]  Mann - German for man
[    ( )           (X)             ( )     ]  Frau - German for woman
[    [X]           [ ]             [ ]     ]  Junge - German for boy
[    ( )           ( )             (X)     ]  Mädchen - German for girl
[    [X]           [X]             [ ]     ]  Paprika - German for bell pepper
[    (X)           (X)             (X)     ]  Joghurt - German for yogurt
<script>alert("@input")</script>
```


**Result:**

[[male (der<!-- class="notranslate"-->)]   (female [die<!-- class="notranslate"-->])   [neuter (das<!-- class="notranslate"-->)]]
[    [X]           [ ]             [ ]     ]  Mann<!-- class="notranslate"--> - German for man
[    ( )           (X)             ( )     ]  Frau<!-- class="notranslate"--> - German for woman
[    [X]           [ ]             [ ]     ]  Junge<!-- class="notranslate"--> - German for boy
[    ( )           ( )             (X)     ]  Mädchen<!-- class="notranslate"--> - German for girl
[    [X]           [X]             [ ]     ]  Paprika<!-- class="notranslate"--> - German for bell pepper
[    (X)           (X)             (X)     ]  Joghurt<!-- class="notranslate"--> - German for yogurt
<script>alert("@input")</script>

********************************************************************************



                            {{6}}
********************************************************************************

---

**Generic:**

                          --{{6}}--
In case of a generic quiz, the developer is responsible for defining and storing
state. Thus, there will be no input. The only case where `@input` gets
substituted by a value, is when the user clicks onto the resolve button. This is
indicated by the input `true`.

``` markdown
[[!]]
<script>alert("@input")</script>
```


[[!]]
<script>alert("@input")</script>

********************************************************************************

##### Async & Errors

                          --{{0}}--
There might be the rare case, where you have to send the user input to an
external service to check them. Scripts in LiaScript can also define
asynchronous code, as it is displayed within the example.

``` markdown
What is $37 + 15$?

[[52]]
<script>
setTimeout(function(){
  alert("your input was: '@input'")
  send.lia("true")
}, 1000)

"LIA: wait"
</script>
```

                          --{{1}}--
In LiaScript, we can use some command strings that trigger a certain behavior,
these are global to all scripts and will be described in more detail in section
[Communication](#communication).


                            {{1}}
- `"LIA: wait"`: mark the script as still running
- `"LIA: stop"`: halt the execution of the script


                          --{{2}}--
Additionally, you can see a function-call within the example. `setTimeout`
triggers the execution of the internally defined function, which performs an
`alert` with the  user input and then sends "true" back to the internal
quiz-event handler. Every script is executed with an additional `send` object
and `send.lia` means send this back to LiaScript. Thus, the result could also be
evaluated by an external service, and this result will then be used to control
the quiz.

                            {{2}}
- `send`: general object to for communicating with the LiaScript internal
  event-handler for a specific entity, for more information see section
  [Communication](#communication)


                          --{{3}}--
Let us extend this example a little bit further. The `send` to `lia` can have
two meanings, one if everything was ok while the second might be the result of
an error. `send.lia` can have three values, the first is the message, the second
one contains more detailed information about the result, which is not required
at the moment, while the last value tells LiaScript if everything was ok or by
using `false` that an error has occurred. The default value is always ok.


                            {{3}}
``` markdown
What is $37 + 15$?

[[52]]
<script>
setTimeout(function(){
  alert("your input was: '@input'")

  if ("@input" === "") {
    // generic error message
    send.lia("You have to fill in something into the input field", [], false)
  } else {
    // this is equal to send.lia("some message", [], true)
    send.lia("true")
  }
}, 1000)

"LIA: wait"
</script>
```

                          --{{4}}--
Thus, if you try out the following example, you will have to wait one second
until the result is evaluated, which in this case always results in a solved
quiz. But, if you do not add any input, then an error message will be displayed.

                            {{4}}
********************************************************************************

**Result:**

What is $37 + 15$?

[[52]]
<script>
setTimeout(function(){
  alert("your input was: '@input'")

  if ("@input" === "") {
    // generic error message
    send.lia("You have to fill in something into the input field", [], false)
  } else {
    // this is equal to send.lia("some message", [], true)
    send.lia("true")
  }
}, 1000)

"LIA: wait"
</script>

********************************************************************************


##### Obfuscate Quizzes

                          --{{0}}--
We would like to note, that this is only one method to obfuscate a quiz, by
using JavaScript, in this case by using the function `btoa`.

``` markdown
[[...]]
<script>
// btoa("solution") == "c29sdXRpb24="
"c29sdXRpb24=" == btoa( "@input".trim().toLowerCase() )
</script>
```

                          --{{1}}--
[`btoa`](https://developer.mozilla.org/en-US/docs/Web/API/btoa) creates a
[Base64](https://developer.mozilla.org/en-US/docs/Glossary/Base64)-encoded ASCII
string, while [`atob`](https://developer.mozilla.org/en-US/docs/Web/API/atob)
does the opposite. You can try out to the following two scripts to encode and
decode different strings.

                            {{1}}
* `btoa`: <script input="text" value="solution" input-always-active modify="false">btoa(`@input`)</script>

  (Beautiful TO Awful)

* `atob`: <script input="text" value="c29sdXRpb24=" input-always-active modify="false">atob(`@input`)</script>

  (Awful TO Beautiful)


                            {{2}}
********************************************************************************

                          --{{2}}--
The result is a quiz, where it is not possible to see the solution immediately,
simply by getting a glimpse onto the raw course document.

**Result:**

[[...]]
<script>
// btoa("solution") == "c29sdXRpb24="
"c29sdXRpb24=" == btoa( "@input".trim().toLowerCase() )
</script>

********************************************************************************

##### Quizzes & Macros
<!--
@customQuiz
[[...]]
<script>
"@0" == btoa( "@input".trim().toLowerCase() )
</script>
@end
-->

                          --{{0}}--
It might look tedious to create these trailing scripts and to add them again and
again to your document, which makes a course harder to maintain and to develop.
However, in LiaScript you can define macros, that can be used to solve
repetitive tasks.

                          --{{1}}--
As depicted in the example, you can define custom macros within an HTML-comment
of a section or within the main comment at the head of every document. Wherever
you write the macro `@customQuiz` within your document, this macro will be
substituted by the content defined in the HTML-comment, which comes between
`@customQuiz` and `@end`. For more information see section [Macros](#macros).

                            {{1}}
``` markdown
##### Quizzes & Macros
<!--

@customQuiz
[[...]]
<script>
"@0" == btoa( "@input".trim().toLowerCase() )
</script>
@end

-->

...

@customQuiz(c29sdXRpb24=)


@customQuiz(NTI=)
```

                          --{{2}}--
You can further parameterize your macros, as you can see in the code, there is
an `@0`, which can be interpreted as a placeholder that shall be substituted by
the first parameter of your macro call.

                          --{{3}}--
That's it, you can add as much as `@customQuiz`-macros and if you do some
changes, you do not have to go through all scripts, but instead you only have to
change one single macro.


                            {{3}}
********************************************************************************

The solution should be "solution":

@customQuiz(c29sdXRpb24=)

What is $37 + 15$?

@customQuiz(NTI=)

********************************************************************************


                           --{{4}}--
By defining macros it is furthermore possible to create LiaScript libraries that
can imported into other courses, see therefor also section [Macros](#macros).


##### Final thoughts on wrong solution

                          --{{0}}--
The quiz for adding two numbers was actually taken from the presentation of Greg
Wilson, and it gives a good example for what scripts can be used for. Instead of
logging and checking if an answer is correct or not, we should use it to assist
students while they are learning and try to identify patterns in wrong answers.

                           {{0-1}}
!?[What Everyone in Tech Should Know About Teaching and Learning](https://www.youtube.com/watch?v=ewXvFQByRqY&start=717s)

                          --{{1}}--
As you have seen it for [tasks](#tasks-and-scripting), the result of a script
can also be published, in this case the topic is defined by the `output`
attribute.


                            {{1}}
``` markdown
What is $37 + 15$?

[[52]]
<script output="quiz:37+15">
  if ("@input" == "52") {
    true
  } else {
    "@input"
  }
</script>
```

                          --{{2}}--
Other scripts can be defined, that are subscribed to the output of the quiz, see
the different `@input` macro. These scripts are executed when the output of the
previous script changes. Every script can be used to identify another pattern,
since students can be wrong for different reasons. We need to identify such
patterns and react properly instead of measuring only fail and success.


                            {{2}}
``` markdown
<script style="display: block">
//   3(7)       (3)7
// + 1(5)     + (1)5       The first and second steps were correct,
// ------ ->  ------  ->   but the student forgot to carry the 1
//   (12)       (4)2       in the 10 digit column.

if ("@input(`quiz:37+15`)" == "42") {
  send.liascript(`## Maybe you forgot to carry...

Checkout the follow video to recap carrying.

!?[Carrying for larger digits](https://www.youtube.com/watch?v=VPsYRPdlIpU)
`)
} else ""
</script>

<script style="display: block">
//   3(7)       (3)7       The first and second steps were also
// + 1(5)     + (1)5       correct, but carrying was not provided
// ------ ->  ------  ->   properly, maybe there is a problem with
//   (12)      (4)12       understanding digit columns...


if ("@input(`quiz:37+15`)" == "412") {
  send.lia(`You are nearly there, there might be a problem with the 10 digit columns...`)
} else ""
</script>
```

                          --{{3}}--
With LiaScript you do not have to come up immediately with a perfect online
course, you can adapt it in little steps and let it increasingly grow.


                            {{3}}
********************************************************************************

What is $37 + 15$? This time you should make the mistakes 42 and 412.

[[52]]
<script output="quiz:37+15">
  if ("@input" == "52") {
    true
  } else {
    "@input"
  }
</script>


<script style="display: block">
//   3(7)       (3)7
// + 1(5)     + (1)5       The first and second steps were correct,
// ------ ->  ------  ->   but the student forgot to carry the 1
//   (12)       (4)2       in the 10 digit column.

if ("@input(`quiz:37+15`)" == "42") {
  send.liascript(`## Maybe you forgot to carry...

Checkout the follow video to recap carrying.

!?[Carrying for larger digits](https://www.youtube.com/watch?v=VPsYRPdlIpU)
`)
} else ""
</script>

<script style="display: block">
//   3(7)       (3)7       The first and second steps were also
// + 1(5)     + (1)5       correct, but carrying was not provided
// ------ ->  ------  ->   properly, maybe there is a problem with
//   (12)      (4)12       understanding digit columns...


if ("@input(`quiz:37+15`)" == "412") {
  send.lia(`You are nearly there, there might be a problem with the 10 digit columns...`)
} else ""
</script>

********************************************************************************


##### Generic++
<!--
@article: <script output="@0" value="select" input="select" options="der|die|das|dem|den|des">
            if("@input(`articles`)" == "true") {
              "@1"
            } else {
              "@input"
            }
          </script>
-->

                          --{{0}}--
Ok, German articles behave strangely. This is a more complex example of a
generic quiz that is connected to multiple scripts with an input, which are
implemented with a single LiaScript macro.

Do you know which German articles belong to which gender in which case?

[[!]]
<script output="articles">
if ("@input" !== "true") {
  "@input(`11`)"=="der"  &&  "@input(`21`)"=="die"  &&  "@input(`31`)"=="das"  &&  "@input(`41`)"=="die" &&
  "@input(`12`)"=="des"  &&  "@input(`22`)"=="der"  &&  "@input(`32`)"=="des"  &&  "@input(`42`)"=="der" &&
  "@input(`13`)"=="dem"  &&  "@input(`23`)"=="der"  &&  "@input(`33`)"=="dem"  &&  "@input(`43`)"=="den" &&
  "@input(`14`)"=="den"  &&  "@input(`24`)"=="die"  &&  "@input(`34`)"=="das"  &&  "@input(`44`)"=="die"
}
</script>

| Case      | Masculine        | Feminine         | Neuter           | Plural           |
| --------- | ---------------- | ---------------- | ---------------- | ---------------- |
| Nominativ | @article(11,der) | @article(21,die) | @article(31,das) | @article(41,die) |
| Genitiv   | @article(12,des) | @article(22,der) | @article(32,des) | @article(42,der) |
| Dativ     | @article(13,dem) | @article(23,der) | @article(33,dem) | @article(43,den) |
| Accusativ | @article(14,den) | @article(24,die) | @article(34,das) | @article(44,die) |


                          --{{1}}--
The following code-block shows how this quiz was actually implemented.

                            {{1}}
``` markdown
##### Generic++
<!--
@article: <script output="@0" value="select" input="select" options="der|die|das|dem|den|des">
            if("@input(`articles`)" == "true") {
              "@1"
            } else {
              "@input"
            }
          </script>
-->

                          --{{0}}--
Ok, German articles behave strangely. This is a more complex example of a
generic quiz that is connected to multiple scripts with an input, which are
implemented with a single LiaScript macro.

Do you know which German articles belong to which gender in which case?

[[!]]
<script output="articles">
if ("@input" !== "true") {
  "@input(`11`)"=="der"  &&  "@input(`21`)"=="die"  &&  "@input(`31`)"=="das"  &&  "@input(`41`)"=="die" &&
  "@input(`12`)"=="des"  &&  "@input(`22`)"=="der"  &&  "@input(`32`)"=="des"  &&  "@input(`42`)"=="der" &&
  "@input(`13`)"=="dem"  &&  "@input(`23`)"=="der"  &&  "@input(`33`)"=="dem"  &&  "@input(`43`)"=="den" &&
  "@input(`14`)"=="den"  &&  "@input(`24`)"=="die"  &&  "@input(`34`)"=="das"  &&  "@input(`44`)"=="die"
}
</script>

| Case      | Masculine        | Feminine         | Neuter           | Plural           |
| --------- | ---------------- | ---------------- | ---------------- | ---------------- |
| Nominativ | @article(11,der) | @article(21,die) | @article(31,das) | @article(41,die) |
| Genitiv   | @article(12,des) | @article(22,der) | @article(32,des) | @article(42,der) |
| Dativ     | @article(13,dem) | @article(23,der) | @article(33,dem) | @article(43,den) |
| Accusativ | @article(14,den) | @article(24,die) | @article(34,das) | @article(44,die) |
```



## Surveys

                             --{{0}}--
A script should not define a one-way road to the student! So surveys are
required.

### Text-Inputs

Similar to text-quizzes, use the following syntax to define a text-survey, where
the number of underlines defines the presented line numbers:

   `[[___ ___ ___ ___]]`

What is your opinion on ... :

    [[____ ____ ____ ____]]

---

Or a single line only:

`[[___]]`

    [[___]]

### Single Choice Vector

                              --{{0}}--
And also this kind of survey is similar to a single choice quiz, but in this
case numbers within parenthesis are used to define some kind of variable
identifier. That is why they do not have to be in order.

```markdown
[(1)] option 1
[(2)] option 2
[(3)] option 3
[(0)] option 0
```

You can only select one option:

    [(1)] option 1
    [(2)] option 2
    [(3)] option 3
    [(0)] option 0


### Multi Choice Vector

                               --{{0}}--
Similar to multi-choice quizzes, you can define multi-choice survey vectors with
a number in double square brackets. But, and this is also possible for all other
kinds of surveys you can define some kind of variable name with a starting colon.

```markdown
[[red]]         is it red
[[green]]       green
[[blue]]        or blue
[[dark purple]] no one likes purple ( last chance ;-) )
```

Select some of your favored colors!

    [[red]]         is it red
    [[green]]       green
    [[blue]]        or blue
    [[dark purple]] no one likes purple ( last chance ;-) )

### Single Choice Matrix

                              --{{0}}--
For defining survey blocks you only have to a header row, whose definition is
also used by the trailing rows.

Markdown-format:

```markdown
[(totally)(agree)(unsure)(maybe not)(disagree)]
[                                             ] liaScript is great?
[                                             ] I would use it to make online **courses**?
[                                             ] I would use it for online **surveys**?
```

    [(totally)(agree)(unsure)(maybe not)(disagree)]
    [                                             ] liaScript is great?
    [                                             ] I would use it to make online **courses**?
    [                                             ] I would use it for online **surveys**?

### Multi Choice Matrix

                               --{{0}}--
I guess, multi-choice blocks are self-explanatory...

Markdown-format:

```markdown
[[1][2][3][4][5][6][7]]
[                     ] question 1 ?
[                     ] question 2 ?
[                     ] question 3 ?
```

Result:

    [[1][2][3][4][5][6][7]]
    [                     ] question 1 ?
    [                     ] question 2 ?
    [                     ] question 3 ?






## JavaScript

                                 --{{0}}--
In contrast to common Markdown-Parsers it is also possible to include and
execute javascript code. If you combine it with your HTML elements, you are free
to integrate whatever you want.

                                 --{{1}}--
The last statement of your script defines also the result, that will be shown,
if and only if it is not `undefined`, or simply use `console.log` to log the
script activities. As the examples below show, you can combine your scripts with
LiaScript animations. Thus, they will only be execute in the right
fragment/context. But. you can do much much more with scripts.

                                  {{1}}
> Checkout Section [JavaScript](#JavaScript-or-JS-Components) for more information!

``` html
Do some internal calculation <script> 99 * 88  </script>, the next script
contains an error <script> 99 * a </script>.

                                  {{1}}
<div class="ct-chart ct-golden-section" id="chart"></div>
<script>
    // Initialize a Line chart in the container with the ID chart
    new Chartist.Line('#chart', {
        labels: [1, 2, 3, 4],
        series: [[100, 120, 180, 200]]
    });

    console.debug("loaded #chart") // or undefined
</script>
```

Do some internal calculation <script> 99 * 88  </script>, the next script
contains an error: <script> 99 * a </script>.

                                {{2-3}}
<div class="ct-chart ct-golden-section" id="chart1"></div>
<script>
// Initialize a Line chart in the container with the ID chart1
new Chartist.Line('#chart1', {
  labels: [1, 2, 3, 4],
  series: [[100, 120, 180, 200]]
});

console.debug("loaded #chart1")
</script>


                                {{3}}
<div class="ct-chart ct-golden-section" id="chart2"></div>
<script>
// Initialize a Line chart in the container with the ID chart2
new Chartist.Line('#chart2', {
  labels: [1, 2, 3, 4],
  series: [[-100, 120, 180, 20]]
});

console.debug("loaded #chart2")
</script>

                                --{{3}}--
Note, you have to include all required JavaScript-resourses in the initial
comment after the script definition. And by combining this feature with
LiaScript effects, you can build even more sophisticated courses.






## Syntax Highlighting

The following section shows a three types of code blocks, simple inline and
block-code as well as interactive block-code, as an extension to common
Markdown.

### Inline-Code

Inline code via \` enter some code in here 1\#\#\#\$& \` -> ` enter some code in here 1###$& `

### Block-Code

                                --{{0}}--
Syntax highlighting is enabled with highlight.js. Blocks of code are either by
lines with three back-ticks \`\`\` and an identifier for the language. See a
complete list of examples and how to write language names at the
[highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).

````` markdown
```language <- (python, c, javascript, ...)  +OptionalTitle

code ...

```
`````

C example:

``` c Sample.cpp
#include "test.h"

int main () {
    printf("this is an example\n");
    return 0;
}
```

Python example:

``` python
import math

def lia_sqrt(val):
    return math.sqrt(val) + 22
```

### Interactive Code

                                    --{{0}}--

Why should code examples not be interactive and editable, especially if it is
JavaScript or any other language that has been ported to it? Simply add the
required resources to the initial comment with keyword `script`.

1. Add resource to main-comment: `script: url.js`

2. Add a trailing script-tag to your code: `<script>@input</script>`

3. A project with multiple files can be realized with `@input(0)`, `@input(1)`, ...,`@input(n)`.


                                     --{{1}}--
And add an additional script tag to the end of your language definition with an
`@input` macro. This element is afterwards substituted with your code and
executed. We provide some basic examples within the following section.

                                    --{{2}}--
Use the `@input` macro as a parameterized function in projects. The number
defines the the file, starting from 0.



#### JavaScript

                                    --{{0}}--
Click on the run-button to execute the script or double-click on the code to
edit it and to change the output ...

Double-click on the code to switch to edit mode and double-click to get out:

``` javascript
var i=0;
var j=0;
var result = 0;

for(i = 0; i<1000; i++) {
    for(j = 0; j<i; j++) {
        result += j;
    }
}
// the last statement defines the return statement
result;
```
<script>@input</script>

#### Projects

                --{{0}}--
Multiple different code snippets can be combined to form a larger project. It
requires to write them in a row. You can give them names, if you add a second
parameter after the highlighting definition. Add a `+` or `-` to the front of
your filename, in order to indicate, if it should be visible by default or not.

                --{{1}}--
As mentioned earlier the `@input` macro gets substituted by the input of the
editor and you can pass a number to indicate which macro should be substituted
by which code block (`@input(0)` is equivalent to `@input`).

```` markdown
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
<script>
  // insert the JSON dataset into the local variable data
  let data = @input(1);

  // eval the script that uses this dataset
  eval(`@input(0)`);
</script>

````

``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
<script>
  // insert the JSON dataset into the local variable data
  let data = @input(1);

  // eval the script that uses this dataset
  eval(`@input(0)`);
</script>


#### Communication

> If you want to write Markdown, you can skip this section, if you want to learn
> more about creating editable code for various different languages and purposes
> you will have to read this.
>
> Check out https://github.com/LiaTemplates to see more sophisticated examples.

The easiest way to execute some code, is simply to add a script-tag to the end
of your code-block. But, sometimes an execution takes longer or requires to
execute some asynchronous code. For this purpose, LiaScript offers a simple
event system that will be explained in more detail. For simplicity the entire
code block will contain all JavaScript code that can be edited and executed.
This can be placed afterwards below the code block.


To every executed peace of code a `send` module is associated, that is intended
to handle all required communication with that specific code-block or project
and the outer world. Thus, every `send` module is module does only exists in
this particular scope.

To start with, there is a `log` method, which can be used to send different
types of outputs directly to the console. But, you can of course also use the
`console.log` functions that do quite the same. Nevertheless, `send.log` gives
you a little more power when you start to create your own LiaScript libraries
and you have to handle multiple outputs.

``` js
/* send.log(type, sep, content)
*
* params:
*  - type: one of the follow strings "debug", "info", "warn", "error", "html"
*  - sep: a string like separator, mostly for newlines "\n"...
*  - content : represents a list of list
*/

console.debug("these are short hands for send.log('debug' ... ")
console.warn("warn")
console.log("info")
console.error("and red for errors")

console.html("<b>Some more fancy stuff:</b> <img width='40px' src='https://www.math.uni-bielefeld.de/~jsauter/Octahedron.gif'/>")

"fin"
```
<script>@input</script>


As you may have noticed, the last statement of an executed code-block does also
define the `return` statement. However, there are some results that are treated
differently. These are strings that start with `"LIA: "`. The string
`"LIA: stop"` for example, is used to tell the system to simply stop the
execution, without any further output.

``` js
33*33

"LIA: stop" // if you remove this string the result of the
            // calculation will be visible in the shell
```
<script>@input</script>

If the execution of your code may take longer, include some asynchronous calls
or you need to call an external service, you can tell this by finishing with the
statement `"LIA: wait"`, which will show arrows that loop forever or until they
receive a `"LIA: stop"` signal.

``` js
setTimeout(function(){
  console.warn("end of execution")

  send.lia("some other ouput")

  send.lia("LIA: stop") // this stops the execution
}, 3000)


"LIA: wait" // wait until you you send a stop
```
<script>@input</script>

You might probably wonder, why there is a need for `send.lia`, if you could also
pipe output to the console by using `send.log` or the shorthand `console.log`.
As it will be described in the section about error handling, `send.lia` gives
you more control, not only over the shell but also over the editor, see section
[Error Handling](#Error-Handling).

The code example below, depicts how the terminal can be exposed, following the
previous logic, we only have to define `"LIA: terminal"` as the last statement
in order to switch on the terminal mode, that will be active until the user
clicks on the stop button, formerly known as the execute button, or a
`"LIA: stop"` is send from the script, or the browser gets refreshed.

In order to handle the `input` and the `stop` events from the terminal in the
JavaScript world, we have to define handles, as it is done in the code below.
Simply add a function, that evaluates or sends your terminal inputs to a foreign
server or a websocket, or ... whatever you want ... And use the stop handle to
close a connection or do some other stuff, if the user clicks onto the stop
button.

``` js
send.handle("input", input => {
  try{
    console.log(eval(input))
  } catch (e) {
    console.error(e.message);
  }
})

send.handle("stop", e => { alert("execution stopped") })

function close(){
  send.lia("LIA: stop")
}

"LIA: terminal" // execute the code and
```
<script>@input</script>

A little side note, there is also a function called `console.clear`, that does
what it says it clears the console, but it is not a realized by `send.log`,
instead this is a shortcut for `send.lia("LIA: clear")`. These were all

`"LIA: ..."` commands, the next section you will learn how to use the custom
built in event system to get even more stuff done.

##### Ping Pong

All previous functions were executed only within the scope of a single
code-block, but sometimes it is necessary to connect with other external events.
For this purpose, the `send` object also contains two further generic functions,
these are `register` and `dispatch`. Simply use a unique identifier to name an
event, which is followed by a callback-function that does whatever you want.
Both callbacks are defined in local scope, but by using `register` and
`dispatch` you can send messages to any code-block. The example below also
delivers the messages successfully, if both code-blocks would be defined on
different slides.


``` js
send.register("ping", function(e){
  console.warn("ping", e)
})

send.handle("input", input => {
  send.dispatch("pong", input)
})

"LIA: terminal" // execute the code and
```
<script>@input</script>



``` js
send.register("pong", function(e){
  console.warn("pong", e)
})

send.handle("input", input => {
  send.dispatch("ping", input)
})

"LIA: terminal" // execute the code and
```
<script>@input</script>


Adding such script-tags to the end of every code-block can be very tedious and
cumbersome. Your Markdown will contain a lot of not necessary copy & paste code.
To reduce this, LiaScript offers the possibility to define custom macros, and
even more, you can directly import macros from other courses. Section
[Macros](#Macros) is used to describe this issue in more.


##### Error Handling

As mentioned earlier, `send.lia` can do more then just passing messages to the
terminal output. The editor that is currently used by LiaScript is
[ace](https://ace.c9.io), which allows to mark lines with warnings and errors.
Since there is no name associated to a file (like with the `@input(0)` macro).
You have to use a list of lists,  which contain all necessary information that
you want to pass to the editor. The list element is associated with the
code-block, starting from top to bottom.

``` js
send.lia( "ups, something went wrong",
  [[{ row : 1,
      column : 1,
      text : "insert your error info here",
      type : "error"
    },
    {
      row : 2,
      column : 1,
      text : "some general warnings about this line",
      type : "warning"
    }
  ]],
  false); // use true if the output should appear in "info" mode

"LIA: stop";
```
<script>@input</script>


If this seems to complicated, you can also throw and error by using `LiaError`.
The second parameter is used to define the number of code-blocks you use and
then the only thing you require, is to add as much detailed information, which
is similar to the previous example.


``` js
// create a new error with an error message that is
// connected to only one code-block, if you have more,
// increase the number ...
var error = new LiaError("ups something went wrong", 1);

error.add_detail(0, // <- associated code-block
  "insert your error info here",
  "error", 1, 1);

error.add_detail(0, // <- associated code-block
  "some general warnings about this line",
  "warning", 2, 1);


throw(error);
```
<script>@input</script>


#### Styling

As for Tables, it is also possible to apply some basic styling attributes to the
editor. At default code-snippets that ar not executable will not show line
numbers in order to be used also for pseudo-code, while executeable blocks will
show line numbers, while the later ones can be edited and not the others. However,
you can apply the follow attributes to make some definitions explicit. We tried
to apply the common ACE notation. Attributes have to be applied per code-block,
as it is shown in the example:

````` markdown
<!-- data-showGutter="false" -->
```cpp
// some C++ code without line numbers
...
```
<!-- data-readOnly="true" -->
```hpp
// some header-file with lineNumbers,
// that cannot be edited
```
<script>
...// your execution code
</script>
`````

__Attributes:__

* `data-firstLineNumber`: change the initial line number to any number you
  prefer (default: `data-firstLineNumber="0"`).
* `data-fontSize`: change the default font-size, which has to be defined with
  `pt` (default `data-fontSize="12pt"`).
* `data-readOnly`: whether it is an executable snippet or not, there are
  different default values, you can either set only `data-readOnly` to make it
  read-only or pass it a boolean value (`data-readOnly="false"`)
* `data-showGutter`: same as with read-only
* `data-tabSize`: this takes an integer to represent the default tab-size
  replacement (default `data-tabSize="2"`)
* `data-theme`: your default theme as in your settings is applied, but you can
  change this to any of the ace-themes, eg: `Chaos`, `Eclipse`,
  `Soliarized Light`, ...
* `data-marker`: use this to highlight aspects of your code, you have to apply
  the following pattern `data-marker="y1 x1 y2 x2 color type;"`. You start
  with a row and column and end with a row and a column. Then you can apply one
  of the predefined colors, for `error`, `log`, `warn`, `debug` or `info`, or
  you can set your own color with the css rgba function,
  __do not use spaces in this function__!

  The type is optional, but you can choose between one of the following
  ace-marker types: `text`, (default `fullLine`), `screenLine`

  If you want more than one marker, then simply separate different marker
  definitions with a colon ...

<!-- data-marker="
0 0 0 100 error screenline;
2 0 4 200 log;
6 12 6 33 rgba(55,255,100,0.5) text"
data-showGutter="true"
data-theme="chaos"
data-readOnly="false" -->
```
this will be red

this is blue ...
until the next
line

and this is rgba(55,255,100,0.5)
```


#### Examples

##### JavaScript Chartist

A drawing example, for demonstrating that any javascript library can be used,
also for drawing.

<link rel="stylesheet" href="//cdn.jsdelivr.net/chartist.js/latest/chartist.min.css">

``` javascript
// Initialize a Line chart in the container with the ID chart1
new Chartist.Line('#chart1', {
  labels: [1, 2, 3, 4],
  series: [[100, 120, 180, 200]]
});

// Initialize a Line chart in the container with the ID chart2
new Chartist.Bar('#chart2', {
  labels: [1, 2, 3, 4],
  series: [[5, 2, 8, 3]]
});
```
<script>@input</script>

<div class="ct-chart ct-golden-section" id="chart1"></div>
<div class="ct-chart ct-golden-section" id="chart2"></div>


##### Computer-Algebra
<!--
script:   https://cdn.rawgit.com/davidedc/Algebrite/master/dist/algebrite.bundle-for-browser.js
-->


An example of a Computer-Algebra-System (Algebrit), see http://algebrite.org for more examples:

``` javascript
x + x
```
<script> Algebrite.run(`@input`) </script>



```javascript
f=sin(t)^4-2*cos(t/2)^3*sin(t)

f=circexp(f)

defint(f,t,0,2*pi)
```
<script> Algebrite.run(`@input`) </script>



##### Elm

```elm
-- Read more about this program in the official Elm guide:
-- https://guide.elm-lang.org/architecture/user_input/buttons.html

import Html exposing (beginnerProgram, div, button, text)
import Html.Events exposing (onClick)


main =
  beginnerProgram { model = 0, view = view, update = update }


view model =
  div []
    [ button [ onClick Decrement ] [ text "-" ]
    , div [] [ text (toString model) ]
    , button [ onClick Increment ] [ text "+" ]
    ]


type Msg = Increment | Decrement


update msg model =
  case msg of
    Increment ->
      model + 1

    Decrement ->
      model - 1
```


##### C++

Teaching other language-basics is also possible, for this example we applied [JSCPP](https://github.com/felixhao28/JSCPP)
to run simple C++ programs:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 120;
    int rslt = 0;
    for(int i=1; i<a; ++i) {
        rslt += i;
        cout << "rslt: " << rslt << endl;
    }
    cout << "final result = " << rslt << endl;
    return 0;
}
```
<script>
  var output = "";
  JSCPP.run(`@input`, "", {stdio: {write: s => { output += s }}});
  output;
</script>

##### Prolog
<!--
script:   https://curiosity-driven.github.io/prolog-interpreter/parser.js
          https://curiosity-driven.github.io/prolog-interpreter/interpreter.js
-->


See the implementation details at: https://curiosity-driven.org/prolog-interpreter


** Load Database and Rules: **

```prolog
exists(A, list(A, _, _, _, _)).
exists(A, list(_, A, _, _, _)).
exists(A, list(_, _, A, _, _)).
exists(A, list(_, _, _, A, _)).
exists(A, list(_, _, _, _, A)).

rightOf(R, L, list(L, R, _, _, _)).
rightOf(R, L, list(_, L, R, _, _)).
rightOf(R, L, list(_, _, L, R, _)).
rightOf(R, L, list(_, _, _, L, R)).

middle(A, list(_, _, A, _, _)).

first(A, list(A, _, _, _, _)).

nextTo(A, B, list(B, A, _, _, _)).
nextTo(A, B, list(_, B, A, _, _)).
nextTo(A, B, list(_, _, B, A, _)).
nextTo(A, B, list(_, _, _, B, A)).
nextTo(A, B, list(A, B, _, _, _)).
nextTo(A, B, list(_, A, B, _, _)).
nextTo(A, B, list(_, _, A, B, _)).
nextTo(A, B, list(_, _, _, A, B)).

puzzle(Houses) :-
  exists(house(red, english, _, _, _), Houses),
  exists(house(_, spaniard, _, _, dog), Houses),
  exists(house(green, _, coffee, _, _), Houses),
  exists(house(_, ukrainian, tea, _, _), Houses),
  rightOf(house(green, _, _, _, _), house(ivory, _, _, _, _), Houses),
  exists(house(_, _, _, oldgold, snails), Houses),
  exists(house(yellow, _, _, kools, _), Houses),
  middle(house(_, _, milk, _, _), Houses),
  first(house(_, norwegian, _, _, _), Houses),
  nextTo(house(_, _, _, chesterfield, _), house(_, _, _, _, fox), Houses),
  nextTo(house(_, _, _, kools, _),house(_, _, _, _, horse), Houses),
  exists(house(_, _, orangejuice, luckystike, _), Houses),
  exists(house(_, japanese, _, parliament, _), Houses),
  nextTo(house(_, norwegian, _, _, _), house(blue, _, _, _, _), Houses),
  exists(house(_, _, water, _, _), Houses),
  exists(house(_, _, _, _, zebra), Houses).

solution(WaterDrinker, ZebraOwner) :-
  puzzle(Houses),
  exists(house(_, WaterDrinker, water, _, _), Houses),
  exists(house(_, ZebraOwner, _, _, zebra), Houses).
```
<script>
var rules = parser(lexer(`@input`)).parseRules();
window['prolog_db'] = new Database(rules);

"database loaded";
</script>

** Query: ( it may take some time ;-) ) **

```prolog
solution(WaterDrinker, ZebraOwner)
```
<script>
var rslt = "";

var goal = parser(lexer(`@input`)).parseTerm();

for (var item of window.prolog_db.query(goal)) {
    rslt += "Yes: " + item + "\n";
}

if (rslt === "") {
   'No';
} else {
   rslt;
}
</script>

#### More

We provide a list of templates with more examples that can be used to start
developing your own courses. See:

[preview-lia](https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/templates/master/README.md)


## Effects

There are currently four types of effects, that are supported by liaScript:

1. Inline effects
2. Block effects
3. a narrator
4. and Playback functions

Every effect is defined by two braces around one or two numbers `{{1-2}}`, which
marks the order of their appearance. The second and optional number defines, at
which step the element becomes invisible again.

### Inline Effects

                                   --{{0}}--
Inline effects can be used in nearly all liaScript elements, as already
mentioned, the first number within curly braces defines the number of appearance
while the second part defines those Markdown elements that should be revealed
step wise. If you use 0, then the effect will be revealed immediately.

Use this to highlight important facts and to structure your slides (multiple
effects can be combined, due to the usage of equal numbers):

``` markdown
* no effect here
* but in this line {1}{show *** first ***}
* as well as this one {1-2}{show *** first ***}, which contains two effects
  {2}{![image](https://upload.wikimedia.org/wikipedia/commons/d/d0/Creative-Tail-Animal-lion.svg)}
```

* no effect here
* but in this line {1}{show *** first ***}
* as well as this one {1-2}{show *** first ***}, which contains two effects
  {2}{![image](https://upload.wikimedia.org/wikipedia/commons/d/d0/Creative-Tail-Animal-lion.svg)}


### Animations

                                   --{{0}}--
To define animations and transitions, you can use the animate.css notation,
simply place an animation definition within the comment tag after the effects,
as it is done within the examples.


See https://daneden.github.io/animate.css for more animation effects.

``` markdown
* {0}{ *bounce* } <!-- class = "animated infinite bounce" style = "animation-delay: 5s;" -->
* {1-2}{zoomIn} <!-- class = "animated zoomIn" -->
* {2-3}{zoomOut} <!-- class = "animated zoomOut" -->
* {3}{![image](https://upload.wikimedia.org/wikipedia/commons/d/d0/Creative-Tail-Animal-lion.svg)} <!-- class = "animated rubberBand" -->
```

* {0}{ *bounce* } <!-- class = "animated infinite bounce" style = "animation-delay: 5s;" -->
* {1-2}{zoomIn} <!-- class = "animated zoomIn" -->
* {2-3}{zoomOut} <!-- class = "animated zoomOut" -->
* {3}{![image](https://upload.wikimedia.org/wikipedia/commons/d/d0/Creative-Tail-Animal-lion.svg)} <!-- class = "animated rubberBand" -->

### Block Effects

                                   --{{0}}--
Block effects as animations are defined similarly to inline effects, just with
one additional newline after the effect definition. The following Markdown block
is then entirely associated with this effect.

                                   --{{1}}--
You can combine blocks by enclosing them into two lines of equality signs, as
you can see from the examples below, an effect can also contain further effects.


``` markdown
                               {{1-3}}
This is an example for a *single* block effect.

                               {{2-4}}
********************************************************************************

This is an example for a ... wait a second {3 rubberBand}{**multi**} ...
block effect.

* alpha
* beta
* gamma

********************************************************************************
```

                                  {{1-3}}
This is an example for a *single* block effect.

                                  {{2-4}}
********************************************************************************

This is an example for a ... wait a second {3}{**multi**} ...
block effect.

* alpha
* beta
* gamma

********************************************************************************

                                --{{4}}--
You can put spaces before the definition of a block effect, to prevent github
and others from adding the definition to a Markdown paragraph, and thus, to
render the script properly.

### Narrator
<!--
language: en_UK

narrator: UK English Male

@Tom
UK English Male
@end

@Tanja
Russian Female
@end
-->


1. we are using the text-to-speech engine of https://responsivevoice.org
2. the narrator voice must be defined within the initial comment of a script
3. use `--{{number}}--` to indicate what is spoken and when
4. use `--{{number voice}}--` to change the voice for this particular comment
5. you can have multiple comments with the same number, those will be combined,
   but only the voice of the first one is used

``` markdown
                                --{{1}}--
The entire ***Markdown*** paragraph right below the effect definition in double
minus notation is sent to responsivevoice to speak the text out loud. If you
click on the ear button at the navigation panel, then this paragraph gets
rendered at the place where it is defined.

                               --{{3 Deutsch Female}}--
Markdown ist eine vereinfachte Auszeichnungssprache, die von John Gruber und
Aaron Swartz entworfen und im Dezember 2004 mit Version 1.0.1 spezifiziert ...

                               --{{4 @Tanja}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений ...
```

                                --{{1}}--
The entire ***Markdown*** paragraph right below the effect definition in double
minus notation is sent to responsivevoice to speak the text out loud. If you
click on the ear button at the navigation panel, then this paragraph gets
rendered at the place where it is defined.

                                --{{2}}--
The narrator voice is defined within the initial comment, but you can reset this
for the entire section, by adding such a definition directly after the title
tag, or you can add a voice directly after the comment number to let your script
talk in different languages. Proceed and listen ;-)

                                --{{3 Deutsch Female}}--
Markdown ist eine vereinfachte Auszeichnungssprache, die von John Gruber und
Aaron Swartz entworfen und im Dezember 2004 mit Version 1.0.1 spezifiziert
wurde. Ein Ziel von Markdown ist, dass schon die Ausgangsform ohne weitere
Konvertierung leicht lesbar ist.

                               --{{4 @Tanja}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах. Реализации языка Markdown преобразуют
текст в формате Markdown в валидный, правильно построенный XHTML и заменяют
левые угловые скобки («<») и амперсанды («&») на соответствующие коды сущностей.

#### Hidden TTS

Sometimes it might be necessary to add a comment or to read a part aloud to
underline a certain point, which might be necessary in the narrated mode, but
not in the Textbook. Therefor it is possible to put your TTS output into simple
HTML comments. This wont be shown to anyone and also not visible on most other
Markdown parsers and renderer.

```html
<!-- --{{1}}--
Speak this out, but do not show it to anyone.
-->
```

<!-- --{{1}}--
Speak this out, but do not show it to anyone.
-->

### Playback

Since Text2Speech output is baked into the LiaScript notation, why not using it
on purpose for language learners. Thus, you can use `{{|>}}` or `{{!>}}` to
indicate, what should be spoken out loud. You can of course also use different
voices.

```Markdown
    {{|>}}
This entire paragraph will be spoken out __LOUD__.

    {{!> Australian Female}}
* But in this case, this can also be combined
* with a couple of
* - different
  - Markdown elements
  - whether it makes sense or not.
```

    {{|>}}
This entire paragraph will be spoken out __LOUD__.

    {{!> Australian Female}}
* But in this case, this can also be combined
* with a couple of
* - different
  - Markdown elements
  - whether it makes sense or not.

#### Playback-Blocks


And of course, it is also possible to combine various elements by using the
LiaScript block notation. Simply add as many Markdown-blocks between two lines
of asterisks and they will be interpreted as one larger block.


```Markdown
                  {{|>}}
**************************************************
This entire paragraph will be spoken out __LOUD__.

* But in this case, this can also be combined
* with a couple of
* - different
  - Markdown elements
  - whether it makes sense or not.

**************************************************
```

                  {{|>}}
**************************************************
This entire paragraph will be spoken out __LOUD__.

* But in this case, this can also be combined
* with a couple of
* - different
  - Markdown elements
  - whether it makes sense or not.
**************************************************


#### Animations to Playback

Since we are using the double braces notation for playback elements, this can
also be used in combination with animation effects, simply by adding an a
appearance number or  an appearance and dissappearance number. Depending o the
current state of the animation, this will result in different sentences.


```Markdown
    {{1 |>}}
This is an example where {|> 1-2}{I go} _{|> 2}{I am going}_ to work.
```


    {{1 |>}}
This is an example where {|> 1-2}{I go} _{|> 2}{I am going}_ to work.


#### Inlining

And as presented before, you can also use inlining for Playback elements, as it
was used for animations by simply using two pairs of braces
`{|>}{text to speak}` or `{!>}{text to speak}`. While the first looks familiar,
the second type of writing can be used in tables, so it does not interfear with
other Markdown interpreters.


```Markdown
| English              | German                            | Russian                                 | Arabic male               | Arabic female               |
| -------------------- |:--------------------------------- |:--------------------------------------- |:------------------------- | --------------------------- |
| {!>}{I go}           | {!> Deutsch Male}{ich gehe}       | {!> Russian Male}{я хожу}               | {!> Arabic Male}{أذْهبُ}  |                             |
| {!>}{you go}         | {!> Deutsch Male}{du gehst}       | {!> Russian Male}{ты ходишь}            | {!> Arabic Male}{تذْهبُ}  | {!> Arabic Female}{تذْهبين} |
| {!>}{he/she/it goes} | {!> Deutsch Male}{er/sie/es geht} | {!> Russian Male}{он / она / оно ходит} | {!> Arabic Male}{يذْهبُ}  | {!> Arabic Female}{تذْهبُ}  |
| {!>}{we go}          | {!> Deutsch Male}{wir gehen}      | {!> Russian Male}{мы ходим}             | {!> Arabic Male}{نذْهبُ}  |                             |
| {!>}{you go}         | {!> Deutsch Male}{ihr geht}       | {!> Russian Male}{вы ходите}            | {!> Arabic Male}{تذْهبون} | {!> Arabic Female}{تذْهبْن} |
| {!>}{they go}        | {!> Deutsch Male}{sie gehen}      | {!> Russian Male}{они ходят}            | {!> Arabic Male}{يذْهبون} | {!> Arabic Female}{يذْهبْن} |
```


| English              | German                            | Russian                                 | Arabic male               | Arabic female               |
| -------------------- |:--------------------------------- |:--------------------------------------- |:------------------------- | --------------------------- |
| {!>}{I go}           | {!> Deutsch Male}{ich gehe}       | {!> Russian Male}{я хожу}               | {!> Arabic Male}{أذْهبُ}  |                             |
| {!>}{you go}         | {!> Deutsch Male}{du gehst}       | {!> Russian Male}{ты ходишь}            | {!> Arabic Male}{تذْهبُ}  | {!> Arabic Female}{تذْهبين} |
| {!>}{he/she/it goes} | {!> Deutsch Male}{er/sie/es geht} | {!> Russian Male}{он / она / оно ходит} | {!> Arabic Male}{يذْهبُ}  | {!> Arabic Female}{تذْهبُ}  |
| {!>}{we go}          | {!> Deutsch Male}{wir gehen}      | {!> Russian Male}{мы ходим}             | {!> Arabic Male}{نذْهبُ}  |                             |
| {!>}{you go}         | {!> Deutsch Male}{ihr geht}       | {!> Russian Male}{вы ходите}            | {!> Arabic Male}{تذْهبون} | {!> Arabic Female}{تذْهبْن} |
| {!>}{they go}        | {!> Deutsch Male}{sie gehen}      | {!> Russian Male}{они ходят}            | {!> Arabic Male}{يذْهبون} | {!> Arabic Female}{يذْهبْن} |

#### Hiding Text
<!--
@play: {!> @0}{<span style="display: none">@1</span>}
@en: @play(UK English Male,@0)
@de: @play(Deutsch Male,@0)
@ru: @play(Russian Female,@0)
@ar: @play(Arabic @0,@1)
-->

If you only want to show only the play buttons but not the text, it is possible
to use some HTML tricks. The easiest way is to put your text into an HTML
element like `<span style="display: none">Text to read</span>` and make it
invisible by using the attribute `display: none`.

But, since it is possible to define custom [Macros](#macros), you can use also a
more elegant way. Simply add the following comment directly after your Markdown
heading. The `@play` macro has two parameters one for the voice and the other
for the text, the other macros simply define the voice and pass the text as a
second parameter. Within the Arabic macro it is also possible to set the gender
of the narrator.

``` Markdown
#### Hiding Text
<!--
@play: {!> @0}{<span style="display: none">@1</span>}
@en: @play(UK English Male,@0)
@de: @play(Deutsch Male,@0)
@ru: @play(Russian Female,@0)
@ar: @play(Arabic @0,@1)
-->

| go        |         EN          |         DE          |            RU             |      AR male      |      AR female      |
| --------- |:-------------------:|:-------------------:|:-------------------------:|:-----------------:|:-------------------:|
| I         |      @en(I go)      |    @de(ich gehe)    |        @ru(я хожу)        | @ar(Male,أذْهبُ)   |                     |
| you       |     @en(you go)     |    @de(du gehst)    |      @ru(ты ходишь)       | @ar(Male,تذْهبُ)   | @ar(Female,تذْهبين) |
| he/she/it | @en(he/she/it goes) | @de(er/sie/es geht) | @ru(он / она / оно ходит) | @ar(Male,يذْهبُ)   | @ar(Female,تذْهبُ)   |
| we        |     @en(we go)      |   @de(wir gehen)    |       @ru(мы ходим)       | @ar(Male,نذْهبُ)   |                     |
| you       |     @en(you go)     |    @de(ihr geht)    |      @ru(вы ходите)       | @ar(Male,تذْهبون) | @ar(Female,تذْهبْن)  |
| they      |    @en(they go)     |   @de(sie gehen)    |      @ru(они ходят)       | @ar(Male,يذْهبون) | @ar(Female,يذْهبْن)  |

```


The result is a table with playback buttons only:


| go        |         EN          |         DE          |            RU             |      AR male      |      AR female      |
| --------- |:-------------------:|:-------------------:|:-------------------------:|:-----------------:|:-------------------:|
| I         |      @en(I go)      |    @de(ich gehe)    |        @ru(я хожу)        | @ar(Male,أذْهبُ)  |                     |
| you       |     @en(you go)     |    @de(du gehst)    |      @ru(ты ходишь)       | @ar(Male,تذْهبُ)  | @ar(Female,تذْهبين) |
| he/she/it | @en(he/she/it goes) | @de(er/sie/es geht) | @ru(он / она / оно ходит) | @ar(Male,يذْهبُ)  | @ar(Female,تذْهبُ)  |
| we        |     @en(we go)      |   @de(wir gehen)    |       @ru(мы ходим)       | @ar(Male,نذْهبُ)  |                     |
| you       |     @en(you go)     |    @de(ihr geht)    |      @ru(вы ходите)       | @ar(Male,تذْهبون) | @ar(Female,تذْهبْن) |
| they      |    @en(they go)     |   @de(sie gehen)    |      @ru(они ходят)       | @ar(Male,يذْهبون) | @ar(Female,يذْهبْن) |


## Charts

In many cases, a diagram is only used to present some kind of signal paths,
some primitive functions, some clusters or point clouds.

You can still generate images, but why not applying some basic kind of ASCII-art
to solve the most common tasks.

### Line-Plots 1

Markdown-format:

```text
                                  diagram title
1.5 |           *
    |                                 (* stars)
  y |        *      *
  - |      *          *
  a |     *             *       *
  x |    *                 *
  i |   *
  s |  *
    | *                              *        *
  0 +------------------------------------------
     2.0              x-axis                100
```

Result:

                            diagram title
    1.5 |           *                     (* stars)
        |
      y |        *      *
      - |      *          *
      a |     *             *       *
      x |    *                 *
      i |   *
      s |  *
        | *                              *        *
      0 +------------------------------------------
         2.0              x-axis                100


### Line-Plots 2

                                --{{0}}--
All diagram titles, labels, limits are optional, and if you do not define
limits, then the min max values 0 and 1 are used by default.

Markdown-format:

```text
     1 |                   *                       *
       |               *       *               *       *
       |*             *         *             *         *
y-axis | *           *           *           *           *
       |  *         *             *         *             *
       |   *       *               *       *               *
       |       *                       *                      *
    -1 +--------------------------------------------------------
```

         1 |                   *                       *
           |               *       *               *       *
           |*             *         *             *         *
    y-axis | *           *           *           *           *
           |  *         *             *         *             *
           |   *       *               *       *               *
           |       *                       *                      *
        -1 +--------------------------------------------------------


### Multi-Line-Plots

                             --{{0}}--
Next to stars, you can also use any kind of character to define another line,
where the character defines the color. For example an r marks the color red and
a b the color blue.

Markdown-format:

```markdown
| r          *                               (* stars)
|    r                                       (r imaginary course)
|       r *      *       B  B  B  B  B  B  B (B big dots)
|        * r       *
|       *      r      *       *
|      *            r    *
|     *                 r
|   *                          r
| *                              *    r    *
+-------------------------------------------
```

    | r          *                              (* stars)
    |    r                                      (r imaginary course)
    |       r *      *      B  B  B  B  B  B  B (B big dots)
    |        * r       *
    |       *      r      *       *
    |      *            r    *
    |     *                 r
    |   *                          r
    | *                              *    r    *
    +-------------------------------------------



### Dot-Plots

                                 --{{0}}--
If the there are more point with the same character for one x-value, then only
dots are plotted. And by using upper and lower case characters you can also
define the size of the dots.

Markdown-format:

```markdown
    10 |        rrrrrrrrrrrr    x
       |    rrrrrrrrrrrrrrrr
       |  rrrrrrrrrrrrrrrrr  BBBBB
       | rrrrrrrrrrrrrrrr  BBBBBBBB
       |rrrrrrrrrrrrrrr  BBBBBBBBBBB
       |rrrrrrrrrrrrr  BBBBBBBBBBBBB
       |rrrrrrrrrrr  BBBBBBBBBBBBBBB
       | rrrrrrrr  BBBBBBBBBBBBBBBB
       |  rrrrr  BBBBBBBBBBBBBBBBB
       |        BBBBBBBBBBBBBBBB
       |   x    BBBBBBBBBBBBB
       +-----------------------------
         0                           2
```


    10 |        rrrrrrrrrrrr    x
       |    rrrrrrrrrrrrrrrr
       |  rrrrrrrrrrrrrrrrr  BBBBB
       | rrrrrrrrrrrrrrrr  BBBBBBBB
       |rrrrrrrrrrrrrrr  BBBBBBBBBBB
       |rrrrrrrrrrrrr  BBBBBBBBBBBBB
       |rrrrrrrrrrr  BBBBBBBBBBBBBBB
       | rrrrrrrr  BBBBBBBBBBBBBBBB
       |  rrrrr  BBBBBBBBBBBBBBBBB
       |        BBBBBBBBBBBBBBBB
       |   x    BBBBBBBBBBBBB
       +-----------------------------
         0                           2

### Colors

The color codes are somehow defined by the character itself, see the list.

| char | color        | hex       |
| ---- | ------------ | --------- |
| `a`  | Amber        | `#FFBF00` |
| `b`  | Blue         | `#0000FF` |
| `c`  | Cyan         | `#00FFFF` |
| `d`  | Dark red     | `#8B0000` |
| `e`  | Ebony        | `#555D50` |
| `f`  | Forest green | `#014421` |
| `g`  | Green        | `#008000` |
| `h`  | Heliotrope   | `#DF73FF` |
| `i`  | Indigo       | `#4B0082` |
| `j`  | Jade         | `#00A86B` |
| `k`  | Kaki         | `#C3B091` |
| `l`  | Lime         | `#00FF00` |
| `m`  | Mint         | `#3EB489` |
| `n`  | browN        | `#88540B` |
| `o`  | Orange       | `#FF7F00` |
| `p`  | Pink         | `#FFC0CB` |
| `q`  | Queen blue   | `#436B95` |
| `r`  | Red          | `#FF0000` |
| `s`  | Silver       | `#C0C0C0` |
| `t`  | Teal         | `#008080` |
| `u`  | Ultramarine  | `#3F00FF` |
| `v`  |              | `#EE82EE` |
| `w`  |              | `#FFFFFF` |
| `y`  |              | `#FFFF00` |
| `z`  | Zomp         | `#39A78E` |

### Shapes

The shape of the dot is also defined by the character, see the example below.

```text
6 | + * #           A a B b
  | C c D d E e F f G g H h
  | I i J j K k L l M m N n
  | o O P p Q q R r S s T t
  | U u V v W w X x Y y Z z
1 +------------------------
  0                      24
```

    6 | + * #           A a B b
      | C c D d E e F f G g H h
      | I i J j K k L l M m N n
      | o O P p Q q R r S s T t
      | U u V v W w X x Y y Z z
    1 +------------------------
       0                     24


### Line types

As depicted in the line diagrams below, next to different colors, lines and dots
can have different shapes, whether they are dashed, dotted, smoothed or not.

```text
|                 * *    +  +    #  #
|                *   *  +    +  #    #
| N   O   P   Q   R   S   T   U   V   W   X   Y   Z
|NA NOB OPC PQD QRE RSF STG TUH UVI VWJ WXK XYL YZM Z
|An ABo BCp CDq DEr EFs FGt GHu HIv IJw JKx KLy LMz M
|na nob opc pqd qre rsf stg tuh uvi vwj wxk xyl yzm z
|a  ab  bc  cd  de  ef  fg  gh  hi  ij  jk  kl  lm  m
+----------------------------------------------------
```


    |                 * *    +  +    #  #
    |                *   *  +    +  #    #
    | N   O   P   Q   R   S   T   U   V   W   X   Y   Z
    |NA NOB OPC PQD QRE RSF STG TUH UVI VWJ WXK XYL YZM Z
    |An ABo BCp CDq DEr EFs FGt GHu HIv IJw JKx KLy LMz M
    |na nob opc pqd qre rsf stg tuh uvi vwj wxk xyl yzm z
    |a  ab  bc  cd  de  ef  fg  gh  hi  ij  jk  kl  lm  m
    +----------------------------------------------------



## Fun with Tables


As already mentioned, tables cannot only be interpreted as structural elements
within a Markdown document, but also as datasets. In fact, there is little
difference between a diagram and collection of values.


      9 |                                       (* dots)
        |
      y |                              *
      - |
      a |                    *
      x |
      i |          *
      s |
        |*
      0 +------------------------------------
        0            x-axis                 36

The same values collected within a list. If you click onto the little icon above
this list, you will get the same plot as depicted above.

|   x | dots |
| ---:| ----:|
|   0 |    0 |
|  10 |    2 |
|  20 |    4 |
|  30 |    6 |


One of the biggest problems in science is the lack of primary data. Projects
such as the Open-Science-Framework (http://osf.io) try to leverage this, by
offering a plattform, where scientists can store and document vast amounts of
data. But why not directly add and visulaize the data, so that they could be
used and inspected by others, instead of using external tools to create
visualizations.

Everyone who is creating some kind of data or putting it into a Markdown already
performs some kind of configuration. Based on that table's/data's structural
settings, we can __visualize data automatically__. Actually it is quite
surprising, why there has never been an attempt to treat Markdown tables as
datasets. The following sections are intended to give a brief overview on different
visualization options and how the systems determines, which one gets applied.
And of course, you can also enforce your visualization style.

### `LinePlot`

The following dataset was taken from https://ourworldindata.org and it shows
the government expenditure on education in percentage to the GDP. Thus the
first column defines the x-values while the later ones define the categories.

If you click on the image icon again, you will see a more elaborate
representation with title and labels.

<!--
data-title="Government expenditure on education"
data-xlabel="year"
data-ylabel="% of GDP"
-->
| Year | Finland |     USA | Germany |   China |
| ---- | -------:| -------:| -------:| -------:|
| 1995 | 6.80942 |         | 4.42079 | 1.84192 |
| 1996 | 6.86052 |         | 4.48319 | 1.85338 |
| 1997 |         |         |         |         |
| 1998 |         |         | 4.45345 | 1.84432 |
| 1999 | 5.86960 |         |         | 1.88803 |
| 2000 | 5.71687 |         |         |         |
| 2001 | 5.84797 |         |         |         |
| 2002 | 6.02477 |         |         |         |
| 2003 | 6.17476 |         |         |         |
| 2004 | 6.16849 |         |         |         |
| 2005 | 6.03605 |         |         |         |
| 2006 | 5.93809 |         | 4.27930 |         |
| 2007 | 5.68608 |         | 4.34302 |         |
| 2008 | 5.84676 |         | 4.40954 |         |
| 2009 | 6.48517 |         | 4.88047 |         |
| 2010 | 6.54070 | 5.42001 | 4.91368 |         |
| 2011 | 6.48200 | 5.22389 | 4.80779 |         |
| 2012 | 7.19254 | 5.19485 | 4.93331 |         |
| 2013 | 7.15848 | 4.94378 | 4.93496 |         |
| 2014 | 7.15155 | 4.98948 | 4.93112 |         |

https://ourworldindata.org/financing-education#all-charts-preview


The reason for this is, you can actually add additional settings as it was done
to style different Markdown elements, simply by attaching an HTML-comment to the
front of this table. The type of representation is still automatically
determined based on the table structure, but it is still possible to add
attributes like `data-title`, `data-xlabel`, `data-ylabel` to tweak the
graphical representation. See section [Attributes](#attributes) for more
information.


``` markdown
<!--
data-title="Government expenditure on education"
data-xlabel="year"
data-ylabel="% of GDP"
-->
| Year | Finland | USA | Germany |   China |
| ---- | -------:| ---:| -------:| -------:|
| 1995 | 6.80942 |     | 4.42079 | 1.84192 |
| 1996 | 6.86052 |     | 4.48319 | 1.85338 |
| ...  |     ... | ... |     ... |     ... |
```

You can of course also visualize any kind of table, that does not fullfill this
type of classification to line or scatterplot. Define another kind of
presentation and if not all values within the first column can be parsed as
numbers, then they are interpreted as categories. If you change the order of the
table, then also the order of categories in the visualization is changed.

``` md
<!-- data-type="line" -->
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |
```

<!-- data-type="line" -->
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


### `ScatterPlot`


If your table is similar to the one in a LinePlot, but the first column
contains numbers which appear twice or more times, than this data cannot be
interpreted as a "function" in a mathematical sense. This data is then simply
visualized as a scatter plot only showing the dots.


| Random |    I |  II |
| ------:| ----:| ---:|
|    5.0 |  1.0 |   5 |
|    6.0 |  1.0 |   4 |
|    7.0 |  1.0 |   5 |
|    8.0 |  1.0 |   5 |
|    9.0 |  1.0 |   4 |
|   10.0 |  1.0 |   5 |
|    5.0 | 10.0 |   7 |
|    6.0 | 10.0 |   8 |
|    7.0 | 10.0 |   7 |
|    8.0 | 10.0 |   7 |
|    9.0 | 10.0 |   8 |
|   10.0 | 10.0 |   7 |


### `BoxPlot`


If you have a ScatterPlot like representation, but actually want to use this
data as primary data for your BoxPlot, you can manually change the type of
visualization to BoxPlot, simply by adding the following attribute to the head of
your table, as it is shown in the snippet below. Columns are then treated as
datasets and get visualized accordingly.

``` Markdown
<!-- data-type="boxplot" -->
| Random |    I |  II |
| ------:| ----:| ---:|
|    5.0 |  1.0 |   5 |
|    ... |  ... |  .. |
```

<!-- data-type="boxplot" -->
| Random |    I |  II |
| ------:| ----:| ---:|
|    5.0 |  1.0 |   5 |
|    6.0 |  1.0 |   4 |
|    7.0 |  1.0 |   5 |
|    8.0 |  1.0 |   5 |
|    9.0 |  1.0 |   4 |
|   10.0 |  1.0 |   5 |
|    5.0 | 10.0 |   7 |
|    6.0 | 10.0 |   8 |
|    7.0 | 10.0 |   7 |
|    8.0 | 10.0 |   7 |
|    9.0 | 10.0 |   8 |
|   10.0 | 10.0 |   7 |
|        |      |   1 |

### `BarChart`

In contrast to a line or a scatter plot, if the first colum contains at least
one entry thant cannot be parsed as a number, this might be represented also as
BarChart. Which works perfectly with the following example. If the maximum
values of the columns do not differ to much, then this dataset it represented as
a BarChart, otherwise you might end up seeing only one huge bar, while the other
bars are indistiguishable from each other. In this case other visualization are
chosen.


| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


### `Radar`


If for example humans and sheeps are removed from the dataset, then wheight in
kg would not be visible in a BarChart at all. In this case a Radar is selected,
that allows to analyze data visually with different "y"-axis.

| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |


### `PieChart`

If you have a table with only one row full of numbers, this will be
automatically presented as an pie chart. The head represents the categories and
the body the quatities.


| Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
| -------:| -------:| ------:| -------:| ---------:| -----:|
|      50 |      50 |    100 |     200 |       350 |   250 |


You can use the first column to give some more information about your data. If
the first element of the list body contains a text, that cannot be directly
interpreted as a number, then these two text snippets are used to the define the
main title and the subtitle of your chart.

| Music-Style 1994 | Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
|:---------------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| Student rating   |      50 |      50 |    100 |     200 |       350 |   250 |


#### `PieChart`(s)

The default behavior for the Table below, would be to represent it as a bar-chart.
But, you can enforce the usage of pie charts, simply by adding the attribute
`piechart` into the HTML comment, directly above the table:

```markdown
<!-- data-type="PieChart" -->
| Music-Style | Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
|:----------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| 1994        |      50 |      50 |    100 |     200 |       350 |   250 |
| ...         |     ... |     ... |    ... |     ... |       ... |   ... |
```

The result looks as follows:

<!-- data-type="PieChart" -->
| Music-Style | Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
|:----------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| 1994        |      50 |      50 |    100 |     200 |       350 |   250 |
| 2014        |      20 |      30 |    100 |     220 |       400 |   230 |
| demo 2034   |       5 |      12 |     98 |     293 |       345 |    32 |

Since data is parsed at runtime, you can also use animations to change the
values  of chart, while go on in your slide or move back. But keep in mind, that
this might lead to negative effects, if your audience preferes the textbook
mode:

| Music-Style {0-1}{1994} {1}{2014} |           Classic |           Country | Reggae |             Hip-Hop |           Hard-Rock |               Samba |
|:--------------------------------- | -----------------:| -----------------:| ------:| -------------------:| -------------------:| -------------------:|
| Student rating                    | {0-1}{50} {1}{20} | {0-1}{50} {1}{30} |    100 | {0-1}{200} {1}{220} | {0-1}{350} {1}{400} | {0-1}{250} {1}{230} |


If the upper table might be too long and you prefer to use only two columns and
grow your data vertically, then you can use the attribute `data-transpose`,
which flips mirrows your data along an imaginary vertical axis.

```markdown
<!-- data-transpose -->
| Music-Style {0-1}{1994} {1}{2014} |    Student rating |
|:--------------------------------- | -----------------:|
| Classic                           | {0-1}{50} {1}{20} |
| Country                           | {0-1}{50} {1}{30} |
| ...                               |               ... |
```

The result is the same as above, but it might be easier to handle your data.

<!-- data-transpose -->
| Music-Style {0-1}{1994} {1}{2014} |      Student rating |
|:--------------------------------- | -------------------:|
| Classic                           |   {0-1}{50} {1}{20} |
| Country                           |   {0-1}{50} {1}{30} |
| Reggae                            |                 100 |
| Hip-Hop                           | {0-1}{200} {1}{220} |
| Hard-Rock                         | {0-1}{350} {1}{400} |
| Samba                             | {0-1}{250} {1}{230} |

### `Funnel`

Funnel is a similar representation as PieChart, but it is not set automatically.
If you want to use funnel, you will have to set the `data-type` parameter to
funnel.

``` markdown
<!-- data-type="funnel" -->
| Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
| -------:| -------:| ------:| -------:| ---------:| -----:|
|      50 |      50 |    100 |     200 |       350 |   250 |
```

<!-- data-type="funnel" -->
| Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
| -------:| -------:| ------:| -------:| ---------:| -----:|
|      50 |      50 |    100 |     200 |       350 |   250 |

The rest is the same as for piecharts, you can also use effects to generate
animated diagrams.

<!-- data-type="funnel" data-transpose -->
| Music-Style {0-1}{1994} {1}{2014} |      Student rating |
|:--------------------------------- | -------------------:|
| Classic                           |   {0-1}{50} {1}{20} |
| Country                           |   {0-1}{50} {1}{30} |
| Reggae                            |                 100 |
| Hip-Hop                           | {0-1}{200} {1}{220} |
| Hard-Rock                         | {0-1}{350} {1}{400} |
| Samba                             | {0-1}{250} {1}{230} |


### `Map`

A map is similar to a BarChart from the table structure, but if you want to
depict your data on a real map, you will have to add a geojson-file, that
contains all relevant data about the form of your countries, states, cities,
etc. The first column has to match the names of your objects in your geojson
data, that is attached to your table in the following way:

``` markdown
<!-- data-type="map" data-src="https://code.highcharts.com/mapdata/custom/europe.geo.json" -->
| Country                | percent |
| ---------------------- | ------- |
| Albania                | 73.5    |
| Andorra                | 98.9    |
```


<!-- style="height: 600px" data-type="map" data-src="https://code.highcharts.com/mapdata/custom/europe.geo.json" -->
| Country                | percent |
| ---------------------- | ------- |
| Albania                | 73.5    |
| Andorra                | 98.9    |
| Armenia                | 72.4    |
| Austria                | 87.9    |
| Azerbaijan             | 79.8    |
| Belarus                | 79.7    |
| Belgium                | 93.9    |
| Bosnia and Herzegovina | 80.8    |
| Bulgaria               | 66.7    |
| Croatia                | 91.5    |
| Cyprus                 | 84.4    |
| Czech Republic         | 87.7    |
| Denmark                | 97.8    |
| Estonia                | 97.9    |
| Finland                | 94.0    |
| France                 | 92.3    |
| Georgia                | 68.1    |
| Germany                | 96.0    |
| Greece                 | 72.9    |
| Hungary                | 89.0    |
| Iceland                | 99.0    |
| Ireland                | 91.9    |
| Italy                  | 92.5    |
| Latvia                 | 87.1    |
| Liechtenstein          | 98.1    |
| Lithuania              | 90.9    |
| Luxembourg             | 97.8    |
| Macedonia              | 79.2    |
| Malta                  | 83.1    |
| Moldova                | 76.1    |
| Monaco                 | 97.5    |
| Montenegro             | 71.5    |
| Netherlands            | 95.6    |
| Norway                 | 98.4    |
| Poland                 | 78.2    |
| Portugal               | 78.2    |
| Republic of Serbia     | 73.4    |
| Romania                | 73.8    |
| Russia                 | 80.9    |
| San Marino             | 60.2    |
| Slovakia               | 84.9    |
| Slovenia               | 79.9    |
| Spain                  | 92.5    |
| Sweden                 | 96.4    |
| Switzerland            | 93.7    |
| Turkey                 | 83.3    |
| Ukraine                | 93.4    |
| United Kingdom         | 94.9    |
| Vatican City           | 60.1    |

> Currently there is only support to visualize one column, but this will be
> fixed in the future ...



### `HeatMap`

Another type of visualization is a HeatMap, which is used, if the table head and
the first column do only contain numbers, in other words coordinates. If you
want to use categories instead of coordinate numbers, you can enforce the usage
of a heatmap, with the comment shown below:

``` markdown
<!--
data-type="heatmap"
data-title="Seattle mean temperature in Fahrenheit"
data-show
-->
| Seattle |  Jan |  Feb |  Mar |  Apr |  May |  ... |
| -------:| ----:| ----:| ----:| ----:| ----:| ----:|
|       0 | 40.7 | 41.5 | 43.6 | 46.6 | 51.4 |  ... |
|       2 |  ... |  ... |  ... |  ... |  ... |  ... |

```

The attribute `data-show` simply shows the diagram at default, instead of using
the table.

<!--
data-type="heatmap"
data-title="Seattle mean temperature in Fahrenheit"
data-show
-->
| Seattle |  Jan |  Feb |  Mar |  Apr |  May |  Jun |  Jul |   Aug |  Sep |  Oct |  Nov |  Dec |
| -------:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| -----:| ----:| ----:| ----:| ----:|
|       0 | 40.7 | 41.5 | 43.6 | 46.6 | 51.4 | 56.0 | 60.5 |  61.2 | 57.0 | 50.1 | 44.1 | 39.6 |
|       2 | 40.2 | 40.7 | 42.7 | 45.3 | 50.0 | 54.4 | 58.5 |  59.2 | 55.4 | 49.2 | 43.5 | 39.3 |
|       4 | 39.7 | 40.0 | 41.9 | 44.4 | 48.9 | 53.2 | 57.0 |  57.7 | 54.2 | 48.6 | 43.1 | 38.9 |
|       6 | 39.6 | 39.5 | 41.3 | 44.2 | 49.5 | 54.2 | 57.8 |  57.4 | 53.6 | 48.2 | 42.8 | 38.7 |
|       8 | 39.6 | 39.9 | 42.9 | 47.1 | 52.7 | 57.3 | 61.3 |  61.1 | 56.7 | 49.5 | 43.1 | 38.7 |
|      10 | 41.3 | 42.7 | 46.4 | 50.7 | 56.4 | 60.9 | 65.2 |  65.4 | 60.9 | 52.8 | 45.5 | 40.4 |
|      12 | 43.8 | 46.0 | 49.5 | 53.8 | 59.6 | 64.3 | 69.4 |  69.8 | 65.1 | 56.0 | 47.8 | 42.6 |
|      14 | 45.1 | 47.7 | 51.3 | 55.9 | 61.9 | 66.9 | 72.6 |  73.2 | 67.7 | 57.8 | 48.8 | 43.6 |
|      16 | 44.5 | 47.5 | 51.4 | 55.9 | 62.3 | 67.5 | 73.9 |  74.3 | 68.2 | 57.4 | 47.8 | 42.6 |
|      18 | 42.6 | 44.7 | 48.7 | 53.8 | 60.3 | 65.9 | 72.3 |  72.2 | 64.6 | 53.9 | 46.0 | 41.2 |
|      20 | 42.0 | 43.3 | 46.4 | 50.2 | 56.0 | 61.4 | 66.9 |  66.6 | 60.7 | 52.3 | 45.2 | 40.7 |
|      22 | 41.4 | 42.5 | 45.0 | 48.3 | 53.5 | 58.2 | 63.2 |  63.5 | 58.7 | 51.1 | 44.5 | 40.1 |

https://datavizpyr.com/heatmaps-with-seaborn-in-python/

### `Parallel`


A Parallel representation jumps in, if there are simply too many categories, so
that your BarChart would contain only thin lines.

<!-- data-show -->
| Country                |    GDP growth (%) | Births per woman | Life expectancy at birth (years) | Population ages >= 65 (%) | Pop. ages 15-64 (%) | Pop ages 0-14 (%) | Pop (total) |
| ---------------------- | -----------------:| ----------------:| --------------------------------:| --------------------------:| -------------------:| -----------------:| -----------:|
| Albania                |               7.5 |            1.858 |                 76.6337073170732 |            9.3330694913874 |    66.4522208535245 |  24.2147096550882 |     3143291 |
| Andorra                |  3.57073718591123 |            1.260 |                              NaN |                        NaN |                 NaN |               NaN |     83810.5 |
| Austria                |  2.17880778069679 |            1.414 |                 80.4475609756098 |           17.0078802490015 |    67.7942859199021 |  15.1978338310964 |     8336926 |
| Byelarus               | 11.29603925282670 |            1.420 |                 70.6328780487805 |           13.8161084682917 |    71.3440867491758 |  14.8398047825325 |     9680850 |
| Belgium                |  1.00416891576425 |            1.820 |                 80.1095609756098 |           17.2425951179457 |    65.9073170003941 |  16.8500878816601 |    10708433 |
| Bosnia and Herzegovina |  5.41999999999929 |            1.209 |                 75.1063170731708 |           13.7875788575916 |    70.5586044787057 |  15.6538166637027 |     3773100 |
| Bulgaria               |  6.21712220063873 |            1.478 |                 73.3165853658537 |           17.3328904412356 |    69.2610054713067 |  13.4061040874577 |     7623395 |
| Channel Islands        |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Croatia                |  2.35925308110710 |            1.470 |                 75.9121951219512 |           17.1754953634927 |    67.5174504975681 |  15.3070541389392 |     4434000 |
| Czech Republic         |  2.46366103329814 |            1.497 |                 77.2112195121951 |           14.6644147081870 |    71.1889763214880 |  14.1466089703250 |    10424336 |
| Denmark                | -0.86969912719333 |            1.892 |                 78.7004878048781 |           15.9364325701275 |    65.6692750948847 |  18.3942923349878 |     5493621 |
| Estonia                | -5.12891873578752 |            1.661 |                 73.9731707317073 |           16.9573479430650 |    68.0747344729978 |  14.9679175839372 |     1340675 |
| Faroe Islands          |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |       48511 |
| Finland                |  0.92209645431238 |            1.846 |                 79.7919512195122 |           16.5283868561977 |    66.6427434111131 |  16.8288697326892 |     5313399 |
| France                 |  0.21695181782435 |            1.998 |                 81.5204878048781 |           16.6134150592142 |    64.9880225189894 |  18.3985624217964 |    62277432 |
| Germany                |  0.98801573506542 |            1.376 |                 80.0885365853659 |           19.9652972040776 |    66.3351760329956 |  13.6995267629268 |    82110097 |
| Greece                 |  2.01498162894308 |            1.506 |                 79.9631707317073 |           18.1870521529388 |    67.5883962990861 |  14.2245515479751 |    11237094 |
| Hungary                |  0.59999999999994 |            1.352 |                 74.0090243902439 |           16.0592099507043 |    68.9813743902960 |  14.9594156589996 |    10038188 |
| Iceland                |  0.95512219949856 |            2.140 |                 81.5751219512195 |           11.6851788453979 |    67.3938402627208 |  20.9209808918813 |      317414 |
| Ireland                | -3.03575424255612 |            2.100 |                 79.8568292682927 |           11.1093456408398 |    68.3358023622894 |  20.5548519968708 |     4425675 |
| Isle of Man            |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Italy                  | -1.31844836660481 |            1.414 |                 81.9452097560976 |           20.0909973618083 |    65.7289363852644 |  14.1800662529273 |    59832179 |
| Kosovo                 |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Latvia                 | -4.55213597961080 |            1.453 |                 72.2382926829268 |           17.1863911389844 |    69.0425815911418 |  13.7710272698738 |     2266094 |
| Liechtenstein          |  1.79808929851180 |            1.400 |                 82.6341463414634 |                        NaN |                 NaN |               NaN |       35629 |
| Lithuania              |  2.76144078921502 |            1.470 |                 71.8217073170732 |           15.9677094440150 |    68.7509466357882 |  15.2813439201968 |     3358115 |
| Luxembourg             |  0.03220273485962 |            1.605 |                 80.5246341463415 |           14.0365040657173 |    67.9773784654310 |  17.9861174688517 |      488650 |
| Macedonia              |  4.80000000000011 |            1.438 |                 74.2113170731707 |           11.5845850425847 |    69.9825898844976 |  18.4328250729177 |     2041342 |
| Malta                  |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Moldova                |  7.76484641287229 |            1.495 |                 68.4371463414634 |           11.1369548727738 |    71.6754849214449 |  17.1875602057813 |     3633369 |
| Monaco                 |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Republic of Montenegro |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Netherlands            |  1.99580842581707 |            1.775 |                 80.4007317073171 |           14.7235949405444 |    67.3305328508120 |  17.9458722086436 |    16445593 |
| Norway                 |  1.81507058553292 |            1.960 |                 80.7414634146342 |           14.6455888097593 |    66.2064766744808 |  19.1479345157599 |     4768212 |
| Poland                 |  5.00408460108383 |            1.390 |                 75.5331707317073 |           13.3256480555872 |    71.4634305149354 |  15.2109214294774 |    38125759 |
| Portugal               | -0.03467455605676 |            1.374 |                 79.2497560975610 |           17.5012814880078 |    67.1365409199047 |  15.3621775920875 |    10622413 |
| San Marino             |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |         NaN |
| Serbia                 |  5.51795169957776 |            1.400 |                 73.6365853658537 |           14.5167655385706 |    67.6335858157006 |  17.8496486457288 |     7350221 |
| Slovakia               |  6.17046824289093 |            1.320 |                 74.8107317073171 |           11.9677699353106 |    72.3868259638361 |  15.6454041008533 |     5406626 |
| Slovenia               |  3.49251997044142 |            1.528 |                 78.9739024390244 |           16.0267556735963 |    70.1117152095851 |  13.8615291168186 |     2021316 |
| Spain                  |  0.85776978982683 |            1.461 |                 81.0880487804878 |           16.9394050582152 |    68.3398363315641 |  14.7207586102207 |    45555716 |
| Sweden                 | -0.40879886604371 |            1.910 |                 81.2371707317073 |           17.7223651519496 |    65.5617228818501 |  16.7159119662004 |     9219637 |
| Switzerland            |  1.89715399119828 |            1.480 |                 82.1617073170732 |           16.6721873799941 |    67.8197089730996 |  15.5081036469063 |     7647675 |
| Ukraine                |  2.09999999999999 |            1.390 |                 68.2514634146342 |           15.9037623084261 |    70.1546462864768 |  13.9415914050970 |    46258200 |
| United Kingdom         |  0.54791121956627 |            1.940 |                 79.9033658536585 |           16.3019124620612 |    66.1561282590033 |  17.5419592789355 |    61406928 |
| Montenegro             |  6.89999999999999 |            1.642 |                 74.0975365853659 |           12.8497239486590 |    67.5957824239814 |  19.5544936273596 |      622344 |
| Isle of Man            |               NaN |              NaN |                              NaN |                        NaN |                 NaN |               NaN |       80543 |
| Romania                |  9.42580218461200 |            1.350 |                 73.3734146341464 |           14.8579664297396 |    69.8993946432444 |  15.2426389270160 |    21513622 |


### `Graph`

If the first column and the head of the table are equal, then the interpreter
tries to interpret the content of the table as an adjacency matrix, which
defines a graph. If those values are symetrical according to the diagonal, then
the matrix defines an __undirected graph__.

<!-- data-title="Undirected Graph" -->
| Graph |  A  |  B  |  C  |  D  |  E  |
|:----- |:---:|:---:|:---:|:---:|:---:|
| A     |  0  |  1  |  0  |  1  |  0  |
| B     |  1  |  0  |  0  |  1  |  0  |
| C     |  0  |  0  |  0  |  0  |  0  |
| D     |  1  |  1  |  0  |  0  |  1  |
| E     |  0  |  0  |  0  |  1  |  0  |

In contrast to this, if those values differ, then the result is simply an an
__directed graph__, whereby the values define the strength of the line.

<!-- data-title="Directed Graph" -->
| Graph |  A  |  B  |  C  |  D  |  E  |
|:----- |:---:|:---:|:---:|:---:|:---:|
| A     |  0  | 12  |  0  |  1  |  0  |
| B     | -22 |  0  |  0  | 0.4 |  0  |
| C     |  0  |  0  |  0  |  0  |  0  |
| D     |  2  | 12  |  0  |  0  |  1  |
| E     |  0  |  0  |  0  |  2  |  0  |

> Unfortunatelly, self referenceing or multigraphs are currently not supported.


#### `Sankey`

A Sankey diagram is a special type of directed graph that can be used to streams
or the flow of something, such as engergy, money, etc.

https://en.wikipedia.org/wiki/Sankey_diagram

<!-- data-type="sankey" -->
| Sankey |  A  |  B  |  C  |  D  |  E  |
|:------ |:---:|:---:|:---:|:---:|:---:|
| A      |     |  2  |     |     |     |
| B      |  3  |     |     |     |     |
| C      |  1  |  1  |     |     |     |
| D      |     |  1  |  1  |     |     |
| E      |  2  |  1  |  1  |  1  |     |


### `None`

Simply `data-type="none"` to prevent any kind of visualization.

<!-- data-type="none" -->
| Sankey |  A  |  B  |  C  |  D  |  E  |
|:------ |:---:|:---:|:---:|:---:|:---:|
| A      |     |  2  |     |     |     |
| B      |  3  |     |     |     |     |
| C      |  1  |  1  |     |     |     |
| D      |     |  1  |  1  |     |     |
| E      |  2  |  1  |  1  |  1  |     |


### Attributes

* __`data-type`__: You can use `data-type="map|boxplot|barchart|..."` to
  overwrite the automatically identfied representation with your desired one.
  The names can be taken from the previous titles, it is not relevant if you
  use lower or upper-case. This way it is also possible to use types that cannot
  be automatically infered at the moment, such as Sankey or BoxPlot.

  If you do not want to show tables as diagrams, you can also use
  `data-type="None"` and only the table will be visible.

* __`data-show`__: Simply add this attribute or set it to true
  (`data-show="true"`), if you want to visualize your data immediately, without
  the need to click in the switch-button. It is still possible for your users to
  switch to the table representation.

* __`data-transpose`__: Like in the mathematical sense, set this attribute or
  set it to true (`data-transpose="true"`), if you want to switch rows and
  columns. One benefit is, that you can for example use PieChart and let your
  table grow vertically instead of using a horizontal monster.

* __`data-title`__: Normaly, the first cell defines the title of your diagram,
  but if you want larger titles and not have to write gigantic table headers,
  apply this attribute `data-title="Use whatever title you want to ..."`

* __`data-xlabel`__: As above, you can also define the strings for the labels,
  in this case for the x label

* __`data-ylabel`__: or the y label.

* __`data-src`__: Currently this attribute is used to refere to your geojson
  data, if you use the `data-type="Map"` representation, but this might change
  in the future to load and visualize data directly, such as csv.

  If you are using geojson files from external websites such as:

  https://code.highcharts.com/mapdata/

  It can be usefull to use anycors, if the data cannot be visualized due to
  CORS restrictions:

  `data-src="https://cors-anywhere.herokuapp.com/https://code.highcharts.com/mapdata/custom/europe.geo.json"`

### custom

<script input="range" value="2" output="range">@input</script>

<script input="range" value="50" output="amplitude">@input</script>


<script run-once style="display: inline-block; width: 100%">
function func(x) {
    x /= 10;
    return Math.sin(x) * Math.cos(x * @input(`range`) + 1) * Math.sin(x * 3 + 2) * @input(`amplitude`);
}

function generateData() {
    let data = [];
    for (let i = -200; i <= 200; i += 0.1) {
        data.push([i, func(i)]);
    }
    return data;
}

let option = {
    animation: false,
    grid: {
        top: 40,
        left: 50,
        right: 40,
        bottom: 50
    },
    xAxis: {
        name: 'x',
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    yAxis: {
        name: 'y',
        min: -100,
        max: 100,
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    dataZoom: [{
        show: true,
        type: 'inside',
        filterMode: 'none',
        xAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }, {
        show: true,
        type: 'inside',
        filterMode: 'none',
        yAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }],
    series: [
        {
            type: 'line',
            showSymbol: false,
            clip: true,
            data: generateData()
        }
    ]
}

"HTML: <lia-chart option='" + JSON.stringify(option) + "'></lia-chart>"

</script>



<lia-chart
option='{
  "xAxis": {
    "type": "category",
    "data": ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
  },
  "yAxis": {
    "type": "value"
  },
  "series": [{
    "data": [820,932,901,934,1290,1330,1320],
    "type":"line"
  }]
}'></lia-chart>




## ASCII-Art #2

Well, thanks to the great project [SvgBob](https://github.com/ivanceras/svgbob)
the newest version of LiaScript also has support for some basic ASCII art
drawings (not everything is supported yet). Simply use 4 or more backtics to
enclose your artwork and draw whatever you want. And as with any other element,
you can add some styling within HTML comments at the head of this element.

The following examples are taken from the examples on the SvgBob project site.


If you want to use a drawing tool for this, visit the online editor at:

https://ivanceras.github.io/svgbob-editor/

### Graphs

<!-- style="display: block; margin-left: auto; margin-right: auto; max-width: 315px;" -->
``` ascii
                           .--->  F
  A       B     C   D     /
  *-------*-----*---*----*----->  E
           \            ^ \
            v          /   '--->  G
             B --> C -'
```

<!-- style="display: block; margin-left: auto; margin-right: auto; max-width: 315px;" -->
```    ascii
  +------+   +-----+   +-----+   +-----+
  |      |   |     |   |     |   |     |
  | Foo  +-->| Bar +---+ Baz |<--+ Moo |
  |      |   |     |   |     |   |     |
  +------+   +-----+   +--+--+   +-----+
                ^         |
                |         V
  .-------------+-----------------------.
  | Hello here and there and everywhere |
  '-------------------------------------'
```

### Diagrams


``` ascii
  E +-------------------------*--+     E |                         o
  D |-------------------*--*--|--*     D |                   o  o  |  o
  C |-------------*--*  |  |  |  |     C |             o  o  |  |  |  |
  B |-------*--*  |  |  |  |  |  |     B |       o  o  |  |  |  |  |  |
  A +-*--*--+--+--+--+--+--+--+--+     A +-o--o--|--|--|--|--|--|--|--|
      5 10 15 20 25 30 35 40 45 50         5 10 15 20 25 30 35 40 45 50


  85.67 ┤                                       ╭╮
  78.20 ┤                                       ││                  ╭╮
  70.73 ┤                                       ││  ╭╮ ╭╮ ╭╮   ╭╮  ╭╯╰─╮
  63.27 ┤                        ╭╮         ╭─╮ ││ ╭╯╰╮│╰─╯╰╮╭╮│╰──╯   │╭
  55.80 ┤   ╭╮                 ╭╮││╭╮ ╭╮╭╮  │ ╰─╯╰─╯  ││    ││││       ╰╯
  48.33 ┤   │╰╮      ╭──╮      │││││╰╮│╰╯│  │         ╰╯    ╰╯╰╯
  40.87 ┤╭╮ │ ╰╮╭╮  ╭╯  ╰─╮╭╮╭─╯╰╯╰╯ ╰╯  ╰──╯
  33.40 ┤││ │  ╰╯╰╮╭╯     ││╰╯
  25.93 ┤││╭╯     ╰╯      ╰╯
  18.47 ┼╯││
  11.00 ┤ ╰╯
        └───────────┴───────────┴───────────┴───────────┴───────────┴────
      2011        2012        2013        2014        2015        2016
```

### UML


```` ascii
   ____[]
  | ___ |
  ||   ||  device
  ||___||  loads
  | ooo |----------------------------------------------------------.
  | ooo |    |                          |                          |
  | ooo |    |                          |                          |
  '_____'    |                          |                          |
             |                          |                          |
             v                          v                          v
   .-------------------.  .---------------------------.  .-------------------.
   | Loadable module C |  |     Loadable module A     |  | Loadable module B |
   '-------------------'  |---------------------------|  |   (instrumented)  |
             |            |         .-----.           |  '-------------------'
             '------------+-------->| A.o |           |             |
                 calls    |         '-----'           |             |
                          |    .------------------.   |             |
                          |   / A.instrumented.o /<---+-------------'
                          |  '------------------'     |    calls
                          '---------------------------'
````

```` ascii
                                          .--> Base::Class::Derived_A
                                         /
                                        .----> Base::Class::Derived_B
        Something -------.             /         \\
                         \\           /           \\---> Base::Class::Derived
       Something::else    \\         /             \\
            \\             \\       /               '--> Base::Class::Derived
             \\             \\     /
              \\             \\   .-----------> Base::Class::Derived_C
               \\             \\ /
                '------ Base::Class
                        /  \\ \\ \\
                       '    \\ \\ \\
                       |     \\ \\ \\
                       .      \\ \\ '--- The::Latest
                      /|       \\ \\      \\
  With::Some::fantasy  '        \\ \\      '---- The::Latest::Greatest
                      /|         \\ \\
          More::Stuff  '          \\ '- I::Am::Running::Out::Of::Ideas
                      /|           \\
          More::Stuff  '            \\
                      /              '--- Last::One
          More::Stuff
````


### Chemical Structures

```` ascii
    -----. O
          \
           \________
           /        \
          /        \ \
         /            \____________ N
         \            /
          \        / /
           \________/
````

```` ascii
       HO
        \
         \
          \____________
          /------------ O
         /
   _____/
 H2N
````


### Geometrical Shapes


```` ascii
  +------+.      +------+       +------+       +------+      .+------+
  |`.    | `.    |\     |\      |      |      /|     /|    .' |    .'|
  |  `+--+---+   | +----+-+     +------+     +-+----+ |   +---+--+'  |
  |   |  |   |   | |    | |     |      |     | |    | |   |   |  |   |
  +---+--+.  |   +-+----+ |     +------+     | +----+-+   |  .+--+---+
   `. |    `.|    \|     \|     |      |     |/     |/    |.'    | .'
     `+------+     +------+     +------+     +------+     +------+'
````


```` ascii
  ____  ____  ____  ____                      ______________________
 /\   \/\   \/\   \/\   \                    /\                     \
/  \___\ \___\ \___\ \___\                  /  \    _________________\
\  / __/_/   / /   / /   /                  \   \   \                /
 \/_/\   \__/\/___/\/___/                    \   \   \__________    /
   /  \___\    /  \___\                       \   \   \    /   /   /
   \  / __/_  _\  /   /                        \   \   \  /   /   /
    \/_/\   \/\ \/___/                          \   \   \/   /   /
      /  \__/  \___\                             \   \  /   /   /
      \  / _\  /   /                              \   \/   /   /
       \/_/\ \/___/                                \      /   /
         /  \___\                                   \    /   /
         \  /   /                                    \  /   /
          \/___/                                      \/___/
````


```` ascii
                   _______
                  / _____ \
            _____/ /     \ \_____
           / _____/  311  \_____ \
     _____/ /     \       /     \ \_____
    / _____/  221  \_____/  412  \_____ \
   / /     \       /     \       /     \ \
  / /  131  \_____/  322  \_____/  513  \ \
  \ \       /     \       /     \       / /
   \ \_____/  232  \_____/  423  \_____/ /
   / /     \       /     \       /     \ \
  / /  142  \_____/  333  \_____/  524  \ \
  \ \       /     \       /     \       / /
   \ \_____/  243  \_____/  434  \_____/ /
   / /     \       /     \       /     \ \
  / /  153  \_____/  344  \_____/  535  \ \
  \ \       /     \       /     \       / /
   \ \_____/  254  \_____/  445  \_____/ /
    \_____ \       /     \       / _____/
          \ \_____/  355  \_____/ /
           \_____ \       / _____/
                 \ \_____/ /
                  \_______/
````


```` ascii
  .----------------------------------------------------------------------.
  |_.-._.-._.-._.-._.-._.-.    _.-._.-._.-.    _.-._.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._. .::db .-._.-._. .::db .-._.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._ .::d88b -._.-._ .::d88b -._.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-. .::d8888b       .::d8888b ._.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.- .::d88!::::::::::::d888888b _.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.- \  Y88\_________\  Y888888P _.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-. \  Y8888P ._.-. \  Y8888P ._.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._ /dbY88Pdb _.-._ /dbY88Pdb _.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-. /d8P_YP Y8b .-. /d8P_YP Y8b .-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-     /d8P .-.\ Y8b   /d8P .- \ Y8b -._.-._.-._.-._.-._.|
  |_.-._.-._.-._ .::db/d8P _.-. \.::db/d8P _.-. \ Y8b ._.-._.-._.-._.-._.|
  |_.-._.-._.-. .::d88bYP ._.-. .::d88LSP ._.-._ \ Y8b    ._.-._.-._.-._.|
  |_.-._.-._.- .::d8888b       .::d8888b`b _.-._. \ Y8b:db _.-._.-._.-._.|
  |_.-._.-._. .::d88!::::::::::::d888888b`b .-._.- \ YPd88b .-._.-._.-._.|
  |_.-._.-._. \  Y88\_________\  Y888888Pd8b       .::d8888b -._.-._.-._.|
  |_.-._.-._.- \  Y8888P -._.- \  Y8888P!::::::::::::d888888b ._.-._.-._.|
  |_.-._.-._.-. \  Y88Pdb ._.-. \  Y88Pdb_________\  Y888888P ._.-._.-._.|
  |_.-._.-._.-._ \__YP Y8b _.-._ \__YP Y8b`P -._.- \  Y8888P -._.-._.-._.|
  |_.-._.-._.-._.-._. \ Y8b .-._.-. /d\ Y8b .-._.-. /dbY88P .-._.-._.-._.|
  |_.-._.-._.-._.-._.- \ Y8b -._.- /d8P\ Y8b -._.- /d8P_YP _.-._.-._.-._.|
  |_.-._.-._.-._.-._.-. \ Y8b     /d8P _\ Y8b     /d8P _.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._ \ Y8b:db/d8P ._ \ Y8b:db/d8P ._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._. \ YPd88bYP -._. \ YPd88bYP -._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._. .::d8888b       .::d8888b .-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._ .::d88!::::::::::::d888888b -._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._ \  Y88\_________\  Y888888P -._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._. \  Y8888P .-._. \  Y8888P .-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._.- \  Y88P _.-._.- \  Y88P _.-._.-._.-._.-._.-._.|
  |_.-._.-._.-._.-._.-._.-. \__YP ._.-._.-. \__YP ._.-._.-._.-._.-._.-._.|
  `----------------------------------------------------------------------'
````



### Fun

````````````````````````````
                      |
  ____________    __ -+-  ____________
  \_____     /   /_ \ |   \     _____/
   \_____    \____/  \____/    _____/
    \_____                    _____/
       \___________  ___________/
                 /____\

        .---.        .-----------
       /     \  __  /    ------
      / /     \(  )/    -----
     //////   ' \/ `   ---
    //// / // :    : ---
   // /   /  /`    '--
  //          //..\\
         ====UU====UU====
             '//||\\`
               ''``
          Daron Brewood
````````````````````````````

### Unicode

And of course, if your ASCII table does not give you enough pleasure, you can
also use any kind of Unicode symbol (also within the text).

````````````````````````````````
  ┌─┬┐  ╔═╦╗  ╓─╥╖  ╒═╤╕
  │ ││  ║ ║║  ║ ║║  │ ││
  ├─┼┤  ╠═╬╣  ╟─╫╢  ╞═╪╡
  └─┴┘  ╚═╩╝  ╙─╨╜  ╘═╧╛
  ┌───────────────────┐
  │  ╔═══╗ Some Text  │▒
  │  ╚═╦═╝ in the box │▒
  ╞═╤══╩══╤═══════════╡▒
  │ ├──┬──┤           │▒
  │ └──┴──┘           │▒
  └───────────────────┘▒
   ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
````````````````````````````````

### Unicode Art

````````````````````````````
  4 ◇ Sep @tw1tt3rart
 ▀▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀
 ▄▀─▄▀─▄▀─▄▀─▄▀─▄▀─▄▀─▄
 ▀─▄▀─▄▀─▄▀─▄▀─▄▀─▄▀─▄▀
 ▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀▄
 ▀▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀▄─▀
 ▄▀─▄▀─▄▀─▄▀─▄▀

 23 ◇ Apr @tw1tt3rart
 ║█║█║║█║█║█║║█║█║║█║█║█
 ║█║█║║█║█║█║║█║█║║█║█║█
 ║║║║║║║║║║║║║║║║║║║║║║║
 ╚╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩╩

 19 ◇ Jan @tw1tt3rart
 ─────█─▄▀█──█▀▄─█─────
 ────▐▌──────────▐▌────
 ────█▌▀▄──▄▄──▄▀▐█────
 ───▐██──▀▀──▀▀──██▌───
 ──▄████▄──▐▌──▄████▄──
 RT
 @140artist
````````````````````````````

### Unicode Converter

Image generated with:


http://www.underware.nl/fonts/zeitung_mono/features/ASCII+/#feature_info


`````````
........................................................................................................................
........................................................................................................................
........................................................................................................................
........................................................................................................................
........................................................................................................................
.........................................................=...=..........................................................
......................................................=.====.===.=.=....................................................
....................................................========.==========.................................................
...............................................===========I================.............................................
.........................................=...=========I===II=III=III=I======............................................
.........................................=.========I==III=II=III=II==I======............................................
.......................................=.=========III=IIIIII=I=IIII=I=====I=.===........................................
.....................................=..========I==IIIIIIIII=IIIIII=I=I==II======.==....................................
.....................................==========I=I=II=IIIIIIIAIIIAI=I====II========.==..................................
....................................=====I=I===I=.=III=IIIIAAIIIIAI=I==IIII============.................................
.....................................=====II==III==IIAIIIIIAII=AIAIIIIIIII===II=======..................................
...................................==.======II=III==IAIIIIIAII=AAIII=II==I===II=I=====.==.=.............................
....................................========IIIIIII=IIAIIIAAIIIAAIII==I==I==IIIII==I=======.............................
.............................=....=========IIIIIIIIIIIAIIAAAIIIIAIII=IAIII=IIIIIIII=========..==........................
.............................====.======I===IIAAAIIIIAAAIAAAAIAIAIIIIIAIIIAIIAAI======.=======.==.......................
............................===I===========IIIIAAAIIIIAAAAAAAIAIAIAI=IIIIAAIII=I=I==============........................
..............................==II=====III==IIIIIIAAI=AAIAAXAAAAIAAIIAAIAAIIIIII=I===IIII======....=....................
............................=..=IAI===IIIIIIIIIIIAAAAAIAIXIXAAXAIAXAAIIAAAIIAII=IIIIIII========.====....................
...........................====..IAII=IIIII=IIIIAIAIAAAAAXAXAAXAIAAAIAAAAIIIAIIIIIIIIII=====.=.===......................
..................=.......========IIIIIIIIIAIIIIIIIAAXAAAXAAXXXAIXAIAXIAAAIAIIA==I=II=====I=====........................
..................==......=========IIAIIIAIIIIAAAIIIAAAAAXAXXXXAAXAAAAAAAIAIIIII=III=======.=========...................
...................=I==..=====I======IIIIIAAIAIIIAAAAAXXAXXXXAXAAXAXXIAAIAIIIIIIAII==.==IIII==IIII==....................
....................=II===II===IIIIIIIAAAAIAAAAAIIIAXXXXXXXXXXXAAAAAAAXAAAAAAAAAIIIAAAAAIIIIII====......................
....................==IIIIIIIIIIIIAAAAAAXAAAAIIIAIIIAXXXMXXXMXAAXXIAXXAXAAAAIII=IIII======IIII=I=====...................
................==..====IIIAAAAIIIIAIAAAAAXAAXAIIIAAAIXAAMXMMMXXAAXXXXXXAAIIIIIAIIIIIIIIIIIIIII========.................
...............=====II===IIAAAAAIII=====IIAXXAXXAAIAAAAXIAMMMMXAAAXMMXAIIAAAI=====IAIIIIIAII========....................
...................=====IIIIIIAAAAAAAIIIIIIAAAIAAXMMXXXXXXMMMMMXXMMXAIAAAAAIII====IIAAAAIIII=======........=............
...................========IIIIIAXXAAAAIAIIIIIAAAIAXAAAXXXXMMMXXMMMAAAAAAAAAIAIIIIAAAIAIII===========.=====.............
................=======II=========IAXAAXXXXAAAAAXXAAXAAIMMMMMXXMMMAIAAAAIAAXXAAAAAAI==II=========..=======..............
..........========.======IIIIIIIIIIIAAAXXXXXXXXAAXXXMXXXAMMMMMMMXXAAAXAAAAAXAAAAAIIIIIIIIIIIIIIIIIII===.................
............===IIIAIIIIIIIIAAAAAAXXXXXXXXXXXXXAXXAXAXXMXXMMMMMMXMXXXXAAAAAAAIIAIIAAAAAAAAAAIIIIII=====..................
................======IIIIIIIIAAAAAAAAAXAXAAAAXMMMXXAAMXIAMMMMMMMXMXXXXXXXXXXXAAAIIIIIIIIIIAIAII========................
.................====II==I=IIIAIIIIAIAAXAAAAXXXXXXXMXXXMMAMMMMXIAMXAXXXXXXXXXXXAAAAAAAAAIAAIIIIII=I===..................
...............====================IIAAAAXXXXXXXAXXMMMMMXMMWWMMMXXXXXAAAAAAAAAXXXAAAAAII=================...............
....................===...======IIIAAAXXXXAAAXAXIAAIAXMMAAMWWMXAXXAXXXAXAAXXAXAXXXAIIIIIII====I==I====.=................
..................=====IIIIIIAAAAAAAAAAAI=IAIAAA=IIAXXAXMXMWMMIAAAAXXXXXAXAIAAAXAAAAAAAAIIIIII==========................
.................=====IIIIIIAAAIIIII=IIIIIIAXAAIAAAAXXXAIMMMMXIAIXAXXXAAXXXXXAIIIAAAIAAIAIIIII====II====................
.................=======III=I======IIIIIIIAXAAAAIIAAIIIAAAMMMAAAAAIIIAXXXMXXXXAIII==IIIII==IIIII========................
................=================II==IIIAAAAAAAIIAI===IIIMMMMXAIIAIIIIIAAXXXXXXXAAII==IIII========.====.................
.................=====..=============IIAAAAAIIIIIII===IIIXMMMAIIAIIAIII=IAAAAAXXAAAIAII==============...................
........................============IAAAIAAI===I======I==AMMMAIII=IAI====IIIAAAAAAAAIIIIIII===========..................
=....................=======..=====IIII===II============IIMMMIIIIIII=====I===IAAAAAAAI=I=========.......................
====================...====...==============I=============MMMI=================IIAAIIIIIIII========.....................
===========================....===========================MMMI===================IIIIII====I==.==.......................
===============================================..=========MMMI==.=....=================I===I====........................
==========================================================MMMA=============......===..===.===.==........................
==========================================================MMMA===========================..=====...===========.=........
==========================================================MMMX==========================================================
=========================================================IMMMX==========================================================
========II==IIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIAAAIIAIIXMMMMAIIIIAAAIIIIIIIIIIIIIII=IIIII=IIIIIIIIIIII================
XXXXXXXXXXXXXXXXXXXXXXXXXXMXXMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMXXXXMXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMXMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMWMMMMMMMWMWWWWMMWMMWWWWMMWWWWWWWWWWWWMWWWMMWMWWMMMMWWMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
`````````

## Macros

Macros are an easy way in LiaScript to hide reoccurring or tedious tasks. In
essence, they define a simple textsubstitution-system that can be parameterized
and also imported from other courses. Actually, everything that starts with an
`@`-symbol can be replaced by something that has been defined in the main-header
or sub-header of your document.

By now, you will have seen or changed macros like `author`, `logo`, or `comment`,
but you can do even more.

``` markdown
<!--
author: someone who wants to create something new

email: your contact-information
-->

# Main Title
```


### Single Line

There are actually two types of macros, single line macros and block macros.
While the first one only returns a single line, the latter one preserves your
custom indentation. This single line macros start with a macro-name, which is
followed by a colon. The name has to start with a word-character. The starting
`@`-symbol is optional, but I would suggest to use it for custom macros and to
increase readability.

``` markdown
<!--
author: someone who wants to create something new

@Single.line: you can add as much content as you
  want to your single-line macro!

  The only thing that is important, is to use
     indentation.

     Not __matter__ how [much](#12) it is.

-->

# Main Title

@Single.line  <-- this will be replaced at compile-time by: v

you can add as much content as you want to your single-line macro! The only
thing that is important, is to use indentation. Not __matter__ how [much](#12)
it is.

@author <-- by: someone who wants to create something new
```

By the way, macros are case-sensitive, thus there is a difference between
`@author` and `@Author`.

### Blocks

Block-macros are not followed by an colon and are parsed until they reach the
`@end` symbol. Every macro can also be used to define Markdown content, HTML,
CSS, or even JavaScript.

``` md
<!--
@smile: ;-)

@block
this type of macro preserves the structure.

<h1>
@smile and you can also use macros, that
define other macros
</h2>

| Header 1   | Header 2   | Header 3   |
| :--------- | :--------- | :--------- |
| Item 1     | Item 2     | Item 3     |

<script>alert("hello world")</script>
@end
-->

# Main Title

@block
```


### Comments

Commenting macros out or simply adding additional "personal" information to
to a section happens with two additional `@@` for single-line, and three `@@@`s
to comment blocks...

``` md
<!--
@@comment: this is a single line macro
  that has been commented out

@@ if you prefer it, comment blocks can
@@ be defined like this
@@ ...

@@@block-comments

start with three @s and go until the
parser reaches ...

@end
-->
```

### Overwriting Macros

Actually every section can define its own set of macros, that only exist in that
in that single section. Only the initial main-header at the start of a document
defines a set of global macros. This might be useful, if you want to switch the
voice of the narrator, authorship, etc.


``` markdown
<!--
...
narrator: US English Female

-->

# Main Title

....

### Some other section
<!--
author: another author for this section
...
narrator: Australian Male

-->


```

### Passing Parameters

It is also possible to pass parameters to macros, which looks like calling a
function in most common programming languages. Simply call a macro with
parentheses and put into everything, that you want to place within the macro,
where something is placed is simply defined by an `@ + a number`, thus `@0`,
`@1`, .., `@n`. Like most programming languages start counting at `0`, also in
LiaScript `@0` defines the first parameter.

``` markdown
<!--
@highlight: <b style="color: red">@0</b>
-->

@highlight(I want this text to be read and bold)

```


The following example shows, how multiple parameters can be passed to a macro,
they are simply separated by commas. The main problem which appears is that, if
you want to pass a string that contains commas, then this string has to be
placed in backticks. As also depicted, a macro can also call/substitute another
macro, which might be extremely useful if you have defined a very complex macro.
You can define more "simple" macros, that call the "complex" one by setting some
some default values, see therefor section [uid](#uid).

``` markdown
<!--
@highlight: <b style="color: red">@0</b>

@red_and_green:
  @highlight(@0) <i style="color: green">@1</i>
-->

@red_and_green(red,`simply, simply, green`)
```


Last but not least, in order to go on with the basic Markdown syntax, it is also
possible to pass multi-line parameters. How would you do this? Of course simply
by using a common Markdown code-block with three backtics.

````` markdown
@red_and_green(red,```please to not use
this in production...

* it is better to write Markdown
* directly
```)
`````

As mentioned in the code, try to avoid this, since it generates ugly Markdown
code on GitHub or on any other Markdown-interpreter/editor. But you can also use
a code-block, which contains information about syntax highlighting and a macro,
that defines the title. The part within the code-block is then simply passed to
the macro as the last and multi-line parameter.

````` markdown
<!--
link:   https://pannellum.org/css/style.css
        https://cdn.pannellum.org/2.4/pannellum.css

script: https://cdn.pannellum.org/2.4/pannellum.js

@panorama
<div id="panorama_@0" style="width: 100%; height: 400px;"></div>
<script>
  pannellum.viewer('panorama_@0', {
    "type": "equirectangular",
    "panorama": "@1",
    "autoLoad": false,
    "hotSpots": [@2]
});
</script>
@end
-->

```json @panorama("0",https://pannellum.org/images/cerro-toco-0.jpg)
{
  "pitch": 14.1,
  "yaw": 1.5,
  "type": "info",
  "text": "Baltimore Museum of Art",
  "URL": "https://artbma.org/"
},
{
  "pitch": -0.9,
  "yaw": 144.4,
  "type": "info",
  "text": "North Charles Street"
}
```
`````

### Escaping


In some cases, for example if you want to pass content to a javascript string
and you need to escape the content of the LiaScript content, wich could be a
multiline string for example. Then you can simply add a `'` to your macro, for
example:

* `@'input` will result in an escaped version of the input string
* `@'input(1)` is the same as above
* `@'1` as a parameter will also get escaped
* similarly to any other `@'macro(with, some, params)`

> But be carefull to apply it only once in your macro chain as multiple escape
> sequences might result in multiple backslashes (`\\\"`) for special characters.

### Debugging
<!--
@highlight: <b style="color: red">@0</b>

@red_and_green:
  @highlight(@0) <i style="color: green">@1</i>
-->

Creating macros, can be quite difficult, especially if it is about creating and
calling macros nested macros with various parameters. And defining macros in
Atom is somehow similar to navigating in the dark, since it is not possible to
inspect the DOM. But you can escape a macro by and additional `@`, which outputs
a gray and escaped HTML `pre` `code` block.

``` markdown
<!--
@highlight: <b style="color: red">@0</b>

@red_and_green:
  @highlight(@0) <i style="color: green">@1</i>
-->

@@red_and_green(red,`simply, simply, green`)
```

<lia-keep>
<pre style="background:#CCCCCC"><code>
\<b style="color: red"\>red\</b\> \<i style="color: green"\>simply, simply, green\</i\></code></pre></lia-keep>

### Special Macros

The following macros are special ones that are used by the LiaScript to deal with a couple of convenience functions.

#### `attribute`

Attribution is an important issue.
With the attribute command, you can define the attribution that is showed within the info field within the navigation panel.
These elements get also imported if you import the functionality from another course.

A good attribution might look like the following ones...

```md
<!--
attribute: [AlaSQL](https://alasql.org)
  by [Andrey Gershun](agershun@gmail.com)
  & [Mathias Rangel Wulff](m@rawu.dk)
  is licensed under [MIT](https://opensource.org/licenses/MIT)

attribute: [PapaParse](https://www.papaparse.com)
  by [Matthew Holt](https://twitter.com/mholt6)
  is licensed under [MIT](https://opensource.org/licenses/MIT)
-->
```

#### `author`

The author information is visible within the information panel as well as on the course-card on the home-screen.

```md
<!--
author: Your name
-->
```

#### `comment`

This information is shown at the course-card at the home-screen.
It should contain a short and precise description of your course.
This macro will only show one paragraph, even if you define more content.

```md
<!--
comment: Learn something about ...
  even if you insert multiple paragraphs

  there will only be one paragraph
-->
```


#### `date`

A convenience function that can be used to show the latest update time to the user.
This is also shown at the information panel.

```md
<!--
date: 08/03/2020
-->
```


#### `dark`

You can change the default appearance of your document, either if you prefer dark mode or light mode.
This will not change the user preferences.
The default mode is defined by the user settings.

```md
<!--
dark: true

@@ or ...

dark: false
-->
```


#### `email`

Simply add some contact information that is shown in the information panel.
This can also be overwritten for every section.

```md
<!--
email: contact@web.de
-->
```


#### `import`

You can import the main macros of other courses, simply by using the `import` command, which is followed by the raw URL of the foreign course.
You can also import various different courses, every URL will be loaded before the course is loaded.
Only the definitions in the main header are loaded, this includes, scripts, css, macros, attribution, and onload.
Our basic templates are currently hosted at https://github.com/LiaTemplates .
Every course basically describes its macros and how to apply them.
Only the content of this course is loaded for speed-reasons, it is currently not possible to load a course, that requires macros of another course and so on.

```` md
<!--
import: https://raw.githubusercontent.com/liaTemplates/rextester_template/master/README.md
    https://other_url

import: this will import a third url
-->

``` python
print("Hello World")
```
@Rextester.eval(@Python)
````


#### `input`

Use this only in conjunction with executable code and projects or with quizzes.
This macro can only be used in a script tag and gets replaced by the current user input.

To refer to the inputs in a project, use the parameterized macro:

``` md
@input(0)   <== equal to @input
@input(1)
```


#### `language`

Set the internationalization of the course.
This will set basic button information
The currently available languages are defined in:

https://github.com/liaScript/lia-localization

``` md
<!--
@@bulgarian
language: bg

@@english
language: en

@@german
language: de

@@persion
language: fa

@@armenian
language: hy

@@dutch
language: nl

@@ukrainian
language: ua
-->
```


#### `link`

If you need to load additional CSS files, use `link` followed by the URL of your stylesheet.
Similar to `import` or `script`, you can load multiple files.
See https://github.com/liaScript/custom-style for more information on how to define custom styling.

```md
<!--
link: https://some.css
  https://another.css
-->
```


#### `logo`

The logo definition requires a URL of an image, weather absolute or relative.
It is used to define a background image for the course-card at the home-screen.

```md
<!--
logo: ./pics/logo.png
-->
```

#### `mode`

You can change the default style of your document, either if you do not have any effects you can set mode to `Textbook` or start with and interactive `Presentation`.
The three modes a the same as defined within the document at the upper right button. The default mode is defined by the user settings.

```md
<!--
mode: Presentation

mode: Slides

mode: Textbook
-->
```


#### `narrator`

Set the narrator-voice of your course-speaker.
The voice is a service of https://responsivevoice.org that is free for non-commercial educational content.
The list below shows all currently available voices and languages.

```md
<!--
narrator: Afrikaans Male
-->
```


| Female                        | Male                        |
| ----------------------------- | --------------------------- |
| UK English Female             | UK English Male             |
| US English Female             | US English Male             |
|                               | Afrikaans Male              |
|                               | Albanian Male               |
| Arabic Female                 | Arabic Male                 |
|                               | Armenian Male               |
| Australian Female             | Australian Male             |
| Bangla Bangladesh Female      | Bangla Bangladesh Male      |
| Bangla India Female           | Bangla India Male           |
|                               | Bosnian Male                |
| Brazilian Portuguese Female   | Brazilian Portuguese Male   |
|                               | Catalan Male                |
| Chinese Female                | Chinese Male                |
| Chinese (Hong Kong) Female    | Chinese (Hong Kong) Male    |
| Chinese Taiwan Female         | Chinese Taiwan Male         |
|                               | Croatian Male               |
| Czech Female                  | Czech Male                  |
| Danish Female                 | Danish Male                 |
| Deutsch Female                | Deutsch Male                |
| Dutch Female                  | Dutch Male                  |
|                               | Esperanto Male              |
|                               | Estonian Male               |
| Filipino Female               |                             |
| Finnish Female                | Finnish Male                |
| French Canadian Female        | French Canadian Male        |
| French Female                 | French Male                 |
| Greek Female                  | Greek Male                  |
| Hindi Female                  | Hindi Male                  |
| Hungarian Female              | Hungarian Male              |
|                               | Icelandic Male              |
| Indonesian Female             | Indonesian Male             |
| Italian Female                | Italian Male                |
| Japanese Female               | Japanese Male               |
| Korean Female                 | Korean Male                 |
| Latin Female                  | Latin Male                  |
|                               | Latvian Male                |
|                               | Macedonian Male             |
| Moldavian Female              | Moldavian Male              |
|                               | Montenegrin Male            |
| Nepali                        | Nepali                      |
| Norwegian Female              | Norwegian Male              |
| Polish Female                 | Polish Male                 |
| Portuguese Female             | Portuguese Male             |
| Romanian Female               | Romanian Male               |
| Russian Female                | Russian Male                |
|                               | Serbian Male                |
|                               | Serbo-Croatian Male         |
| Sinhala                       | Sinhala                     |
| Slovak Female                 | Slovak Male                 |
| Spanish Female                | Spanish Male                |
| Spanish Latin American Female | Spanish Latin American Male |
|                               | Swahili Male                |
| Swedish Female                | Swedish Male                |
| Tamil Female                  | Tamil Male                  |
| Thai Female                   | Thai Male                   |
| Turkish Female                | Turkish Male                |
| Ukrainian Female              |                             |
| Vietnamese Female             | Vietnamese Male             |
|                               | Welsh Male                  |


#### `onload`

Sometimes it might be necessary to preload some JavaScript code that is gets executed before the course is loaded.
Or you want to define some global functions that can be used afterwards everywhere.
`onload` actually does the same as its HTML counterpart and is used to accomplish this task.

``` md
<!--
@onload
// this macro contains some important functions that are loaded
// only once ...

alert("Hello World")
@end
-->
```

#### `script`

Load all required JavaScript files/libraries with this command.

``` md
<!--
script: https://some.js
  https://another.js
  ...
-->
```

#### `translation`

If you already have some translated versions of your course or know where they can be found, then use this macro.
Simply add the name and the URL.
This links will be also visible within the information panel of your course.

``` md
<!--
translation: Deutsch  translations/German.md
translation: Français translations/French.md
translation: Русский  translations/Russian.md
-->
```

#### `uid`

This macro can only be used within the document, not within the header.
Sometimes it is necessary to define unique identifiers if you want to access some HTML nodes and do not want to name every manually.
In this case it might be useful to define hidden macros, that make use of `@uid` which generates a unique identifier, whenever it is called.
See for example https://github.com/liaTemplates/Rextester to see the application of this pattern for creating macros.


```md
<!--
@eval: @hidden_eval(@uid,@input)

@hidden_eval
<script>
// eval @input
...
// and do somethint with the content of "name_.."
document.getElementByName("name_@0")
</script>


<div id="id_@0"></div>

@end
-->
```


#### `version`

A very important information is the `version`, it follows the major.minor.patch
notion. If you start to develop a course, you can leave this out, and you will
be in some kind of development-version or as long as you are in major-version 0
the course should be parsed, every time it is loaded. This is fine for small
courses and no persistent content. But, if you include executable code or
quizzes, this content is stored persistently at IndexedDB directly within your
browser.

If your course is ready or very large, it might make sense to define a major
version, such as `1.0.12`. The benefit of this is, that every time, the user
loads the course, the app tries to download the raw Markdown file and then it
checks the version information, if the version is the same as the one that is
currently stored within IndexedDB, then it does not require to preprocess the
entire document again, instead it directly loads the preprocessed version
directly. This is especially useful for smart phones.

``` markdown
<!--
version: 0.0.1
...
-->

# Main Title
```


__So how to change the version information?__

If you only fix typos or add or change static content, it is sufficient enough
to increase the patch element and thus for example `1.0.14` to `1.0.15`.

If you add slides to the end of your document, it is okay to increase the minor
version number, eg. going from `1.0.15` to `1.1.0`.

Major versions changes are required, if you change the structure of your
document, especially quizzes and code. As already mentioned these persistent
state information are stored within IndexedDB, but moving code or quizzes from
one slide to another will might destroy previous states. For this purpose major
version changes are required (`1.1.0` -> `2.0.0`), which will result in a new
version also in IndexedDB. The old code/state is still available and can be
restored.

## JavaScript or JS-Components

> By the time of writing this, I do strongly believe that the script-tag, that
> was introduced by Netscape in 1995 (cf.
> [Wikipedia](https://en.wikipedia.org/wiki/JavaScript#History)), is used in the
> wrong way. It is still somehow outside of HTML, although, if it could embedded
> as part of the DOM, we would not have to search the DOM for IDs and try to
> manimpulate the content of a certain node. Much of the work, that we try to
> put into the development of Web-Components could be easily achieved by using
> only the script-tag slightly different.

In LiaScript we now have the power to insert script everywhere and to connect
them with a simple publish-subscribe mechanism, in order to create even more
interactive books and courses. Thus you can add additional calculations
everywhere within your document and the internal LiaScript- event-system handles
their execution. This can be seen as an inverse attempt to Jupyther- or
R-Notebooks, where content is placed around code for documentation. We try to
integrate code as a native element into content.

> All scripts are executed only after all external javascript-files have been
> imported.

### Basics

Simply use the well-know `<script> ... </script>` (nearly) everywhere within
your document to perform any kind of calculation 10 percent from 99 \$ is equal
to <script>99 * 0.1</script>. Or, you can also query any kind of external
service such as https://www.wikidata.org, weather forecasting from
https://openweathermap.org or random gifs of cats from https://giphy.com, as it
is depicted below.

    <script run-once>
    fetch('https://api.giphy.com/v1/gifs/random?api_key=XuS4MlQmIR6WQpMA8Zpxv4shNfJW8Aci&tag=cat')
      .then(response => response.json())
      .then(data => send.html(`<img height="250px" src="${data.data["image_url"]}">`))

    "loading"
    </script>


> If you are "reading" this course in LiaScript, you will have noticed, that the
> background of those script-results is actually gray. You can double-click on
> them to see what is actually inside and edit the code. If you click somewhere
> else, so that the object loses its focus, the script gets reevaluted.

Usage
=====

The snippet below depicts how such scripts can be defined. The result of a
script is directly used as the content of the cell and placed exactly there
where the script-tag was originaly defined. The result of the first cell is
obvious, it is a number. The larger second script actually has two different
results, the first result is the string `loading`, the second one is generated
by the promise of the JavaScript fetch-API, it triggers a download process for
the given url and if this is successful, the send-object is used to send back a
string that is internally interpreted as a new HTML-image.


``` markdown
Some inline calculation: <script>99 * 0.1</script>

<script run-once>
fetch('https://api.giphy.com/v1/gifs/random?api_key=...tag=cat')
  .then(response => response.json())
  .then(data => send.html(`<img height="250px" src="${data.data["image_url"]}">`))

"loading"
</script>
```

The following code snippet shows a more obvious example, the script generates  a
timeout that triggers the execution of the function after 5 seconds. Which
means, that the first result is the string `waiting for 5 seconds` and after
this time a new result is generated: `I am ready!`.

``` markdown
<script run-once>
setTimeout(function(){
  send.lia("I am ready!")
}, 5000)

"waiting for 5 seconds"
</script>
```

However, there is a better way of doing this. Within the example above, the
script is marked by LiaScript that is not running anymore, since a first valid
result was already generated, which means, that this script is triggerd also for
the next time, if you go to the next slide and return. One way of dealing with
this issue, is to used the attribute `run-once` or `run-once="true"` to
indicate, that the code should only be executed once. The result of the script
is stored and the script is never again executed. But, you can also use the same
methids as they were introduced in section [Communication](#communication).

That means, you can use the two return strings, but you can use also the two
functions:

* `"LIA: wait"` --> `send.wait()`
* `"LIA: stop"` --> `send.stop()`

``` markdown
<script>
setTimeout(function(){
  send.lia("I am ready!")
}, 5000)

"LIA: wait" // or send.wait()
</script>
```

The function `send.lia` marks the execution of the script to be finished, but in
the case that your produce continous results, you can use the following:

``` markdown
<script>
function counter(i) {
  if (i > 0) {
    send.output("HTML: <h"+i+" style='display: inline-block'>hallo " + i +"</h"+i+">")
    setTimeout(() => counter(i-1), 1000)
  } else {
    send.stop()
  }
}

counter(6)

send.wait() // or "LIA: wait"
</script>
```

Actually only two functions, `send.lia` and `send.output`. The functions
`send.wait` and `send.stop` are actually only shortcuts for
`send.lia("LIA: wait")` and `send.lia("LIA: stop")`. In the same way `send.html`
is only a shortcut for `send.lia("HTML: " + ...)`, as it is depicted below.

``` markdown
<script>
let html_string = "<h2>Markdown</h2>"
send.html(html_string)
send.lia("HTML: " + html_string)
"HTML: " + html_string
</script>
```

Errors
======

Every script can contain errors, and so does the follow script <script> a * 33
</script>. The error message is printed in red, even if you only wanted to
execute a script, that does not produce any outputs. You can double-click onto
the error message to edit the code and define the variable `a`.


### Execution & Animations

You can combine scripts with LiaScript animations and thus trigger their
execution. If you are in textbook mode all scripts will be executed. If a script
does not belong to an animation, it will be executed immediately when you open a
slide on every time you visit the slide, if you do not set the parameter
`run-once` or if the the slide is not marked as running.

``` html
<script>alert("0")</script>

{{1}} <script>alert("1")</script>

{{2}} <script>alert("2")</script>

{{3}} <script>alert("3")</script>
```

<script run-once>alert("0")</script>

{{1}} <script>alert("1")</script>

{{2}} <script>alert("2")</script>

{{3}} <script>alert("3")</script>

A script is only executed within the local scope of a slide. It is not possible
to trigger the execution of scripts from slides that have not been visited. But
scripts can remain active, even if you go to another slide.


### `input`

Using only static scripts is actually boring, we want to interact with the
scripts and pass input values. In LiaScript this is achieved through a
combination of script-tags with input-tags. Simply add the parameter `input`
to with an additional type information to the script tag.

> All possible types that are defined by the HTML5 standard can be used, as well
> as their specific parameters. These are automatically passed to the generated
> input:
>
> https://www.w3schools.com/tags/tag_input.asp


Scripts that are combined with an input are marked by a thin frame, you can
click on them and change the input. And, different inputs pruduce different
result and might trigger the execution slightly differently 😏

#### `button`

The code as depicted below, will implement a simple clickable button. The script
is loaded once, when the slide is rendered and then every time you click on it.


``` html
<script input="button">
alert("click")

"click me"
</script>
```

<script input="button">
alert("click")

"click me"
</script>


#### `text`

This is also the default input. It shows also the usage of the `@input` macro.
It defines the place, where the current the input value should be placed. Since
with the same input, text, numbers, code, etc. could be defined, you have to
decide if it is interpreted as a string in `""` or used as part of your code.
The attribute `value` is used as the default initial input to your script, for
the first execution. If no `value` is defined, then the default input is an
empty string.

``` html
<script input="text" value="reverse">
let str = "@input"
// the input string gets reversed
str.split("").reverse().join("")
</script>
```


Text inputs are evaluted emediately on every change.


<script input="text" value="reverse">
let str = "@input"

str.split("").reverse().join("")
</script>


> For more information about text inputs see:
>
> https://www.w3schools.com/tags/att_input_type_text.asp

#### `number`

The number input is similar to text, but only numbers are allowed as input and
you can set additional parameters such aus `min`, `max`, and `step`.

``` markdown
<script input="number" value="1" min="0" max="1000000">
let i = @input // direct usage as a number

"Square of " + i + " = " + i * i
</script>
```

As for texts, the input is evaluted on every change.

<script input="number" value="1" min="0" max="1000000">
let i = @input

"Square of " + i + " = " + i * i
</script>

> For more information about number inputs see:
>
> https://www.w3schools.com/tags/att_input_type_number.asp

#### `range`

The range is actually a slider, that generates numbers as input and you can set
additional parameters such aus `min`, `max`, and `step`.

``` markdown
<script input="number" value="1" min="0" max="1000" step="0.1">
let i = @input // direct usage as a number

"Square of " + i + " = " + i * i
</script>
```

The input is evaluted on every change.

<script input="range" value="0" min="0" max="360" step="0.1">
let i = @input

"Sinus of " + i + " = " + Math.sin(i)
</script>

> For more information about range inputs see:
>
> https://www.w3schools.com/tags/att_input_type_range.asp


#### `search`

The search input is actually text input, but in contrast to text, the script is
only executed after the input field looses its context.

``` markdown
<script input="search" value="abcdefg">
let str = "@input"

"reverse of \"" + str + "\" -> " + str.split("").reverse().join("")
</script>
```

---

<script input="search" value="abcdefg">
let str = "@input"

"reverse of \"" + str + "\" -> " + str.split("").reverse().join("")
</script>

> For more information about search inputs see:
>
> https://www.w3schools.com/tags/att_input_type_search.asp


#### `password`


The password input is actually text input, but in contrast to text the input is
not directly visible and the script is only executed after the input field
looses its context.

``` markdown
<script input="password">
let password = "@input"

if (password == "LiaScript") {
  "You got it!"
} else {
  "please enter the correct password"
}
</script>
```

---

<script input="password">
let password = "@input"

if (password == "LiaScript") {
  "You got it!"
} else {
  "please enter the correct password"
}
</script>

> For more information about password inputs see:
>
> https://www.w3schools.com/tags/att_input_type_password.asp


#### `radio`

In contrast to the commonly usage of radio buttons, which requires the
definition of multiple radio inputs, LiaScript achieves the same with input
`radio` and the definition of the `options` parameter. All possible options are
separated by `|`. Thus, the user can only select one of the defined options.


``` html
<script input="radio" value="1" options="1|2|3|Hello World|true">
"Selected option: @input"
</script>
```

Changes will trigger an immediate execution of the script.

<script input="radio" value="1" options="1|2|3|Hello World|true">
"Selected option: @input"
</script>

> `options` is not a standard HTML parameter, for more information on radio
> inputs see:
>
> https://www.w3schools.com/tags/att_input_type_radio.asp

#### `select`

`select` is actually not an input type, but we added it, since it allows to
perform the same task as radio-buttons, but the representation is a drop-down
list. The usage of `options` and their separation by `|` is equal to radio
buttons.

``` html
<script input="select" value="1" options="1|2|3|Hello World|true">
"Selected option: @input"
</script>
```

Changes will trigger an immediate execution of the script.

<script input="select" value="1" options="1|2|3|Hello World|true">
"Selected option: @input"
</script>

> `options` is not a standard HTML parameter, for more information on radio
> inputs see:
>
> https://www.w3schools.com/tags/tag_select.asp


#### `checkbox`

Checkboxes in contrast to radio-buttons or select allow you to select multiple
elements at once or none.

If no options are defined, a checkbox is treated as a single input that switches between true and false, wheather, the checkbox is checked or not:

``` html
<script input="checkbox" value="true">
"@input"
</script>
```

<script input="checkbox" value="true">
"@input"
</script>

---

If you define `options` the current value as well as the result is treated
as a list of strings in JSON format:

``` html
<script input="checkbox" value='["Ben"]' options="Ben|Jerry|Tom|Hardy" >
@input
</script>
```

<script input="checkbox" value='["Ben"]' options="Ben|Jerry|Tom|Hardy" >
@input
</script>

---

This might not be a sufficient and readable, therefor it is also possible to
define formats for outputs (see section
[Formatting with Intl](#Formatting-with-Intl)). The `list` format for example
allows to add language specific textual formatting for list. If you do not add
locale information the document language is used as a default.

``` html
<script
  input="checkbox"
  value='["Ben", "Jerry", "Tom"]'
  options=" Ben | Jerry | Tom | Hardy "

  format="list" locale="en"
>
  let list = @input

  if (list.length == 0)
    ["no one"]
  else
    list
</script>
```

<script
  input="checkbox"
  value='["Ben", "Jerry", "Tom"]'
  options=" Ben | Jerry | Tom | Hardy "

  format="list" locale="en"
>
  let list = @input

  if (list.length == 0)
    ["no one"]
  else
    list
</script>


> For more information about checkbox inputs see:
>
> https://www.w3schools.com/tags/att_input_type_checkbox.asp


#### `date`

Date allows offers a datepicker. The normal return value is a string of the
format `YYYY-MM-DD` (Year-Month-Day), but it is also possible to tweak this
output according to some language specific formats.

``` html
<script input="date" value="2020-10-10" format="datetime" locale="en">
"@input"
</script>
```

The execution is triggered on every change.

<script input="date" value="2020-10-10" format="datetime" locale="en">
"@input"
</script>

> For more information about date inputs see:
>
> https://www.w3schools.com/tags/att_input_type_date.asp


#### `datetime-local`

Datetime-local includes the date and time. The standard return format is
`YYYY-MM-DDTHH:MM` (Year-Month-DayTHour:Minutes). The execution is triggered on
every change.

``` html
<script input="datetime-local" value="2020-11-20T12:30">
"@input"
</script>
```

<script input="datetime-local" value="2020-11-20T12:30">
"@input"
</script>

But of course, it is also possible to format time and date:

``` html
<script input="datetime-local"
        value="2020-11-20T12:30"
        format="datetime"
        locale="en"
        dateStyle='full'
        timeStyle='short'>
"@input"
</script>
```

<script input="datetime-local"
        value="2020-11-20T12:30"
        format="datetime"
        dateStyle='full'
        timeStyle='short'>
"@input"
</script>

> For more information about datetime-local inputs see:
>
> https://www.w3schools.com/tags/att_input_type_datetime-local.asp


#### `time`

``` html
<script input="time" value="11:30">
"@input"
</script>
```

<script input="time" value="11:30">
"@input"
</script>

> For more information about time inputs see:
>
> https://www.w3schools.com/tags/att_input_type_time.asp



#### `email`


``` html
<script input="email" placeholder="please your Email">
let email = "@input"

if (email) {
  email
} else {
  "email"
}
</script>
```

<script input="email" placeholder="please your Email">
let email = "@input"

if (email) {
  email
} else {
  "email"
}
</script>

> For more information about time inputs see:
>
> https://www.w3schools.com/tags/att_input_type_email.asp


#### `url`


``` html
<script input="url" value="url">
"@input"
</script>
```

<script input="url" value="url">
"@input"
</script>

> For more information about url inputs see:
>
> https://www.w3schools.com/tags/att_input_type_url.asp


#### `tel`

``` html
<script input="tel" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" placeholder="123-45-678">
let tel = "@input"

if (tel) {
  tel
} else {
  "tel"
}
</script>
```

<script input="tel" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" placeholder="123-45-678">
let tel = "@input"

if (tel) {
  tel
} else {
  "tel"
}
</script>

> For more information about tel inputs see:
>
> https://www.w3schools.com/tags/att_input_type_tel.asp


#### `submit`

I qually used as the `button` input, see therefor section [button](#button)

#### `month`

``` html
<script input="month" value="1999-12">
"@input"
</script>
```

<script input="month" value="1999-12">
"@input"
</script>

> For more information about month inputs see:
>
> https://www.w3schools.com/tags/att_input_type_month.asp

#### `week`


``` html
<script input="week" value="2020-W40">
"@input"
</script>
```

<script input="week" value="2020-W40">
"@input"
</script>

> For more information about week inputs see:
>
> https://www.w3schools.com/tags/att_input_type_week.asp

#### `file`

not working yet ...

> For more information about file inputs see:
>
> https://www.w3schools.com/tags/att_input_type_file.asp


#### `hidden`

This type is special, as it does not produce any visible output, but as shown in
section [output](#output), this can be used to hide complex calculation, that
might be used by various different elements as input.

``` html
<script input="hidden">
{value: 12, height: "12px", points: 123.12}
</script>
```

#### `color`

Defines a color picker. The normal return value has the format `#RRGGBB` (red
green blue). The number values are defined in hex ranging from 00 to FF.

```html
<script input="color" value="#FF0000">
"HTML: <b style='color:@input'>@input</b>"
</script>
```

<script input="color" value="#FF0000">
"HTML: <b style='color:@input'>@input</b>"
</script>

> For more information about color inputs see:
>
> https://www.w3schools.com/tags/att_input_type_color.asp


#### `image`

Not used atm.

#### `textarea`

This is also not a input type, but instead the application of the textarea HTML
element. This can be used to edit more complex multiline strings. The script is
only executed after the element has lost its context.

``` html
<script input="textarea" value="<span style='font-size: 32px'>hallo</span>" style="width:100%">
`HTML: @input`
</script>
```

<script input="textarea" value="<span style='font-size: 32px'>hallo</span>" style="width:100%">
`HTML: @input`
</script>

> For more information about textareas see:
>
> https://www.w3schools.com/tags/tag_textarea.asp


### `output`
<!--
boolean: <script input="checkbox" value="true" output="@0" modify="false">
         @input
         </script>

and:     <script modify="false">@input(`@0`) && @input(`@1`) </script>
-->


You can use the `output="channel-name"` parameter to define a dedicated channel,
on which the script publishes its changed outputs and other scripts can
subscribe to these changes via `input(channel-name)`, but the channel name has
to be in markdownish style backtics, as depicted below:

``` html
publishing node P
<script input="checkbox" value="true" output="P">
@input
</script>
AND Q
<script input="checkbox" value="true" output="Q">
@input
</script>
result in:
<script output="AND">
@input(`P`) && @input(`Q`)
</script>
```

publishing node P
<script input="checkbox" value="true" output="P">
@input
</script>
AND publishing node Q
<script input="checkbox" value="true" output="Q">
@input
</script>
result in:
<script output="AND">
@input(`P`) && @input(`Q`)
</script>

Within the example above you can also see the difference between scripts with
and without associated inputs. Scripts with inputs do have a frame, while
scripts without inputs do only have grey backgound.


Combining scripts with macros
=============================

Such scripts are of course complicated to read and require a lot of boilerplate
code, which could and should be hidden behind macros, to make the text event
more readable. The example below, shows how two macros can be defined that could
be used everywhere within your code, also with changing parameters.


``` markdown
### `output`
<!--
boolean: <script input="checkbox" value="true" output="@0" modify="false">
         @input
         </script>

and:     <script modify="false">@input(`@0`) && @input(`@1`) </script>
-->

@boolean(p), @boolean(q) --> @and(p,q)
```

@boolean(p), @boolean(q) --> @and(p,q)


> The parameter **`modify="false"`** removes the the gray backgound, so that
> scripts without any input become indistinguishable from the rest of the
> content. This gray backgound also indicates, that the code behind the script
> is **editable**. You can switch to the edit mode via a double-click on the
> script element. Thus you can inspect every script and also edit it, the code
> will only be executed after the textinput has lost the focus.

#### `default` & Execution-Graphs

If you connect scripts, this connection should actually form a directed graph,
without cycles. But of course, if you want to, can produce also cycles, that
stop only if the results do not change anymore.

``` html
<script input="range" value="1" default="1" output="x">
@input * @input(`y`)
</script>
<script input="number" value="1" default="1" output="y">
@input + @input(`x`)
</script>
```

The `default` parameter is used to define a the default output of this script.
Otherwise the initial calculation will result in an error, since the scripts do
require the outputs of the other script that can never be calculated, due to the
circular dependency.

<script input="range" value="1" default="1" output="x">
@input * @input(`y`)
</script>
<script input="number" value="1" default="1" output="y">
@input + @input(`x`)
</script>

### Further settings

`value`
=======

Set the default input value, if it is a number or a string or something else,
depends on the usage of the `@input` macro within the script.

---

`update-on-change`
==================

As mentioned earlier, every input-field has a specific update handling, `range`,
`number`, `text`, `radio`, `checkbox`, trigger the execution of the script on
every change, while the others are triggered only after the user hits enter or
if the input field loses the focus. However, by using the parameter
`update-on-change` you can change this behavior. It can be switched off or on by passing true or false, if you only pass `update-on-change` true is used as the default:

* `update-on-change`
* `update-on-change="true"`
* `update-on-change="false"`

---

`input-active`
==============

Inputs are only visible, if the user clicks on the script representation. If you
pass the parameter `input-active`, then the input will be visible on the first
appearance, but it will be closed if the element loses the focus again.

---

`input-always-active`
=====================

Using this parameter, it is possible to switch on the input-field for ever, it
will not be closed if the focus is lost.

---

`run-once`
==========

A script will be executed multiple times, if the site is rendered, or if it is
associated to a certain effect number. If the calculation should be executed
only once use this parameter. The result is preserved and displayed on every
appearance.

---

`modify`
========

By double-clicking onto a script, you get into edit-mode. The code is displayed
to the user and can be edited and it is executed again if the code-input field
loses the context. By setting `modify="false"` to false, this editing function
is switched of furthermore there is **no gray background** displayed.

This is a script: <script modify="false">12</script>



### Formatting with Intl

By using the `format` parameter you can set a specific kind of visual
formatting. This will be visible to the user, but if you connect different
script with input/output then the original result of an execution will be passed
to the subsequent scripts. The links below show contain all information to the associated formatting all params are directly passed to the formatting function.

Use `locale` to change the type of language/localization. If you do not pass
such a value, then the default document language setting is used as default.

> There is one difference by using the `style` parameter. `style` is used format
> the output with inline CSS. But some formattings also contain a `style`
> parameter. In order to don't mess up with styles you have to use `localeStyle`
> to set the locale language formatting style ;)

* `format="datetime"`:

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat/DateTimeFormat

* `format="number"`:

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat/NumberFormat

* `format="list"`

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/ListFormat/ListFormat

* `format="relativetime"`:

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/RelativeTimeFormat/RelativeTimeFormat

* `format="pluralrules"`:

  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/PluralRules/PluralRules



### Further Examples


#### Tables
<!--
sin: <script format="number"
             localeStyle="currency"
             currency="EUR"
             locale="de-DE"
             modify="false"
    > Math.sin(@input(`result`) + @input(`amp`) * @0) </script>
-->

``` markdown
#### Tables
<!--
sin: <script format="number"
             localeStyle="currency"
             currency="EUR"
             locale="de-DE"
             modify="false"
    > Math.sin(@input(`result`) + 0.5 * @0) </script>
-->

<script run-once
        default="0"
        output="result"
        input="range" value="2" min="0" max="25" step="0.1"
        >
@input
</script>


<script run-once
        default="0"
        output="amp"
        input="range" value="2" min="0" max="25" step="0.1"
        >
@input
</script>


<!-- data-type="barchart" id="tabelle" -->
| Header 1 | <script>@input(`result`)</script> |
|:-------- |--------: |
| 1        | @sin(1)  |
| 2        | @sin(2)  |
| ...      | ....     |
```

Pos: <script run-once
        default="0"
        output="result"
        input="range" value="2" min="0" max="25" step="0.1"
        >
@input
</script>
and amplitude:
<script run-once
        default="0"
        output="amp"
        input="range" value="1" min="0" max="2" step="0.1"
        >
@input
</script>


<!-- data-type="barchart" id="tabelle" -->
| Header 1 | <script>@input(`result`)</script> |
|:-------- |--------: |
| 1        | @sin(1)  |
| 2        | @sin(2)  |
| 3        | @sin(3)  |
| 4        | @sin(4)  |
| 5        | @sin(5)  |
| 6        | @sin(6)  |
| 7        | @sin(7)  |
| 8        | @sin(8)  |
| 9        | @sin(9)  |

#### Search

To change the current search subject
<script input="search" output="search" value=cats default="cats">"@input"</script>
to something else, simply click on the search and start to type...
If you click on the image below, a new random search will be triggerd.


<script input="button" run-once style="display: inline-block">
fetch('https://api.giphy.com/v1/gifs/random?api_key=XuS4MlQmIR6WQpMA8Zpxv4shNfJW8Aci&tag=' + encodeURI("@input(`search`)"))
  .then(response => response.json())
  .then(data => send.html(`<img height="350px" src="${data.data["image_url"]}">`))

"loading"
</script>

#### Diagrams

The first value defines some kind of range:
<script input="range" value="2" output="range">@input</script>
, while the second can be interpreted as range
<script input="range" value="50" output="amplitude">@input</script>.
You can double-click on any gray element to inspect and edit its javascript code.


<script run-once style="display: inline-block; width: 100%">
function func(x) {
    x /= 10;
    return Math.sin(x) * Math.cos(x * @input(`range`) + 1) * Math.sin(x * 3 + 2) * @input(`amplitude`);
}

function generateData() {
    let data = [];
    for (let i = -200; i <= 200; i += 0.1) {
        data.push([i, func(i)]);
    }
    return data;
}

let option = {
    animation: false,
    grid: {
        top: 40,
        left: 50,
        right: 40,
        bottom: 50
    },
    xAxis: {
        name: 'x',
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    yAxis: {
        name: 'y',
        min: -100,
        max: 100,
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    dataZoom: [{
        show: true,
        type: 'inside',
        filterMode: 'none',
        xAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }, {
        show: true,
        type: 'inside',
        filterMode: 'none',
        yAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }],
    series: [
        {
            type: 'line',
            showSymbol: false,
            clip: true,
            data: generateData()
        }
    ]
}

"HTML: <lia-chart option='" + JSON.stringify(option) + "'></lia-chart>"

</script>

#### Calculator
<!--
calc: <script run-once format="number" locale="en" notation="compact">@0</script>
-->


``` markdown
#### Calculator
<!--
calc: <script run-once format="number" locale="de" notation="compact">@0</script>
-->

Interim calculation @calc(22*12345.98726) or @calc(`Math.pow(3.141592, 12)`)...
```

Interim calculation @calc(22*12345.98726) or @calc(`Math.pow(3.141592, 12)`)...


## Future Work

* Better integration with github/gitlab and the versioning of courses
* Automagically analyzed surveys
* Integration of WebGl and a 3D navigation
* Better Inline function-plotter

## Contributors and Credit


{1}{<h2> <a href="https://github.com/andre-dietrich">André Dietrich</a> </h2>} <!-- class = "animated fadeInUpBig" -->

--{{1}}--
Programming paradigm experimenter and creator of LiaScript and SelectScript...



{2}{<h2> <a href="https://github.com/SebastianZug">Sebastian Zug</a> </h2>} <!-- class = "animated fadeInUpBig" -->

--{{2}}--
The mind in the dark and the man behind the eLab-project ...


{3}{<h2> <a href="https://github.com/kfessel">Karl Fessel</a> </h2>} <!-- class = "animated fadeInUpBig" -->

--{{3}}--
Embedded systems developer, creator or arduinoview, and Markdown evangelist ...


{4}{<h2> <a href="https://github.com/stvrhm">Steve Rehm</a> </h2>} <!-- class = "animated fadeInUpBig" -->

    --{{4}}--
CSS & SASS crack and friendly face behind new face of LiaScript ...


# Appendix

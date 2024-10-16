<!--
author:   André Dietrich

email:    LiaScript@web.de

version:  0.0.1

language: en

narrator: US English Female

comment:  A demo on Python and LiaScript.

icon:     https://pbs.twimg.com/profile_images/1388100423094087681/08Nvxq--_400x400.jpg

import:   https://github.com/LiaTemplates/Pyodide/blob/0.1.4/README.md
          https://github.com/LiaScript/CodeRunner/blob/master/README.md

@@ can also be replaced by @Pyodide.eval

@eval:  @LIA.eval(`["main.py"]`, `python -m compileall .`, `python main.pyc`)

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://github.com/LiaPlayground/PythonProgramming/blob/main/README.md)

# Python Programming


If you want to teach Python or at least run some Python snippets within your
course, we currently recommend two different packages for LiaScript.

1. [Pyodide](https://github.com/LiaTemplates/Pyodide)
2. [CodeRunner](https://github.com/liascript/coderunner)

What is the difference? Pyodide will load all libraries into your browser and
execute it locally, while CodeRunner will compile and execute the code on a
foreign server. The first project might cover only a reduced set of libraries,
but it scales and adds plotting functionality, in contrast to the second one.
In CodeRunner, plots can at the moment only be generated with R.

## 1. Pyodide


> To use this functionality, you will have to import:
>
> ``` html
> <!--
> ...
> import: https://github.com/LiaTemplates/Pyodide/blob/0.1.4/README.md
>
> -->
> ```
>
> Afterwards you can attach the macro `@Pyodide.eval` to every Python-Code
> snippet.
>
> **Note: All scripts are executed in one global environment**

### Examples

``` python
import sys

for i in range(5):
	print("Hello", 'World #', i)

sys.version
```
@Pyodide.eval


---

> Currently you can only plot one image, but this is shown within the terminal
> and also stored persitently. Thus, you can switch between different versions
> of your code and the resulting images will change too.

``` python
import numpy as np
import matplotlib.pyplot as plt

t = np.arange(0.0, 2.0, 0.01)
s = np.sin(2 * np.pi * t)

fig, ax = plt.subplots()
ax.plot(t, s)

ax.grid(True, linestyle='-.')
ax.tick_params(labelcolor='r', labelsize='medium', width=3)

plt.show()

plot(fig) # <- this is required to plot the fig also on the LiaScript canvas
```
@Pyodide.eval

> **NOTE:** You can resize the terminal and you can click onto the image to
> enlarge it. The additional loading of libraries is only required once, then
> they are stored locally...

## 2. LiaScript Code-Runner

> This allows, to run and execute your code on a real
>
> ```` markdown
> <!--
> ...
> import: https://github.com/LiaScript/CodeRunner/blob/master/README.md
>
> -->
>
> # ...
>
> ```python
> for i in range(10):
>   print "Hallo Welt", i
> ```
> @LIA.eval(`["main.py"]`, `python -m compileall .`, `python main.pyc`)
> ````
>
> Afterwards you can attach the macro `@LIA.eval` to every Python-Code
> snippet.
>
> The `@LIA.eval` macro might look a bit cryptic, but it actually consists
> of three steps.
>
> 1. A list of filenames, if you use require more than one files for your
>    project, then these have to be defined in order. A project can consist of
>    multiple code-snippets attached to each other
> 2. A compilation command
> 3. A execution command


### Example


```python
for i in range(10):
  print "Hallo Welt", i
```
@LIA.eval(`["main.py"]`, `python -m compileall .`, `python main.pyc`)


## Best Practice


If you you have a couple of code-snippets and you do not want to add always the
same complex macro, which might eventually change in the future. The best way is
to define a custom macro, which defines the macro with all parameters. You can
modify this in the future, just by changing the macro-definition an also the
import. It is thus not required to change every macro separately:

```` markdown
<!--
...

import:   https://github.com/LiaTemplates/Pyodide/blob/0.1.4/README.md
          https://github.com/LiaScript/CodeRunner/blob/master/README.md

@@ can also be replaced by @Pyodide.eval
@eval:  @LIA.eval(`["main.py"]`, `python -m compileall .`, `python main.pyc`)

-->

# ...

```python
for i in range(10):
  print "Hallo Welt", i
```
@eval


```python
for i in range(10):
  print "Hello World", i
```
@eval
````


---


```python
for i in range(10):
  print "Hallo Welt", i
```
@eval


```python
for i in range(10):
  print "Hello World", i
```
@eval

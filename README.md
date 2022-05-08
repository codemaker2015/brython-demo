# Brython demo

<img src="demo.gif" width="" height="" />


## [Brython](https://github.com/brython-dev/brython/)

Brython (Browser Python) is an implementation of Python 3 running in the
browser, with an interface to the DOM elements and events.

Here is a simple example of an HTML page running Python:

```html
<html>

    <head>
        <script type="text/javascript" src="/path/to/brython.js"></script>
    </head>

    <body onload="brython()">

        <script type="text/python">
        from browser import document, alert

        def echo(event):
            alert(document["zone"].value)

        document["mybutton"].bind("click", echo)
        </script>

        <input id="zone"><button id="mybutton">click !</button>

    </body>

</html>
```

To use Brython, all there is to do is:

1. Load the script [brython.js](http://brython.info/src/brython.js "Brython from the site brython.info").
2. Run the function `brython()` on page load, like `<body onload="brython()">`.
3. Write Python code inside tags `<script type="text/python">`.


Main features
=============
Brython supports the syntax of [Python 3](https://www.python.org "Python Homepage"),
including comprehensions, generators, metaclasses, imports, etc.
and many modules of the CPython distribution.

Since version 3.8.0, Brython implements the Python version of the same major /
minor version number.

It includes libraries to interact with DOM elements and events,
and with existing Javascript libraries such as jQuery, D3, Highcharts, Raphael etc.
It supports the latest specs of HTML5/CSS3, and can use CSS Frameworks like
Bootstrap3, LESS, SASS etc.


Getting started
===============
Zero install !
--------------
The most simple way to get started, without anything to install, is to use the
distribution available online through [jsDelivr](https://www.jsdelivr.com/).
You can choose the latest stable release :

```html
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3.10.5/brython.min.js">
</script>
```

The previous code will allow you to use raw python code, but if you import
modules from the standard library you have to load a single javascript file
with the [available stdlib](https://github.com/brython-dev/brython/tree/master/www/src/Lib):

```html
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3.10.5/brython_stdlib.js">
</script>
```

jsDelivr supports version ranges, so if you want the latest of the
3.10.x versions:

```html
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3.10/brython.min.js">
</script>
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3.10/brython_stdlib.js">
</script>
```

or the latest of the 3.x.y versions:

```html
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3/brython.min.js">
</script>
<script type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/brython@3/brython_stdlib.js">
</script>
```

If you want to use the latest development version, you can load these scripts
instead:
```html
<script src="https://raw.githack.com/brython-dev/brython/master/www/src/brython.js"></script>
<script src="https://raw.githack.com/brython-dev/brython/master/www/src/brython_stdlib.js"></script>
```

Test Brython online
===================
If you want to test Brython online you can visit the following:

- [Editor](http://brython.info/tests/editor.html "Online Brython Editor")
- [Console](http://brython.info/tests/console.html "Online Brython Console")


Documentation
=============
You can start by reading the official [Brython tutorial](https://brython.info/static_tutorial/en/index.html).

Full documentation is available on the [official site](http://www.brython.info "Brython Homepage").
You can read the docs in [English](http://brython.info/static_doc/en/intro.html),
[French](http://brython.info/static_doc/fr/intro.html) and
[Spanish](http://brython.info/static_doc/es/intro.html).

The most updated docs usually are the English and French versions so if you
want to be up-to-date, please, use these versions.

Curious about [how Brython works](https://github.com/brython-dev/brython/wiki/How%20Brython%20works) ?

A [tutorial](https://github.com/brython-dev/brython/wiki/Writing-an-Android-application)
explains how to build Android applications with Brython.
pycodestyle (formerly called pep8) - Python style guide checker
===============================================================

pycodestyle is a tool to check your Python code against some of the style
conventions in [PEP 8](http://www.python.org/dev/peps/pep-0008/).

Note: This package used to be called ``pep8`` but was renamed to ``pycodestyle`` to reduce confusion. Further discussion [here](https://github.com/PyCQA/pycodestyle/issues/466).

Features
--------

* Plugin architecture: Adding new checks is easy.

* Parseable output: Jump to error location in your editor.

* Small: Just one Python file, requires only stdlib. You can use just
  the ``pycodestyle.py`` file for this purpose.

* Comes with a comprehensive test suite.

Installation
------------

You can install ``pycodestyle.py`` with ``pip``:

    $ pip install pycodestyle


Example usage and output
------------------------

    $ pycodestyle --first optparse.py
    optparse.py:69:11: E401 multiple imports on one line
    optparse.py:77:1: E302 expected 2 blank lines, found 1
    optparse.py:88:5: E301 expected 1 blank line, found 0
    optparse.py:222:34: W602 deprecated form of raising exception
    optparse.py:347:31: E211 whitespace before '('
    optparse.py:357:17: E201 whitespace after '{'
    optparse.py:472:29: E221 multiple spaces before operator
    optparse.py:544:21: W601 .has_key() is deprecated, use 'in'

You can also make ``pycodestyle.py`` show the source code for each error, and
even the relevant text from PEP 8:

    $ pycodestyle --show-source --show-pep8 testsuite/E40.py
    testsuite/E40.py:2:10: E401 multiple imports on one line
    import os, sys
             ^
        Place imports on separate lines.

        Okay: import os\nimport sys
        E401: import sys, os


Or you can display how often each error was found::

    $ pycodestyle --statistics -qq Python-2.5/Lib
    232     E201 whitespace after '['
    599     E202 whitespace before ')'
    631     E203 whitespace before ','
    842     E211 whitespace before '('
    2531    E221 multiple spaces before operator
    4473    E301 expected 1 blank line, found 0
    4006    E302 expected 2 blank lines, found 1
    165     E303 too many blank lines (4)
    325     E401 multiple imports on one line
    3615    E501 line too long (82 characters)
    612     W601 .has_key() is deprecated, use 'in'
    1188    W602 deprecated form of raising exception

Links
-----

[![Build Status](https://img.shields.io/travis/PyCQA/pycodestyle.svg)](https://travis-ci.org/PyCQA/pycodestyle) [![Wheel Status](https://img.shields.io/pypi/wheel/pycodestyle.svg)](https://pypi.python.org/pypi/pycodestyle)

* Read the documentation: https://pycodestyle.readthedocs.io/

* Fork me on GitHub: http://github.com/PyCQA/pycodestyle

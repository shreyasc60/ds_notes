
## Python 3 vs Python 2

Python 3 is much newer, and Python 2 reached "end if life" on January 1, 2020. So, unless you're working on a code which was written a long ago in the past, you're gonna use the latest Python 3. Python is actually a specification of language that can be implemented in many ways.
## Implementations of Python

When people speak of _Python_ they often mean not just the language but also the CPython implementation.

There are various implementations of python:
1. CPython
2. PyPy
3. Jyton
4. IronPython
5. PythonNet

#### CPython[](https://docs.python-guide.org/starting/which-python/#cpython "Permalink to this headline")

[CPython](http://www.python.org) is the reference implementation of Python, written in C. It compiles Python code to intermediate bytecode which is then interpreted by a virtual machine. CPython provides the highest level of compatibility with Python packages and C extension modules.

Python is a Dynamically typed language, meaning that the data types of the variable are assigned on runtime, and are based off the type of data the variable hold. Data types of variables don't have to be explicitly mentioned while initialization.

## Modules

You can import modules using the ```import ``` or ```from ... import``` statement.

As soon as you use import statements, you use modules. These can be either built-in modules such as *os* and *sys*, third-party modules you have installed in your environment, or your project’s internal modules.

Built-in modules:
1. os
2. sys


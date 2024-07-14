# Python In Depth

7/14/2024: Up Skill: Learn Python in-depth

What is a programming language: a way to instruct computers; w/o code, computers couldn't do anything.

Computers speak in binary: on or off 1, 0.

_Insert Compiler, Interpreter Photo_

To get from JS, PY, and JAR to 0s and 1s, you need another one of the two following programs:
    1. Interpreter - goes line by line through our code and executes it (python usually uses an interpreter)
    2. Complier - Takes code  all at once, reads the entire file all at once, and then translates it to machine code

These programs act as translators in the human world.

Understanding Python in Depth

When you go and download Python, you are downloading CPython. You are downloading an interpreter that follows the Python specification. It is a machine built by a developer.

When most people talk about Python, they mean CPython.

What are you downloading when you "download Python?"
    1. Downloading a machine that takes our py code
    2. It goes through our interpreter, which we download using CPython
    3. CPython is going to create something called a byte code
    4. This byte code gets run on the CPython VM
    5. The CPython VM runs on our computers, phones, laptops

When you dl python from python.org, you dl the interpreter and the python vm

_Insert byte code image_

Create a perfessional Python setup

Terminal
    1. iTerm2
Code Editors
    1. Vim
    2. Sublime Text
    3. VS Code
IDEs
    1. PyCham
    2. Spyder
Notebooks
    1. Jupyter Notebook

Before we set up this whole py env, set up repl.it account

The account is set up and authenticated through GH; the profile is added to GH links for future reference and bookmarking.

 Python2 vs Python3

 Python was written by Guido van Rossum in 1991 and the Python was updated to version 3 (Python3) in 2008.

 Python is constantly updated, just like an app on someone's phone or the iPhone OS (iOs)

Named after Monty Python the British Comedy Group

Python3 introduced 'Breaking Changes' when devs updated to Python3, and all your python2 code didn't work.

Create Comments in Python3 using the hash key '#'

Now all python2 is considered legacy. Meaning in 2020, it won't be maintained any longer.

## Sunday, July 14th, 2024 - Building In-depth Python Knowledge (Day 10)

Why are there so many programming languages? Depending on the use case, specific languages are better than others. A language is a tool and there are different tools for different jobs.

It's all about trade offs. What are you trying to solve and which is the best tool (language) is best at solving that problem?


### My current understanding of Python: Code is written in Python, it's passed to the interpreter that's provided for you, this interpreter take the py code and converts it into bytecode, it's then run in the CPython VM, then the code is run as binary (1s & 0s baby).

## Photo Needed: Insert Photo of the process above

**First Python Program**
``` 
name = input ("What is your name? ")
    print('Hello, ' + name + ', how are you?')

```

###









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

### Photo Needed: Insert Photo of the process above

**First Python Program**
``` 
name = input ("What is your name? ")
    print('Hello, ' + name + ', how are you?')

```

## Python Basics

To Learning a new language you must know the following:

**Understand the Vocabulary (Terms)**

**Understand the Datatype**
    1. What sort of data can a program hold (thin of values)

**Understand the Actions**
    1. At the end of the day, all programming does tell our machines, "Hey, store this data then retreive this data and performing some actions on it."

**Understand the Best Practives**

###  Fundamental Data Types
    1. int = intergeres
    2. float
    3. bool
    4. str
    5. list
    6. tuple
    7. tuple
    8. tuple
    9. set
    10. dict 

A Program is simply a set of instructions that tell a computer what to do

All about storing information (or a datatype) and modifying that information (datatype)

**Two Crucial Steps to Learn in Programming:**
    1. Understand the data types
    2. Understand how to perform actions on  the data tpes (remove, store, change) 

### Classes -> custom types

### Specialized Data Types

Think of these as extensions you can add.

### None

Means nothing. Like Zero in Math.

**Understanding  int, float.**

    1. int: Interger
    2. float: floating point number

### End Notes
This was a short day, the goal here is to stay consistent and nver miss a day. If you keep coming back daily, this will get easier. Keeping my daily streak alive for the 10th day now. :)

Day 11 - Monday, July 15, 2024
______

## Python Basics

### Numbers
     1. int = intergeres
     2. float
This video explains floating point numbers well. https://www.youtube.com/watch?v=PZRI1IfStY0&ab_channel=Computerphile

**A float is larger in memory than an interger. Because floating point numbers recur.**

Humans read numbers like this:
Base 10: 10 Digits
```100 10 1 . 10ths 100ths 1000ths
1/10 in decimals = 0.1
```
Machines read numbers like this:
Base 2: 2 Digits

4 2 1 . 1/2 1/4 1/8 1/16

0.1 in binary = 0.00011 and that recurs to infinity

Computers don't understand recurring numbers.

1/3 + 2/3 [27;6;85~] 3/10


This video explains floating point numbers well. https://www.youtube.com/watch?v=PZRI1IfStY0&ab_channel=Computerphile

### Math Functions

### DEVELOPER FUNDEMENTALS I

### Operator Precedence

### Replit Code

### Execsuse: Operator Precedence

### Operational: bin() and complex

### Endorsements on LinkedIn

### Variables

### Expressions vs Statements

### Augmented

### Strings

### String Concatenation

### Type Conversion

### Escape Sequences

### Formatted Strings

### String Indexes

### Immutability

### Built-in Functions + Methods

### Booleans

### Exercise: Type Conversion

### DEVELOPER FUNDEMENTALS II

### Exercise: Password Checker

### Lists

### Lists Slicing

### Matrix

### List Methods

### List Methods 2

### List Methods 3

### Common List Patterns

### List Unpacking

### None

### Dictionaries

### 3.7 Updates: Ordered Dict

### DEVELOPER FUNDEMENTALS III

### Dictionary Methods

### Tuples

### Tuples 2

### Sets

### Sets 2

### < > Unlimited Updates

#### \* Add Asterisk without activating it
**Splat combines zero or more positional arguments into a tuple, while splatty-splat combines zero or more keyword arguments into a dictionary.**
```python
def add(*a):
    return sum(a)

add(1, 2, 3) # 6
```

##### Create 
```python
def f(*args):                  # f(1, 2, 3)
def f(x, *args):               # f(1, 2, 3)
def f(*args, z):               # f(1, 2, z=3)
def f(x, *args, z):            # f(1, 2, z=3)

def f(**kwargs):               # f(x=1, y=2, z=3)
def f(x, **kwargs):            # f(x=1, y=2, z=3) | f(1, y=2, z=3)

def f(*args, **kwargs):        # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3) | f(1, 2, 3)
def f(x, *args, **kwargs):     # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3) | f(1, 2, 3)
def f(*args, y, **kwargs):     # f(x=1, y=2, z=3) | f(1, y=2, z=3)
def f(x, *args, z, **kwargs):  # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3)
```





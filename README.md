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

```
100 10 1 . 10ths 100ths 1000ths
1/10 in decimals = 0.1

```

Machines read numbers like this:
Base 2: 2 Digits

4 2 1 . 1/2 1/4 1/8 1/16

0.1 in binary = 0.00011 and that recurs to infinity

Computers don't understand recurring numbers.

1/3 + 2/3 [27;6;85~] 3/10

This video explains floating point numbers well. https://www.youtube.com/watch?v=PZRI1IfStY0&ab_channel=Computerphile

``` Python 
# Fundmental Data Types
# in and float
print(type(6))
print(type(2-4))
print(type(2 * 4))
print(type(2 / 4))

# Printing Operator Names
# Example usage

# 1st Define function
def get_operator_name(operator):
    operator_names = {
        # define operator names
        '+': 'Addition',
        '-': 'Subtraction',
        '*': 'Multiplication',
        '/': 'Division',
        '//': 'Floor Division',
        '%': 'Modulus',
        '**': 'Exponentiation',
        '-u': 'Unary Negation'  # Representing unary negation
    }
    return operator_names.get(operator, 'Unknown Operator')
    # Examples
    print(get_operator_name('+'))   # Output: Addition
    print(get_operator_name('**'))  # Output: Exponentiation
    print(get_operator_name('=='))  # Output: Equality
    print(get_operator_name('//'))  # Output: Floor Division
    print(get_operator_name('@'))   # Output: Unknown operator



```
## The Feynman Technique & How it will make you a better Developer

### It Boild down to a four step process
    1. Pick something you want to learn
    2. Write and Explain the concept as simply as possible
    3. Identify Shortcomings and Points of Improvement
    4. Review and Simplify (further if needed)

### Example of Applying the Feynman Technique
    1. Understand the React state
    2. In React, state refers to the data that determines how a component is rendered and behaves. It's a plain JavaScript Object that contains info about the components current state, such as user input or changes in data from a database. When the state changes, React will re-render the component to reflect the updated state. 
        a. Further simplification: "Have you ever played with a toy that you can change like a puzzle or a building set? React State is kind of like that. When we build a website with React, we use different building blocks called components. Each component can have its own box called state, where it keeps important information. For example, if you're filling out a form on a website, the state might hold the things you type in. When you change something in the state, React will automatically update what you see on the screen to show the new information. Just like how you can change a puzzle or a building set to make it look different"
    3. After writing this explaination, the author realizes he didn't explain how to update the state and the annlogy could be better. This is a vital point that was not conveyed well.
        a. This could either be a lack of knowledge or the fact he just forgot to include it. It's important to pinpoint gaps that must be closed in your explaination.
        b. Third attempt at simplification: "Have you ever built a sand castle or a tower with blocks? In React, we use building blocks called components to build a website. Each component can have its own special box called state, where it keeps important info. For example, if you're playing a game on a website, the state might hold your score when you do something that changes the state, like scoring a point in a game, we use a unique tool called setState() to update the state. When the state changes Reactt will automatically update what you see on the screen to show the new info. Just like how you can add more blocks to a tower to make it taller"

The beauty of this method is that it doesn't need to be perfect your first go around. You refine it constantly until it it's easier to grasp for you and your audiance.

### Four Takeaways: 
    1. Simplify, Simplify, Simplify (The goal is for a 10 year old to understand it.)
    2. Use clear and simple language -> using complex language to cover up knowledge gaps and insecurities is the easies to know you don't fully understand the concept.
    3. Test Your Understanding by asking yourself these questions: 
        a. Do I understand the underlying principles and assumptions of the concept?
        b. Can I provide examples that illustrate how the concept works
        c. Can I identify the limitations of the concepts?
    4. Iterate and repeat
        a. Researcher shows that you lose 50% of information you learnred 1 hour after it repeats and up to 70% in 24 hours
        b. So you have to work to perfect this practice; by no means it a one and done.

# Day 12 -> Making Better Notes

### Math Functions

```Python

    # Fundemental data types
    # int and float

    # Get data type
       print(type(6))       # Int
       print(type(2 / 4))   # Float
       print((10.56))       # Float -> Float store the numbers in front and behind the decimal in two different places and it requires more memory
    # Math operations
        print(2 -  4)   # Subtraction
        print(2 *  4)   # Multiplication
        print(2 /  4)   # Float
        print(2 ** 2)   # Exponent:  2 to the power of 2 = 4
        print(2 // 4)   # Floor Division: devides left operand by right operand, rounding down to the nearest interger. Example a // b
        print(6 %  4)   # Modulus: Returns the remainder of the division of the left operand by the right operand

        print(get_operator_name('%'))
  ```
```Python

    # Math Functions
    print(round(3.9))   # Built-in Rounding Function
    print(abs(-20))     # Absolute Value

    # Now that you know about math functions, you can use ChatGPT to discover more built-in Python 3 functions

```


### DEVELOPER FUNDEMENTALS I

```Python

# Don't read the dictionary. 
# Figure things out on the fly.
# Use ChatGPT (Google) to figure out which tools you are best for solving the specific problem.

```

### Operator Precedence

```Python

# PEMDAS: P:Parentheses, E:Exponents (including roots, such as square roots, M:Multiplication, D: Division, A: Addition, S:Subtraction 

# ()
# **
# * /
# + _

```

### Replit Code

```Python

# GitGub code repo for the next exervises: https://github.com/aneagoie/ztm-python-course-exercises
# Operator Presidence Replit: https://replit.com/@aneagoie/Operator-Precedence#main.py
# # GitHub ZTM Python Course Exervises: https://replit.com/@aneagoie/Operator-Precedence#main.py

```

### Execsuse: Operator Precedence

```Python

    # Remember PEMDAS and you will be good

```

### Operational: bin() and complex


### Variables

```Python

    # variables store values and can be changed
    # be a good dev and name your vars so another dev can understand and follow your code

```
    # variables store values and can be changed
### Expressions vs Statements

```Python 

    # an expression is something that returns a value
    # for example
        iq = 100 
        user_age = iq / 5 
    
    # the statement is an entire line of code that performs an action
        user_age = iq / 5
        
    # the expression
        iq / 5 # because it returns a value

```

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

## Sets 2

## < > Unlimited Updates

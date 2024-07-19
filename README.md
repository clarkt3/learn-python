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

##  Day 12 -> Jul 16 2024

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

```Python

    # complex isn't going to be used 99.9% of the time
    # bin() stands for binary
        bin() # returns the binary representation of an interger
        print(bin(5)) # returns 0b101, which just means binary 

    # print a binary number as an interger
        print(int('0b101' + 2)) # returns 0b101 and 5 because it's converting 0b101, which is a base 2 number back to base 10 (human readable)
    # base 2 numbers must be written in as an str to convert to base 10

```

### Variables

```Python

    # variables store values and can be changed
    # variables store values and can be changed
    # be a good dev and name your vars so another dev can understand and follow your code

```
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

### Augmented Assignment Operator

```Python 

    some_value =  5

    some_value *= 5
    some_value += 5
    some value -= 5

```


```Python

    # augmented assignment operator
    some_value = 5
    some_value = some_value * 2

    print(some_value)

    # subtract some_value with augmented operator
    some_value -= 2

    # add some_value with augmented operator
    some_value += 2

    # multiple some_value with augmented operator
    some_value *= 2

    # remember: the operator comes to the left of the equals sign
    '-+'
    '-+'
    '*+'

```


## Day 13 -> Wed  Jul 17  2024

### Strings (str)

```Python 

    # single-line strings
        print(type"hi hello there 24!")) # output -> str
        username = 'supercoder'
        password = 'supersecret'

    # multi-line string
        long_string = '''

        WOW
        0 0
        ____

   '''

    # print two strings together
        first_name = 'Tom'
        last_name = 'Clark'
        full_name = first_name + last_name

        print(full_name)

        # add space between first and last name
        first_name = 'Tom'
        last_name = 'Clark'
        full_name = first_name + ' ' + last_name

        print(full_name)


```

### String Concatenation

```Python

    # simply add two string together with the + operator
        print('Hello' + ' Tom')

    # str  concatenation only works with strings
        print('hello' + 5) # this returns an error
```

### Type Conversion

```Python

    # conversion expression
        print(type(int(str(100))))

    # convserion broken into steps
        a = str(100)
        b = int(a)
        c = type(b)
        print(c)

    # this is type conversion

```

### Escape Sequences

```Python

    # excape sequence ->  double and single quotation marks
        weather = "It\'s "kind of"  sunny" # returns error; escape sequence required

    # escape sequence -> add tab
        weather = "\t It\'s \"kind of\" sunny" # letting python know whatever comes after \ is a str

        print(weather)

    # escape sequence -> add tabshow a backslash as a str after you enter an  escape sequence \
        "\\" # the first backslash is the escape sequence, the second backslash is returned as a str
        weather =  "\t It\'s \"kind of\" sunny\\hazy" # syntax highlighting will help identify if you are missing an escape sequence

    # escape sequence -> add new line
        weather = "\t It's \"kind of\" sunny \n hope you have a good day"

```

### Formatted Strings

```Python

    # f str is cleaner but only available in Python3
        name = 'Johnny'
        age = 55

    # print cleaner with f str

        print(f'hi {name}. You are {age} years old')

    # the python2 version
        pring('hi {0}. You are {1} year old'.format(name, age)) # this version is not as thought through

```
## Day 14 - 2023-7-18

### String Indexes

```Python

    # high-level ideas points from the lesson
        # 1. in python, chars and spaces are stored within a corresponding vlue (0,1, 2, 3, 4, etc.) 
        # 2. access different parts of a string by their indexes
        # 3. [start:stop:stepover]

    # code samples from the lesson - write by hand for muscle memory, clean code, attention to detail
        selfish = '01234567'
                # 01234567

                # [start:stop:stepover] 
                print(selfish[1:]) # starts at 1 and goes to the end with no stop value entered

                # no start value
                print(selfish[:5])

                # [start:stop:stepover] w/o start, stop value
                print(selfish[::1])

                # [start:stop:stepover] w/ negative numbers
                print(selfish[-1]) # starts from the end, prints the last value within the str

                # [start:stop:stepover] - step over from the back to get the reverse order
                print(selfish)[::-1] # prints 76543210 which is the above str in reverse 

```
### Immutability

```Python

# storing this amazing find/replace command here for future reference!!! 
    # replace w/o prompting -> :%s/oldword/newword/g
    # replace w/  prompting -> :%s/oldword/newword/gc

# high-level ideas from the lesson
  # key point: str values assigned to a var cannot be changed
  # key point: if you assign a new value it redefines the var 
  # key point: every time you rename the var, the previous value is lost

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail
    selfish = '01234567'
            #  01234567
    selfish = selfish + '8' # adds 8 to the end of the original value of 01234567 so it's now 012345678

    print(selfish)
```

### Built-in Functions + Methods

```Python

    # high-level ideas points from the lesson
        # key point: you must know built-in functions & method exist 
        # key point: you must NOT memorize built-in functions & methods
        # key point: know where you have tools at your disposal and learn to understand and use the docs

    # code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail
        # print to versions of a value; since strs are immutable, you must define another var to print second value
         quote  = 'to be or not to be'
         quote2 = quote.replace('be', 'me')

         print(quote2)

         print(quote)

    # find method
        quote = 'to be or not to be'
        print(quote.find('be')) # prints index value of the first instance of 'be' begins

    # change to uppercase
        quote = 'to be or not to be'
        quote.upper() # prints all caps version of the str

    # capitalize()
        quote = 'to be or not to be'
        print(quote.capitalize) # prints quote in all caps

    # replace - replace w/e is pass to the braces
        quote = 'to be or not to be'
        print(quote.replace('be', 'me')) # this prints a new value but this is not 

```
#### Closing Notes

```python 
    # formatting notes ahead of time worked well for me today
    # watching to lessons once w/o taking notes  
    # start your day applying to become a Technical Support Engineer at a company that focuses on AI, ML

```

## Day 15 - 2024-07-19

### Booleans

```Python

# high-level ideas points from the lesson
  # key point: true or false 
  # key point: bool is the snytax 
  # key point: false = 0 and true = 1 is all it is 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

        # booleans
        name = 'Thomas'
        is_cool = False

        is_cool = True

        print(bool('True')) # true = 1 false = 0; all there is too it

```

### Exercise: Type Conversion

```Python

        # built-in method definition: a method that is bound to an object, and it operates on that object
        my_string = "hello, World!"
        lowercase_string = my_string.lower()
        print(lowercase_string)

        # engineer a program that guessses a users age based on the birth yeaer input

        # import datetime function
        from datetime import datetime


        # store birthdate input in var user_age
        user_age = input("Please enter your birthdate (YYYY-MM-DD): ")

        # convert user age  str to a datetime obj
        birth_date = datetime.strptime(user_age, '%Y-%m-%d')

        # get current date
        current_date = datetime.now()

        # calculate the age
        age = current_date.year - birth_date.year - ((current_date.month, current_date.day) < (birth_date.month, birth_date.day))

        # use f to format string with expression inside
        print(f"The user is {age} years old.")

        # this is how it was solved in the lesson plan. I used google and chatGPT to help me answer mine
        # Andre also stores input into a variable
        birth_year = input('What year were you born?')

        age = 2024 - int(birth_year)

        print(f'your age is: {age}')

         # 3-line solution
         birth_year = input('What year were you born?: ')

         # subtract birth year from current year
         age = 2024 - int(birth_year)

         # pint birth year with f-str to add expression inside
         print(f'your age is: {age}')


```

### DEVELOPER FUNDEMENTALS II

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Exercise: Password Checker

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Lists

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Lists Slicing

```Python

# high-level ideas points from the lesson
  # key point:
  # key point:
  # key point:

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail


```

### Matrix

```Python

# high-level ideas points from the lesson
  # key point:
  # key point:
  # key point:

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### List Methods

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### List Methods 2

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### List Methods 3

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Common List Patterns


```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### List Unpacking

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### None

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Dictionaries

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### 3.7 Updates: Ordered Dict


```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### DEVELOPER FUNDEMENTALS III

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Dictionary Methods

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Tuples

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Tuples 2

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

### Sets

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

## Sets 2

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```

## < > Unlimited Updates

```Python

# high-level ideas points from the lesson
  # key point: 
  # key point:
  # key point: 

# code samples: hand written to improve muscle memory, develop clean code, and improve attention to detail

```



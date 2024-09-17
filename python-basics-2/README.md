### Day 21 of 100 | 2024-07-25
#### Breaking The Flow

```Python

# key point: use machines to do repetitive tasks really fast; know how to break up your code

```

 #### Conditional Logic

 ```Python

    # gist: python programs are just boolean aggregrations with if, elif, and else statements

    # syntax:
    Conditional Keywords:
    if (evaluate something for true or false)
    elif (evaluate something else for true or false)
    else (when all evaluates to false, run else)

    # code:
    is_old = False
    is_licensed = True

    if is_old:
        print('you are old enough to drive!')
    elif is_licensed:
        print('you can drive now!') # output: b/c is_licensed = true
    else:
        print('you are not of age!')

    # code (long-form)
    is_old = False
    is_licensed = False

    if is_old:
        print('you are old enough to drive!')
    elif is_licensed:
        print('you can drive now!')
    else:
        print('you are not of age!') # output: b/c is_old, is_licensed =  False

    # code (short-form)
    if is_old and is_licensed :
        print('you are old enough to drive!')
    else: print('you are not of age!')

    # instructor note:
        elif    # most statements have 1 if and 1 else; elif helps evaluate multiple conditions

        elif: condition     # evaluates another condition after if
        elif: condition     # evaluates another condition after if and elif
 ```

 #### Indentation In Python

```Python

    # gist: spaces help the interpreter break code into blocks

    # syntax:
    keep it clean
    4 spaces or 1 tab is interperted the same
    if:
        print('hi')
    else:
        print('bye')

    # code:
    is_old = True
    is_licensed = True

    if is_old and is_licensed:
        print('you are old enough to drive, and you have a license!')   # output: True
    else:
        print('you are not of age!')

        print('alright, alright, alright')

    is_old = True
    is_licensed = False

    if is_old and is_licensed:
        print('you are old enough to drive, and you have a license')    # output: not printed

    else:
        print('you are not of age!')    # output: 'you are not of age' b/c is_licensed = False

        print('Alright - come back when you\'re old enough')    # output: b/c else is run

```

#### Truthy vs Falsey

 ```Python

 # gist: Python3 has dictated what values are truthy and what and what values are falsey 

 # list of falsy:
    # None
    # False
    # 0
    # 0.0
    # 0j
    # Decimal(0)
    # Fraction(0,1)
    # [] - empty list
    # {} - empty dict
    # () - empty tuple
    # '' - empty str
    # b''- empty bytes
    # set() - empty set
    # an empty range, like range(0)
    # objects for which
        # obj.__bool__() returns False
        # obj.__len__()  returns 0

 # all other items are truthy.

 # code:
    password = '1,2,3'
    username = 'Tommy'

    # Truthy and Falsy
    if password and username:    # password & username = Truthy b/c they exist'
        print('Welcome - you have logged in successfully!')
    else:
        print('Please provide your username and password.')

 ```
#### Short Circuiting

```Python

    # gist: the keyword or is more performant than and b/c it short circuits the if statment 

    # syntax:
    if var_name or var_name2    # evaluates 1st var for Truthy, runs the remainder of the code

    # code:
    is_Friend = True
    is_User = True

    if is_Friend or is_User
        Print('Best friends Forever')   # output: b/c is_Friend = Truthy; remainder isn't run

    # or is more performant than and b/c if first question = truthy remainder doesn't  execute

    # and works the same way if one value is Fals(y) remainder of code isn't executed

```
### Day 22 of 100 | 2024-07-26

#### Logical Operators

```Python

    # gist: understand operand values, how  operators wrok and how to looks them up if needed

    # syntax:
    ==   # equal to w/o reassigning value
    !=   # not equal to
    >    # greater than
    <    # less than
    >=   # greater than or equal to
    <=   # less than or equalt to

    and  # must meet both conditions on either side of the if elif statement
    or   # only needs to meet one of the if statement qualifiers
    not  # the opposite of what ever value is w/i the statement

    # code:
    print(4 > 5)        # False b/c 4 is less than 5
    print(4 < 5)        # True b/x 4 is less than 5
    print(4 == 5)       # False, b/c 4 and 5 are NOT equal
    print('a' > 'b')    # False b/c python assigns numerical values to all letters

    print('a' > 'A')    # Ture, b/c python3 assigns numerical value to all letters

    print(1 < 2 <3)     # True, b/c it's all true
    print(1 < 2 > 3 < 4)# False, b/c 2 is NOT greater than 3; program short curcuits - done
    print(1 <= 2)       # False b/c 1 is less than 2 but NOT equal; only one need to be true

    print(0 != 0)       # False b/c 0 IS = 0

    print( 0 != 1)      # True because 0 is NOT equal to 1

    print(not(True))    # output: False: not prints the oposite of the value in paraenthesis
```

#### Exercise: Logical Operators

```Python

    """ gist: conditional logic can be correctly written
    in more ways than one. They idead is to make it easy
    to understand for yourself and other programmers: when
    they look at your code in a collaborative env"""

    # exercise solution below

    is_magician = True
    is_expert = False

    # check if magician and expert: 'you are the master magician'
    if is_magician and is_expert: 
        print('you are the master magician')
    # check if magician but not expert: 'at least you're getting there'
    elif is_magician:  # more easily readable: is_magician and not is_expert
        print("at least you're getting there")
    # if you're not a magician: 'you need magical powers'
    else: # readability: else not is_magician
        print('you need magical powers')

```

#### is vs ==

```Python

    # == checks only the values not for the exact match
    # is checks for the exact thing you're looking for
    # when comparing lists, tupples, dicts w/ is they will never be the same
    # output of print([1,2,3] is [1,2,3]) is False because they are in different 
        # spot in memory and a therefor not the same

    # syntax:
        # ==
    print(True == 1)    # output: True
    print('' == 1)      # output: False
    print([] == 1)      # output: False
    print(10 == 10.0)   # output: True
    print([] == [])     # output: True

        # is
    print(True is 1)    # output: False
    print('' is 1)      # output: False
    print([] is 1)      # output: False
    print(10 is 10.0)   # output: False
    print([] is [])     # output: False b/c lists are always stored in a different part of memory regardless

    # is auto save working??
    # Testing auto save in vim

    # turned on auto save in Vim - YAY!!!
```
### Day 22 of 100 | 2024-07-27

#### For Loops

```Python

    # gist: machines do repetative things faster than humans
        # machines do them millions of times ttoo

    # syntax:
    for item in 'Tom Clark':     # item has no intrinsic value; can be called anyhting
    for i in 'Tom Clark':        # i is used in most programs
    for i in 'Tom Clark':        # 'tom clark' is the iterable - it gets looped over
        print(i

        )
    # use case(s):
    for i in [1,2,3,4,5,6,7,8,9,10]:
        print(i)

    # works with tupple, and sets -- dicts will be discussed later

    # nested loops
    for i in [1,2,3,4,5]:
        for x in ['a', 'b', 'c']:
        print(item x)

```

#### Iterables

```Python

    # gist: a collection of items: list, dict, set, tuple, string
        # because they can be iterated -> go one-by-one to check
        # each item in the collection
    # add iterating (looping) over something when you're speaking
        # to other programmers
    # iterable is the noun, iterate is the verbe

    # syntax -> dict
    user = {
    'name': 'Chaz'
    'age': 45
    'can_skate': True
    }
    for i in user:
        print(i)        # output: key w/o value

    for i in user.items():
        print(i)        # output: key/value pair in tuple

    for i in user.values():
        print(i)
    for i in user.keys():
        print(i)        # output: only keys

    # unpacking the tuple
    for i in user.items():
        key, value = i
        print(i)

    # short-hand v. of unpacking a tuple
    for key, value in user.items():     # even shorter k, v (for key and value)
        print(key, value)

    # ***integers cannot be iterated over***

 ```

#### Exercise: Tricky Counter

```Python

    # code:
    # counting my solution

    my_list = [1,2,3,4,5,6,7,8,9,10]
    # iterate over this loop and sum up the total
    for i in my_list:
    print(i)

print(sum(my_list))     # all number iterations and 55 as the sum

# instructor feedback

my_list = [1,2,3,4,5,6,7,8,9,10]

# you didn't set a counter variable in your solution
counter = 0
for i in my_list:
  counter = counter + i
print(counter)

# counter variable needs to be set before / outside eof the for loop or it will always stop at 10


```

### Day 23 of 100 | 2024-07-28

#### range()

```Python
    # gist: print numbers by loog within  a range()

    # syntax: 
    for i in range(beginning_number, ending_number):
        print(i)        # output: beginning number to one less than ending umber

    # syntax (third parameter):
    for _ in range(beginning_number, ending_number, step_over_number):
        # the default step-over value is 1
        print(_)        # output: lopp from beginning to ending steped over by step-over value


    # code:
    for i in range(0, 100):
        print(i)        # output: 0 to 99 printed to screen
    # the same result can be derived with this syntax
    for i in range(100):
        print(i)

    # real-world example: 
    for i in range(10):
        print(i)

    # real-world example:

    # if the var name is unimportant when looping use _
    for _ in range(0, 100):
        print(_)        # output: 0 to 99 looped
    # -1 for step-over value
    for _ in range(0, 10, -1):
        print(_)        # output: nothing

    for _ in range(10, 0, -1):
        print(_)        # output: 10 - 1
                        # if you want to do something in reverse, make sure the value of beginning_number is largest
                        # if you want to iterate in reverse but skip every other number, use -2

    # list() of range()
    for _ in range(10):
        print(list(rang(10)))

```


#### enumerate()

```Python

    # gist: enumerate() provides index of output values

    # syntax:
    for i, char in enumerate('Hello')
        print(i, char)      # output: index value next to char value

    # code exercise:
    for i, char in enumerate(list(range(100))):
        if char == 50:
            print(f'index of 50 is {i}')
    # in each exervise think of how you can combine all previous sections in solution

    # keep this one document don't seperate docs for each section on github

```
### Day 24 of 100 | 2024-07-29

#### While Loops

```Python

    # gist: while a condition is happening do isomething 
        # to break out of a while loops, you must turn 
        # the condition to false or use a break statement

    # syntax:
    while condition:
        print()

    # code:
    i = 0               # infinate loop until machine crashes
    while i < 50:
        print(i)        # output: repeats until stopped b/c 0 is always < 50

    # be careful with while loops
    # add break statements
    i = 0 
    while i < 50 :
        print(i)
        break           # breaks the loop 

    i = 0
    while i < 50:
        print(i)        # output: prints i 50 times
        i = i + 1       # break statement in code; stops after 50 iterations


    # short-hand code
    i = 0
    while i < 50:
        print(i)
        i += 1

    # add else statement to code:
    i = 0 
    while i < 50:
        print(i)
        i++ 1
    else: 
        print('All done!')

```
#### While Loops 2

```Python

    # gist:
        # when to use for loop:
            # for simple loops
            # for iterating over iterable obj(s)
        # when to use while loop:
            # not sure how many times to loop over something
            # not sure how long it's going to take to loop


    # syntax:
    while True:
        print(my_list[i])
        break

    # code:
    while True:
        input('Say something: ')
        break

    # add conditional logic
    i = 0
    while i < len(my_list):
        print(my_list[i])
        i += i
        break

    while True:
        response = input('Say something: ')
        if (response == 'Bye'):
            break
```

#### break, continue, pass

```Python

    # gist: 

    # syntax:
    while True:
        print(i)
        continue

    # code:

    # for loop example of continue
    my_list = [1,2,3]
    for item in my_list:
        continue
        print(item)

    # while loop example of continue
    i = 0
    while i < len(my_list):
        i += 1
        continue
        print(my_list[i])


    # pass: esentially does nothing - jus passes to the next line
        # pass acts as a placeholder so your code runs w/o error
        # come back and add the code you need to add and delete pass


```

 #### Our 1st GUI

 ```Python

     # gist: building a graphical UI

     # exercise
    #Display the image below to the right hand side where the 0 is going to be ' ', and the 1 is going to be '*'. This will reveal an image!
    picture = [
    [0,0,0,1,0,0,0],
    [0,0,1,1,1,0,0],
    [0,1,1,1,1,1,0],
    [1,1,1,1,1,1,1],
    [0,0,0,1,0,0,0],
    [0,0,0,1,0,0,0]
    ]

     # sudo code = break it into smaller problems

     # use loop to print the current image

     # add conditional logic to either print ' ' or '*'

    # get the sequence printed out as is with a loop
    i = 0
    while i < len(picture):
        print(picture[i])
        i += 1

    # add conditional logic to print ' ' for 0 and '*' for 1

    i = 0
    while i < len(picture):
        print(picture[i])
        i += 1
    if i = 0:
        print(' ')
    elif i = 1:
        print('*')


    # alsways start out solving these exercises w/ sudo code

    # 1. iterate over picture
        # for loop
        for image in picture:
        # nested for loop
            for pixel in image:
        # add conditional logic
                if (pixel == 1):
                    print('*'. end='')      # if 1 -> print '* '
                else:
                    print(' ', end='')      # if 0 -> print ' '
            print('')

    # alsways start out solving these exercises w/ sudo code

    # 1. iterate over picture
    # for loop
    for row in picture:
        for pixel in row:
            if (pixel == 1):
            print('*', end='')          # if 1 -> print '* '
            else:
                print(' ', end='')      # if 0 -> print ' '
        print('')                       # output: chirstmas tree designed by * and ' '
 ```

#### Developer Fundementals: IV

```Python

    # gist: What is good code? What does it mean to be a good programmer?
        # clean -> following the best practices?
        # readability -> can you and other programmers understand your code
            # now and in the future...
        # predictability -> can you write code w/o obscure syntax/tools so 
            # other devs can understand and predict what the output of your
            # code will be?
        # DRY--Do NOT Repeat Yourself
            # make code reusable


    # code:
    for row in picture:
        for pixel in row:
            if (pixel == 1):
                print('*', end='')      # if 1 -> print '* '
            else:
                print(' ', end='')      # if 0 -> print ' '
        print('')                   # output: chirstmas tree designed by * and ' '

    # refactored code:
    fill = '*'
    empty = ' '
    for row in picture:
        for pized in row:
            if pixell:
                print(fill, end='')
            else(empty, end='')
```

### Day 25 of 100 | 2024-07-30

#### Exercise: Find Duplicates

```Python

     # gist:

     # syntax:

     # code:
     some_list = ['a', 'b', 'c', 'b', 'd', 'm', 'n', 'n']
     # 1. set duplicates var
     duplicates = []
     # 2. loop over provided list
     for value in some_list:
        if some_list.count(value) > 1       # remember count allows us to count how many times an item in a list exists
            if value not in  duplicates:
                duplicates.append(value)
    print(duplicates)                       # output: 'b', 'b', 'n', 'n'
```

#### Functions

```Python

     # gist: create your own functions so you don't have to repeat your self
        # remember DRY

     # syntax:
     def function_name():
        print("function_name was printed")

    # now you call the function and it runs the above code
        function_name()


    def function_name():
        print("function_name")

# now you call the function and it runs the above code
function_name()

    def say_hello():
        print("hello there")

    say_hello()

     # code:
```
### Day 26 of 100 | 2024-07-31


#### Arguements vs Parameters

```Python

     # gist: 
        # parameters are used when defining the function
            # parameters: define
        # arguements are used when we call--or invoke--the function
            # arguements: call

     # syntax, code
     # parameters
    def say_hello(name, emoji):
         print(f"hello {name} {emoji}")  # make sure all text after f is w/i quotes (single or double; doesn't matter it just needs to be consistent and fast for you to type

    # arguements
    say_hello('Thomas', '🤣')
    say_hello('Kyleigh', '😍')
    say_hello('Benny', '😭')

```


#### Default Parameters and Keyword Arguements


```Python

     # gist: 
        # positional parameters and keywords are clean
        # you can use keyword arguements, but keep them in the same order the function dictates to keep things clean

        # defualut parameters
        def say_hello(name="Darth Maul", emoji="😈"):
            print(f'hello {name} {emoji}')

        say_hello()

        # keyword arguemen - keeps the code in order for future use
        say_hello(name='Thomas', emoji='😇')

```


#### return

```Python

    # gist: functions don't return/print anything unless you add a return/print keyword within the function
        # functions either modify or return something within the program

    # function rules:
        # should do one thing well; should be easy to understand
        # should return something

    # code:
    # define function
    def sum(num1, num2)
        return num1 + num2

    # assign to var
    total = sum(10, 5)      # output: 15
    print(sum(10, total))   # output: 25

    # code: 
    def sum(num1, num2):
        return num1 + num2
    print(sum(1, 5))

    # conplicated, unclear function
    def sum(num1, num2):
  return num1 + num2
print(sum(1, 5))

# nested function (not clean)
def sum(sumnum1, sumnum2):
  def div_nums(divnum1, divnum2):
    return sumnum1 + sumnum2  # return for unnested function
  return divnum1 / divnum2 # return for nested function


totalsum = sum(10, 20)
totaldiv = div_nums(100, 10)
print(totalsum)
print(totaldiv)

# so confused ^; don't do this because debugging is exhausting



# nested function (not clean) - cleaner than above
def sum(num1, num2):
  def another_func(n1, n2):
    return n1 + n2  # return for unnested function
  return another_func(num1, num2) # return for nested function

total = sum(10, 20)
print(total)
```

### Day 27  of 100 | 2024-08-01

#### Tesla Exercise

```Python

    # gist: work through this issue as a Python Engineer

    # code:

age = input("What is your age?: ")

if int(age) < 18:
	print("Sorry, you are too young to drive this car. Powering off")
elif int(age) > 18:
	print("Powering On. Enjoy the ride!");
elif int(age) == 18:
	print("Congratulations on your first year of driving. Enjoy the ride!")

    #1. Wrap the above code in a function called checkDriverAge(). Whenever you call this function, you will get prompted for age. 
    # Notice the benefit in having checkDriverAge() instead of copying and pasting the function everytime?

    #2 Instead of using the input(). Now, make the checkDriverAge() function accept an argument of age, so that if you enter:
    #checkDriverAge(92);
    #it returns "Powering On. Enjoy the ride!"
#also make it so that the default age is set to 0 if no argument is given.


Problem Solving Steps

    1. Psudo Code

        # define a function called checkDriverAge()

        # add the code within the function

        # change the input() to accept arguements of age

        # check by typing an age above 18 to make sure the function works correctly

        # ensure the return == Pwering On. Enjoy the ride!

        # make the default age=0 if no imput is given


    2. create the function

    3. add the code into the function

    4. change the function to accept arguments

    5. add default age to function

```

### Day 28 of 100 | 2024-08-02

#### Continuation of Tesla Problem Set

```Python
    # defin function
    def checkDriverAge():
    # add original code to function
    age = input("What is your age?: ")
        if int(age) < 18:i
            print("Sorry, you are too young to drive this car. Powering off")
        elif int(age) > 18:
	        print("Powering On. Enjoy the ride!");
        elif int(age) == 18:
	        print("Congratulations on your first year of driving. Enjoy the ride!")= input("What is your age?: ")

    # clean v.  of the Tesla code:
    age = ("What is your age?: ")

    #Wrap the above code in a function called checkDriverAge()
    # function should work this way
    def checkDriverAge():
        if int(age)  < 18:
            print("Sorry, you are too young to drive this car. Powering off")
        elif int(age) > 18:
            print("Powering On. Enjoy the ride!");
        elif int(age) == 18:
            print("Congratulations on your first year of driving. Enjoy the ride!")
    
    # function update w/ parameters/arguements
    age = ("What is your age?: ")
    # replace input() to make the checkDriverAge() function accept an argument of age
    def checkDriverAge(age):
        if int(age) < 18:
            print("Sorry, you are too young to drive this car. Powering off")
        elif int(age > 18):
            print("Powering On. Enjoy the ride!");
        elif int(age) == 18:
            print("Congratulations on your first year of driving. Enjoy the ride!")
    
    # if driver age = checkDriverAge(92);
    # output =  'Powering On. Enjoy the ride'

    # also make it so that the default age is set to 0 if no argument is given.


```
#### Methods vs. Functions

```Python

    # Methods: are owned by the data type preceeding them
    'Hello'.capitalize()    # str 'hello' owns the .capitalize method

    # Functions()
    def this_is_a_new_function():
        pass

    this_is_a_new_function()

```

#### Docstrings

```Python

    # gist: docstrings help you and other developers understand your functions/methods

    # syntax:
    def do_something_new(a):
        '''
        info: this tells others and you what the function does
         this function tests and prints param a
        '''
        print(a)

        print(test.__doc__)

```


#### Clean Code

```Python

    # code: 
    def is_even(num):
        if num % 2 == 0:
            return True
        elif num % 2 != 0
            return False

    print(is_even(50))  # return: True
    print(is_even(21))  # return: False

    # clean up  ^ function
    def is_even(num):
        return num % 2 == 0:

    print(is_even(50))  # return: True -  same as above - less code
    print(is_even(50))  # return: False - same as above - less code

```
### Day 29 of 100 | 2024-08-03

#### # *args and # '''**kwargs'''

```Python

    # *args
    def superfunc(*args):   # *args enables as many args to be passed to this function
        return sum(agrs)

    super_func(1, 2, 3, 4, 5, 6) # will now accept as many args as passed b/c *args keyword was added to the function def

    # clean up 
    def superfunc(*args):
        print(*args)        # outpdut: all args: 1, 2, 3, 4, 5
        print(args)         # output: (1, 2, 3, 4, 5)
        return sum(args)
    superfunc(1, 2, 3, 4, 5, 6)

    # print answer
    def superfunc(*args):
        print(args)
        return sum(args)

    print(superfunc(1, 2, 3, 4, 5))

    # funct from replit.com that runs currectly 
    # **kwargs
    def superfunc(*args, **kwargs): # *args and **kwargs can be called anything (i.e., *hello **yoyo) but *args, **kwargs  are convention
        total = 0
        for items in kwargs.values():
            total += items
    return sum(args) + total

    print(superfunc(1, 2, 3, 4, 5, num1=5, num2=10))

    # funct w/o replit.com indentions, corrections
    def superfunc(*args, **kwargs): # *args and **kwargs can be called anything (i.e., *hello **yoyo) but *args, **kwargs  are convention
        total = 0
        for items in kwargs.value():
            total += items
        return sum(args) + total

    print(superfunc(1, 2, 3, 4, 5, num1=5, num2=6))

    # ordering (*args, **kwargs)

    # rule: params, *args, default parameters, **kwargs

    def superfunc(name, *args, i='hi', **kwargs)    # this is convention, for ordering but this is super confusing
    def superfunc(name, *args)                      # most functions olny have 1 maybe 2 of these
```

#### Exercise: Functions

```Python

    # starter code:
    def highest_even(li):
        pass

    print(highest_even([10, 2, 3, 4, 8, 11]))
 
    # the answer should be printed as 10

    # solution:

    def highest_even(li):
        evens = []
        for item in li:
            if item % 2 == 0:
                evens.append(item)
        return max(evens)
    print(highest_even([1, 2,3 ,4, 8, 11]))


    # code runs in replit env

    def highest_even(li):
     evens = []
     for item in li:
         if item % 2 == 0:
             evens.append(item)
     return max(evens) # all the way to this line folds up into the function
print(highest_even([10, 1, 2,3 ,4, 8, 11])) # this line is seperate from the funct.


   # code runs in replit env

    def highest_even(li):
    evens = []
        for item in li:
            if item % 2 == 0:
                evens.append(item)
      return max(evens) # all the way to this line folds up into the function
 print(highest_even([2, 10, 1, 2,3 ,4, 8, 11])) # this line is seperate from the funct.
    
    # the response should be 2 b/c the loop stops at 2 since it's an even number

```

## Short Break Taken to focus on Prompt Engineering

## Day 30 of mr| Sat, Aug 10, 2024

#### Walrus Operator

```Python
    
    # := : assigns values to variables as part of a larger expression

    # walrus is a new feature

    # you can see new features in what's new in python
        # language is constantly evolving
    
    # walrus is an assignment operator

    # 

    a = 'helloooooooooooooo'

    if (len(a)> 10):
    print(f"too long {len(a)} elements")

    # now with the walrus operator

    # assign n w/e the value of a is with walrus operator

    a = 'helloooooooooooo'

    if ((n := len(a)) > 10):
        print(f"Too long {n} elements")
    
    # one more exercise to to make sure you grasp the concept
    a = 'hellooooooooooooo'
    while ((n := len(a)) > 1):
        print(n)
        a = a [:-1] # this is the minus 1 short form a [:-1]

        print(a)    # h will be the only character left and will print after 2
```
## Day 31 of 100 | Tue, Aug 20, 2024 (started Prompt Engineering Course and focused was moved there)

#### Scope

```Python

    # Sope simply means: what variables do I have access to?

    # global scope: a var at the top of the doc that the whole doc has access to

    # local Scope

    def some_func():
        total = 100

    primt(total) # output: total is not defined b/c you're tying to access it outside of the function

    # if a var is not inside of a func, it's part of the global scope; inside of the func, it's local

    # example: 

    if True:
        x = 10

    def some_func():
        total = 100

    print(x) # output: 10 b/c x is part of the glocal scope

    # scope is simply who has access to who/what
```
#### Scope Rules

```Python

    # who has access to who in this code?

    a = 1

    def confusion():
        a = 5
        return a

    print(a) # output: 1
    print(confusion())  # output: 5


    # Evaluation 2 - 

    # Scope - what variables do I have access to?

    a = 1

    def parent():
        a = 10
        def confusion():
            return a
        return confusion()

    print(parent()) # outputs: 10 
    print(a) # outputs: 1 

    
    # How the python interperter evaluates scope:
    
    # Evaluation 1 - start w/ local
    # Evaluation 2 - Parent local?
    # Evaluation 3 - Global
    # Evaluation 4 - built-in python functions

```
#### global Keywords

```Python

    # what about parameters?

    a = 10
    def confusion():
        print(b)
        a = 90

    confusion(300) # outputs: 300

    # parameters are considered local vars
    
        # able to use it inside of the function but we not ouside of those functions

    # create counter to further understanding

    total = 0 

    def count():
        total += 1
        return total

    print(count())  # outputs: local variable 'total' referenced before assignment

    # count doesn't know about total yet

    # but we need to reference total from the global scope

    # understanding local/global scope
    
    total = 0

    def count():
        total = 0
        total += 1
        return total

    count()
    count()
    print(count())  # outputs: 1 b/c the function was reset and the total is set back to 0


    # global keywork:

    total = 0

    def count():
        global total # this global keyword gives you access to total in the global space
        total += 1
        return total

    count()
    count()
    print(count())

    # create a parameter and pass in the parameter/argument
     total = 0

     def count():
         global total # this global keyword gives you access to total in the global space
         total += 1
         return total

     print(count(count(count)count()))) # output: 3 b/c you're calling count 3x

```
#### nonlocal Keyword

```Python

    # nonlocal is a new Python3 Keyword

    # Example Code:

    def outer():
        x = "local"
        def inner():
            nonlocal x
            x = "nonlocal"
            print("inner:", x)

    inner()                 # output: inner: nonlocal
    print("outer:", x)      # output: outer: nonlocal
    
    # What it does

    # Evaluation 1: start w/ local (scope)?
    # Evaluation 2: Parent local (scope)?
    # Evaluation 3: Global

    # KEY POINT: this makes code more complicated than it needs to be

        # aim to avoid using things like local and nonlocal vars; make code predictable

        # only use local and nonlocal in specail cases: i.e. closures 
        
        # just understand that these local and nonlocal keywords are there for a reason

    # Goal: Keep Code Clean; Make Code Predictable
```
## Day 32 of 100 | Wed, Aug 21, 2024

#### Why Do We Need Scope?

```Python

    # why not just have all global vars?

    # machine don't have infinate memory, drive space

    # the python garbage collector works to remove unused vars and clean up memory space 

```
#### Python Exam: Testing Your Understanding

```Python

    # Syntax for defining a TUPLE?

    ("apple", "banana", "cherry")

    # Syntax for defining a SET?

    {"apple", "banana", "cherry"}

    # Incorrect Var Naming

    my-var # cannot use a dash

    # Two ways to define a var w/ a numerica value

    x = 5
    x = int(5)

    # Two ways to defin a var w/ floating point value

    x = 2.8
    x = float(2.8)

    # Syntax for defining a DICRIONARY?

    {"name": "apple", "color": "green"}

    # Which collection is ordere, changable, and allows duplicate members?

    LIST

    # Which collection does not allow duplicate members?

    SET

```
### Developer Environment

#### MAC - Python Install

```Python

    # ran brew install python3 in warp terminal (at the beginning of this course)

```
#### Python Developer Tools

```Python

    # List of Tools

    '''
    - Terminal
    - Code Editors
    - IDEs (PC or Spyder)
    '''

    # code editors are lightweight
    # IDEs are bigger and heavier but have auto compleition, code snipits, etc.

    # Notebooks - Jupyter

```
#### Optional: Terminal Commands

```Python

    # ls = list
    # pwd = print working dir
    # cd .. goes up one dir
    # clear clears term
    # cd / takes you to root dir
    # cd ~ user dir
    # open . open current dir
    # mkdir webapp
    # cd webapp # go into the dir
    # touch index.html
    # open index.html
    # open -a "VS Code"
    # open -a "VS Code" index.html
    # open index.html

    # you can do things much faster

    # mv index.html about.html = changes the name of a file to the new name 

    # up arrow will bring up the history 

    # rm about.html

    # rm -r[f] to remove dirs

    # but you alread knew all of this

    # in mac terminal you can do this and it will speak to you

        # say this is soooo cool
        # screen reader voice reads it back to you

    # always create files and folder using the cli (never point and click)

```
## Day 33 of 100 | Thu, Aug 22, 2024

#### iTerm Setup

##### My Terminal Setup
```Python

    # customize bash

    # nano ~/.bash_profile

    #  then add one of these useful bash prompts: https://www.maketecheasier.com/8-useful-and-interesting-bash-prompts/

    # for ZSH customization visit this site: https://ohmyz.sh/

    # homebrew installs anything from the web (boom; roasted.)

    # brew install fish

    # iTerm (specific to mac)
```
##### My Terminal Setup 2

```Python

    # customize terminal: https://osxdaily.com/2013/02/05/improve-terminal-appearance-mac-os-x/

    # iTerm2: https://iterm2.com/index.html

    # customize iTerm2: https://sourabhbajaj.com/mac-setup/iTerm/README.html

    # Homebrew: https://brew.sh/

    # Two Options for Different Shells
    '''
    1. https://ohmyz.sh/
    2. https://fishshell.com/
    '''

    # 8 Interesting Bash Prompts: https://www.maketecheasier.com/8-useful-and-interesting-bash-prompts/
```
## Day 34 of 100 | Fri, Aug 23, 2024

#### Using the Command Line/Terminal

```Python

    # all we are doing is writing a program that gets run by a machine - keep that in mind

    # you can use the terminal to run python3 code - easy alread knew that one!

```
#### Visual Studio Code (Setup)

```Python

    '''
    1. download vs code
    2. go through setup guide
    3. create hello.py (new tab -> command + s -> name it hello.py)
    4. install pylint
    5. Run hello.py by using the vs code terminal command - python3 hello.py -> Hello World.
    6. Use the PROBLEMS window to solve lint issues
    7. Enable Dracula Official Theme
    ''' 
 ```
### Day 35 of 100 | Sat, Aug 24, 2024


#### PyCharm

```Python

    # most used IDE (at time of filming) in the Python community   

    # only focused on Python 

    # download the community version of PyCharm

    # just use VS code of VIM; don't worry about PyCharm

    # even gives you english spell checfk 
```
### Day 36 of 100 | Sun, Aug 25, 2024

#### Code Formatting - PEP 8

```Python

    # PEP 8 – Style Guide for Python Code - https://peps.python.org/pep-0008/
        
        # PEP stands for Python Enhancement Proposals
        # PEP is the most popular style guid for Python
    
    # Code Editors / IDEs take care of this with Fomatting auto pep 8

    # install autopep8 to vs code

    # learn how to install pep8 in vim using ChatGPT

    # setup pep8 so it formats automatically when you click save in vim and VS Code

    # PyCharm alread has pep8 formatting built into the IDE

    # Turned on AutoSave, and Format on Save for VS Code
```
#### Quick Note: Jupyter Notebooks

```Python

    # Jupyter Notesbooks are for ML and Datascience, whis is perfect for me!!

```
### Day 37 of 100 | Mon, Aug 26, 2024

#### Jupyter Notebooks

```Python

    # Tool for DS and ML

    # Anaconda.com - the distribution website

    # Anaconda Mac Install Guide: 

    '''
    https://problemsolvingwithpython.com/01-Orientation/01.04-Installing-Anaconda-on-MacOS/
    '''
    # Account Created w/ GH authentication used for singin

    # Most Popular Python/R Data Science Platform

    # Installed Anaconda: Brew Install --cask anaconda

    # PyCharm is now bundeled w/ Anaconda

    # Waiting on Install

        # Once installed click Jupyter Notebook

        # Local Host is opened once Jupyter Notebook is installed

    # now you can use Anaconda in Chrome (any Browser really)

    # You can run Jupyter Notebooks offline even though they're in the browser
        
        # no WiFi Required

    # you get immediate code execution, which is great for Data Visulization, ML, Data Science

    # Brew Install Anaconda didn't execute b/c I'm on a pre-release version of MacOS

    # Install it Manually

```

#### Section Review

```Python

    # Remember: what you want and what you like will change throughout your dev life

        # you can change things as you evolve as a developer

    # Jupyter is good for immediate input/output

    # There's no BEST tool; it's what you like/need in your development career
    
    # I choose VIM and I'm liking it a lot now; light weight, fast, clean, highly customizable

```
#### <> Implement a New Life System

```Python

    # Design your life to become happy - KEEP LEARNING EVERY DAY!!

    # Think in Systems - Think like an Engineer an shape your entire life
    
    # Make sure you can commit to learning; if you can't don't take this step
```
### Day 38 of 100 | Tue, Aug 27, 2024

## Advanced Python: Object Oriented Programming

#### Note on Upcoming Sections

```Python

    # instructor will still use Replit but you need to use your dev env since you set it up

    # when we start building projects, the instructor will start using Sublime Text, Jupyter

```
## Day 38 of 100 | Tue, Aug 27, 2024  

#### What Is OOP?

```Python

    # Why it's important

        # everything in Python is an object b/c everything is built by the Class Keyword

    # We can use different methods to perform actions on any object

    # What's an object?
    
        # objects have methods and atributes that can be accessed by the .method

    # We can create our own custom Objects

    # Use Case:

    '''
    we need to program an amazon deliver drone 

    the problem is when code gets bigger and more complex, it becomes multiple files
    with millions of lines of code
    '''

    # How can OOP be used to make code more managable?

    '''
    OOP is a paradigm (e.g., it's a way for use to think about and structure our code)

    We can break up a program that controls a delivery drone, we can break it into 
    small pieces (little objects) that represent the real world
    '''
    # One Developer develops the claws that hold the package

    # Another Dev handles  the signling so that we're able to send signals from AMZ to Drone

    # break up functionality into small peices that represent the real world

    # If you need to make a small tank (in addition to the drone), you can reuse Objects

    # KEY TAKE AWAY: OOP is a Paradigm - a way to think about our code

        # a way to structure our code and keep things organized and split them into dev groups
```
### Day 39 of 100 | Wed, Aug 28, 2024
#### What is OOP? Part 2 

```Python

    # History of Programming Languages: 
    '''
    https://en.wikipedia.org/wiki/History_of_programming_languages
    '''
    # Before OOP it was Procedural Code

        # do this do that

    # OOP models real-world objects

    # Think in terms of models; organize things

    # CREATE NEW CLASS:

    class BigObject:
        pass

    print(type(obj1)) # outputs: '__main__.BigObject'
    # must use SnakeCase; not like python vars

    # Class v. Obj

    # Class = blueprint for following objects

    # Instantiating a class means to create a new Obj

    #OOP

    class BigObject: #Class
        #code
       pass

    obj1 - BigOjects() #instanciate
    obj2 - BigOjects() #instanciate
    obj3 - BigOjects() #instanciate
```
### Day 40 of 100 | Thu, Aug 29, 2024

#### Creating Our Own Objects

```Python

    # code our own class for a wizard game

    # think about it in OOP

    # we will need players

    # class for players

    class PayerCharacter: # do not add s here
        def __init__(self, name):
            self.name = name

        def run(self):
            print('run')

    # at this point we don't know what self or init is

    player1 = PlayerCharacter() # instantiate player


    print(player1) 

    # output error:

    '''
    Traceback (most recent call last):
    File "main.py", line 9, in <module>
        player1 = PlayerCharacter()
    TypeError: __init__() missing 1 required
    positional arguement: 'name'
    '''
    player1 = PlayerCharacter('Cindy') # removes error

    __init__ # this is called a dunder/magic method

    # What is the self Keyword?

    # Self defines self and refers to the PlayerChar

    # outputs Cindy

    class PlayerCharacter:
        def __init__(self, name):
            self.name = name

        def run(self):
            print('run')

    player1 = PlayerCharacter('Cindy')

    print(player1.name) # prints Cindy

    # instantiate second player

    class PlayerCharacter:
        def __init__(self, name):
            self.name = name

        def run(self):
            print('run')

    player1 = PlayerCharacter('Cindy')
    player2 = PlayerCharacter('Tom')

    print(player1.name) # outputs: Cindy
    print(player2.name) # outputs: Tom

    # KEY POINT: 

    '''
    Write code once that can be reused 
    multiple times; REMEMBER DRY (Do not Repeat
    Yourself)

    Write dynamic code that changes based on 
    what you pass to it
    '''
    # Add Age Attribute

    class PlayerCharacter:
        def __init__(self, name, age):
            self.name = name # attributes
            self.age = age

        def run(self):
            print('run')

    player1 = PlayerCharacter('Cindy', 44)
    player2 PalyerCharacter('Tom', 21)

    print(player1.age)  # outputs: 44
    print(player2.age)  # outputs: 21

    # use .notation to access properties

    player1.age, 
    player2.age, 
    player1.name,
    playe2.name

    # two players in different locations in memory

    print(player1)  # object at 0x134lk
    print(player2)  # object at 0x134lx

    # Use class to duplicate objects easily
```
### Day 41 of 100 | Fri, Aug 30, 2024 
#### Attributes and Methods
```Python

    # OOP Allows us to create objects w/ their own

        # methods - like run 
        # attribute - properties

        '''
        Best way to add functionality to a language 
        and mimic the real world!
        '''

    # Think in terms of functionality not procedures

    '''
    Group data, like attributes, w/ methods
    to create class
    '''
    # KEY POINT:

        # new function 
        help() # gives you the blue print of the obj

    # Class Obj Attribute

    class PlayerCharacter:
        # class object Attribute
        membership = True # static; not dynamic
        def __init__(self, name, age):
            self.name = name # attributes
            self.age = age

        def run(self):
            print('run')
            return 'done'

    player1 = playerCharacter('Cindy', 44)
    player2 = PlayerCharacter('Tom', 21)
    player2.attack = 50

    print(player2.membership) # outputs: True
    print(player1.membership) # outputs: True

    # this is not dynamic though

    '''
    only use if all objects you will instantiate 
    will have this class attribute; it's not going
    to change for any of the objects
    '''

    # Class Obj attr doesn't change accross instances

    # Class attr = dynamic/specific to each class obj

    class PlayerCharacter:
        # class object attribute
        membership = True
        def __init__(self, name, age):
            if (PlayerCharacter.membership):
                self.name = name # attribute
                self.age = age

        def shout(self):
            print(f'my name is {self.name}')

    player1 = PlayerCharacter('Cindy', 44)
    player2 = PlayerCharacter('Tom', 21)
    Player2.attack = 50

    print(player1.shout())

```
### Day 42 of 100 | Sat, Aug 31, 2024

#### __init__
```Python

     class PlayerCharacter:
         # class object attribute
         membership = True
         def __init__(self, name='anonymous', age=0):
             if (age > 18):
                 self.name = name # attribute
                 self.age = age

         def shout(self):
             print(f'my name is {self.name}')

     player2 = PlayerCharacter('Tom', 21)

     print(player1.shout())
    
    # since Tom is only 10, self is not instantiated

    '''
    Add controls/safe guards so we receive the correct
    data for each player/character/user
    '''
    # Key Point: 

    '''
    __init__ gives you control to make sure 
    everything in the class is setup correctly
    and consistently
    ''' 
```
### Day 43 of 100 | Sun, Sep 1, 2024
#### Exercise: Cats Everywhere
```Python

#Given the below class:
class Cat:
    species = 'mammal'
    def __init__(self, name, age):
        self.name = name
        self.age = age


# 1 Instantiate the Cat object with 3 cats

class Cat:
    species = 'mamal'
    def __init__(self, name, age):
        self.name = name
        self.age = age

cat1 = Cat('Merritt', 12)
cat2 = Cat('Joe', 8) 

# 2 Create a function that finds the oldest cat

class Cat:
    species = 'mamal'
    def __init__(self, name, age):
        self.name = name
        self.age = age

cat1 = Cat('Merritt', 12)
cat2 = Cat('Joe', 8)
cat3 = Cat('Winston', 8)

print(cat1.name, cat1.age)
print(cat2.name, cat2.age)
print(cat3.name, cat3.age)

def oldest_age(*args):
    return max(args)
print(f'The oldes cat is {oldest_age(cat1.age, cat2.age, cat3.age)} years old.') #outputs 'The oldest cat is 12 y/o'

```
### Day 44 | Mon, Sep 2, 2024
### @classmethod and @staticmethod
```Python

    # class methods work w/o instantiation
    
    membership = True
    def __init__(self, name, age):
        self.name = name #attributes
        self.age = age

    @classmethod
    def adding_things(cls, num1, num2):
        return num1 + num2

    print(PlayerCharacter.adding_things(2,3))

    # output: 5 w/o instantiation of the class

    # 95% of your classes will not use a class method

    # however, you should know about this tool

    # adding a PlayerCharacter in @classmethod

         membership = True
     def __init__(self, name, age):
         self.name = name #attributes
         self.age = age

     @classmethod
     def adding_things(cls, num1, num2):
         return cls('Teddy', num1 + num2)

     print(PlayerCharacter.adding_things(2,3))
     print(Player3)

     # static method works the same but no access to cls

     @staticmethod
     def adding_things(num1, num2) #no access to cls here
        return num1 + num2
```
### Day 45 | Tue, Sep 3, 2024
#### Reviewing What We Know So Far
```Python

    # started @ procedural

    # moved to wirting function

    # now we're thinking in Objects OOP

    # we learned how to instantiate classes
    
    class NameOfClass():
    
    # learned about class attributes

    class_attribute = 'value'

    # how to instantiate 

    def __init__(self, param1, param2):
        self.param1 = param1
        self.param2 = param2

    # Learned how to add methods
        # now each obj we create, instantiate has access to class methods

    # learned about @classmethod, @staticmethod

        # which can be called on the class w/o instaiting it

    # learned all this so we can create our own datatype 
    # that models the real world

    # follow these guidelines/structure and that's pretty much it 
```
#### Day 46 | Wed, Sep 4, 2024
### DEVELOPER FUNDAMENTALS: V
```Python

    # Test Your Assumptions

    # You need to know how things work so you can explain it to people/devs

    # Test Self

    class PlayerCharacter:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def run(self):
            return self

    player1 = PlayerCharacter('Thomas', 100)

    print(Player1.run())    # returns: <__main__.PlayerCharacter object at 0>

    # if you don't understand something, test it using return or print, etc...
```
#### Day 47 | Thu, Sep 5, 2024

### Encapsulation
```Python

    # What is Encapsulation?

    '''
    Encapsulation is the binding of data & functions that manipulate the data

    Encapsulate everything in one box so users, code, machines can interact
    with it theses objects in the encapsulated box.
    '''

    # The data and functions are what we call attributes and methods

    # PlayerCharacter Encapsulation

    class PlayerCharacter:
        def __init__(self, name, age):
            self.name = name    # data attribute
            self.age = age      # data attribute

        def run(self):
            print('run')
        
        # Encapsulate functionality so you can use all the functions/data attrs 
        def speak(self):
            print(f'my name is {self.name}, and I am {self.age} years old')
            
    player1 = PlayerCharacter('andrei', 100)
    
    # Why package data and functions into attrs and methods?

    '''
    Because if the player character ddoesn't have any actions, methods
    and only had attributes, it's just like a dictionary, which is
    kind of useless.
    '''

    # W/O functions it's just a fancy dictionary

    player2 = {'name': 'Thomas', 'age': 100}
    print(player2['name'])
    print(player2['age'])
```
#### Day 48 | Fri, Sep 6, 2024 
### Abstraction
```Python

    # Only give access to things devs and machine need access to; hide all else

    # For example: you know you have access to .count but not exactly how it works

        # that's because it's abstracted under a blanket by python3 devs
    
    # Example: you want to use the iPhone camera functions in an app

        # you don't know how the camera is coded but you know you can access it

    # But what if you don't want antoher programmer to overwrite you code

    class PlayerCharacter:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def run(self):
            print('run')

        def speak(self):
            print(f'my name is {self.name}, and I am {self.age} years old')

        # You don't want another programmer to be able to overwrite your functions
        player1.name = '!!!'    # overwrites function
        player.speak = 'BOOO'   # overwrites function
    
        # Trying to call function after overwrite
        print(player1.speak())  # 'str' object is not collable b/c of overwtire
    # You Must Use Abstraction to eliminate overwrites; more in next section
```
#### Day 49 | Sat, Sep 7, 2024
### Private vs Public
```Python

    # Python has no TRUE private variables

    # Underscore convention:
        
        # If you see _name it means that var should be private; don't modify it

    class PlayerCharacter:
        def __init__(self, name, age):
            self._name = name
            self._age = age

        def run(self):
            print('run')

        def speak(self):
            print(f'my name is {self._name}, and I am {self._age} years old')

        # instantiate player1

        player1 = PlayerCharacter('Thomas', 30)

        print(player1.speak())  # my name is Thomas, and I am 30 years old!

        # Double Underscore __ is also conventions; means don't modify or touch

        __init__

        # Dunder methods start with double underscores; don't modify them
```
#### Day 50 | Sun, Sep 8, 2024
### Inheritance
```Python

    # Inheritance enables new objs to take on properties of existing objs

    # If there are no vars attrs to be assigned __init__ not required

    # Users in Game
        - Wizards
        - Archers
        - Ogers

    class User:
    def sign_in(self):
        print('logged in')

    # Create Sub Classes

    class Wizard():
        pass

    class Archer():
        pass

    # Ensure all Users have access to login w/ inheritance

    # All that needs to be happen is pass the parent class w/i the bracket

    class User():
        def sign_in(self):
            print('logged in')

    class Wizard(User):     # Passing (User) enables inheritance
        def __init__(self, name, power):
            self.name = name
            self.power = power

        def attack(self):
            print(f'attacking with power of {self.power}')

    class Archer(User):     # Passing (User) enables inheritance
        def __init__(self, name, num_arrows):
            self.name = name
            self.num_arrows  = num_arrows
 
        def attack(self):
            print(f'attacking with arrows: arrows left - {self.num_arrows}')
    # Instantiate a class

    wizard1 = Wizard('Merlin', 50)  # instantiate Merlin w/ power 50
    archer1 = Archer('Robin', 100)  # instantiate Robin w/ 100 arrows

    # Archer1 and Wizard1 have signin and unique attack for each class

    wizard1.attack()            # return: attacking w/ power of 50
    archer1. attack()           # return: attacking w/ arrows: arrows left 100

    # We did the following
        
        # kept code dry
        # shared functionality
        # made different attack functions
    print(wizard1)              # Wizard Obj created
    print(wizard1.sign_in())    # Wizard1 can access signin b/c of inheritance


```
#### Day 51 | Mon, Sep 9, 2024
### Polymorphism
```Python

    # Recap

    # We've discussed three Pillars of OOP

        # Inheritance
        # Abstraction
        # Encapsulation
        
    # The 4th Pillar of OOP - PloyMorphism
        
        # Poly = Many
        # Morphism = Form
    # So many forms

    class User():
    def sign_in(self):
        print('logged in')

    class Wizard(User):     # Passing (User) enables inheritance
        def __init__(self, name, power):
            self.name = name
            self.power = power

        def attack(self):
            print(f'attacking with power of {self.power}')

    class Archer(User):     # Passing (User) enables inheritance
        def __init__(self, name, num_arrows):
             self.name = name
             self.num_arrows  = num_arrows

        def attack(self):
             print(f'attacking with arrows: arrows left - {self.num_arrows}')

    wizard1 = Wizard('Merlin', 60)
    archer1 = Archer('Robin', 30)

    print(wizard1.attack())
    
    # A different way to attack

    def player_attack(char):
        char.attack()

    player_attack(wizard1)
    player_attack(archer1)

    # Above, you see the same function works differently on archer vs. wizard

    # This is Polymorphism

    # This is the power of OOP; use them to structure your code efficiently

```
#### Day 52 | Tue, Sep 10, 2024
### Exercise: Pets Everywhere
```Python

    # Let's practice bulding some objs using classes

    class Pets():
    animals = []
    def __init__(self, animals):
        self.animals = animals

    def walk(self):
        for animal in self.animals:
            print(animal.walk())

    class Cat():
        is_lazy = True

        def __init__(self, name, age):
            self.name = name
            self.age = age

        def walk(self):
            return f'{self.name} is just walking around'

    class Simon(Cat):
        def sing(self, sounds):
            return f'{sounds}'

    class Sally(Cat):
        def sing(self, sounds):
            return f'{sounds}'

    # 1 Add another Cat
    class Tom(Cat):
        def sing(self, sounds):
            return f'{sounds}'
    
    # 2 Create a list of all of the pets (create 3 cat instances from the above)
    my_cats = [Simon, Sally, Tom]   # my attempt
    
    # The Solution
    my_cats = [] 
    cat1 = Simon('Simon', 10)
    cat2 = Sally('Sally', 15)
    cat3 = Tom('Tom', 2)

    # create 3 cat instances from the above
    my_cats.append(cat1)
    my_cats.append(cat2)
    my_cats.append(cat3)

    # alternative to the above code

    my_cats = [Simon('Simon', 10), Sally('Sally', 15), Tom('Tom', 2)]

    # 3 Instantiate the Pet class with all your cats use variable my_pets
    
    # My 1st  attempt
    my_pets1 = Cat('Simon', 12)
    my_pets2 = Cat('Sally', 10)
    my_pets3 = Cat('Tom', 2)
    
    # Solution
    my_pets = Pets(my_cats)
    
    # 4 Output all of the cats walking using the my_pets instance
    my_pets.walk()
```
#### Day 53 | Wed, Sep 11, 2024
### super()
```Python

    # add __init__ to class User(object)

    class User(object):
        def __init__(self, email):
            self.email = email

        def sign_in(self):
            print('logged in')

    class Wizard(User):
        def __init__(self, name, power):
            self.name = name
            self.power = power

        def attack(self):
            print(f'attack with the power of {self.power}') 

    wizard1 = Wizard('Merlin', 60)
    print(wizard1.email)    # returns: 'Wizard' obj has no attribute 'email'

    # You need to add the __init__ within the Wizard class

    class Wizard(User):
        def __init__(self, name, power, email):     # add email here
        User.__init__(self, email)                  # add init here
        self.name = name
        self.power = power

    wizard1 = Wizard('Merlin', 60, 'merlin#gmail.com')
    print(wizard1.email)                            # returns: merlin@gmail.com

    # Recap of what was done

        # 1. added __init__(self, email): to class User
        # 2. call __init__ w/i the Wizard Class
        # 3. When new wizard is instantiated user.__init__(self, email) is passed in

    # Doing the same thing w/ super()

    class Wizard(User):
        def __init__(self, name, power, email):
            super().__init__(email)
            self.name = name
            self.power = power

    # super() enables us to refer to user 

    # super() was added in Python2.2

```
#### Day 54 | Thu, Sep 12, 2024
### Object Introspection
```Python

    # introspection in CS

    '''
    The ability to determine the type of an object at run time

    What's run time? When the code is running, you can dtermine the 
    type of an object.
    '''

    # dir function

    '''
    The dir function will return all the methods and attributes 
    that an instances has at its disposal.
    '''

    wizard1 = wizard('Merlin', 60, 'merlin#gmail.com')
    print(dir(wizard1))

    # You must pass dir an instances to see what the instance has access to

    print(dir(wizard1))     # return: all method wizard1 has access to 

```
#### Day 55 | Fri, Sep 13, 2024
### Dunder Methods
```Python

    # what do dunder methods do? 

    # __ = special method

    # Code

    class Toy():
        def __init__(self, color, age):
        self.color = color
        self.age = age

    action_figure = Toy('red', 0)
    print(actio>figure.__str__())   # returns: <__main__.Toy object at
    print(str(action_figure))       # returns: same as above  

    # Sometimes it's ok to modify dunder methods if you want you code 
        # to function in a specific way

    # exmaple

    class Toy():
        def __init__(self, color, age):
        self.color = color
        self.age = age

        def )__str__(self):
            return f'{self.color}'

    action_figure = Toy('red', 0)
    print(actio>figure.__str__())   # returns: <__main__.Toy object at
    print(str(action_figure))       # returns: same as above

    # Key Point: You can overwrite dunder methods but it's not best practice
```
#### Day 56 | Sat, Sep 14, 2024
### Exercise: Extending List
```Python

    # Create a __len__ dunder method 

    class SuperList(list):  # add super list as attribute
        def __len__(self):
        return 1000

    super_list1 = SuperList();
    print(len(superlist1))  # returns: 1000

    # Add append to super list

    super_list1.append(5)   # adds 5 to the beginning of 1000
    print(super_list[0]) # access superlist @ 0 index 
    # returns: 1000 5

    # Run a test
    print(issubclass(superList, list))  # returns 1000, 5, True b/c SuperList is a list subclass

    # Another Test
    print(issubclass(list, object)) # returns: True b/c everything in Python is obj inherited from base obj class 
```
#### Day 57 | Sun, Sep 15, 2024
### Multiple Inheritance
```Python

    # what if we want to create a new character?

    class HybridBord(Wizard, Archer)    # HybridBord inherits all methods from Wizard & Archer
        pass

    hb1 = HybridBorg()
    print(hb1.run())    # Error: missing 2 reguired positional arguments. 'name and 'power'

    hb1 = HybridBorg('borgie', 50)
    print(hb1.run())    # returns: 'Ran really fast'
    print(hb1.check_arrows())   # error: hybridborg object has not attribute 'arrows'
                                # this is b/c we inherited wizard 1st then archer 2nd
    
    # tricky issue w/ multiple inheritance - you need to understand how the classes work and not overwrite anything

    # complicate code a bit

    class HybridBorg(Wizard, Archer):
        def __init__(self, name, power, arrows):
            Archer.__init__(self, name, arrows)

    hb1 = HybridBorg('borgie', 50, 100)
    print(hb1.check_arrows())   # returns: 100 remaining

    print(hb1.attack())         # returns no attribute power

    # KEY POINT: When you perform multiple inheritance, things get complicated and fast

        # This will be complicated for other programmer to understand in the future
        # Multiple Inheritance = great power

        '''
        remember, w/ great power comes great responsibility
        '''

    # KEY POINT 2: Be cautions w/ multiple inheritance
```
#### Day 58 | Mon, Sep 16, 2024
### MRO - Method Resolution Order
```Python

    # Method Resolution Order
    # MRO Helps with complicated inheritance structure
        # it "says" do this, do this, then do that - helps with the inheritance relationships
        
    class A:
        num = 10
    
    class B(A):
        pass

    class C(A):
        num = 1

    class D(B, C):
        pass
    
    print(D.num)    # returns: 1

    # MRO defines what's first in line when it comes to inheritance

    # How to find out the MRO

    print(D.mro())  # returns: __main__.D, __main__.B, __main__.C __main__.A

    # Base Obj has __str__

    D.__str__ # checks all the way up to based obj and sees that base obj has __str__

    # Example of why inheritances can be confusing and why you might want to avoide MRO

    class X: pass
    class Y: pass
    class Z: pass
    class A(X,Y): pass
    class B(Y,Z): pass
    class M(B, A, Z): pass

    # KEY POINT: MRO is like an inheritance model

    print(M.__mro__)    # returns: M, B, A, X, Y, Z, base obj

    # MRO algo = depth first search

    # Python changed the MRO rules since v 2 ( You will never get tested on this stuff )
```
#### Day 59 | Tue, Sep 17, 2024
### Functional Programming
```Python

    # Functional Programming is simply another way for use to think about and organize code

```
### What Is Functional Programming?
```Python

    # Functional Programming is all about Seperation of Concerns

    # Seperate things into seperate chunks so everything is organized in a way that makes sense

    # 

```
###### Blue Print for Remaining Sections/Days
## Section X: Section Title
### Subsection Title
#### Day X | Day, Mth XX, 2024

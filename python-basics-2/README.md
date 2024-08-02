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


#### Title


```Python

    # gist:

    # code:

```


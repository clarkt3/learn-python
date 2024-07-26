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
### Day 23 of 100 | 2024-07-26

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


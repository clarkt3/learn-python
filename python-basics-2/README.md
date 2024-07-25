# Python Basics 2

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

#### Indentation In Python

 ```Python

 # key point:

 # syntax example:

 # code samples:


 ```

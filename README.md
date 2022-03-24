# About

Basic cheatsheet for Python mostly based on the book written by Al Sweigart, [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) under the [Creative Commons license](https://creativecommons.org/licenses/by-nc-sa/3.0/) and many other sources. I have modified this to remove what you do not need to know. 


## Read It

- [Website with full cheat sheet](https://www.pythoncheatsheet.org)


## Python Cheatsheet

- [About](#about)
  - [Contribute](#contribute)
  - [Read It](#read-it)
  - [Python Cheatsheet](#python-cheatsheet)
  - [Python Basics](#python-basics)
    - [Math Operators](#math-operators)
    - [Data Types](#data-types)
    - [String Concatenation and Replication](#string-concatenation-and-replication)
    - [Variables](#variables)
    - [Comments](#comments)
    - [The print() Function](#the-print-function)
    - [The input() Function](#the-input-function)
    - [The len() Function](#the-len-function)
    - [The str(), int(), and float() Functions](#the-str-int-and-float-functions)
  - [Flow Control](#flow-control)
    - [Comparison Operators](#comparison-operators)
    - [Boolean evaluation](#boolean-evaluation)
    - [Boolean Operators](#boolean-operators)
    - [Mixing Boolean and Comparison Operators](#mixing-boolean-and-comparison-operators)
    - [indentation and code blocks (:)](#indentation-and-code-blocks)
    - [if Statements](#if-statements)
    - [else Statements](#else-statements)
    - [elif Statements](#elif-statements)
    - [while Loop Statements](#while-loop-statements)
    - [break Statements](#break-statements)
    - [continue Statements](#continue-statements)
    - [for Loops and the range() Function](#for-loops-and-the-range-function)
    - [For else statement](#for-else-statement)
    - [Importing Modules](#importing-modules)
    - [Ending a Program Early with sys.exit()](#ending-a-program-early-with-sysexit)
  - [Functions](#functions)
    - [Return Values and return Statements](#return-values-and-return-statements)
    - [The None Value](#the-none-value)
    - [Keyword Arguments and print()](#keyword-arguments-and-print)
    - [Local and Global Scope](#local-and-global-scope)
    - [The global Statement](#the-global-statement)
  - [Exception Handling](#exception-handling)
    - [Basic exception handling](#basic-exception-handling)
    - [Final code in exception handling](#final-code-in-exception-handling)
  - [Lists](#lists)
    - [Getting Individual Values in a List with Indexes](#getting-individual-values-in-a-list-with-indexes)
    - [Negative Indexes](#negative-indexes)
    - [Getting Sublists with Slices](#getting-sublists-with-slices)
    - [Getting a List’s Length with len()](#getting-a-lists-length-with-len)
    - [Changing Values in a List with Indexes](#changing-values-in-a-list-with-indexes)
    - [List Concatenation and List Replication](#list-concatenation-and-list-replication)
    - [Removing Values from Lists with del Statements](#removing-values-from-lists-with-del-statements)
    - [Using for Loops with Lists](#using-for-loops-with-lists)
    - [The in and not in Operators](#the-in-and-not-in-operators)
    - [Augmented Assignment Operators](#augmented-assignment-operators)
    - [Finding a Value in a List with the index() Method](#finding-a-value-in-a-list-with-the-index-method)
    - [Adding Values to Lists with the append() and insert() Methods](#adding-values-to-lists-with-the-append-and-insert-methods)
    - [Removing Values from Lists with remove()](#removing-values-from-lists-with-remove)
    - [Removing Values from Lists with pop()](#removing-values-from-lists-with-pop)
    - [Indexing and Slicing Strings](#indexing-and-slicing-strings)
    - [The in and not in Operators with Strings](#the-in-and-not-in-operators-with-strings)
    - [The in and not in Operators with list](#the-in-and-not-in-operators-with-list)
    - [The upper(), lower(), isupper(), and islower() String Methods](#the-upper-lower-isupper-and-islower-string-methods)\
    - [Formatted String Literals or f-strings (Python 3.6+)](#formatted-string-literals-or-f-strings-python-36)



## Python Basics

### Symbols and terminology

| symbol| Name         | symbol | Name        |
| ----- | ------------ | ------ | ----------- |
| ‘     |Single Quote  | \      | Backslash   |
| “     |Double Quote  | >      | Greater     |
| !     |Exclamation   | <      | Less        |
| #     |Hash          | :      | Colon       |
| ()    |Parentheses   | ;      | Semi Colon  |
| []    |Square bracket| {}     | curly braket|
| *     |Asterisk      | .      | Dot         |
| /     |Slash         |,       | Comma       |

**Parentheses** () are used to assign code including strings, numbers, variables etc to a particular function
```python
print("this string belongs to the print function")
int(input("this string belongs to the input function, the input function belongs to the int function")) 
# notice the 2 closing parenthesis                                                                   ^
```
**quotation marks** "" or '' are used to enclose strings either double or single quotation marks can be used so long as the same are used on either side
```python
print('I can use single or double quotes')
print("I'm going to use double quotes here because the single is used as an apostrophe')
```
**comma** , is used to seperate arguments to a function
```python
range(5)
range (3, 8)
range (3, 8, 2)
```
The range function can take one, two or, three arguements
**white space**
For the most part spaces in your code do not matter you will notice above in the range command the first command had no space between range the parenthesis but the rest do
There are only a few occasions it really matters if you include a space in your code or not and I will cover when that is the case

### Math Operators

From **Highest** to **Lowest** precedence:

| Operators | Operation         | Example         |
| --------- | ----------------- | --------------- |
| /         | Division          | `22 / 8 = 2.75` |
| \*        | Multiplication    | `3 * 3 = 9`     |
| -         | Subtraction       | `5 - 2 = 3`     |
| +         | Addition          | `2 + 2 = 4`     |

Examples of expressions in the interactive shell:

```python
>>> 2 + 3 * 6
20
```

```python
>>> (2 + 3) * 6
30
```


```python
>>> (5 - 1) * ((7 + 1) / (3 - 1))
16.0
```

[_Return to the Top_](#python-cheatsheet)

### Data Types

| Data Type              | Examples                                  |
| ---------------------- | ----------------------------------------- |
| Integers               | `-2, -1, 0, 1, 2, 3, 4, 5`                |
| Floating-point numbers | `-1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25` |
| Strings                | `'a', 'aa', 'aaa', 'Hello!', '11 cats'`   |

[_Return to the Top_](#python-cheatsheet)

### String Concatenation and Replication

String concatenation:

```python
>>> 'Alice' + 'Bob'
'AliceBob'
```

Note: Avoid `+` operator for string concatenation. Prefer [fStrings](#formatted-string-literals-or-f-strings-python-36) except in some instances.

String Replication:

```python
>>> 'Alice' * 5
'AliceAliceAliceAliceAlice'
```

[_Return to the Top_](#python-cheatsheet)

### Variables

You can name a variable anything as long as it obeys the following rules:

1. It can be only one word.
1. It can use only letters, numbers, and the underscore (`_`) character.
1. It can’t begin with a number.
1. Variable name starting with an underscore (`_`) are considered as "unuseful`.

Example:

```python
>>> spam = 'Hello'
>>> spam
'Hello'
```

```python
>>> _spam = 'Hello'
```

`_spam` should not be used again in the code.
### camelCase
Is used to join multiple words together without spaces or _ and make it readable
Example:
```python
>>> firstName = 'John'
>>> lastName = 'Smith'
```

[_Return to the Top_](#python-cheatsheet)

### Comments

Inline comment:

```python
# This is a comment
```

Multiline comment:

```Python
# This is a
# multiline comment
```

Code with a comment:

```python
a = 1  # initialization
```

Please note the two spaces in front of the comment.

Docstring:
Using 3 quotation marks you can define a multiple line comment or Docstring
Start and end the docstring with 3 quotation marks of the same type

```python

"""
This is a function docstring
With multiple
lines
"""
''' you can also
    put your quotation
    marks at the start and end of a line '''
```

[_Return to the Top_](#python-cheatsheet)

### The print() Function

```python
>>> print('Hello world!')
Hello world!
```

```python
>>> a = 1
>>> print(f'Hello world! {a}')
Hello world! 1
```

[_Return to the Top_](#python-cheatsheet)

### The input() Function

Example Code:

```python
>>> print('What is your name?')   # ask for their name
>>> myName = input()
>>> print(f'It is good to meet you, {myName})
What is your name?
Al
It is good to meet you, Al
```

[_Return to the Top_](#python-cheatsheet)

### The len() Function

Evaluates to the integer value of the number of characters in a string:

```python
>>> len('hello')
5
```

Note: test of emptiness of strings, lists, dictionary, etc, should **not** use len, but prefer direct
boolean evaluation.

```python
>>> a = [1, 2, 3]
>>> if a:
>>>     print("the list is not empty!")
```

[_Return to the Top_](#python-cheatsheet)

### The str(), int(), and float() Functions

Integer to String or Float:

```python
>>> str(29)
'29'
```

```python
>>> print('I am '+ str(29) +'  years old.')
I am 29 years old.
```
You can also use [fstrings](#formatted-string-literals-or-f-strings-python-36) to do this without the str command

```python
>>> str(-3.14)
'-3.14'
```

Float to Integer:

```python
>>> int(7.7)
7
```

```python
>>> int(7.7) + 1
8
```

[_Return to the Top_](#python-cheatsheet)

## Flow Control

### Comparison Operators

| Operator | Meaning                  |
| -------- | ------------------------ |
| `==`     | Equal to                 |
| `!=`     | Not equal to             |
| `<`      | Less than                |
| `>`      | Greater Than             |
| `<=`     | Less than or Equal to    |
| `>=`     | Greater than or Equal to |

These operators evaluate to True or False depending on the values you give them.

Examples:

```python
>>> 42 == 42
True
```

```python
>>> 40 == 42
False
```

```python
>>> 'hello' == 'hello'
True
```

```python
>>> 'hello' == 'Hello'
False
```

```python
>>> 'dog' != 'cat'
True
```

```python
>>> 42 == 42.0
True
```

```python
>>> 42 == '42'
False
```

### Boolean Operators

There are three Boolean operators: and, or, and not.

The _and_ Operator’s _Truth_ Table:

| Expression        | Evaluates to |
| ----------------- | ------------ |
| `True and True`   | `True`       |
| `True and False`  | `False`      |
| `False and True`  | `False`      |
| `False and False` | `False`      |

The _or_ Operator’s _Truth_ Table:

| Expression       | Evaluates to |
| ---------------- | ------------ |
| `True or True`   | `True`       |
| `True or False`  | `True`       |
| `False or True`  | `True`       |
| `False or False` | `False`      |

The _not_ Operator’s _Truth_ Table:

| Expression  | Evaluates to |
| ----------- | ------------ |
| `not True`  | `False`      |
| `not False` | `True`       |

[_Return to the Top_](#python-cheatsheet)

### Mixing Boolean and Comparison Operators

```python
>>> (4 < 5) and (5 < 6)
True
```

```python
>>> (4 < 5) and (9 < 6)
False
```

```python
>>> (1 == 2) or (2 == 2)
True
```

You can also use multiple Boolean operators in an expression, along with the comparison operators:

```python
>>> 2 + 2 == 4 and not 2 + 2 == 5 and 2 * 2 == 2 + 2
True
```

[_Return to the Top_](#python-cheatsheet)
### Indentation and Code Blocks

When using the python keywords [if](#if-statements), [else](#else-statements) [elif](#elif-statements), [for](#for-loops-and-the-range-function), [while](#while-loop-statements), [def](#functions), and you need to end the line with a :
You then need to indent the lines of code you want to belong to that statement using the tab key or multiple spaces (tab is prefered)

```python
if this == that:
  this line belongs to the if statement (line 1)
  so does this line (line 2)
this line does not (line 3)
```
What this means as we will see in the next section if this equals that line 1 and line 2 will run
Line 3 will run regardless if this equals that

Any time you see a : followed by indented lines it means anything that is indented belongs to the statement with the :


### if Statements

```python
if name == 'Alice':
    print('Hi, Alice.')
```

[_Return to the Top_](#python-cheatsheet)

### else Statements

```python
name = 'Bob'
if name == 'Alice':
    print('Hi, Alice.')
else:
    print('Hello, stranger.')
```

[_Return to the Top_](#python-cheatsheet)

### elif Statements

```python
name = 'Bob'
age = 5
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
```

```python
name = 'Bob'
age = 30
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
else:
    print('You are neither Alice nor a little kid.')
```

[_Return to the Top_](#python-cheatsheet)

### while Loop Statements

```python
spam = 0
while spam < 5:
    print('Hello, world.')
    spam = spam + 1
```

[_Return to the Top_](#python-cheatsheet)

### break Statements

If the execution reaches a break statement, it immediately exits the while loop’s clause:

```python
while True:
    print('Please type your name.')
    name = input()
    if name == 'your name':
        break
print('Thank you!')
```

[_Return to the Top_](#python-cheatsheet)

### continue Statements

When the program execution reaches a continue statement, the program execution immediately jumps back to the start of the loop.

```python
while True:
    print('Who are you?')
    name = input()
    if name != 'Joe':
        continue
    print('Hello, Joe. What is the password? (It is a fish.)')
    password = input()
    if password == 'swordfish':
        break
print('Access granted.')
```

[_Return to the Top_](#python-cheatsheet)

### for Loops and the range() Function

```python
>>> print('My name is')
>>> for i in range(5):
>>>     print(f'Jimmy Five Times ({i})')
My name is
Jimmy Five Times (0)
Jimmy Five Times (1)
Jimmy Five Times (2)
Jimmy Five Times (3)
Jimmy Five Times (4)
```

The _range()_ function can also be called with three arguments. The first two arguments will be the start and stop values, and the third will be the step argument. The step is the amount that the variable is increased by after each iteration.

```python
>>> for i in range(0, 10, 2):
>>>    print(i)
0
2
4
6
8
```

You can even use a negative number for the step argument to make the for loop count down instead of up.

```python
>>> for i in range(5, -1, -1):
>>>     print(i)
5
4
3
2
1
0
```

### For else statement

This allows to specify a statement to execute in case of the full loop has been executed. Only
useful when a `break` condition can occur in the loop:

```python
>>> for i in [1, 2, 3, 4, 5]:
>>>    if i == 3:
>>>        break
>>> else:
>>>    print("only executed when no item of the list is equal to 3")
```

[_Return to the Top_](#python-cheatsheet)

### Importing Modules

```python
import random
for i in range(5):
    print(random.randint(1, 10))
```

```python
import random, sys, os, math
```

```python
from random import *
```

[_Return to the Top_](#python-cheatsheet)

### Ending a Program Early with sys.exit()

```python
import sys

while True:
    print('Type exit to exit.')
    response = input()
    if response == 'exit':
        sys.exit()
    print(f'You typed {response}.')
```

[_Return to the Top_](#python-cheatsheet)

## Functions

```python
>>> def hello(name):
>>>     print(f'Hello {name}')
>>>
>>> hello('Alice')
>>> hello('Bob')
Hello Alice
Hello Bob
```

[_Return to the Top_](#python-cheatsheet)

### Return Values and return Statements

When creating a function using the def statement, you can specify what the return value should be with a return statement. A return statement consists of the following:

- The return keyword.

- The value or expression that the function should return.

```python
import random
def getAnswer(answerNumber):
    if answerNumber == 1:
        return 'It is certain'
    elif answerNumber == 2:
        return 'It is decidedly so'
    elif answerNumber == 3:
        return 'Yes'
    elif answerNumber == 4:
        return 'Reply hazy try again'
    elif answerNumber == 5:
        return 'Ask again later'
    elif answerNumber == 6:
        return 'Concentrate and ask again'
    elif answerNumber == 7:
        return 'My reply is no'
    elif answerNumber == 8:
        return 'Outlook not so good'
    elif answerNumber == 9:
        return 'Very doubtful'

r = random.randint(1, 9)
fortune = getAnswer(r)
print(fortune)
```

[_Return to the Top_](#python-cheatsheet)



[_Return to the Top_](#python-cheatsheet)

### Local and Global Scope

- Code in the global scope cannot use any local variables.

- However, a local scope can access global variables.

- Code in a function’s local scope cannot use variables in any other local scope.

- You can use the same name for different variables if they are in different scopes. That is, there can be a local variable named spam and a global variable also named spam.

[_Return to the Top_](#python-cheatsheet)

### The global Statement

If you need to modify a global variable from within a function, use the global statement:

```python
>>> def spam():
>>>     global eggs
>>>     eggs = 'spam'
>>>
>>> eggs = 'global'
>>> spam()
>>> print(eggs)
spam
```

There are four rules to tell whether a variable is in a local scope or global scope:

1. If a variable is being used in the global scope (that is, outside of all functions), then it is always a global variable.

1. If there is a global statement for that variable in a function, it is a global variable.

1. Otherwise, if the variable is used in an assignment statement in the function, it is a local variable.

1. But if the variable is not used in an assignment statement, it is a global variable.

[_Return to the Top_](#python-cheatsheet)

## Exception Handling

### Basic exception handling

```python
>>> def spam(divideBy):
>>>     try:
>>>         return 42 / divideBy
>>>     except ZeroDivisionError as e:
>>>         print(f'Error: Invalid argument: {e}')
>>>
>>> print(spam(2))
>>> print(spam(12))
>>> print(spam(0))
>>> print(spam(1))
21.0
3.5
Error: Invalid argument: division by zero
None
42.0
```

[_Return to the Top_](#python-cheatsheet)

### Final code in exception handling

Code inside the `finally` section is always executed, no matter if an exception has been raised or
not, and even if an exception is not caught.

```python
>>> def spam(divideBy):
>>>     try:
>>>         return 42 / divideBy
>>>     except ZeroDivisionError as e:
>>>         print(f'Error: Invalid argument: {e}')
>>>     finally:
>>>         print("-- division finished --")
>>> print(spam(2))
-- division finished --
21.0
>>> print(spam(12))
-- division finished --
3.5
>>> print(spam(0))
Error: Invalid Argument division by zero
-- division finished --
None
>>> print(spam(1))
-- division finished --
42.0
```

[_Return to the Top_](#python-cheatsheet)

## Lists

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam
['cat', 'bat', 'rat', 'elephant']
```

[_Return to the Top_](#python-cheatsheet)

### Getting Individual Values in a List with Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[0]
'cat'
```

```python
>>> spam[1]
'bat'
```

```python
>>> spam[2]
'rat'
```

```python
>>> spam[3]
'elephant'
```

[_Return to the Top_](#python-cheatsheet)

### Negative Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[-1]
'elephant'
```

```python
>>> spam[-3]
'bat'
```

```python
>>> f'The {spam[-1]} is afraid of the {spam[-3]}.')
'The elephant is afraid of the bat.'
```

[_Return to the Top_](#python-cheatsheet)

### Getting Sublists with Slices

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[0:4]
['cat', 'bat', 'rat', 'elephant']
```

```python
>>> spam[1:3]
['bat', 'rat']
```

```python
>>> spam[0:-1]
['cat', 'bat', 'rat']
```

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[:2]
['cat', 'bat']
```

```python
>>> spam[1:]
['bat', 'rat', 'elephant']
```

Slicing the complete list will perform a copy:

```python
>>> spam2 = spam[:]
['cat', 'bat', 'rat', 'elephant']
>>> spam.append('dog')
>>> spam
['cat', 'bat', 'rat', 'elephant', 'dog']
>>> spam2
['cat', 'bat', 'rat', 'elephant']
```

[_Return to the Top_](#python-cheatsheet)

### Getting a List’s Length with len()

```python
>>> spam = ['cat', 'dog', 'moose']
>>> len(spam)
3
```

[_Return to the Top_](#python-cheatsheet)

### Changing Values in a List with Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[1] = 'aardvark'

>>> spam
['cat', 'aardvark', 'rat', 'elephant']

>>> spam[2] = spam[1]

>>> spam
['cat', 'aardvark', 'aardvark', 'elephant']

>>> spam[-1] = 12345

>>> spam
['cat', 'aardvark', 'aardvark', 12345]
```

[_Return to the Top_](#python-cheatsheet)



### Using for Loops with Lists

```python
>>> supplies = ['pens', 'staplers', 'flame-throwers', 'binders']
>>> for i, supply in enumerate(supplies):
>>>     print(f'Index {i} in supplies is: {supply}')
Index 0 in supplies is: pens
Index 1 in supplies is: staplers
Index 2 in supplies is: flame-throwers
Index 3 in supplies is: binders
```

[_Return to the Top_](#python-cheatsheet)

### The in and not in Operators

```python
>>> 'howdy' in ['hello', 'hi', 'howdy', 'heyas']
True
```

```python
>>> spam = ['hello', 'hi', 'howdy', 'heyas']
>>> 'cat' in spam
False
```

```python
>>> 'howdy' not in spam
False
```

```python
>>> 'cat' not in spam
True
```

[_Return to the Top_](#python-cheatsheet)



### Augmented Assignment Operators

| Operator    | Equivalent        |
| ----------- | ----------------- |
| `spam += 1` | `spam = spam + 1` |
| `spam -= 1` | `spam = spam - 1` |
| `spam *= 1` | `spam = spam * 1` |
| `spam /= 1` | `spam = spam / 1` |
| `spam %= 1` | `spam = spam % 1` |

Examples:

```python
>>> spam = 'Hello'
>>> spam += ' world!'
>>> spam
'Hello world!'

>>> bacon = ['Zophie']
>>> bacon *= 3
>>> bacon
['Zophie', 'Zophie', 'Zophie']
```

[_Return to the Top_](#python-cheatsheet)

### Finding a Value in a List with the index() Method

```python
>>> spam = ['Zophie', 'Pooka', 'Fat-tail', 'Pooka']

>>> spam.index('Pooka')
1
```

[_Return to the Top_](#python-cheatsheet)

### Adding Values to Lists with the append() and insert() Methods

**append()**:

```python
>>> spam = ['cat', 'dog', 'bat']

>>> spam.append('moose')

>>> spam
['cat', 'dog', 'bat', 'moose']
```

**insert()**:

```python
>>> spam = ['cat', 'dog', 'bat']

>>> spam.insert(1, 'chicken')

>>> spam
['cat', 'chicken', 'dog', 'bat']
```

[_Return to the Top_](#python-cheatsheet)

### Removing Values from Lists with remove()

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam.remove('bat')

>>> spam
['cat', 'rat', 'elephant']
```

If the value appears multiple times in the list, only the first instance of the value will be removed.

[_Return to the Top_](#python-cheatsheet)

### Removing Values from Lists with pop()

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam.pop()
'elephant'

>>> spam
['cat', 'bat', 'rat']

>>> spam.pop(0)
'cat'

>>> spam
['bat', 'rat']
```

[_Return to the Top_](#python-cheatsheet)

### Sorting the Values in a List with the sort() Method

```python
>>> spam = [2, 5, 3.14, 1, -7]
>>> spam.sort()
>>> spam
[-7, 1, 2, 3.14, 5]
```

```python
>>> spam = ['ants', 'cats', 'dogs', 'badgers', 'elephants']
>>> spam.sort()
>>> spam
['ants', 'badgers', 'cats', 'dogs', 'elephants']
```

You can also pass True for the reverse keyword argument to have sort() sort the values in reverse order:

```python
>>> spam.sort(reverse=True)
>>> spam
['elephants', 'dogs', 'cats', 'badgers', 'ants']
```

If you need to sort the values in regular alphabetical order, pass str. lower for the key keyword argument in the sort() method call:

```python
>>> spam = ['a', 'z', 'A', 'Z']
>>> spam.sort(key=str.lower)
>>> spam
['a', 'A', 'z', 'Z']
```

You can use the built-in function `sorted` to return a new list:

```python
>>> spam = ['ants', 'cats', 'dogs', 'badgers', 'elephants']
>>> sorted(spam)
['ants', 'badgers', 'cats', 'dogs', 'elephants']
```

[_Return to the Top_](#python-cheatsheet)



### Multiline Strings with Triple Quotes

```python
>>> print('''Dear Alice,
>>>
>>> Eve's cat has been arrested for catnapping, cat burglary, and extortion.
>>>
>>> Sincerely,
>>> Bob''')
Dear Alice,

Eve's cat has been arrested for catnapping, cat burglary, and extortion.

Sincerely,
Bob
```

### Indexing and Slicing Strings

    H   e   l   l   o       w   o   r   l   d    !
    0   1   2   3   4   5   6   7   8   9   10   11

```python
>>> spam = 'Hello world!'

>>> spam[0]
'H'
```

```python
>>> spam[4]
'o'
```

```python
>>> spam[-1]
'!'
```

Slicing:

```python

>>> spam[0:5]
'Hello'
```

```python
>>> spam[:5]
'Hello'
```

```python
>>> spam[6:]
'world!'
```

```python
>>> spam[6:-1]
'world'
```

```python
>>> spam[:-1]
'Hello world'
```

```python
>>> spam[::-1]
'!dlrow olleH'
```

```python
>>> spam = 'Hello world!'
>>> fizz = spam[0:5]
>>> fizz
'Hello'
```

[_Return to the Top_](#python-cheatsheet)



### The in and not in Operators with list

```python
>>> a = [1, 2, 3, 4]
>>> 5 in a
False
```

```python
>>> 2 in a
True
```

[_Return to the Top_](#python-cheatsheet)

### The upper(), lower(), isupper(), and islower() String Methods

`upper()` and `lower()`:

```python
>>> spam = 'Hello world!'
>>> spam = spam.upper()
>>> spam
'HELLO WORLD!'
```

```python
>>> spam = spam.lower()
>>> spam
'hello world!'
```

```python
>>> firstName = "john"
>>> firstName.capatilize()
'John'
```

isupper() and islower():

```python
>>> spam = 'Hello world!'
>>> spam.islower()
False
```

```python
>>> spam.isupper()
False
```

```python
>>> 'HELLO'.isupper()
True
```

```python
>>> 'abc12345'.islower()
True
```

```python
>>> '12345'.islower()
False
```

```python
>>> '12345'.isupper()
False
```

[_Return to the Top_](#python-cheatsheet)


### Formatted String Literals or f-strings (Python 3.6+)

```python
>>> name = 'Elizabeth'
>>> print (f'Hello {name}!')
'Hello Elizabeth!
```

It is even possible to do inline arithmetic with it:

```python
>>> a = 5
>>> b = 10
>>> f'Five plus ten is {a + b} and not {2 * (a + b)}.'
print ('Five plus ten is 15 and not 30.')
```
**fstings are one place where a space does matter you cannot put a space between the f and the quotation marks**

[_Return to the Top_](#python-cheatsheet)



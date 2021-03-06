# python-examples
Examples for people who want to learn Python

These are designed to be typed into a Python interpreter. These should be simple enough to be useful, but no simpler.

Topics to cover:

- [Topics](#topics)
  - [Output](#output)
  - [Variables](#variables)
  - [Input](#input)
  - [Primitive Data Types (`bool`, `int`, `float`, `string`)](#primitive-data-types)
  - [Type Conversion](#type-conversion)
  - [Collections 1 (`list` and `tuple`)](#collections-1-tuple-and-list)
    - [Tuples](#tuples)
    - [Lists](#lists)
  - [Collections 2 (`set` and `dictionary`)](#collections-2-set-and-dictionary)
    - [Sets](#sets)
    - [Dictionaries](#dictionaries)
  - [Conditionals / Control Flow Basics](#conditionals--control-flow-basics)
  - [Looping Basics](#looping-basics)
  - [TBD](#tbd)


## Output

```python
# Lines that begin with a '#' are called comments
# They're ignored by Python and used for documentation

# This line prints "hello"
print("hello")

print(1234)

```


## Variables

```python
foo = 1234  # Create a variable called foo whose value is 1234

print(foo)

name = "hello"  # Create a variable called name

print(name)

```

## Input

```python
number = input("Please enter a number: ")
print(number)

name = input("What is your name? ")
print("hello " + name)
```


## Primitive Data Types

```python
# Boolean (True/False) values
print(True)

print(False)

is_hungry = True

print(is_hungry)

# Toggle between True/False using 'not'
is_hungry = not is_hungry

print(is_hungry)


# Integers

print(1 + 1)  # Addition

print(999)  # Other numbers

print(1e4)  # Scientific notation 1e4 is 1000

print(1_000_000)  # Python ignores _ in numbers

print(-42)  # Negative Numbers

print(12 - 2)  # Subtraction

print(12 * 2)  # Multiplication

print(12 // 2)  # Integer division, converts result to int


# Floats aka Floating Point Numbers

print(3.14159)  # Approximation of pi

print(1/3)  # Converts a rational number into imprecise "float" value

print(12 / 2)  # Regular division, converts to float

print(13 / 2)  # Regular division

print(round(2.3))  # Round a number from float to int

print(round(2.7))  # Round another number from float to int


# Strings

language = "python"

print(language)

letters = "abcd1234"

print(letters)

number_string = "1234"

print(number_string)
```


## Type Conversion

If we want to add values of different types together, we usually need to convert them to the same type (except with int and float).
```python
type(23)

type(3.14)

type(True)

type(-12.4)

type("hello")

type("a")


# Convert from float to int
number = int(3.14)
type(number)

# Convert from int to float
number = float(3)
type(number)

# Convert from string to int
number = int("1234")
type(number)

# Convert from string to float
number = float("12.345")
type(number)

# Convert from bool to string
value = str(True)
type(value)

# Convert from string to bool
value = bool('False')

# Convert from int to bool
bool(0)
bool(1)
bool(5)
bool(-2)

# Convert from float to bool
bool(0.0)
bool(0.1)
bool(-0.0)

# Weird behaviour:
1234 + True  # gives 1235 because "True" is 1 internally.
1234 + 5*True  # gives 1239
1234 - True  # gives 1233
1234 / False  # gives ZeroDivisionError

```

## Collections 1 (tuple and list)

### Tuples

```python
# A tuple is a read-only data structure for storing collections that
# don't need to be changed. You create one using ( and ) characters.

# Create a tuple with ( and )
my_tuple = (1, 2, "hello", 3.14, False, "hello")

print(type(my_tuple))

# Access an item by index using [ and ]. Indexes start at 0
print(my_tuple[0])

print(my_tuple[3])

print(my_tuple[10])  # IndexError.

# Access a container from right-to-left
print(my_tuple[-1])
print(my_tuple[-3])

# Count number of items in a tuple
my_tuple.count("hello")
my_tuple.count(3.14)
my_tuple.count("blahblah")

# Search and get the index of an item
my_tuple.index("hello")

my_tuple.index(3.14)
my_tuple.index(False)
my_tuple.index("blah")  # ValueError.


# Trying to change the value of an item in a tuple causes an error.
my_tuple[2] = "newvalue"  # TypeError.


# Warning: If creating a tuple with only 1 item, you need to use this special syntax with a comma.
my_tuple2 = (42, )
type(my_tuple2)  # is a 'tuple' type

# If you forget the comma, then Python doesn't create the tuple.
fake_tuple = (42)
type(fake_tuple)  # is an 'int' type
```

### Lists

```python
# Unlike arrays in most other languages, Python lists can store data of any type.

# Create a list with [ and ]
my_list = [1, 2, "this is a list", 4.56, True]

# Lists have the following methods:
# append, clear, copy, count, extend, index, insert, pop, remove, reverse, sort

# Accessing an item in a list using index, same as tuples.
my_list[2]  # displays "this is a list"

# Appending an item (only 1 item can be appended at a time).
my_list.append(123)  # Appends 123 on to the end of the list.

# Insert an item at a particular index.
my_list.insert(0, 'hello')  # inserts 'hello' at the beginning (index 0) of list.
my_list.insert(2, 'blahblah')  # inserts 'blahblah' at index 2.

# "pop" an item from a list, which accesses an item and removes it.
# defaults to end of list if no index is given as an argument.
my_list.pop()  # removes last item from the list
my_list.pop(2)  # gets and removes item at index 2

# "remove" differs from pop. pop uses an index. remove searches for the value and removes the first instance of it.
my_list.remove("hello")  # searches for "hello" and removes 1st instance if found.

# Reverse the list (changes the actual list "in place").
my_list.reverse()

# Sort the list in ascending order. Advanced sorting can control how it's
sorted.
my_list.sort()

# Copy the list. Returns a "shallow copy". Read more about what this means
later.
my_list2 = my_list.copy()

# Count the number of occurrences of a value.
my_list.count("hello")

# Extend the list, aka add multiple items at a time.
my_list.extend(["x", 102, False])

# Return the first index of a value. (without changing the list)
my_list.index("hello")  # You can also tell it where to start/stop searching.

# Clear the list.
my_list.clear()
```


## Collections 2 (set and dictionary)
=======

### Sets

```python
# A set is an unordered collection of things without duplicates.
# Python will automatically remove duplicates from a set.
# Important methods you can use on sets are: add, difference,
# intersection, union. Run help(set) for others.

# Create two sets
set_a = {'Apple', 'Banana', 'Carrot', 'Banana'}  # duplicate gets removed
set_b = {'Carrot', 'Date', 'Elderberry'}

# Add an item
set_b.add('Hamster')

# Remove an item
set_b.remove('Date')

# Perform a "union" operation on the sets, aka join them together and return a new set.
set_a.union(set_b)

# Perform an "intersection" operation, aka return the set of items in both sets.
set_a.intersection(set_b)

# Perform a "set difference" operation on the two sets. (objects in set A but not set B)
set_a.difference(set_b)

# Objects only in one or the other, but not both.
set_a.symmetric_difference(set_b)

# See help(set) for more methods. These are the most common ones though.

# You can also perform these operations on multiple sets at a time using operators.
set_c = {'Banana', 'Elderberry', 'Plum'}

# & is intersection. Items only in all sets.
set_a & set_b & set_c

# | is union. Join all sets together.
set_a | set_b | set_c

# - is difference (not-symmetric). Items in A but not others.
set_a - set_b - set_c

# ^ is symmetric difference. Items unique to each set but not overlapping.
set_a ^ set_b ^ set_c
```

### Dictionaries

```python
# Dictionaries are a key-value object in Python.
# Like sets, you create them using { and }, but unlike sets, they must be
# created as key-value pairs using the : symbol.
# The values used can be any object.
my_dictionary = {'banana': '$10.00', 'cheese': True}

# Access items like with lists, except keys are usually strings.
my_dictionary['banana']  # returns the string '$10.00'
my_dictionary['cheese']  # returns True

# If accessing a key that doesn't exist using [ ], Python raises a KeyError.
# e.g. my_dictionary['optimus'] will raise a KeyError.

# Adding new items.
my_dictionary['optimus'] = 'Truck'

# Changing existing items.
my_dictionary['cheese'] = False

# Get all the keys. (used for looping/iterating later on)
my_dictionary.keys()

# Get all the values.
my_dictionary.values()

# Get all the items (key-value pairs)
my_dictionary.items()

# See help(dict) for other methods.
```

## Conditionals / Control Flow Basics

Often you want your program to do different things based on user input.
You do this with the `if` and `else` keywords.

```python
magic_word = input('Please enter the magic word: ')
if magic_word == 'Ni!':
  print('We are the knights who say Ni!')
else:
  print('Bring me a shrubbery!')
```


## Looping Basics
Now you know how to use collections in Python.
The next thing to do is learn how to loop and iterate through collections.

A while loop will continue running and looping until its conditional
(called the *loop invariant*) is false.

```python
# The easiest possible loop is an "infinite loop".
# Press Ctrl-C to stop it.
while True:
  print('looping')
```

A loop will automatically end when its loop invariant is no longer true.
```python
number = 1
while number < 100:
  print(number)
  number = number + 1
```

If you want to **break** out of a loop early, you can use the `break`
keyword.
```python
number = 1
while True:
  print(number)
  number = number + 1
  if number >= 20:
    break
```

You can also tell the loop to **continue** using the `continue` keyword.

```python
# Skip printing all numbers between 10 and 40
number = 1
while number <= 50:
  number = number + 1
  if 10 < number < 40:
    print('skipping')
    continue  # continue from next iteration of the loop

  print(number)
```

The alternative to `while` loops are `for` loops. They're usually used
for looping through collections, and there are a few ways to use them.

```python
my_list = [1, 2, 'hello', 4]

# How does Python know what 'something' is?
# Try a different name instead of 'something' here.
# Any name will work. It gets reassigned on each iteration.

for something in my_list:
  print(something)
```

Next is the `range` function which returns a range of numbers.
(called a `range object`)
The letter `i` is usually used when looping through numbers.
It's just a convention though.

```python
for i in range(1, 10):
  print(i)
```

These are the basics of looping. We'll cover more later. For now this will
allow you to create programs that ask for input until some correct value
is entered.

```python
# Exercise: Create a program that runs forever until the user enters
a correct word.
# Hint: use input(), a while loop, and an if statement.
```



### TBD

```python
while
for / in
range()
break / continue
pass
match
enumerate()
List Comprehensions

```

* Conditionals (if/elif/else)
* Exceptions
* Files (and `with` keyword)
* Modules (and packages / using pip)
* Python Modules
* Basic data structures. (stack, queue)

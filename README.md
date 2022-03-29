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
  - [Collections 1 (`list` and `tuple`)](#collections-1)
  - [Collections 2 (`set` and `dictionary`)](#collections-2)
  - [TBD](#tbd)


### Output

```python
# Lines that begin with a '#' are called comments
# They're ignored by Python and used for documentation

# This line prints "hello"
print("hello")

print(1234)

print("hello " + 1234)

```


### Variables

```python
foo = 1234

print(foo)

name = "hello"

print(name)

test = name + foo

print(test)
```

### Input

```python
number = input("Please enter a number: ")
print(number)

name = input("What is your name? ")
print("hello " + name)
```


### Primitive Data Types

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


### Type Conversion


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
```

### Collections 1 (tuple and list)

Tuples.

```python
# A tuple is a read-only data structure for storing collections that
# don't need to be changed. You create one using ( and ) characters.

# Create a tuple
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
```

Lists.

Coming soon.


### TBD

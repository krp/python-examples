# python-examples
Examples for people who want to learn Python

These are designed to be typed into a Python interpreter. These should be simple enough to be useful, but no simpler.

Topics to cover:

* 00 - Output
* 01 - Variables
* 02 - Input
* 03 - Primitive Data Types (`bool`, `int`, `float`, `string`)
* 04 - Type conversion
* 05 - Collections 1 (`list` and `tuple`)
* 06 - Collections 2 (`set` and `dictionary`)
* 07 - TBD


### 00 - Output

```python
# Lines that begin with a '#' are called comments
# They're ignored by Python and used for documentation

# This line prints "hello"
print("hello")

print(1234)

print("hello " + 1234)

```


### 01 - Variables

```python
foo = 1234

print(foo)

name = "hello"

print(name)

test = name + foo

print(test)
```

### 02 - Input

```python
number = input("Please enter a number: ")
print(number)

name = input("What is your name? ")
print("hello " + name)
```


### 03 - Primitive Data Types

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


----------------------------------------------------------------
# Day 2

* Python Basics
    * Common Data Types 
    * Simple Operators in Python
    * Assignment Operators
* Scalar Data Types 
* Declaring Variables
    * Variable Naming Syntax
* Logic Operators	
* Control Flow
* Homework

----------------------------------------------------------------
# Numeric Data Types 
* A data type can be thought of as a form in which a piece of data can exist
    * `int`   :  whole numbers
    * `float` :  decimal numbers
    * `bool`  :  `True` or `False`
* The `type()` function will tell you the data type:

```python
print(type(34)) # --> <class 'int'>
print(type(72.935)) # --> <class 'float'>
print(type(True)) # --> <class 'bool'>
```

----------------------------------------------------------------
# Numeric Type Encoding
* `int` and `float` datatypes are encoded differently, but are able to share operators in Python. 
    * Notice the values are considered equivalent, while the type of each data is different:

```python
print(1.0 == 1) # --> True
print(type(1.0) == type(1)) # --> False
```

----------------------------------------------------------------
# Python is a “duck-typed” language
* _"If it walks like a duck, and quacks like a duck, then it must be a duck."_
* The data type is automatically inferred
* Gives ability to share operations between data type through type inference:

```python
print(type(1)) # --> <class 'int'>
print(type(1.3)) # --> <class 'float'>
print(type(1 == 1.0)) # --> True
print(type(1 == 1.9)) # --> False> 
```

----------------------------------------------------------------
# Simple Operators in Python
* Basic Arithmetic Operators: `+`, `-`, `*`, `/`
* Floor Division: `//`
* Modulo: `%`
* Order of Operations: PEMDAS
* Exponentiate: `**`
* Casting: `int(x)`, `float(x)`

----------------------------------------------------------------
# Basic Arithmetic Operators
The basic arithmetic operators are intuitive and follow basic PEMDAS (Parentheses, Exponents, Multiplication/Division, Addition/Subtraction)

```python
print(2**2)             # --> 4
print(2 * 2)            # --> 4
print(2 / 2)            # --> 1.0
print(2 + 2)            # --> 4
print(2 - 2)            # --> 0
print((2 + 2)**(3 - 2)) # --> 4
```

----------------------------------------------------------------
# BREAKOUT (2 minutes)
* print the result of multiplying by 7 the addition of 6 and 3
* print the product of 7 times 6, squared, with 23 subtracted from the result
* print the division of the result of 4 minus 2 times 2 into twenty

----------------------------------------------------------------
# BREAKOUT Solution:
* print the result of multiplying by 7 the addition of 6 and 3

```python
print(7 * (6 + 3)) # --> 63
```

* print the product of 7 times 6, squared, with 23 subtracted from the result

```python
print((7 * 6)**2 - 23)) # --> 1741
```

* print the division of the result of 4 minus 2 times 2 into twenty

```python
print((20 / (4 - 2 * 2)) # --> Will throw an error in this interpretation
# or
print((4 - 2) * (20 / 2)) # --> 20
```

----------------------------------------------------------------
# Floor Division
`//`
* Truncates anything after the decimal,
    * gives an int if both data types are int
* `x // y`: Returns the quotient of x divided by y

```python
print(20 // 4)     # --> 5
print(100 // 102)  # --> 0
print(27 // 3)     # --> 9
print(72.6 // 3.3) # --> 21.0
print(72 // 3.3)   # --> 21.0
print(72.6 // 3)   # --> 24.0
```

----------------------------------------------------------------
# Modulo
`%`
* Returns the remainder after dividing y into x
* Wildly helpful, as it turns out
    * can check even-ness or odd-ness using `num % 2`
    * can check divisibility

```python
if num % 2 == 0: print('num is even')
if num % 2 == 1: print('num is odd')
if num % 4 == 0: print('num is divisible by 4')

print(21 % 4) # --> 1
print(20 % 4) # --> 0
print(5 % 20) # --> 5
print(6 % 20) # --> 6
```

----------------------------------------------------------------
# Modulo with `float` values
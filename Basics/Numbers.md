# Numbers in Python

### Numeric Types

Python supports the following numeric types:

- **int**: Integer values without any fractional or decimal component.
- **float**: Floating-point values with a decimal point or an exponent notation.

![alt](https://th.bing.com/th/id/OIP.t_i3btxR5fPlJtl71_UikAHaD4?rs=1&pid=ImgDetMain)

## Common Operations

### Arithmetic Operations

- **Addition**: `+` 
- **Subtraction**: `-`
- **Multiplication**: `*`
- **Division**: `/`
- **Floor Division**: `//` Returns the integer part of the quotient
- **Modulo**: `%` Returns the remainder of the division
- **Exponentiation**: `**`
```python
5 + 2 # 7
5 - 2 # 3
5 * 2 # 10
5 / 2 # 2.5
5 // 2 # 2
5 % 2 # 1
5 ** 2 # 25
```
Note - 
```python
'Sita' + 'Ram' # 'SitaRam'

'abc' + 1 # TypeError: can only concatenate str (not "int") to str

40 + 2.23 # 42.23 as python explicitly maintains the data type to be same but avoid to do so.

40 + int(2.23) # 42 rather do this.

1+1, 2+2 # -> (2, 4) - tuple
```

### Comparison Operations

- **Equal to**: `==`
- **Not equal to**: `!=`
- **Greater than**: `>`
- **Less than**: `<`
- **Greater than or equal to**: `>=`
- **Less than or equal to**: `<=`
```python
2 == 3 # False
2 != 3 # True
2 > 3 # False
2 < 3 # True
2 >= 3 # False
2 <= 3 # True
```

## Built-in Functions

Python provides several built-in functions for working with numbers:

- **`abs(x)`**: Returns the absolute value of x.
- **`pow(x, y)`** or **`x ** y`**: Returns x to the power of y.
- **`round(x, n)`**: Returns x rounded to n digits after the decimal point. If n is omitted, returns the nearest integer.
- **`max(iterable)`**: Returns the maximum value in the iterable.
- **`min(iterable)`**: Returns the minimum value in the iterable.
- **`sum(iterable)`**: Returns the sum of all elements in the iterable.
- **`divmod(x, y)`**: Returns a tuple containing the quotient and remainder of the division of x by y.
- **`hex(x)`**: Converts an integer x to a hexadecimal string.
- **`bin(x)`**: Converts an integer x to a binary string.
- **`oct(x)`**: Converts an integer x to an octal string.
- **`float(x)`**: Converts x to a floating-point number.
```python
abs(-5) # 5
pow(2, 3) # 8
round(1.1414, 2) # 1.14 
divmod(5, 2) # (2, 1) - tuple
max([1, 2, 3]) # 3
min([1, 2, 3]) # 1
sum([1, 2, 3]) # 6
oct(64) # '0o100'
hex(64) # '0x40'
bin(64) # '0b1000000'
float(2) # 2.0
int('64', 8) # 52
int('64', 16) # `00
int('100000', 2)  # 32
```

## Bitwise operations
- **AND `&`**: Returns 1 if both bits are 1, otherwise, it returns 0.
- **OR `|`**: Returns 1 if either of the bits is 1, otherwise, it returns 0.
- **XOR `^`**: Returns 1 if the bits are different, otherwise, it returns 0.
- **NOT `~`**: Flips all the bits of the integer, turning 0s into 1s and 1s into 0s.
- **Left Shift `<<`**: Each shift by 1 position is equivalent to multiplying the number by 2.
- **Right Shift `>>`**: Each shift by 1 position is equivalent to dividing the number by 2.
```python
5 & 3 # 1
5 | 3 # 7
5 ^ 3 # 6
~5 # -6
1 << 4 # 16
16 >> 2 # 4
```

## Math Module

Python's `math` module provides additional mathematical functions and constants:

- **`import math`**: Import the math module.
- **`math.sqrt(x)`**: Returns the square root of x.
- **`math.pi`**: Mathematical constant π.
```python
import math

print(math.sqrt(4)) # 2 
print(math.pi) # 3.14...
math.floor(3.5) # 3 closest below value
math.trunc(2.8) # 2 towards zero value  
```

## Random Module

Python's `random` module provides functions for generating random numbers:

- **`import random`**: Import the random module.
- **`random.random()`**: Returns a random floating-point number in the range `[0.0, 1.0)`.
- **`random.randint(a, b)`**: Returns a random integer between a and b (inclusive).
- **`random.choice(['a', 'b', 'c', 'd'])`**: Gives random from the choices.
- **`random.shuffle(user_list)`**: Shuffles the list.
```python
import random

print(random.random()) # 0.4
print(random.randint(1, 10)) # 3
print(random.choice(['a', 'b', 'c', 'd'])) # 'b'
```

## Decimal and Fraction Libraries

### Decimal Library

Provides support for decimal floating-point arithmetic.
```python
# if we simply add decimal numbers like this then it will create problem due floating-point precision errors.
0.1 + 0.1 + 0.4 # 0.6000000000000001
0.1 + 0.1 + 0.1 # 0.30000000000000004
(0.1 + 0.1 + 0.1) - 0.3 # 5.551115123125783e-17
```
So Decimal was introduced for precision, accuracy and control for such errors.
```python
from decimal import Decimal 
Decimal('0.1') + Decimal('0.1') + Decimal('0.1') - Decimal('0.3') # Decimal('0.0')
Decimal('0.1') + Decimal('0.1') + Decimal('0.1') # Decimal('0.3')
```

### Fraction Library

Provides support for rational numbers (fractions).
```python
1/3 + 2/3 # 1.0
from fractions import Fraction
x = Fraction(1, 3)
y = Fraction(2, 3)
x + y # 1
```

## Set Opetarions

- **`Union`**: `|`
- **`Intersection`**: `&`
- **`Difference`**: `-`
- **`Symmetric Difference`**: `^`
```python
set1 = { 1, 2, 3, 4, 5 }
set2 = { 1, 5 } 
set1 | set2 # {1, 2, 3, 4, 5}
set1 & set2 # {1, 5}
set1 - set2 # {2, 3, 4}
set1 ^ set2 # {2, 3, 4}

set1 = {1, 2, 3}
set2 = {3, 4, 5}
set1 ^ set2 # {1, 2, 4, 5}
set1 - {1,2,3} # will give set() and not {} bcoz type({}) is 'dict' and type(set1) is 'set'
```

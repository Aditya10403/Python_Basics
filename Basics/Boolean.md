# **Boolean in Python**

Booleans are a fundamental data type in Python used to represent truth values. They have two possible values: `True` and `False`.
- *`internally Boolean are also numbers -> 0 / 1`*
![alt](https://th.bing.com/th/id/OIP.fB2rsYEq0BNIFz2AhXeX9AHaFL?rs=1&pid=ImgDetMain)

## Boolean Operations

- **Logical AND `and`**
- **Logical OR `or`**
- **Logical NOT `not`**

```python
print(True and False) # False
print(True or False) # True
print(not True) # False
```
**`Note`** - 
```python
print(bool(0)) # False
print(bool(1)) # True

print(bool(False)) # False
print(bool(True)) # True

print(bool("")) # False
print(bool("a")) # True

print(bool([])) # False
print(bool([0])) # True

print(bool({})) # False
print(bool({1})) # True

print(bool(None)) # False
```

### `is` Operator
The is operator is used to compare the identity of two objects. It checks whether two variables refer to the same object in memory. If they do, it returns True; otherwise, it returns False.
```python
x = [1, 2, 3]
y = [1, 2, 3]

result = x is y
print(result)  # False bcoz x and y are different objects in memory

z = x
result = x is z
print(result)  # True bcoz x and z refer to the same object in memory

```

### `not` Operator
The not operator is a logical operator used to negate the value of a boolean expression. It returns True if the expression is False, and False if the expression is True.
```python
result = not True
print(result)  # False

result = not False
print(result)  # True

x = 5
y = 10

result = not x > y
print(result)  # True bcoz 5 is not greater than 10
```
**`Note`** - 
```python
# True -> 1
# False -> 0
type(True | False) # <class 'bool'>

print(True == 1) # True
print(False == 0) # True

print(True is 1) # False
print(False is 0) # False

print(True + 4) # 5
print(False + 4) # 4
```

## Comparison Operations

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

- **`bool()`**: Converts a value to its boolean equivalent.
- **`all()`**: Returns True if all elements of an iterable are True, otherwise returns False.
- **`any()`**: Returns True if any element of an iterable is True, otherwise returns False.
```python
bool(0) # False
all([True, True, False]) # False
any([True, True, False]) # True
```
# Types of Errors in Python

## Syntax Errors
Grammatical mistakes in code.
```python
print("Hello, world!)
# SyntaxError: unterminated string literal
```

## Runtime Errors (Exceptions)
Problems during execution.

```python
numerator = 10
denominator = 0
result = numerator / denominator
# ZeroDivisionError: division by zero
```

## Name Errors
Undefined variable names.

```python
print(unknown_variable)
# NameError: name 'unknown_variable' is not defined
```

## Type Errors
Incompatible data types.

```python
age = "twenty"
age_in_years = age + 5  # TypeError: can only concatenate str (not "int") to str
```

## Index Errors
Out-of-range indices.

```python
my_list = [1, 2, 3]
print(my_list[3])  # IndexError: list index out of range
```

## Value Errors
Invalid data inputs.

```python
int("hello")  # ValueError: invalid literal for int() with base 10: 'hello' 
```

## Attribute Errors
Non-existent object attributes.

```python
my_list = [1, 2, 3]
my_list.upper()  # AttributeError: 'list' object has no attribute 'upper'
```


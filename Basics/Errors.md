# Types of Errors in Python

## Syntax Errors
Grammatical mistakes in code.
```python
print("Hello, world!")
```

## Runtime Errors (Exceptions)
Problems during execution.

```python
numerator = 10
denominator = 0
result = numerator / denominator
```

## Name Errors
Undefined variable names.

```python
print(unknown_variable)
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


# **Strings in Python**

**In Python, strings are sequences of characters enclosed within single `(' ')` or double `(" ")` or `(""" """)` triple quotes. They are immutable, meaning their contents cannot be changed once defined.**

![alt](https://codelucky.com/wp-content/uploads/2023/02/Python-Strings.png)

## Contents

- **[Common Operations](#co)**
- **[String Methods](#sm)**
- **[Importing Modules for String Operations](#im)**
- **[Ordered Formatting / Printing methods](#of)**

## Common Operations {#co}

### Concatenation

Strings can be concatenated using the `+` operator:

```python
"Sita" + "Ram" # SitaRam
```

### String Slicing
Strings can be sliced using square brackets []:

```python
string = "0123456789"
string[:]     # "0123456789"
string[3:7]   # "3456"
string[:7]    # "0123456"
string[1:5:3] # "14"
```

### Containing

```python
string = "Sita Ram"
"Sita" in string # True
```

## <span id="sm">String Methods</span> 

Python provides numerous built-in methods for string manipulation:

- **`count(sub[, start[, end]])`**
```python
string = "Sita Ram"
print(string.count("a"))  # 2
```
- **`encode(encoding="utf-8", errors="strict")`**: Returns the encoded version of the string.
```python
string = "Sita Ram"
print(string.encode())  # b'Sita Ram'
```
- **`endswith`(suffix`[, start[, end]]`) and `startswith`(prefix`[, start[, end]]`)**
```python
string = "Sita Ram"
print(string.endswith("Ram"))  # True
print(string.startswith("Sita"))  # True
```
- **`find(sub[, start[, end]])`**: Returns the lowest index of substring in the string, or -1 if not found.
```python
string = "Sita Ram"
print(string.find("Ram"))  # 5
```
- **`index(sub[, start[, end]])`**: Returns the lowest index of substring in the string, or raises ValueError if not found.
```python
string = "Sita Ram"
print(string.index("Ram"))  # 5
```
- **`isalnum()`**: for alphanumeric
```python
string = "SitaRam123"
print(string.isalnum())  # True
```
- **`isalpha()`**: for alphabetic only.
```python
string = "SitaRam"
print(string.isalpha())  # True
```
- **`isdigit()`**: for digits only.
```python
string = "123"
print(string.isdigit())  # True
```
- **`islower()`**
```python
string = "sita ram"
print(string.islower())  # True
```
- **`isupper()`**: Returns True if all characters in the string are uppercase.
```python
string = "SITA RAM"
print(string.isupper())  # True
```
- **`join(iterable)`**: Concatenates elements of an iterable with the string as a separator.
```python
words = ["Sita", "Ram"]
print(" ".join(words))  # Sita Ram
```
- **`lower()` and `upper()` and `capitalize()`**
```python
string = "Sita Ram"
print(string.lower())  # sita ram
string = "sita ram"
print(string.upper())  # SITA RAM
string = "Sita Ram"
print(string.capitalize())  # Sita ram
```

- **`lstrip([chars])` and `rstrip([chars])`**: Returns a `copy` of the string with leading and trailing characters removed respectively.
```python
string = "   Sita Ram"
print(string.lstrip())  # 'Sita Ram'
string = "Sita Ram   "
print(string.rstrip())  # 'Sita Ram'
```
- **`replace(old, new[, count])`**: Returns a `copy` of the string with all occurrences of substring replaced.
```python
string = "Shiv Shankar"
print(string.replace("Shankar", "Parvati"))  # Shiv Parvati
```
- **`rfind(sub[, start[, end]])`**: Returns the highest index of substring in the string, or -1 if not found.
```python
string = "Sita Ram"
print(string.rfind("a"))  # 7
```
- **`rsplit(sep=None, maxsplit=-1)`**: Splits the string into a list of substrings from the right.
```python
string = "Sita Ram"
print(string.rsplit())  # ['Sita', 'Ram']
```
- **`split(sep=None, maxsplit=-1)`**: Splits the string into a `list` of substrings.
```python
string = "Sita Ram"
print(string.split())  # ['Sita', 'Ram']
```
- **`strip([chars])`**: Returns a `copy` of the string with leading and trailing characters removed.
```python
string = "   Sita Ram   "
print(string.strip())  # 'Sita Ram'
```
- **`swapcase()`**: Converts lowercase characters to uppercase and vice versa.
```python
string = "sITA rAM"
print(string.swapcase())  # Sita Ram
```

## <span id="im">Importing Modules for String Operations</span> 

### `string` Module

- provides a collection of string constants and helper functions:

```python
import string

print(string.ascii_letters)  # abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
print(string.digits)         # 0123456789
print(string.capwords("sita ram"))  # Sita Ram
```

### `re` Module

- used for regular expression operations, including string searching and manipulation:

```python
import re

pattern = r"\b[A-Z][a-z]*\b" # -> # Match words that start with an uppercase letter followed by zero or more lowercase letters
string = "Sita Ram"
matches = re.findall(pattern, string)
print(matches)  # ['Sita', 'Ram']
```

## <span id="of">Ordered Formatting / Printing methods</span>

- **`print(string)`**
```python
string = "Sita Ram"
print(string) # Sita Ram
```
- **`print(f"{variable}")`**
```python
name = "Ram"
print(f"Jai shri {name}!") # Jai shri Ram!
```
- **`print("{}".format(variable))`**
```python
name = "Hanuman"
print(f"Jai {name}!") # Jai Hanuman!
```
- **`print("%s" % variable)`**
```python
name = "Ram"
print("Jai shri %s!" % name) # Jai shri Ram!
```
- **`print(string, end="")`**
```python
string = "Sita "
print(string, end="")
print("Ram") # Sita Ram
```
- **`print(string, sep=",")`**
```python
strings = ["Sita", "Ram"]
print(*strings, sep=", ") # Sita, Ram
```
- **`print(string, sep=",")`**
```python
strings = ["Sita", "Ram"]
print(*strings, sep=", ") # Sita, Ram
```

### Raw Strings

***a string that is prefixed with an `r` or `R`. It is used to treat backslashes `'\'` as literal characters.***

```python
# Without raw string
path = "C:\new\test"

# With raw string
path = r"C:\new\test"
```
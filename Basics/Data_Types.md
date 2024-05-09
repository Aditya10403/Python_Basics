# Data Types / Object Types 

## Immutable and Mutable

**Immutable Objects**
- *Cannot be changed after creation.*
- *Examples: integers, strings, tuples.*

**Mutable Objects**
- *Can be changed after creation.*
- *Examples: lists, dictionaries, sets.*

## Types -
- **Number** : `1234`, `3.1415`, `3+4j`, `0b111`, `Decimal()`, `Fraction()`.
    - *Numeric values, including integers, floats, complex numbers, and others like binary numbers.*

- **String** :  `'spam'`, `"Bob's"`, `b'a\x01c'`, 
`u'sp\xc4m'`.
    - *Immutable sequence of characters, enclosed in single `('')` or double `("")` quotes.*

- **List** : `[1, [2, 'three'], 4.5]`, `list(range(10))`
    - *Mutable ordered sequence of elements, enclosed in square brackets `([])`, allows duplicates, and elements can be of different types.*

- **Tuple** : `(1, 'spam', 4, 'U')`, `tuple('spam')`, `namedtuple`
    - *Immutable ordered sequence of elements, enclosed in parentheses `(())`, allows duplicates, and elements can be of different types.*

- **Dictionary** : `{'food': 'spam', 'taste': 'yum'}`, `dict(hours=10)`
    -   *Collection of key-value pairs, enclosed in curly braces ({}), keys must be unique and immutable, values can be of any data type.*

- **Set** : `set('abc')`, `{'a', 'b', 'c'}`
    - *Unordered collection of unique elements, enclosed in curly braces `({})`, does not allow duplicates, and elements must be immutable.*

- **File** : `open('files.txt')`, `open(r'C:\users.bin', 'wb')`
    - *Represents files in the file system, opened using the `open()` function with various modes like 'r' for reading, 'w' for writing, etc.*

- **Boolean** : `True`, `False`

- **None** : `None`
    - *Represents the absence of a value or a `null` value.*

- **Functions, modules, classes**

- **Advance**: Decorators, Generators, Iterators, MetaProgramming
    - *`decorators` for modifying behavior*
    - *`generators` for lazy evaluation*
    - *`iterators` for traversing containers*
    - *`metaprogramming` techniques for manipulating code at runtime*

- **Note :**
    - *`String` is internally treated as `array`*
    - *Python treates `Numbers` and `Strings` more efficiently. e.g. late `Garbage Collection` for numbers and strings.*
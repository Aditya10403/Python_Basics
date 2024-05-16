# Lists in Python

Lists are a fundamental data structure in Python used to store collections of items. They are mutable, ordered, and allow duplicate elements. Lists are denoted by square brackets `[]` and can contain any data type, including other lists.

![alt](https://i1.faceprep.in/Companies-1/lists-in-python.png)

## Contents

- **[Functions of Lists](#fl)**
- **[Built-in Functions Related to Lists](#bf)**
- **[List Comprehension](#lc)**

## <span id="fl">Functions of Lists</span>

- **Creation**
    ```python
    my_list = [0, 1, 2, 3, 4, 5]
    ```

- **Accessing Elements**
    ```python
    first_element = my_list[0]  # 0
    ```

- **Slicing**
    ```python
    sublist = my_list[1:4]  # [1, 2, 3]
    ```

- **Appending and Extending**: using the `append()` and `extend()` method.
    ```python
    my_list = [0, 1, 2, 3, 4, 5]
    my_list.append(6)   
    print(my_list) # [0, 1, 2, 3, 4, 5, 6]
    my_list.extend([7, 8])  
    print(my_list) # [0, 1, 2, 3, 4, 5, 6, 7, 8]
    ```

- **Inserting**
    ```python
    my_list.insert(2, 10)
    print(my_list) # [0, 1, 10, 2, 3, 4, 5, 6, 7, 8]
    ```
- **Removing Elements**: using `remove()`, `pop()`, or `del` methods.
    ```python
    my_list = [0, 1, 2, 3, 4, 5]
    my_list.remove(3)  # Removes the element 3 from the list
    print(my_list)     # [0, 1, 2, 4, 5]
    popped_element = my_list.pop(4) # Removes and returns the element at index 4 -> 4
    print(my_list)     # [0, 1, 2, 4]
    del my_list[0]     # Deletes the element at index 0
    print(my_list)     # [1, 2, 4]
    ```

- **Searching**: using `index()` function.
    ```python
    my_list = [0, 1, 2, 3, 4, 5] 
    index_of_5 = my_list.index(5)  # Finds the index of the element 5 -> 5
    ```

- **Sorting**: using the `sort()` method, either in ascending or descending order.
    ```python
    my_list = [-3, 0, 3, -2, 1, -1, 2]
    my_list.sort()            # Sorts the list in ascending order
    print(my_list)            # [-3, -2, -1, 0, 1, 2, 3]
    my_list.sort(reverse=True)  # Sorts the list in descending order
    print(my_list)            # [3, 2, 1, 0, -1, -2, -3]
    ```

- **Copying Lists**: using the `copy()` method or simply `=`. 
    ```python
    new_list = my_list.copy()  # Creates a copy of my_list (Different references)
    new_list = my_list         # Assigns a reference to the original list
    ```

## <span id="bf">Built-in Functions Related to Lists</span>

Python provides several built-in functions to perform operations on lists:

- **`len()`**
    ```python
    my_list = [3, -7, 12, -5, 8, -2, 10, -6]
    length = len(my_list) # 8
    ```

- **`min()`**
    ```python
    smallest = min(my_list) # -7
    ```

- **`max()`**
    ```python
    largest = max(my_list) # 12
    ```

- **`sum()`**- works for numeric elements only.
    ```python
    total = sum(my_list) # 13
    ```

- **`sorted()`:** Returns a new sorted list from the elements of the given iterable.
    ```python
    my_list = [3, -7, 12, -5, 8, -2, 10, -6]
    sorted_list = sorted(my_list)
    print(sorted_list)      # [-7, -6, -5, -2, 3, 8, 10, 12]
    ```

- **`reversed()`:** Returns an iterator that yields items in reverse order.
    ```python
    my_list = [3, -7, 12, -5, 8, -2, 10, -6]
    reversed_list = list(reversed(my_list))
    print(reversed_list)     # [-6, 10, -2, 8, -5, 12, -7, 3]
    ```

## <span id="lc">List Comprehension</span>

List comprehension provides a concise way to create lists. It consists of an expression followed by a `for` clause, then zero or more `for` or `if` clauses. The result will be a new list resulting from evaluating the expression in the context of the `for` and `if` clauses.

For example:
```python
squared_numbers = [x**2 for x in range(10)]
print(squared_numbers)      # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
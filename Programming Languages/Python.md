# Python

Python is a high-level multi-paradigm programming language.

### Data Types
There are six fundamental data types in Python. They are:
1. Numbers `<int>, <float>, <complex>, <long>`
2. String `<str>`
3. List `<list>`
4. Dictionary `<dict>`
5. Set `<set>`
6. Tuple `<tuple>`

#### Numbers
- Numbers include integer, float, complex & long data types.

#### String
- Strings are a series of Unicode characters.
- It is similar to C++ `<string>` class.

#### List
- List is an ordered sequence of items.
- A **list**, similar to a C++ `<vector>` container, is **mutable**.

#### Dictionary
- Dictionary is an unordered collection of key-value pairs.
- It is similar to a C++ `<map>` container.

#### Set
- **Set** is an unordered collection of **unique** items.
- It is defined by values separated by comma inside curly braces.
- It is similar to a C++ `<set>` container.

#### Tuple
- Tuple is an ordered sequence of items similar to a list.
- The only difference is that **tuples** are **immutable**.
- It is similar to a C++ `<array>` container.

### Variables
Python doesn't require declaring variables with data types. Directly assign values to variables using the _assignment_ (`=`) operator.
```python
my_integer_variable = 7
my_float_variable = 1.67
my_complex_variable = 1+2j
my_bool_variable = False
my_string_variable = "A string type variable."
my_list_variable = [1, 2, 3]
my_dict_variable = {"key1": "value1", "key2": "value2"}
my_set_variable = set([1, 2, 3, 2, 1]) # {1, 2, 3}
```

### Comments
Similar to other programming languages, Python allows single line and multi-line comments.

Single line (or inline comments) start with an _hash_ (`#`) sign.
```python
# This is a single line (or inline) comment.
```

Multi-line comments start with _triple-quotation_ (`"""`) blocks.
```python
"""
This is a multi-line comment.
This is the second line of a multi-line comment.
"""
```

### Mathematical Operations
Mathematical operations can be performed in Python as follows:
```python
sum_vars = 176 + 371
diff_vars = 371 - 176
product_vars = 17 * 9
divide_vars = 18 / 9
modulo_vars = 17 % 9
```

Exponentiation in Python works with a _double-asterisks_ (`**`) operator.
```python
seventeen_squared = 17 ** 2
```

**NOTE**: Please avoid using `^` for exponentiation. `^` in Python stands for `Bitwise XOR`.

### Escaping Characters
Consider the string: `'There's a snake in my boat!'`. The apostrophe in `There's` causes Python to think that the string ends there. To fix this, use a _backslash_ (`\`). The correct way of using _backslash_ is:

```python
string = 'There\'s a snake in my boat!'
```

### `type()` Method
The `type(variable_name)` method returns the data type of the passed variable.
```python
print (type(17)) # Prints <class 'int'>
print (type("Hello World!")) # Prints <class 'str'>
```

### Integer & Float Methods
- #### Maximum: `max()`
  - Returns the largest of the values passed in the parenthesis.
```python
print (max(17, 24)) # Prints 24
```
- #### Minimum: `min()`
  - Returns the smallest of the values passed in the parenthesis.
```python
print (min(17, 24)) # Prints 17
```
- #### Absolute: `abs()`
  - Returns the absolute of the value passed in the parenthesis.
```python
print (abs(-17)) # Prints 17
```

### String Methods
- #### Length of a string: `.len()`
```python
string = "This is a string."
a = string.len()
print (a) # Prints 17.
```
Alternatively, you can directly use:
```python
a = "This is a string.".len()
print (a)
```

- #### Convert a string to lower or upper case: `.lower()` / `.upper()`
```python
a = "This is string."
b = a.lower()
c = a.upper()
print (b) # Prints "this is a string."
print (c) # prints "THIS IS A STRING."
```

- #### Alphabet Check: `.isalpha()`
Checks if the string contains all alphabets & returns False/True respectively. Even a string with spaces shall return False.
```python
"This is a string".isalpha() # False
"Thisisastring".isalpha() # True
```

- #### Explicit String Conversions: `str()`
```python
my_int = 17
my_float = 15.33
my_str = str(my_int)
my_str2 = str(my_float)
print (my_str, type(my_str)) # Prints 17 <class 'str'>
print (my_str2, type(my_str2)) # Prints 15.33 <class 'str'>
```
- #### String Concatenation: `+`
Strings can be concatenated simply using the `+` operator. To combine a string with something that isn't a string, use `str()` method.
```python
str1 = "Hello"
str2 = "World!"
str3 = str1 + " " + str2 + "!"
print (str3) # Prints Hello World!
pi = 3.14
print ("The value of Pi is: " + str(pi))
```

- #### String Formatting with `%`:
The `%` operator after a string is used to combine a string with variables. The `%` operator will replace a `%s` in the string with the string variables that comes after it.
```python
str1 = "Camelot"
str2 = "place"
print ("Let's not go to %s. 'Tis is a silly %s." % (str1, str2))
```

- #### String Slicing: `string[start:stop:stride]`
A string can be considered as a list of characters. Characters of a string can be accessed by using index. The syntax is:
```python
string_name[start_index : end_index : stride]
```
  - `start_index` is the index you need to start slicing from.
  - `end_index` is the index you need to end slicing at.
    - **NOTE**: The element at index `end_index` is not included in the sliced index. So an extra 1 should be added to include the left over element.
  - `stride` is the jump factor. If you want all the characters, stride should be 1. If you want every alternate character, stride should be 2, and so on.
    - **NOTE**: `stride` is an _optional_ parameter. If not passed explicitly, Python assumes the
    default value of `stride` equal to `1`.

  ```python
  str1 = "This is a string."
  str2 = str1[10:16] # stride is not passed.
  print (str2) # Prints "string"
  ```

### List Methods
An empty list can be declared as:
```python
empty_list = []
```

- #### Appending into list: `.append()`
An item can be added to the end of the list using the append method.
```python
empty_list = []
empty_list.append(1)
empty_list.append("Hello")
print (empty_list) # Prints [1, "Hello"]
```
- #### Searching for an item: `.index()`
Used to print the index of an element in a list. In case, the list contains repetitive elements, the index of the first occurrence of the item is returned.
```python
list1 = [1, 2, 3]
print (list1.index(2)) # Prints 1
list2 = [1, 1, 2, 2, 3]
print (list2.index(2)) # Prints 2 and doesn't print 3.
```
- #### Insert item at an index: `.insert()`
Used to insert an element at a specific index. If the list contains an element at the given index, the whole list is pushed down by 1 index & then the element is added to the list.
```python
list1 = [1, 2, 3]
list1.insert(2, 4)
print (list1) # Prints [1, 2, 4, 3]
```
- #### Removing items from a list:
  - `list_name.pop(index)`: Will remove the item at index from the list and return it to you
  - `list_name.remove(item)`: Will remove the actual item from the list if it finds it. In case of multiple occurrences, the first occurrence is removed.
  - `del(list_name[index])`: This is similar to `.pop()`, but this doesn't return the value.

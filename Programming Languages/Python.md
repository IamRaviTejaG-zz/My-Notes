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
Numbers include integer, float, complex & long data types.
#### String
Strings are a series of Unicode characters.
#### List
List is an ordered sequence of items. A **list**, similar to a C++ `<vector>` is **mutable**.
#### Dictionary
Dictionary is an unordered collection of key-value pairs. It is similar to C++'s `<map>`.
#### Set
**Set** is an unordered collection of **unique** items. It is defined by values separated by comma inside curly braces.
#### Tuple
Tuple is an ordered sequence of items same as list. The only difference is that **tuples** are **immutable**. Tuples once created cannot be modified.


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
# my_set_variable = {1, 2, 3}
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

### List Methods

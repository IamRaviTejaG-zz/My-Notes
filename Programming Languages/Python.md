# Python

Python is a high-level multi-paradigm programming language.

## Data Types
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

## Variables
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

## Comments
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

## Mathematical Operations
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

## Escaping Characters
Consider the string: `'There's a snake in my boat!'`. The apostrophe in `There's` causes Python to think that the string ends there. To fix this, use a _backslash_ (`\`). The correct way of using _backslash_ is:

```python
string = 'There\'s a snake in my boat!'
```

## `type()` Method
The `type(variable_name)` method returns the data type of the passed variable.
```python
print (type(17)) # Prints <class 'int'>
print (type("Hello World!")) # Prints <class 'str'>
```

## Integer & Float Methods
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

## String Methods
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

- #### String Slicing:
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

- #### Reversing Strings
Setting `stride` to `-1` gives you the reversed string.
```python
my_string = "Hello"
backwards = my_string[::-1]
print (backwards) # "olleH"
```

## List Methods
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

- #### List Slicing:
```python
list_name[start_index : end_index : stride]
```

  - `start_index` is the index you need to start slicing from.
  - `end_index` is the index you need to end slicing at.
    - **NOTE**: The element at index `end_index` is not included in the sliced index. So an extra 1 should be added to include the left over element.
  - `stride` is the jump factor. If you want all the characters, stride should be 1. If you want every alternate character, stride should be 2, and so on.
    - **NOTE**: `stride` is an _optional_ parameter. If not passed explicitly, Python assumes the default value of `stride` equal to `1`.

```python
list1 = [1, 2, 3, 4]
list2 = list1[0:2] # stride is not passed.
list3 = list1[::2] # only stride is passed
print (list2) # Prints [1, 2]
print (list3) # Prints [1, 3]
```

- #### Joining Lists
Use the `+` operator to join the lists.
  ```python
  list1 = [1, 2, 3]
  list2 = [4, 5, 6]
  list3 = list1 + list2
  print (list3) # [1, 2, 3, 4, 5, 6]
  ```

- #### Reversing Lists
Setting `stride` to `-1` gives you the reversed list.
```python
my_list = range(1, 11)
backwards = my_list[::-1]
print (backwards) # [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

## Dictionaries
A dictionary is similar to a list, but you access values by looking up a key instead of an index. A key can be any string or number.
```python
dict1 = {"key1": 1, "key2": 2, "key3": 3}
print (dict1['key1']) # Prints 1
print (dict1['key2']) # Prints 2
```

- #### Inserting items to dictionary:
```python
dict1 = {"key1": 1, "key2": 2, "key3": 3}
dict1['key4'] = 4 # Adds "key4": 4 to dict1
dict1['key5'] = 5 # Adds "key5": 5 to dict1
print (dict1) # Prints dict1 = {"key1": 1, "key2": 2, "key3": 3, "key4": 4, "key5": 5}
```

- #### Deleting from dictionary:
```python
del dict_name['key_name']
```

## `range()` Method
The python `range()` method is just a shortcut for generating a list, so you can use ranges in all the same places you can use lists. The range has the syntax:
```python
range(start, stop, step)
```
In all cases, the `range()` method returns a list of numbers from `start` upto `stop` (but not including `stop`). Each item increases by step.

**NOTE**: If omitted, `start` defaults to `0` and `step` defaults to `1`.

## Conditional & Control Flow
- #### Comparators
  1. Equal To (`==`)
  2. Less Than (`<`)
  3. Greater Than (`>`)
  4. Not equal to (`!=`)
  5. Less than or equal to (`<=`)
  6. Greater than or equal to (`>=`)

- #### Boolean Operators
  1. `and` checks if both statements are true.
  2. `or` checks if either of the statement is true.
  3. `not` gives the opposite of the statement.

- #### Order of precedence of Boolean Operators
`not` is evaluated first, `and` is evaluated next and `or` is evaluated at last.

- #### `if`, `elif` & `else`
    ```python
    someRandomInt = 3
    if (someRandomInt < 2): # if (condition):
      print ("someRandomInt < 2")
    # elif & else are optional statements.
    elif (someRandomInt > 2 and someRandomInt < 4): # elif (condition):
      print ("someRandomInt > 2 and someRandomInt < 4")
    else:
      print ("someRandomInt > 4")
    ```

## Loops
- #### For Loop
  ```python
  for i in range(0, 5, 1): # range(start, stop, step)
    print (i)
  # Prints 0 1 2 3 4
  ```
  ```python
  list1 = [1, 2, 3, 4]
  for i in list1:
    print (i) # Prints all items in list
  ```
  ```python
  list1 = [[1, 2, 3, 4], [5, 6, 7, 8]] # List of lists
  for i in list1:
    for j in i:
      print (j) # Prints each element in the list of lists.
  ```

- #### For/Else Loop
  ```python
  for i in range(0, 5, 1): # range(start, stop, step)
    print (i)
  else:
    print (i)
  # Prints 0 1 2 3 4 4
  ```

- #### While Loop
  ```python
  while (condition):
    print ("Condition true!")
  ```

- #### While/Else Loop
  ```python
  while (condition):
    print ("Condition true!")
  else:
    print ("Condition false!")
  ```

## `enumerate()` Method
`enumerate()` method works by supplying a corresponding index to each element in the list that you pass it. Each time you go through the loop, `index` will be one greater and `item` will be the next item in the sequence.
```python
choices = ["pizza", "pasta", "salad", "nachos"]
for index, item in enumerate(choices):
  print (index+1, item)
```

##  List Comprehensions
List comprehensions are a powerful way to generate lists based on some logic - for example, a list of all the even numbers from 0 to 50. This can be done using `for`, `in` & `if` keywords.
```python
ints_1to5 = [x for x in range(1, 6)] # [1, 2, 3, 4, 5]
doubles = [x*2 for x in range(1, 6)] # [2, 4, 6, 8, 10]
doubles_by_3 = [x*2 for x in range(1, 6) if (x*2)%3 == 0] # [6]
even_squares = [x**2 for x in range(1, 12) if (x%2) == 0] # [4, 16, 36, 64, 100]
```

## Imports
In Python, depending upon the necessity, different modules might need to be imported. There are different types of import:
- #### Generic Import
This imports the whole module, and thus all the methods of the module. You need to use the `module_name.method(argument)` syntax. Do not forget the _dot_ notation.
```python
import math
print (math.sqrt(25)) # Prints 5
```

- #### Function Import
If only a single function needs to be imported from a library, function import is a better way out.
```python
from math import sqrt
print (sqrt(25)) # Prints 5
```

- #### Universal Import
If we want to import all the variables & modules of a function, but do not want to continuously type `module_name.`, then universal import can handle such a situation.
```python
from math import *
print (sqrt(25)) # Prints 5
```
**NOTE**: Universal imports fill your program with tons of variables and methods. So, if you have a function of your own & it contains variables & functions with same name of the imported library, then you won't be able to figure out which variable or function came from where.

## Functions
Use the `def` keyword to define a function.
```python
def myFunction(anyArgument):
  print (anyArgument)
```
- ### Lambdas / Anonymous Functions
Lambdas are useful when you need a quick function to do some work for you. If you plan on creating a function you will use over and over, you're better off using `def` and giving that function a name.
```python
fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
odd_numbers = list(filter(lambda x: x%2, fibonacci))
print (odd_numbers) # Prints [1, 1, 3, 5, 13, 21, 55]
```

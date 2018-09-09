# Python

Python is a high-level multi-paradigm programming language.

### Table of Contents:
* [Data Types](#data-types)
* [Variables](#variables)
* [Comments](#comments)
* [Mathematical Operations](#mathematical-operations)
* [Escaping Characters](#escaping-characters)
* [type() Method](#type-method)
* [Integer & Float Methods](#integer--float-methods)
* [String Methods](#string-methods)
* [List Methods](#list-methods)
* [Dictionaries](#dictionaries)
* [range() Method](#range-method)
* [Conditionals & Control Flow](#conditionals--control-flow)
* [Loops](#loops)
* [List Comprehensions](#list-comprehensions)
* [Imports](#imports)
* [Functions](#functions)
* [Bitwise Operators](#bitwise-operators)
* [File I/O](#file-io)

***

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
- #### Length of a string: `len()`
```python
string = "This is a string."
a = len(string)
print (a) # Prints 17.
```
Alternatively, you can directly use:
```python
a = len("This is a string.")
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

- #### `.items()`, `.keys()` & `.values()` Methods:
  `.items()` returns all the items, `.keys()` returns all the keys & `.values()` returns all the values of a dictionary.
```python
dict1 = {"key1": 1, "key2": 2, "key3": 3}
print (dict1.items()) # Prints dict_items([('key1', 1), ('key2', 2), ('key3', 3)])
print (dict1.keys()) # Prints dict_keys(['key1', 'key2', 'key3'])
print (dict1.values()) # Prints dict_values([1, 2, 3])
```

## `range()` Method
The python `range()` method is just a shortcut for generating a list, so you can use ranges in all the same places you can use lists. The range has the syntax:
```python
range(start, stop, step)
```
In all cases, the `range()` method returns a list of numbers from `start` upto `stop` (but not including `stop`). Each item increases by step.

**NOTE**: If omitted, `start` defaults to `0` and `step` defaults to `1`.

## Conditionals & Control Flow
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
def myFunction(arg, *args, **kwargs):
  print (anyArgument)
```

- ### Variable number of arguments
Python allows you to pass variable number of arguments into the function. This can be achieved using `*args`.
  ```python
  def myFunction(*args):
    print ("Arguments passed via *args:")
    for arg in args:
      print (arg)

  myFunction("Hello", "World", "Python is Amazing!")
  # Prints:
  # Arguments passed via *args:
  # Hello
  # World
  # Python is Amazing!
  ```

- ### Keyword Arguments
`**kwargs` allows you to handle named arguments that you have not defined in advance.
  ```python
  def myFunction(**kwargs):
    for name, value in kwargs.items(): # Since kwargs is a dictionary, so we use .items()
      print (name + " = " + value)

  myFunction(name="Python", description="Amazing Programming Language")
  # Prints:
  # name = Python
  # description = Amazing Programming Language
  ```

- ### Lambdas / Anonymous Functions
Lambdas are useful when you need a quick function to do some work for you. If you plan on creating a function you will use over and over, you're better off using `def` and giving that function a name.
```python
fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
odd_numbers = list(filter(lambda x: x%2, fibonacci))
print (odd_numbers) # Prints [1, 1, 3, 5, 13, 21, 55]
```

## Bitwise Operators
Bitwise operations are operations that directly manipulate bits. In computers, numbers are represented with bits, a series of zeroes and ones. In fact, pretty much everything in a computer is represented by bits. Bitwise operators often tend to puzzle and mystify new programmers, but to be honest, you aren't really going to see bitwise operations in an everyday program. However, they do pop up from time to time, and when they do, you should have a general idea of what is going on.

```python
print (5 >> 4) # Right shift
print (5 << 1) # Left shift
print (8 & 5) # Bitwise AND
print (9 | 4) # Bitwise OR
print (12 ^ 42) # Bitwise XOR
print (~ 88) # Bitwise NOT
```

- #### The `.bin()` Method
`.bin()` converts an integer, octal or hexadecimal number to binary.

  **NOTE**: In Python, all the binary numbers start with the prefix **0b**.
```python
a = 17
b = bin(a)
print (b) # Prints 0b10001
```

- #### The `.int()` Method's Second Parameter
The `.int()` method has an optional second parameter, which is the _base of the number_ you are passing as the first parameter.
```python
print (int("1100", 2)) # Prints 12
print (int("1100", 8)) # Prints 576
print (int("1100", 16)) # Prints 4352
```

- #### Left Bit Shift & Right Bit Shift
These operators work by shifting the bits of a number by a designated number of slots. An example:
```
Left Bit Shift:
0b000001 << 2 = 0b000100 (1 << 2 = 4)
0b000101 << 3 = 0b101000 (5 << 3 = 40)
Right Bit Shift:
0b0010100 >> 3 = 0b000010 (20 >> 3 = 2)
0b0000010 >> 2 = 0b0000000 (2 >> 2 = 0)
```
**NOTE 1**: This operation is mathematically equivalent to floor dividing and multiplying by 2 (respectively) for every time you shift, but it's often easier just to think of it as shifting all the 1s and 0s left or right by the specified number of slots.

  **NOTE 2**: You can only do bitwise operations on an integer. Trying to do them on strings or floats will result in nonsensical output.

- #### Bitwise 'AND' Operator
The Bitwise AND (`&`) operator compares two numbers n a bit level and returns a number where the bits of that number are turned on if the corresponding bits of both the numbers are 1.
```python
a = 0
b = 1
print (a & b) # Prints 0
```

- #### Bitwise 'OR' Operator
The Bitwise OR (`|`) operator compares two numbers on a bit level and returns a number where the bits of that number are turned on if either of the corresponding bits of either number are 1.
```python
a = 0
b = 1
print (a | b) # Prints 1
```

- #### Bitwise 'XOR' Operator
The Bitwise XOR (`^`) operator compares two numbers on a bit level and returns a number where the bits of that number are turned on if either of the corresponding bits of the two numbers are 1, but not both.
```python
a = 0b00101010
b = 0b00001111
print (a ^ b) # Prints 0b00100101
```

- #### Bitwise 'NOT' Operator
The Bitwise NOT (`~`) operator just flips out all the bits in a single number. What this actually means to the computer is actually very complicated, just know that, this is equivalent to adding one to that number and then making it negative.
```python
a = 55
print (~a) # Prints -56
```

- #### Bit Mask
A bit mask is just a variable that aids you with bitwise operations. A bit mask can help you turn specific bits on, turn others off, or just collect data from an integer about which bits are on or off.
  - ##### `AND` Bit Mask
```python
num = 0b1100
mask = 0b0100
desired = num & mask
if (desired > 0):
  print ("Bit was on!")
```

  In the above example, we want to see if the third bit from the right was on.   
  1. First, we create a variable `num` containing the number 12.
  2. Next, we create a variable `mask` with only the third bit on.
  3. Then, we use the bitwise AND to see if the third bit from right of `num` is on.
  4. If `desired` > 0, then the third bit of `num` must have been one.

  - ##### `OR` Bit Mask
  ```python
  a = 0b110
  mask = 0b1
  desired = a | mask
  ```
  - ##### `XOR` Bit Mask (Flipping Out)
  ```python
  a = 0b110
  mask = 0b111
  desired = a ^ mask
  ```
  - ##### Left Shift, Right Shift Bit Mask
  ```python
  a = 0b101
  # Tenth bit mask
  mask = (0b1 << a) # one less than ten
  desired = a ^  mask
  ```

## File I/O
- #### Opening a file: `open()` Method
```python
f = open("output.txt", "w")
```
This says Python to open `output.txt` in `w` mode (write mode).
  - ##### Different modes of opening a file
    - `w`: Write-only mode.
    - `r`: Read-only mode.
    - `r+`: Read & Write mode.
    - `a`: Append mode. Adds any new data to the end of the file.

- #### Writing to file: `write()` Method
```python
f = open("output.txt", "w")
f.write("Hello World!") # Writes to the file 'f' opened above
f.close()
```
**NOTE**: Once finished with writing, you **must** close the file. You can do this by calling `f.close()`.  If you don't close your file, Python won't write to it properly.

- #### Reading from file: `.read()` Method
```python
f = open("output.txt", "r")
print (f.read())
f.close()
```

- #### Reading Between The Lines: `.readline()` Method
To read the file line by line, we use the `.readline()` method. If you open a file and call `.readline()` on the file object, you'll get the first line of the file, subsequent calls to the `.readline()` method will return successive lines.
```python
f = open("output.txt", "r")
print (f.readline())
f.close()
```

- #### The `with` & `as` Keywords
Using the `with` & `as` keywords for opening a file is the **most recommended** way since this method automatically closes the file once the work is done.
```python
with open("output.txt", "r") as f:
    print (f.read())
# Once read, the file automatically is closed, thus ensuring your data is written successfully into the file.
```
- #### File Closed?: `.closed` Attribute
Finally, you might want a way to check if the file has been successfully closed. To do this, we use the `.closed` attribute, which is `True` when the file is closed, and `False` otherwise.
```python
f = open("output.txt")
f.closed
# False
f.close()
f.closed
# True
```

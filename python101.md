# Quick summary of Python

## Goal
```
This is a quick resume of the syntax for quick references.
```

## Syntax

Python uses indentation instead of brackets and `#` for the comments
To quickly comment multiple lines, use `command + /`

### Variables

Data types:
|Types           |Types  |Types      |Types       |
|----------------|-------|-----------|------------|
| Text Type      | str   |           |            |
| Numeric Types  | int   | float     | complex    |
| Sequence Types | list  | tuple     | range      |
| Mapping Type   | dict  |           |            |
| Set Types      | set   | frozenset |            |
| Boolean Type   | bool  |           |            |
| Binary Types   | bytes | bytearray | memoryview |


Number: int, float, complex

String: aString = "example", aString[0] = 'e' 

Boolean: True, False

### Operators

| Operator | Name           |
|----------|----------------|
| +        | Addition       |
| -        | Substraction   | 
| *        | Multiplication |
| /        | Division       |
| %        | Modulus        |
| **       | Exponentiation |
| //       | Floor Division |

Assignment Operators:
   - =
   - +=
   - etc.

Comparison operators:

| Operator | Name                     |
|----------|--------------------------|
| ==       | Equal                    |
| !=       | Not equal                |
| >        | Greater than             |
| <        | Less than                |
| >=       | Greater than or equal to |
| <=       | Less than or equal to    |

Logical Operators: and, or, not
### List Type
len() to get size

#### List
List is a collection which is ordered and changeable. Allows duplicate members.
```
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
thisList[0] => "apple"
thislist[2:5] => ['cherry', 'orange', 'kiwi']
```
Add items: append(), insert()
remove items: remove(), pop(), del, clear()
copy: copy()
join two list: +, append(),extend()

#### Tuples
A tuple is a collection which is ordered and unchangeable. In Python tuples are written with round brackets
```
thistuple = ("apple", "banana", "cherry")
thistuple[1] => "banana"
```
Can't add or change or remove

#### Sets
A set is a collection which is unordered and unindexed. In Python sets are written with curly brackets.
```
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x)
```
Add items: add(),update()
Remove items: remove(), discard(), clear(), del
Join two sets: union(), update()

#### Dictionary
A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values.
```
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
x = thisdict.get("model")
```

loop
```
for x in thisdict:
  print(x)
for x in thisdict:
  print(thisdict[x])
for x in thisdict.values():
  print(x)
for x, y in thisdict.items():
  print(x, y)
```

add
```
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
```

remove: pop(), popitem(), del, clear()
copy: copy(), dict()

### Loop

#### While loops
```
i = 1
while i < 6:
  print(i)
  i += 1
```

break, continue

#### For loops
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```
range(), enumerate()

### Functions

A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

A function can return data as a result.

```
def my_function():
  print("Hello from a function")
```

If the number of arguments are unknown, add a * before the parameter name.

Keyword Arguments:
```
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```

Default Parameter:
```
def my_function(country = "Norway"):
  print("I am from " + country)
```

#### Lambda

A lambda function is a small anonymous function.

A lambda function can take any number of arguments, but can only have one expression.

```
x = lambda a : a + 10
print(x(5))

x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```

### Classes

Python is an object oriented programming language.

Almost everything in Python is an object, with its properties and methods.

A Class is like an object constructor, or a "blueprint" for creating objects.

```
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()
```

#### Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.

Parent class is the class being inherited from, also called base class.

Child class is the class that inherits from another class, also called derived class.

```
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()
```

### Try Catch

The try block lets you test a block of code for errors.

The except block lets you handle the error.

The finally block lets you execute code, regardless of the result of the try- and except blocks.



```
try:
  print(x)
except:
  print("An exception occurred")
```

### Other

#### Regex
A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.

RegEx can be used to check if a string contains the specified search pattern.

```
import re

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)
```

Functions: findall, search, split, sub

#### Scope
Local
```
def myfunc():
  x = 300
  print(x)

myfunc()

```

Global
```
x = 300

def myfunc():
  global x
  x = 200

myfunc()

print(x)
```
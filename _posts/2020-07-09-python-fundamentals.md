---
layout: post
title: Python Fundamentals
subtitle: learn by example
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [python, web,programming]
---

## What is Python?
Python is the most powerful programming language and very easy to learn. Python language used for following,

* Web development 
* Machine Learning 
* Data Analysis 
* ..etc.

It works in multiple platforms like  Windows, Linux, Mac and Raspberry Pi. The syntax is easy to learn and designed for readability, not like other programming languages.

{: .box-note}
This tutorial completely covers the python version is greater than 3.x.

{: .box-note}
**Name the python file** :  helloworld.py
this where python file named with an extension .py

Now Let's print the first statement.
```
print("Hello World)
```

### Syntax and Comments

Python Indentation, When you write python code the indentation is very important, Indentation refers to the block of code.

To comment on the single # (hash) is used in the python program and commenting on the multiple lines, it should be wrap inside triple quotes

```
i = input("Enter the value for i:") # assuming the i values are entered as 10
# If condition to check values are greater than 
if i > 20:
    print("10 is greater than 20")

"""
This is an example for multiple 
comment
in python
"""
```

### Variables and Data Types
Variables are created to store the values and python has no command for creating variables. The variables are created when values are assigned

```
x=5
name="Mike"
color= "Yellow"
salary = "30.00"

```
Python allows us to create multiple variables and assign them in a single line 

```
x,name,color,salary = 5,"Mike","Yellow",30.00

```

Datatypes 

Python is used inbuilt function check the data type by using the type()

```
type(x) => Integer
type(name) => String
type(color) => String
type(salary) => float

```

### Operators
Operators are used to performing operations on variables and values.

Python divides the operators into the following groups:

* Arithmetic 
    are used with numerical values to performing the common mathematical operations.
* Assignment 
    are used to assign the values to variables and combined with  **Arithmetic** operators.
* Comparison 
    are used to compare two values to are to return the logical results.
* Logical 
    are used to join the conditionals statements.

###  Collections - Lists , Tuple and Dictionaries 

#### Lists
A list is a collection to store the multiple values in single variables and changeable any time of executions and sort them as per need.

```
fruits = [ "banana","orange","apple"]
print(fruits)
```

To access the values in the list by referring the index values.

```
print (fruits[1])
orange
```

The index starts from zero and referred to the negative index to access the values item from the list.

```
print(fruits[-1])
apple
```

Access the list values by range or values between index values 

```
fruits = ["banana","orange","apple","kiwi","mango"]
print(fruits[1:3])
["orange","apple","kiwi"]
```
It can also return the values from mid to the end of the index by without specifying the end of the index from the list.

```
print(fruits[2:])
["apple","kiwi","mango"]
```

Similarly from start to end. 

```
print(fruits[:-2])
[banana","orange","apple","kiwi"]
```
To change values in the list.

```
fruits = ["banana","orange","apple","kiwi","mango"]
fruits[2]="I changed fruit name here"
print(fruits)
["banana","orange","I changed fruit name here","kiwi","mango"]
```

#### Tuples

Tuples are similar to lists, but it's not changeable and tuples represented inside brackets ()

```
fruits = ("banana","orange","apple","kiwi","mango")
print(fruits)

```

Accessing the values from a tuple by using the index and range 
```
print(fruits[2])
print(fruits[2:5])
print(fruits[:-2])
```

Changing the values in a tuple, Tuple is unchangeable once it declared or tuple object created. But you can the values by converting them into a list and update the values from the list.

```
fruits = fruits = ("banana","orange","apple","kiwi","mango")
fruits_list = list(fruits)
fruits_list[2] = " I Changed the values "
fruits = tuple(fruits_list)
```
#### Dictionaries
A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values.

```
dict = {
  "brand": "Apple",
  "model": "iPhone" 
}
print(thisdict)
```
Accessing the values from dictionaries

```
modelName = dict["model"]
or 
modelName = dict.get("model")

print(modelName)
```

### Condition and Loops

If Statements:



### Functions

### Class and Object, Inheritance 

### Modules

### File Handling

### Error Handling 

### Python Util - Date, Math and JSON

### How to install the python modules 
PIP Installer 





---
layout: post
title: Python Fundamentals
subtitle: learn by example
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [python, web,programming]
---

## What is Python ?
Python is most powerful programming language and very easy to learn ,  It's used for 

* Web development 
* Machine Learning 
* Data Analysis 
* ..etc 

It's works in multiple platforms like  Windows, Linux, Mac and Raspberry Pi. The syntax are very easy to learn and it is designed for readablity not like other programming language.

{: .box-note}
This tutorials complete covers the python version is greater than 3.x

{: .box-note}
**Name the python file** :  helloworld.py

this where python file should be name with extension of .py

Now Let's print the first statement in python
```
print("Hello World)
```

### Syntax and Comments

Python Indentation , When you write python code the indentation is very important , Indentation is refer the block of code.

To comment the single # (hash) is used in the python program and commenting the multiple line, it should be wrap inside triple quotes

```
i = input("Enter the value for i:") # assuming the i values are entered as 10
# If condition to check values are greater than 
if i > 20:
    print("10 is greater than 20")

"""
This is example for multiple 
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
Python allows create multiple variables and assign them in single line 

```
x,name,color,salary = 5,"Mike","Yellow",30.00

```

Datatypes 

Python is use in built function check the datatype by using the type()

```
type(x) => Integer
type(name) => String
type(color) => String
type(salary) => float

```

### Operators
Operators are used to perform operations on variables and values.

Python divides the operators in the following groups:

* Arithmetic 
    are used with numerical values to perform common mathematicals operations
* Assignment 
    are used to assign the values to variables and it can be combine with  **Arthmetic** operators 
* Comparison 
    are used to compare the two values are return the logical results
* Logical 
    are used to combine the conditionals statements 

###  Collections - Lists , Tuple and Dictonaries 

#### Lists
    A list is a collection to store the multiple values in single variables and it can changeable any time of executions and sort them as per need.

```
fruits = [ "banana","orange","apple"]
print(fruits)
```
    To access the values in the list by referring the index values.

```
print (fruits[1])
orange
```
    The index starts from zero and it can referred to negative index to access the values item from the list 

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
It can also return the values from mid of index to end of index by without specifying the the end of index from the list.

```
print(fruits[2:])
["apple","kiwi","mango"]
```

Simlarly from start to end. 

```
print(fruits[:-2])
[banana","orange","apple","kiwi"]
```
To change values in list 

```
fruits = ["banana","orange","apple","kiwi","mango"]
fruits[2]="I changed fruit name here"
print(fruits)
["banana","orange","I changed fruit name here","kiwi","mango"]
```
### Condition and Loops

### Functions

### Class and Object , Inhertiance 

### Modules

### File Handling

### Error Handling 

### Python Util - Date , Math and JSON

### How to install the python modules 
PIP Installer 





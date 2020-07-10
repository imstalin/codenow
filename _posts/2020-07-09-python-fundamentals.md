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
**Name the python file** :  helloworld.py

this where python file should be name with extension of .py

Now Let's print the first statement in python
```
print("Hello World)
```

### Syntax and Comments

Python Indentation , When you write python code the indentation is very important , Indentation is refer the block of code.

To comment the single # (hash) is used in the python program

```
i = 10
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
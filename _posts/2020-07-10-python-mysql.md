---
layout: post
title: Python and MySQL 
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [python, mysql,web,programming]
---

Introduction Python and MYSQL

Python can be used to interactive with database application , one most popular database is MySQL, We can experiment all operation in database like 

* Create Database 
* Create Table
* Insert Record
* Select Record
* Where Clause and Filters
* Joins
* Update Record
* Delete Record
* Drop Table

### Install MySQL Driver
Before the starting with above operations , We need install MySQL driver in python. We install MySQL driver by running the pip command from console. 

~~~
pip install PyMySQL
~~~

### Test Connection

~~~

import pymysql.cursors
 
 # Connect to the database
connection = pymysql.connect(host='localhost',
                             user='root',
                             password='demopassword',
                             db='demodb',
                             charset='utf8mb4',
                             cursorclass=pymysql.cursors.DictCursor)
print(connection)
~~~

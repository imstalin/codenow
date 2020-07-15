---
layout: post
title: Python and MySQL  
tags: [python, MySQL,web,programming]
---

# Introduction Python and MYSQL

Python can be used to interact with a database application, one most popular database is MySQL, We can experiment all operation in a database like 

* Create a Database 
* Create  and Drop table
*  CRUD  
* Joins 

### Install MySQL Driver
Before the starting with above operations, We need to install MySQL driver in python. We install MySQL driver by running the pip command from the console. 

~~~
pip install PyMySQL
~~~
### **Create Database**

 CREATE DATABASE <dbname>

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

### Create Table and Drop Table

####Creating the sample user table 
~~~

CREATE TABLE `users` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `email` varchar(255) COLLATE utf8_bin NOT NULL,
    `password` varchar(255) COLLATE utf8_bin NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin
AUTO_INCREMENT=1 ;
~~~

#### Dropping the user table
~~~
Drop Table users
~~~

### Create Record

 ~~~
 sql = "INSERT INTO `users` (`email`, `password`) VALUES (%s, %s)"
 cursor.execute(sql, ('example@noemail.com', 'my-secret-password'))
 ~~~

### Read Record with Where clause

#### Fetching single record
~~~
 sql = "SELECT `id`, `password` FROM `users` WHERE `email`=%s"
 cursor.execute(sql, ('example@noemail.com',))
 result = cursor.fetchone()
 print(result)
~~~

#### Fetching multiple records 

Here will fetch all records from the Users table.

~~~
 sql = "SELECT `id`, `password` FROM `users` "
 cursor.execute(sql)
 results = cursor.fetchall()
 print(results)
~~~

### Update  records.
Here will update the user email address.
~~~
 sql = "UPDATE`users' set email=%s' FROM `users`  WHERE  `id`=%s"
 cursor.execute(sql,("example2@noemail.com","1")) 
~~~

### Delete record
Here will delete the user record from the user's table by filter with an email address.

~~~
 sql = "DELETE  FROM`users'  WHERE  `email`=%s"
 cursor.execute(sql,("example2@noemail.com")) 
~~~

### Joins

Joins operations in Relational Databases and here represented as Venn diagrams.

Inner Joins :
         Select only those rows that have values in common in the columns specified in the ON clause

LEFT, RIGHT JOIN:
        Select all rows from the table on the left (or right, or both) regardless of whether the other table has values in common and (usually) enter NULL where data is missing.
---
layout: post
title: Python and MySQL  
tags: [python, mysql,web,programming]
---

# Introduction Python and MYSQL

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

### Create Table

Creating the sample user table 
~~~

CREATE TABLE `users` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `email` varchar(255) COLLATE utf8_bin NOT NULL,
    `password` varchar(255) COLLATE utf8_bin NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin
AUTO_INCREMENT=1 ;

~~~

### Insert Record

 ~~~
 sql = "INSERT INTO `users` (`email`, `password`) VALUES (%s, %s)"
 cursor.execute(sql, ('example@noemail.com', 'my-secret-password'))
 ~~~

### Select Record with Where clause

~~~
 sql = "SELECT `id`, `password` FROM `users` WHERE `email`=%s"
 cursor.execute(sql, ('example@noemail.com',))
~~~

Fetching Records 

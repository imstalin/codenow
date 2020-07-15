---
layout: post
title: Python and Flask  
tags: [python, MySQL,web,programming]
---

Python Flask application used to build a web application. Here look minimal flask application looks.

~~~
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'
~~~

Assume that you have already installed python and flask module. To install Flask module in your python work environment, Run below pip command to get install.

~~~
pip install Flask
~~~

A complete minimal flask application looks like as 

helloworld.py

~~~
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__': 
   app.run(debug=True, host='0.0.0.0',port='5000')
~~~

Save your file and switch to the console environment to run your first flask web application.

~~~
>flask helloworld.py
# Flask application will be running on your localhost in the port of 5000
~~~

Rendering the Static Files

You may want to render the static pages on your website. Now let's import the template module from flask module and write code to display the static files.

helloworld.py
~~~
from flask import render_template
@app.route('/')
def hello():
    return render_template('hellohome.html')

~~~

hellohemo.html

~~~
<html>
    <head>
        <title> Home - Hello </title>
    </head>

    <body>
        Hello ,

        Welcome to Home Page of Flask App.
    </body>
</html>
~~~
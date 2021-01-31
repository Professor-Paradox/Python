To install Django 2 run this
`pip install django`



 Run this to check django

python -m django --version


Create a sample project by run this. Don't forget the trailing dot(.)

django-admin startproject my_proj .

Our project is created now. Run this to create an app

django-admin startapp my_app

You have finished. To start the development server run 

python manage.py runserver

1. Jupyter Notebook
pip3 install jupyter notebook

creating a front end for a project:


copy the exisiting code to project and modify accordingly


initiate a new project with django 
django-admin startproject <projectname>

initiate the internal web server of django 
python manage.py runserver

to create a django app:
django-admin startapp boards

add app to project:
go to project settings and add app name to installed apps list

Views are Python functions that receive an HttpRequest object and returns an HttpResponse object
we add our code and response part in views part

urls is the first page that is visited by server and sends request to views
so we import views from our apps
from appname import views 



check project is running without error by 
python manage.py runserver 



to link our database
python manage.py makemigrations

if all files are migrated 
python manage.py migrate


create a sql migrate (for login authentication)
python manage.py sqlmigrate applicationname 0001

create a superuser to write to DB
python manage.py createsuperuser
created a terminaluser password 1234

static folder for html and css and their display

templates for actual html code that can be used for displaying and integrating django
copy them into the project
keep all files on level with manage.py file


edit admin page and add
database name 
from .models import databasename
admin.site.register(databasename)


nothing to add in test.py so skip this

edit models python file to link to database
class databasename(models.Model):
	name=models.CharField(max_length=100)
	clg = models.CharField(max_length=100)

edit settings file to add templates location
TEMPLATE_DIR = os.path.join(BASE_DIR,"templates")

add this  variable to dir location
'DIRS': [TEMPLATE_DIR],

add this to database part
DATABASES = {
	'default': {
    	'ENGINE': 'django.db.backends.postgresql',
    	'NAME': databasename,
    	'USER':'postgres',(sql server name)
    	'PASSWORD':'1234',(default password)
    	'HOST':'localhost',
	}
}

add the location of static folder
STATIC_URL = '/static/'
STATICFILES_DIRS=[os.path.join(BASE_DIR,'static')]





URLS:
import the application views here
add all the links and paths the user will click on browser 
assign a action in views with this keyword
then write a logic for that in views.py of the respective app

from django.contrib import admin
from django.urls import path
from applicationname import views as v
from django.conf.urls import url

we can use path(‘trigger’,v.actionname) or url(‘^trigger’,v.actionname)


views:
define multiple packages here and methods that can be used on triiger of urls actionname
and return respective html page

import required packages
from django.shortcuts import render,redirect(to render,given by default)
import pandas as pd(to read csv files and execute)
import sys(to execute python script)
import requests
from subprocess import run,PIPE(to execute python script and take it’s output)
from django.contrib import messages(to show information to user about login)
from django.contrib.auth.models import User, auth(to authorize user with his input)


create a database in pgadmin4 with gui
name is databasename

our data will be recorded in databasename>>schemas>>tables 
so we have to intigrate




html code to edit and change:
<a href="link">Back</a>
{{loaded_data | safe}}
<!-- 6th page file -->


  <button action="third">Third person</button>


<form action="verify" method="post">
	{% csrf_token %}
	<input type="submit" value="Verify">
</form>



new project 
virtualenv -p python3.7 env
source env/bin/activate
pip install django
django-admin startproject projectname
django-admin startapp applicationname
copy all files to env level



to give output to browser 
use 
from django.http import httpresoponse

use this with 
return httpresponse(text/html code to return)

create a single url file for single application of django
and link to the project url file


import path,include(for linking to url apps in main project url) 
from django.urls import path,include 
from . import views(in the application urlsfile)


in the path of url use the format
path(‘nametolinktheapp/’,include(‘applicationname.urls’))


url and regex for the link and code is the beginning method of django but with path in later vesions its pretty easy and simple

the entire process of retrieve and show is 

link in browser>>>urlofproject>>>(check if the path matches anything in file and then does the views code)>>>if have another include then passes the remaining url after the current url
ex:localhost/base/something (in url path(base,include(application.urls))) the include will parse the link till base then the url after it i.e, something is sent to the include/application urls and respective output is given back from views.







jinger 2 templates for django




to take data from django
we take data in form of list
then use it as a dictionary
ex:
post=[sdlk,aldfkj,asdklfj]
context={‘keyname’:’actualvalue’}
and send it to html with just the dictionary name
render(request,htmlfile,dictionaryname(context in this case))



using this data in html 

we use {% logic in html to render%}
we take data from python file dictionary and use it with it’s keyname only not the dictionary name
ex:{% for post in keyname%}
end it with {%endfor%}

use {{}} for variables
ex:
{{post}}---->>this will give us a dictionary value, if we want to access a dictionary then we use 
{{post.keyname}}


DRY:Don’t Repeat Yourself
the concept never repeating the same code twice , but using it effectively to link/inherit it in other files/location/code

this is done by oops concepts, in django html it is used by extends method

create a base.html file that the entire project needs to follow and link it every other file/html 

add a content block that needs to be overwritten in other html files
ex:
<html>
some code that needs to be reused over over and over 

code that is unique to each page 
{% block content %}
{% endblock %}
</html>


now this file can be used in other html files 
by:
{% extends ‘htmlfilenameandlocation’ %}
{% block content %}
code that is unique
{% endblock content %}




any css/js files that needs to be used can be saved in  a static folder and loaded into the file using
{% load static %}
and using the file when needed mentioning it’s name
add this to settings file 
with 
STATICFILES_DIRS=[os.path.join(BASE_DIR,'static')]




and the url that the user will be redirected can be harcoded or given with django url file that can change overtime
ex:
href = “ {% url ‘url path name’ %}”



to use databases we can just as easily code in sqlite then after done it can be sent to postgres

ORM(object relational mapping)

instead of createing a database and table we use framework to do this automatically

here we define a class(for table name) variables for column names

actual objects of class for data of rows

ex:
we do this in models of the specific app
better code eveything in sqlite then when code is working push to postgres

install psycopg to contact postgres and django
pip install psycopg2



this done in following manner

after taking the structure needed

we code accordingly 


class tablename(models.Model):
columnnames = models.CharField(max_length=100)(types of data type and limits)
columnnames = models.CharField(max_length=25, choices=model_type,)
columnnames = models.TextField()
columnnames = models.ImageField(upload_to=None, height_field=None)

after that we migrate to create a script that creates table 
python manage.py migrate

after migrating we link script to database 
python mange.py makemigrations

after that to use it to add to database 
python manage.py sqlmigrate applicationname 0001















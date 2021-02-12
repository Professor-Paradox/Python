First, install Python 3 by running these commands in the terminal:

sudo apt-get install python3.5

Then install pip3 the python package manager by running:

sudo apt-get install python3-pip

Then install virtualenv package:

sudo pip3 install virtualenv

Then create a directory named my_proj which is our project name in your home directory. Then open a terminal window in that directory. Run the following command to create a virtual environment:

virtualenv -p python3 env

Then run this command to activate the virtual environment:

source env/bin/activate

Our virtual environment is activated now. To check it run:

which python3

Installing virtualenv:
Sudo apt install virtualenv

Using virtualenv:
Virtualenv -p pythonversiontouse projectname(use same for all projects)

Install pip:
Sudo apt python3-Pip 
python3.7 -m pip install packagename
python3.7 -m pip install --upgrade pip

in a virtual environment:
Pip install packagename


pip commands:
pip list(to show all packagesJ)
pip show packagename(search for the package)
pip freeze(to show packages)
pip freeze > requirements.txt(save packages needed into a file)
pip install -r requirements.txt(install files from file)



To install Django 2 run this

pip install django

Note that pip, and python commands can be used in our virtual environment instead of pip3 and python3.

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









#print('hello')
#this is a comment
"""multi line comment for python
till the end "this will go on "
"""
#indentation(space or tab from code beginning to end of block)
#  is important for assigning a block of code to python
#if True:
 #print("hi")
#variables are boxes that can store values
x = 3.5
y = 'string cool,their will be something that has to occur'
print(x,y)
#variables in print/addition should be of same type for concatenating, if different use comma
# can use format() to convert and work with diff data types.
# usage "some {1} other {0}".format(vaalues,values,.....)
#print(x,"something cool")
#to know the data type of variable use type(variable name)
#print(type(x))
#print(type(y))
#types int(numbers both positive and negative), float(all decimal and exponential),
# complex(numbers with j as imaginary part)
#import random
#a = random.randrange(0,999)
#print(a)
#to print random numbers use import random, random.randrange(starting,ending value)
# changing type of variable to other type is casting,done by program implicit casting,
# done by programmer explicit casting
# can convert int --> float,string: float --> int,string:
# string(containing numbers)-->float(if decimal,normal),int(if normal)
#print(int(y))
#to get one character of string we use [],
#  use 'in' function to check for the presence of a string in another string
#a = 'ood' not in y
#print(a)
# escape character backslash \ to insert illegal inputs in a string
#\',\\,\n,\r(return),\t(tab),\b(backspace)
# find() to search for the first location of string in another string
# rfind() to search for the last location of string in another string
# replace() to replace one string with other
# swapcase() lower case <-->upper case
#print(y)
#print(y.replace('th','ps'))
#print(y)
#print('SomeDay,People WILL call U baD'.swapcase())

# in [] the last value is exclueded in computing


#Lists:
#collection(grouped data) that is ordered,changable(mutable:changed over time),duplication(allowed)
#used with []
#Tuples:(read only lists)
#collection that is ordered,unchangable(immutable),duplication(allowed)
# used with ()
#can add values by converting(casting) tuple to list,add then list to tuple
#set:
#collection that is unordered(order is random ),unindexed(since unordered no index),duplication(not allowed, takes values but discard them)
# used with {}
# Dictionaries:
# collection that is unordered(inserted at random),indexed(has a key/name that can be used),
#   changable,duplication(not allowed)
#used with {},and key:value pairs





#DRY(Don't Repeat Yourself)
#Classes Objects(oops in general)
# in general we write code in sequence to perform a task,then we group repeated code in to a block of code called a function/method
# we use these functions/methods to create new functions and methods that perform a specified task
# a class is a combination of data(parameters,arguments,attributes,properties) and method(functions,behavious,work done)
# an object is an instance of class i.e, when we create a object, first the variable is linked to the class
# when in need it contacts the class and gets the work done,stores data in it's own location
# a class is a blueprint and a object is the product that can have it's own customization
# we pass arguments to class and store the result in object
# a class has a initialization method that contains all the data
# has methods that actually do the work
# we pass parameters to init when needed using object = class(paramenter)
#
# INHERITANCE
# process of taking class1 and puting it in class2
# class1 parent, class2 child
# used as class child_class(parent_class)
# the child method overrides, parent method.
# but can be used as a backup by writing the parent method in child method as 

parent.init(self,args) or super().init(no self just args)

#  now we can use the parent methods,variables
#  if a method add() is in child and is also in parent then the child add() is used, but the parent add() can be used with variable = super().add()


Scope:(local and global)
A variable inside a function is local variable and can only be used in it
Ex: fun a {x=10,fun b{y=10} }
Fun a 	can have x but not y and fun b can have x and y

A variable outside function and in the beginning of class is a global variable and can be accessed by any function
A local variable can be made global with ‘global’ keyword 

Use
Try: to check for errors
Except: to execute when an error is thrown
Else: when no error occurs
Finally: to execute no matter the error state

pip(pip install python) package manager to install packages to work in python
Module: a single file that is used with import filename
Package: a directory with modules that has __Init.py__ to say it’s a package dir(),used to structure code.organize
Library: same as package,collection of packages that are aimed at providing specific functionality(tool box to builld a table,bench,ship,etc.)
Framework:Collection of packages that is aimed to attain a result(mass production of tables,can build a ship but is difficult)



#print('hello')
#this is a comment
"""multi line comment for python
till the end "this will go on "
"""
#indentation(space or tab from code beginning to end of block)
#  is important for assigning a block of code to python
#if True:
 #print("hi")
#variables are boxes that can store values
x = 3.5
y = 'string cool,their will be something that has to occur'
print(x,y)
#variables in print/addition should be of same type for concatenating, if different use comma
# can use format() to convert and work with diff data types.
# usage "some {1} other {0}".format(vaalues,values,.....)
#print(x,"something cool")
#to know the data type of variable use type(variable name)
#print(type(x))
#print(type(y))
#types int(numbers both positive and negative), float(all decimal and exponential),
# complex(numbers with j as imaginary part)
#import random
#a = random.randrange(0,999)
#print(a)
#to print random numbers use import random, random.randrange(starting,ending value)
# changing type of variable to other type is casting,done by program implicit casting,
# done by programmer explicit casting
# can convert int --> float,string: float --> int,string:
# string(containing numbers)-->float(if decimal,normal),int(if normal)
#print(int(y))
#to get one character of string we use [],
#  use 'in' function to check for the presence of a string in another string
#a = 'ood' not in y
#print(a)
# escape character backslash \ to insert illegal inputs in a string
#\',\\,\n,\r(return),\t(tab),\b(backspace)
# find() to search for the first location of string in another string
# rfind() to search for the last location of string in another string
# replace() to replace one string with other
# swapcase() lower case <-->upper case
#print(y)
#print(y.replace('th','ps'))
#print(y)
#print('SomeDay,People WILL call U baD'.swapcase())

# in [] the last value is exclueded in computing


#Lists:
#collection(grouped data) that is ordered,changable(mutable:changed over time),duplication(allowed)
#used with []
#Tuples:(read only lists)
#collection that is ordered,unchangable(immutable),duplication(allowed)
# used with ()
#can add values by converting(casting) tuple to list,add then list to tuple
#set:
#collection that is unordered(order is random ),unindexed(since unordered no index),duplication(not allowed, takes values but discard them)
# used with {}
# Dictionaries:
# collection that is unordered(inserted at random),indexed(has a key/name that can be used),
#   changable,duplication(not allowed)
#used with {},and key:value pairs





#DRY(Don't Repeat Yourself)
#Classes Objects(oops in general)
# in general we write code in sequence to perform a task,then we group repeated code in to a block of code called a function/method
# we use these functions/methods to create new functions and methods that perform a specified task
# a class is a combination of data(parameters,arguments,attributes,properties) and method(functions,behavious,work done)
# an object is an instance of class i.e, when we create a object, first the variable is linked to the class
# when in need it contacts the class and gets the work done,stores data in it's own location
# a class is a blueprint and a object is the product that can have it's own customization
# we pass arguments to class and store the result in object
# a class has a initialization method that contains all the data
# has methods that actually do the work
# we pass parameters to init when needed using object = class(paramenter)
#
# INHERITANCE
# process of taking class1 and puting it in class2
# class1 parent, class2 child
# used as class child_class(parent_class)
# the child method overrides, parent method.
# but can be used as a backup by writing the parent method in child method as 

parent.init(self,args) or super().init(no self just args)

#  now we can use the parent methods,variables
#  if a method add() is in child and is also in parent then the child add() is used, but the parent add() can be used with variable = super().add()


Scope:(local and global)
A variable inside a function is local variable and can only be used in it
Ex: fun a {x=10,fun b{y=10} }
Fun a 	can have x but not y and fun b can have x and y

A variable outside function and in the beginning of class is a global variable and can be accessed by any function
A local variable can be made global with ‘global’ keyword 

Use
Try: to check for errors
Except: to execute when an error is thrown
Else: when no error occurs
Finally: to execute no matter the error state

pip(pip install python) package manager to install packages to work in python
Module: a single file that is used with import filename
Package: a directory with modules that has __Init.py__ to say it’s a package dir(),used to structure code.organize
Library: same as package,collection of packages that are aimed at providing specific functionality(tool box to builld a table,bench,ship,etc.)
Framework:Collection of packages that is aimed to attain a result(mass production of tables,can build a ship but is difficult)





Numpy:	




Numpy:	




A single file in python is a module
Group of files in a directory/sub-directories with __inti.py__ in each dir is a package
Group of packages that we call is a library
Group of packages that structure our flow(code) is a framework(that call’s code)

Jupyter Notebook:
A interactive documentation that displays code and executes in webpage (40+ languages supported) , used in analysis,data science,mining,learning

Matplotlib(pip3 install matplotlib)
Used to display the data(csv format)

Panda(pip3 install pandas)









Import package and rename for easy use
Import pandas as pd
From matplotlib import pyplot as pl

Take data to a variable 
Road =pd.read_csv(‘filename.csv’)

Isolate part of data, variable.isolation variable equal to name, assign to a new variable
AP = road[road.state == ‘ap’]

Display information using plot
pl.plot(x-axis data,y-axis data,args like  ‘.’,’-’,’o’ to show respective items instead of lines)
pl.plot(ap.year,ap.total,’o’)

Can display comparisons in one graph
pl.plot(an.year,an.total)

To display which line represents what 
pl.legend([‘1st plot name’,’2nd plot na	me’])
Divide data if needed
Ap.total /100

Show graph title
pl.title(‘name’)

Show x-axis name
pl.xlabel(‘name’)
pl.ylabel(‘name’)

Display all these 
pl.show()

To get specified value 

Table.column.iloc[position]

Display the growth in percentages
Take the first value as 100%
Divide all values with first value then multiple with 100











face recognitions:
need cv2 module
install it 


open camera and use 
cv2.videocapture(number)
[number= the camera number 0 for first one]
cv2.isOpened()
[to check if camera is being used]
cv2.imread(‘imagelocation’)
cv2variable.imread()
[to read image from camera ]
cv2.imwrite(‘filename’,cv2variable)
[saves images file]
cv2.imshow(‘caption to show on window’,cv2variable)
[displays output of camera ]
cv2.waitkey(numberof keys)
[waits for key input to continue for next step]
cv2variable.release()
[shutdown camera]
cv2.destroyallwindows()
[close camera application]










 postgres installation:
 sudo apt install postgresql postgresql-contrib
 use 
 su - postgres to use postgres
 psql to go to inteface
 \password postgres to change default password
 0000
 
 sudo apt install pgadmin4 pgadmin4-apache2 -y
 email
 pgadmin4 password  1234
 
 
python install from source:
sudo apt install build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev libffi-dev



cd /usr/src
wget https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tar.xz
tar xf Python-3.7.0.tar.xz

cd Python-3.7.4
sudo ./configure --enable-optimizations
sudo make altinstall

sudo apt install python3-pip 

pgadmin4 web password 9876




virtualenv name(of project)
virtualenv -p pythonversiontouse projectname
source projectname/bin/activate to use the environment

pip install package name
pip list (to see all packages)
pip show(to search for package)
pip freeze > requirements.txt (to save all the packages details)
pip install -r requirements.txt(to install packages in file)






Installing virtualenv:
apt install virtualenv
python3.7 -m pip install virtualenv
python3.7 -m pip install virtualenvwrapper

Using virtualenv:
virtualenv -p pythonversiontouse projectname(use same for all projects)

**Install** pip:
**Sudo** apt python3-Pip 
**pip3** install packagename
python3.7 -m pip install packagename
python3.7 -m pip install --upgrade pip

in a virtual environment:(better to work in a virtualenv always)
Pip install packagename

pip commands:
pip list(to show all packagesJ)
pip show packagename(search for the package)
pip freeze(to show packages)
pip freeze > requirements.txt(save packages needed into a file)
pip install -r requirements.txt(install files from file)

Wake up wifi from terminal:
systemctl enable network-manager

see your network interfaces:
nmcli d
Nmcli c

Connect to wifi:
nmcli c up savedwifinam

Stop system error report:

sudo gedit /etc/default/apport 
enable=0(disable)


open application from scroll wheel:
gsettings set org.gnome.shell.extensions.dash-to-dock scroll-action 'cycle-windows'

add new document option to context menu:
touch ~/Templates/"Untitled Document"



packages:
1. Jupyter Notebook
pip3 install jupyter notebook

2. opencv
Try:
in virtualenv pip install opencv-python opencv-contrib-python(should work in all cases if error proceed forward)
install the opencv global package from repos
sudo apt install python3-opencv(short way)(already present in repos)
(best option is to build it from source)(will take time but will install at specific python version and location)
after successful install/build , locate the cv2 package
dpkg -L python3-opencv
 then symlink it to the virtual env/python dist-packages 
it would be at /usr/lib/python3.x/dist-packages/cv2.cpython.xxxxxx.so 
link to /usr/lib/python3.XX/dist-packages/ and renamed it to cv2.so
or env/lib/python3.7/dist-packages/cv2.so
or env/lib/python3.7/dist-packages/cv2/cv2.so
best option is to link the cv2 file of system python to virtual env pip installed, opencv to work together
rename the exisiting file to backup so can be a backup use
 mv env/lib/python3.7/site-packages/cv2/cv2.cpython-37m-x86_64-linux-gnu.so cv2.cpython-37m-x86_64-linux-gnu-backup.so
link the file instead of copying to pip environment file
ln -s /usr/lib/python3/dist-packages/cv2.cpython-36m-x86_64-linux-gnu.so env/lib/python3.7/site-packages/cv2/cv2.cpython-37m-x86_64-linux-gnu.so

can use both cv2 file of pc and haarcascade files of opencv package of pip
(rename the file to the same name as the cv2 python file to link to system )
(pip install opencv-python) throws error for multiple qt dependencies(kde has its own qt so use apt version)
face detection haarcascade files are located in cv2/data/haarcascade folder can link them with cv2.data.haarcascade

install dlib:

					sudo apt-get update
sudo apt-get install build-essential cmake libopenblas-dev liblapack-dev libx11-dev libgtk-3-dev
sudo apt-get install python python-dev python-pip
sudo apt-get install python3 python3-dev python3-pip





use dpkg -L packagename
to search package location in ubuntu



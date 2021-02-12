
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

Install pip:
Sudo apt python3-Pip 
pip3 install packagename
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

 

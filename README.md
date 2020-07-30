# Django

Start python in linux
- ls : check file in folder
- cd folder_name : into folder
- sh pycharm.sh : run the pycharm

The site for searching the packages to use in python
- https://pypi.python.org/ : python package
- https://www.djangopackages.com/ : Jango package

Enter the VENV
- $ source /home/*user*/VENV/vDjBook/bin/activate  
Out the VENV
- deactivate

and then  
I have to go into the Pycharmprojects folder
- cd /home/*user*/Pycharmprojects

runserver
python3 manage.py runserver 0.0.0.0:8000

## Order for linux
- :w : save
- :sav : save as
- :w file.txt : save the file as text file
- :w > file.txt : save the file over the origin file
- :q : exit vi
- :up : save the content that changed
- ZZ : save and exit
- :wq! : save and exit
- :e file.txt : read file.txt
- :e : read a file
- :e# : read a file that opened before

## How to update latest Python on Linux

1. $ sudo yum install gcc openssl-devel libffi-devel bzip2-devel

2. $ wget (link for python download)

3. tar xzf (tgz file for python)

4. cd Python-ver(ex python3.8.5)

5. ./configure --enable-optimizations

6. sudo make altinstall

7. $ which python3 (Check the link for python3)
      print: /usr/bin/python3
      
8. $ sudo rm /usr/bin/python3

9. $ which python3.8 (To designate symbolic link, Check the location for a file that was installed before) 
      print: /usr/local/bin/python3.8
      
10. $ ln -s /usr/local/bin/python3.8 /usr/bin/python3

11. $ python3 --version
      print: Python3.8

## When it doesn't work cuz "ModuleNotFoundError: No module named '_sqlite3'

I installed Python3.8 on Centos8

1. $ yum install sqlite-devel -y

2. go to python folder
(In my case, "cd /home/sudonnoh/Python-3.8.5
./configure
make altinstall

3. try again "python3 manage.py migrate"


## If you want to initialize DB on Django..

1. $ find . -path "*/migrations/*.py" -not -name "__init__.py" -delete

2. $ find . -path "*/migrations/*.pyc"  -delete

3. $ python3 manage.py makemigrations  
     If it has error for "no module named 'django.db.migrations.migration', you should reinstall Django.  
     First, you must check the version of installed Django.  
     $ python3 -m django --version  
     $ pip install --upgrade -force-reinstall Django==version

4. $ python3 manage.py migrate  

python27-django-ecommerce-website-from-scratch
==============================================

How to build a fully functional ecommerce website in Python Django from scratch on  the Ubuntu Linux OS


1. from your bash command line, run these commands:
mkdir Envs                                #This directory will hold all your python virtual environments
mkdir Projects                            #This directory holds all your future python django projects

pip install virtualenv                    #installs virtual enviroment
cd Envs
virtualenv django                         #Creates a new virtualenv
source Envs/django/bin/activate           #Uses the django virtualenv you just created
pip install django                        #installs django
pip install mysqlserver                   #installs MySQL server 


2.Create your first django project, go to the Projects directory and run this command: 
django-admin.py startproject storename
cd storename 
python manage.py runserver 


3.Enter your mysql prompt,from bash run:
mysql -u root -p
(enter the password)


4.in the mysql prompt:
CREATE DATABASE projectname CHARACTER SET utf8;
CREATE USER 'username'@'localhost' identified by 'password';
GRANT ALL ON projectname.* TO username@localhost;

#Note: MySQL db storage engines are created as MyISAM by default,if you want to handle transactions you want to 
# change the engine to InnoDB


3.Open your settings.py and change the database sections settings to the ones you just created as follows and save: 
DATABASE_ENGINE = 'mysql' # 
DATABASE_NAME = 'projectname' # Or path to database file... 
DATABASE_USER = 'username'
DATABASE_PASSWORD = 'password' 
DATABASE_HOST = '' # or 127.1.0.1 
DATABASE_PORT = '' # or 3306

4.Verify mysql is working successfully
python manage.py dbshell
if you see 'mysql>' and no errors 

5.Django exception handling

6.plan models




# DjangoChecklist

Step 1.
Make sure pipenv is installed

Step 2.
run `pipenv install django`

step 3
Install the library for connecting Django to PostgreSQL
run `pipenv install psycopg2-binary`
Open code editor

Step 4.
run ` pipenv run django-admin startproject (whatever project name is) .`
Dont forget the period at the end

Step 5.
run `pipenv shell` to activate Virtual Enviornment


Step 6.

run `django-admin startapp (whatever your app name is)`

### This will mean you have created the base for a django app

#### Next we will log into PostgreSQL

Step 1.
run `psql -d postgres`

Step 2.
Create Database and user
Dont forget to end the line with a ;
>CREATE DATABASE  (databaseName);
>CREATE USER (userName) WITH PASSWORD '(password)';
>GRANT ALL PRIVILEGES ON DATABASE (databaseName) TO (userName);
>\q

Step 3.
Go into the (startproject name)/settings.py and find the DATABASE and change it to this
>DATABASES = {
>    'default': {
>        'ENGINE': 'django.db.backends.postgresql',
>        'NAME': '(startapp name)',
>        'USER': '(database userName)',
>        'PASSWORD': '(database password)',
>        'HOST': 'localhost'
>    }
>}

Then find the INSTALLED_APPS and add the (startapp name) to the bottom of the list

Step 4.
run `python3 manage.py runserver`
Checkout `python3 manage.py`

### Next you will create the models
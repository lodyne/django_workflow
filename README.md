# django_workflow

## Install virtual environment

When dealing with django, it is advised to use virtual environment so as to make sure the dependencies from various projects do not collide.
There are so many virtual environment options such as pipenv,venv,virtualenv etc. but i prefer to use virtualenv.
And the one i use is specifically for window i.e. virtualenvwrapper-win.

``` pip install virtualenvwrapper-win ```

### Make the virtual environment

After installing virtual environment, you have to make vitual environment for your
preference. This is done by the following command:-

``` mkvirtualenv workflow ```

This command changes the  cmd to have a prefix of the created virtualenv as shown below:-

![virtualenv in cmd](cmd.png)

## Create the django project

Django has the idea of project and apps i.e. the project is the main container in which other apps are contained in it. This is done by using the following command:-

``` django-admin startproject django_workflow . ```

Note:- django_workflow is the name of the django project and the dot(.) at the end is optional so as to reduce redundancy of django project naming.

And you can use tree command to show the file structure of the created django_workflow project as shown below:-

![project structure](projectstructure.png)

## Create the django app

You can now create the django app which resides inside the django project and it is the one presenting the actual app/feature you are trying to build inside the project.Type this command below:-

``` python manage.py startapp myapp ```

Note: myapp is the name of the created app and you can check the file structure of myapp by using *tree* command as shown below:-

![app stucture](appstructure.png)

### Register the app in INSTALLED APPS in settings.py

The INSTALLED APPS is the list which is available in settings.py file in the django project directory i.e. django_workflow.
It contains the list of all pre-installed apps available which help in django web applications ecosystem.
Therefore you must register your created app into INSTALLED APPS so as to be known by the django project.
Go to the apps.py file and copy the *name of the class*, Put  the *name of the app* folllowed by *apps* then the name of the class.
i.e. name_of_the_app.apps.name_of_the_class_copied_from_apps.py

![Installed apps](installedapps.png)

## Run the server

You have to run the server to prove if the configuration is set properly.
The Django framework has in-built server which helps in production stage.

``` python manage.py runserver ```

![Run the server](runserver.png)

The following Django page will appear as shown below:-

![django page after running server](djangopage.png)

# Django

## Installing python and pip

1. Visit [python] (https://www.python.org/downloads/)
2. Install python
3. Setup path variable for python and python/scripts for windows

## Check python and pip version
> python --version **OR**  python3 --version

> pip --version **OR** pip3 --version

## installing virtalenv
> pip install virtualenv

## creating virtual environment [recommended]
> virtualenv DjangoEnv

## activating env
> source DjangoEnv/bin/activate **for linux**

> source DjangoEnv/scripts/activate **for windows**

## deactivating env
> deactivate

## installing Django
> pip install django

## Creating new project
> django-admin startproject mysite

## run the web application

> cd mysite

> python manage.py migrate

> python manage.py runserver

## create web application to the project

> python manage.py startapp blog

## add the application to the site

1. open file mysite/settings.py
2. add the following lines in INSTALLED_APPS array
> 'blog.apps.BlogConfig'

## create models

## create migration for models
> python manage.py makemigration blog

## view migration sql command
> python manage.py sqlmigrate blog 0001

## apply migrations
> python manage.py migrate blog

## register admin
1. open file blog/admin.py
2. add following codes

>from django.contrib import admin

>from .models import Post

> admin.site.register(Post)
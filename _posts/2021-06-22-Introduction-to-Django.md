---
layout: post
title: "Part 1: Introduction to Django"
categories: post
---

[DJANGO]("https://www.djangoproject.com/") is a high level python web framework that is built entirely in python. A web framework is a collection of packages or modules that helps a developer to write web applications or services with less code.

>[Django]("https://www.djangoproject.com/") is free, open-source and relies on Model View Controller (MVC) pattern. Model is the component that contains the Business logic, View contains the User Interface (UI) logic while Controller is the main control component. Django is fast, secure and scalable, hence the phrase “A web framework for perfectionists with deadlines.”

You can check out [official Django documentation]("https://www.djangoproject.com/") for more information.

Prerequisites
===============

<main>
	<ul>
		<li>Python (preferably Python3)</li>
		<li>A Virtual environment</li>
		<li>Django</li>
	</ul>
</main>

Python comes pre-installed on Linux. If you are using windows, you need to download and install python from [here]("https://www.python.org/downloads/windows/").

To check your python installation, open the Terminal and type; for python 2 and python3 respectively.


	python -V #To check python version from your terminal(python2)

	python3 -V #To check python version from your terminal (python3)

>A [python virtual environment]("https://docs.python.org/3/tutorial/venv.html") allows a developer to create isolated environments for his/her python projects. You are not limited to a certain number of virtual environments; You can have as many different virtual environments as you want.

We can use [pip]("https://pypi.org/project/pip/") to install a virtual environment. [Pip]("https://pypi.org/project/pip/") is a package installer for python. In your terminal.

Pip installation - <code>pip install pip</code><br>

To install virtual environments - <code>pip install virtualenv</code><br>

Let’s create a virtual environment. You can use any name for your virtual environment. In your Terminal. 

<code>virtualenv env</code><br>

Activate your virtual environment and navigate into it, then install Django inside your virtual environment

<code>pip install django</code><br>

Let’s create our first Django project.

<code>django-admn startproject Mysite</code><br>

This will create a folder with the name of your project, in our case, Mysite in your current directory. Navigate to your project folder and fire your project.

<code>python manage.py runserver</code>

Visit http://127.0.0.1:8000/ to have a view of your first Django project.

Congratulations! You just created your first Django web app.

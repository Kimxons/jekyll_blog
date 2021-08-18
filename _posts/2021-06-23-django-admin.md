---
layout: post
title:  "The Django Admin"
categories: post
---

In this tutorial, we are going to be checking out the admin functionality that comes with Django. Let’s start by creating an administrator user.

We need to run migrations first in order to be able to create our admin user.

>[Migrations]("https://docs.djangoproject.com/en/3.1/topics/migrations/") are Django’s way of propagating changes that you make to your models e.g adding fields into your database schema.

	python manage.py migrate

You should see this output in your terminal;

 
	Operations to perform:

	Apply all migrations: admin, auth, contenttypes, sessions

	Running migrations:

	Applying contenttypes.0001_initial... OK

	Applying auth.0001_initial... OK

	Applying admin.0001_initial... OK

	Applying admin.0002_logentry_remove_auto_add... OK

	....
	....


Let’s now create our admin user;

  
	python manage.py createsuperuser

You should get this output in your terminal:

	user:~/dir-to-project$ python manage.py createsuperuser

	Username (leave blank to use 'user'):

	Email address: example@gmail.com

	Password: *********

	Password (again): ********

	Superuser created successfully.


Now let’s log into the admin page: [http://127.0.0.1/admin]("http://127.0.0.1/admin")

Log in with the user we have just created and you should see a page an admin page. 

This is the place where you interact with your models via an actual interface; you can modify, add, delete entries for your registered models. You can notice that we have two models: Groups and Users.

<mark>Happy Coding!</mark>
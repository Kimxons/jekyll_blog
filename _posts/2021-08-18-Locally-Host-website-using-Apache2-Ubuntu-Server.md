---
layout: post
title: "Locally Host Website using Apache2 Ubuntu Server"
categories: post
---

This is a simple guide on how to host a simple website locall in Apache
Web Server in Linux.

Install Apache
==============

We install Apache from the apt repository in Linux.
    sudo apt install apache2


Useful Commands
===============

To start apache2 server
    sudo service apache2 start

You can as well restart Apache2 server

    sudo service apache2 restart

You can as well reload the apache2 server
    sudo service apache2 reload

You can check the status of Apache2 server
    sudo service apache2 status

You can stop the server
    sudo service apache2 stop

After starting the apache2 server, you can check it on your browser by visiting this address
http://127.0.0.1/

You should see the default page provided by Apache... to upload an image

Creating our website
====================
We will navigate to /var/www/html and create our project's directory.
    cd /var/www/html
    sudo mkdir Hello

Let's navigate inside our project's directory and create our index.html file.
    cd /Hello/
    sudo nano index.html

Let's add this inside our index.html file
    <html>
        <p>Hello World.</p>
    </html>

Hosting the website on Apache2 web Server
=========================================

Let's check the status of our server and run it if its inactive.
We navigate to http://127.0.0.1/Hello in our browser.

Yeey! it works. We j


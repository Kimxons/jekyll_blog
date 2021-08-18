----
layout: post
title: "Install and Configure phpMyAdmin on Linux"
categories: post
----

phpMyAdmin is a web-based database management program.

Pre-requisites
==============

php 5 and above
mysql5
Apache2

Guidelines
==========

Navigat to Apache2 Document root and download the latest version of phpmyadmin from:
http://www.phpmyadmin.net/home_page/downloads.php

Unzip the files using tar command. 

    tar phpMyAdmin-5.1.1-all-languages.tar.gz

Rename the file to phpMyAdmin

    mv phpMyAdmin-5.1.1-all-languages phpMyAdmin

Configurations
==============

Open a browser and visit:

    http://{your-ip-address}/phpMyAdmin/setup/index.php

or
    http://127.0.0.1/phpMyAdmin/setup/index.php

TODO - we will continue from there

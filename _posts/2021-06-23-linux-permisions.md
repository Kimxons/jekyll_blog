---
layout: post
title:  "The Linux Permissions"
categories: post
---

It is important to understand the permissions model of Linux machines. Understanding how to manage these permissions is helpful in preventing some security threats (attacks) that exploit the Linux system. Files and directories in your Linux System consist of three permissions: Read, Write, and Execute. Linux inherits the Unix model of file ownership and permissions. The permissions dictate who is allowed to do what with any given file or directory in Linux.

<h4>Linux File Permissions</h4>

Linux inherited the Unix model of file Ownership and Permissions. These Permissions specify who has access to what and what they are allowed to perform with the given file or directory.

The Permissions includes: Read, Write, and Execute. A Read permissions on a file or directory enables a user to bread the contents of the given file or directory. A Write permission enables a user to modify the contents of a file or delete the file or directory. An execute permission allows a user to execute the file (run a file as an executable file). 

	$ ls -l 

This command (in your terminal enables a user to view the permissions of a given file or directory. The output might look like this: 

	drwxr-xr-x 
	-rw-rw-r--

You should note that the first character indicates whether the item in question is a directory or a file. The “d” in our first oupt indicates that the item is a directory whereas the dash implies that the item is a file. The next three characters that follow shows the permissions of the owner of the given file, with R representing Read, W for Write and X for eXecute. Notably, a dash indicates the lack of a permission. 

The ‘chmod’ command allows a user to change the permissions of a file. The ownership flags u, g, and o for User, owner Group, and Others respectively. The general look of the chmod command: 

	chmod (ownership flag+permission flag) filepath

Example: To add execution permissions for a user. 

	chmod u+x filepath

To add execute commands for everyone:

	chmod +x filepath

You can also revoke permissions from a file using the chmod command. 

	chmod -x filepath

	asdfgh

The ‘chown’ command can change the ownership of a file or a directory.

	chown user filepath or chown user:group filepath

The ‘chgrp’ command can change the group ownership 

	chrgrp group filename

To change group-owner only, use this command:

	chgrp group_name filepath

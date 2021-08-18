---
layout: post
title: "Part 2: Code editors & Version control system"
categories: post
---

<h3>Configuring our development environment</h3>

<h4>Install a code editor</h4>

A code editor produces rich texts (with fonts and formatting) unlike Word. They are specialized specifically for editing code. 

There are so many code editors out here you can use. Some people prefer IDEs (Integrated Development Environments) such as PyCharm, especially python developers.

I have a few recommendations to help you get going. 

<h4>Visual Studio Code</h4>

Vs-code is a nice code editor developed by Microsoft for windows, macOs and Linux. It is a powerful code editor with support for debugging, syntax highlighting, code snippets, embedded git control and many more. You can download it [here]("https://code.visualstudio.com/download").

<h4>Sublime text 3</h4>

Available for all operating systems. It is a very popular code editor with a free evaluation period. You can download it [here]("https://www.sublimetext.com/3").

<h4>Atom</h4>

It’s a free and open-source code editor. You can download it [here]("https://atom.io/").

<h4>Install git - VCS</h4>

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It is used by many programmers. On Ubuntu, you can install it using this command:

<code>sudo apt install git</code>

On windows, you can download git from [here]("https://git-scm.com/").

After installation, create a free GitHub account [here]("https://github.com/").

Set up your username, email address and code editor, for our case we are using visual studio code. Type these commands on your terminal;

<code>config --global user.name <username><br>
<code>config --global user.email <user-email><br>
<code>config --global core.editor vscode</code>

Now we are ready to start coding!!

<h4>Create a git repository</h4>

In order put your project up on GitHub, you’ll need to create a repo for it to live in. You can follow the guide by [GitHub]("https://docs.github.com/en/get-started/quickstart/create-a-repo") on how to create your first git repo and get going.

Let’s call our repo Mysite. On your terminal, initialize a remote repository on your computer using this command.

<code>git init</code>

You should get this out output:

<code>Initialized empty Git repository in /{directory-name}/.git/ </code>

Add your files to your remote repo using this command:

<code>git add .</code>

Commit your changes using this command:

<code>git commit -m "commit message"</code>

Let’s configure our remote repo;

<code>git remote add origin https://github.com/{your-name}/Mysite.git</code>

Confirm if your remote repo is well configured;

<code>git remote -v</code>

You should see the output below in your terminal;

<code>origin https://github.com/{your-name}/Mysite.git (fetch)
origin https://github.com/{your-name}/Mysite.git (push)</code>

Awesome! It worked!

Let’s push our code..

<code>git push -u origin main or master</code>

You will be prompted to enter your username and password.

Congratulations, you just pushed your code on GitHub!!

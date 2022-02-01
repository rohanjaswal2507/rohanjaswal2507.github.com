---
layout: post
title: "Working with Meteor.js"
description: "My experience with Meteor.js"
category: "Web development"
tags: [Meteorjs, javascript, MongoDB]
---
Hi, Its been very long since I last wrote something here.
Lately, I have been learning to develop web applications using *Meteor.js*.
Meteor.js is a nodeJS based framework which is used to develop reactive web applications.
The development of a web app in using Meteor.js is quite easy.
You get a support of lot of packages which could be used to add various features like logins, social logins, Code editors to the web applications.
Moreover, there is a very good documentation available at .



### Create a Meteor.js App
Creating a new App in Meteor.js is very simple. Just type
	meteor create newApp

This command will create a newApp and would bind the necessary packages to it.
The output on the terminal would be
<center><img src="/assets/media/meteor_create_app.png"/></center>

This would create a basic application with three files *newApp.html*, *newApp.css*, *newApp.js* and a hidden directory named *meteor* in the parent directory *newApp*.
From the names and extensions of these three files, their purpose is pretty clear.


The hidden meteor directory contains all the information about your application.
All the packages and modules required for building and running the application are in this directory.
This kind of structure makes the application really portable and cross-platform.

### Reactive Nature
In the very beginning, I mentioned the development of reactive web applications using meteor.js.
Now, what is the reactive nature of an application.
An application's reactive nature tells that the app will reflect any changes on the database or environment on the client side with minimal development effort.


### Meteor packages
Developing a meteor app becomes super easy with meteor packages. There are thousands of open source meteor packages availabe on atmospere.js.
For almost anything you want to do in your app, you have a package available in atmosphere.js.
For example, there are many packages named accounts-ui-______. These packages help in user account management in the meteor app. So, you need not worry about developing a user account management system for your application if you are using meteor.
Similarly, there are many packages availabe for front-end development which help a lot in creating a beautiful front-end.
I am not at all good in front-end development, but all these packages helped me in creating a nice looking front-end when I was working on a meteor based project.

So, to see all the packages that are being used by an app or are installed in a app, run this simple command on the terminal in the root directory of the application.
	meteor list

This will list all the packages that are installed to that app.


### Blaze Templates

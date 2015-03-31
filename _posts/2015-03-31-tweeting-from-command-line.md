---
layout: post
title: "Tweeting from command line"
description: "Tweeting from command line si fun. This blog post is about a command line tool named TTYtter which is used for microblogging on twitter" 
category: tools 
tags: [linux, command line, ttytter, twitter]
---

{% include JB/setup %}
I use twitter for microblogging. We always access twitter via our web browser or the mobile app developed by twitter. Offcourse, they are best methods to use these sites. Recently, I came to know about using twitter from command line. I read about **TTYtter** from Arch wiki.

**TTYtter is a command line tool for microblogging on twitter. If you do not want to see pictures, or other graphical things on twitter and just want to read others' tweets, TTYtter is the thing for you. TTYtter fetches tweets of the people you follow on your command line. This gives twitter a IRC like interface and it looks cool to me.

Tweets on command line look somewhat like this.
<p>
	<img src = "/images/ttytter.png">
</p>

To install TTYtter on Debian based systems, type this command

`sudo apt-get install ttytter`

To use TTYtter, you have to authorise this app from Twitter. To do this, just run TTYtter from a terminal by entering this command.

`ttytter`

This command will generate a link when run for first time. Open this link to authorise the app. After the authorisation, a PIN would be generated. Enter this PIN on the terminal and go tweeting.
 

---
layout: post
title: "Journey with Linux"
description: "This blog post is about various linux tips and tricks, hacking new things."
category: linux
tags: []
---
{% include JB/setup %}

When we start using some new technology, we get learning more and more as we keep using it. In this blog post, I write about various new things, tips, tricks, tools I learn in linux. I keep updating this post from time to time as learning process should never stop.


###Accessing root graphically
When I started using linux (ubuntu), I learned about users in an linux based operating systems. root was the priveldged user who could do anything. There are many files for which we require root access to modify them. Many times, you can not change the file permissions or owners graphically.For dealing with these kinds of protected files, I always used to open a terminal and then access the particular file or directory using root access.
<p>
    <img src = "/images/linux_journey/withoutroot.png" width="300px">
    <center>Can not change permissions without root access</center>
</p>
But then I came to know about gksudo which lets you use many applications graphically along with root access. gksu is general utility program in linux which lets you run many graphical applications in root access. To install gksudo in Debian based systems, enter this command

`sudo apt-get install gksu`

Now suppose you want to access all the files in your system using nautilus along with root access. Type this in your terminal and you are done.

`gksudo nautilus`

After entering this command, nautilus file explorer opens with root access. Now, you can access and modify any file graphically. See the image.
<p>
    <img src = "/images/linux_journey/root.png" width="300px">
    <center>Now we can do anything we want</center>
</p>

Thanks for reading, will add more updates soon.

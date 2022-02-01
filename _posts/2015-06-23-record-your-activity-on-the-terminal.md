---
layout: post
title: "Record your activity on the terminal"
description: "In this blog post, I have written about a command line utility **script** which can be used to make typescripts of your terminal sessions"
category: Linux
tags: [Terminal, script]
---

Keeping track of everything you do is a good habit.
So, why not record your activity on the terminal.
You must have thought of recording your session on the terminal.

Linux provides you a command line utility named **Script** which can be used to make typescripts of your terminal sessions.
According to the Description of **script** on its manpage,

<center><img src="/assets/media/script_description.png"></center>

<p>

Script makes a typescript of everything displayed on your terminal.
It is useful for students who need a hardcopy record of an interactive sessionas proof of an assignment, as the typescript file can be printed out later.
</p>

For example, If you want to record your activity on the terminal and store it in a file, enter this in your terminal.

{% highlight bash %}
script -a recordfile
{% endhighlight %}

So, all the activity on the terminal after this command is appended to the contents of **recordfile**.
See the pictures for illustration.
<center>
<img src="/assets/media/script_demo.png"><br/>
Screenshot of the terminal
</center>
<br>

<center>
<img src="/assets/media/script_recordfile.png"><br/>
Contents of the recordfile
</center>

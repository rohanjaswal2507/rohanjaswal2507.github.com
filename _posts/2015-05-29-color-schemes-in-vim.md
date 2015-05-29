---
layout: post
title: "Color Schemes in VIM"
description: "Terminal color schemes always attract command line users. This blog post is about changing color schemes in Bash."
category: Linux
tags: [linux, bash, tweaks]
---
{% include JB/setup %}

Text color schemes always attract Command line users. **Vi** is one of the most popular and powerful command line text editor. Every linux user is fan of this text editor.

Syntax coloring makes your code look nice and as well improves the readability of your code.
coloring of various parts of the code according to the syntax of the language in which code is written always fascinates.

**VIM**( Vi IMproved ), just like other text editors offers you various color schemes.
You can set the color scheme of your choice and start coding.

To change the color scheme of your VIM text editor in Ubuntu-like distros, follow these steps.

**1)** Open your VIM configuration file with write access.

    sudo vi /etc/vim/vimrc

**2)** Add this line to the end of the file

    colorscheme delak

And see the difference.<br>
*Note: Make sure that Syntax highlighting is on*

Here, delak is the name of the color scheme. You can choose various color schemes of your choice.

To see all the installed color schemes, type this in **Command Mode**.

    :colorscheme <TAB>

Keep pressing **TAB** and you will be able to list all the color schemes available in your system.

Give colors to your code and keep coding!<br>
You can **Comment** the name of the color scheme you like most. 

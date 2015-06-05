---
layout: post
title: "Recover a lost SSH session"
description: "This post is about recovering a ssh session when you are not allowed any more logins"
category: linux
tags: [linux, ssh, unix]
---
{% include JB/setup %}

It happens many times, when we you are logged in to some remote computer using ssh and your slow network troubles you a lot. In our hostel, we have very poor infrastructure which results in a poor network.

Many times I log in to some other computer or some server, but the poor network gives a lot of pain. The problem occurs when the network disconnects and you lose your session.

It seems an easy task to login again and access the remote computer. But, problem occurs when you are allowed only one ssh session. 

To recover the ssh session and login again, you can type this command in your terminal

    ssh -n username@remotehost kill -HUP -1

This command will not log in, but kill the last session for you and you will be able to log in again. 

PS: This is not guaranteed to work in every case.

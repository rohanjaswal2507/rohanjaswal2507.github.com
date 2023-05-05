---
layout: post
title: "Large and Small Projects"
description: "Working on projects of different size and scale has different kind of impact on the learning of developers."
category: "software-development"
tags: [software-development, engineering, codebase, growth, learning]
---

<img src="/assets/media/large-and-small-codebase.jpg" alt="Large and Small Codebases"/>
<center>Image &copy; <a href="https://unsplash.com/@jstrippa" target="_blank">James Harrison</a> </center>
<br/>

After working on several projects of different scales, built on different technologies, built for different kinds of users, I have seen the effects on the learning they have on me and other engineers around me.
In this post, I will mainly talk about **"large projects"** and **"small projects"**.
**"large"** and **"small"** here refer to the size of the codebase and infrastructure.

When I joined my first company, I had the chance to work on two codebases simultaneously.
One was a huge monolith and the other one was a small microservice.
I have similar projects in the current role as well. Both kinds of projects help you learn different things.
The impact on different aspects of Software Development of these projects is different.

**1. Building things from scratch** 

If you’re working on small projects, you learn to build things from scratch better and faster.
There are lesser and only the important components to manage and worry about.
For example, if you want to learn how to deploy applications on kubernetes, you will refer to a project that has minimal and essential things needed to deploy an application on Kubernetes.
Having smaller k8s manifests to refer to, will help you better in learning to write k8s manifests for your new projects.
On the other hand, large projects have many other things which are of no or little importance in smaller and new projects.
For example, Caching, a new project might not have a very urgent need of caching.
So, for a new developer who’s trying to build something from scratch would have one less thing to learn/worry about while getting their project up and ready.

**2. Better understanding of core/fundamental technologies**

By core/fundamental technologies, I am referring to Databases, messaging queues, web-servers etc.
With the exposure to these core technologies via smaller projects, engineers tend to learn and understand them better.
For example, if you have to add nginx as a web-server to your application and if you refer to a large project that could be using nginx for many other things like load-balancing, reverse-proxy etc, then the numerous amount of config can be a bit overwhelming to you.

**3. Large codebases can make you craftsmen**

Large, or Grown-up projects introduce newbies to standard and best practices, common pitfalls to be avoided, scaling and several other optimization strategies.
While coding smaller projects, developers tend to ignore some basic principles, and do not pay that much heed to the importance of design patterns.
It’s okay since not everything from the “textbook” needs to be taken care of right away.
But, it’s important to learn and practice them if you want to grow and build bigger and better things.
We all might have studied OOPs in our courses, but most of us really understand and more importantly “adapt” it only when we work on large codebases where you can’t get things done without following the principles properly.

**4. Learning from others, collaboration**

In large projects, you are exposed to more of other people’s work.
You get to collaborate with other teams more. There’s a transmission of ideas and learnings.
Everyone evolves and grows together and the same mistakes are less repeated.
Besides that, working in an atmosphere like that helps you improve your people skills too.


These have been a few of my observations so far.
Maybe other people look at things differently, they could have different approaches at work and they could have different stories to tell.


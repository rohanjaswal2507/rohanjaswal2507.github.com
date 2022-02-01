---
layout: post
title: "Setting up custom domain for Blog"
description: "This blog post is about setting up custom domains for github pages"
category: Blogging 
tags: [blogging, github pages, custom domain, ]
---

I recently set up custom domain for my blog <a href="http://rohanjaswal.in">Info Stack</a>. Although, there is a very good documentation available for doing this on github.com, but this post is going to make things easy for you. So, it goes like this.

To add a custom domain for your github pages or projects, you need a custom domain first. I got mine from <a href="http://dnsimple.com">DNSimple</a> under github student pack. The student pack benifited me with 2 years free subscription for this domain.

After getting a custom domain from DNSimple, you have to add your domain as an alias for your github pages. To do this, click on the services against your domain name. On the next screen, you will see many options offering various services for your domain name. Choose github pages and add your repository name.
<p>
    <img src="/assets/media/domain_services.png" width="670px">
</p>

#### Adding CNAME
`CNAME` is a file in your github pages repository which contains information about your custom domain name. In my case, this file contains

    rohanjaswal.in

So, add `CNAME` file with your domain name in it to your github repository and you are done.

Thanks for reading. Please do comment if you face any problem.

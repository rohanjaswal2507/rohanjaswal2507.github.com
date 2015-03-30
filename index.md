---
layout: page
title: Info Stack
---
{% include JB/setup %}

## Hola People!

I have recently hosted my blog on this platform. Earlier, I used blogger. My blog was hosted on <a href ="https://rohannith.blogspot.in">rohannith.blogspot.in</a>. I switched to jekyll bootstrap because I get so much simplicity and customisation here. 

##Recent Posts

{% assign posts = site.posts %}
{% assign listing_limit = 5 %}
{% include JB/post_list.html %} 

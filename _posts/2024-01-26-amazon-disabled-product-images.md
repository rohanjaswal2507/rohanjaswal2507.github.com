---
layout: post
title: "Amazon disabled product images for associate shares"
description: "Amazon has disabled product images for associate shares. This change led me to go the old way to render images for books on my website."
category: "blogging"
cover_image: "/assets/media/bookshelf.jpg"
tags: [books, books-shelf, amazon, APIs]
---

<img src="/assets/media/bookshelf.jpg" alt="A bookshelf">
<div class="img-caption">Photo by <a href="https://unsplash.com/@anetakpawlik" target="_blank">Aneta Pawlik</a></div>


I have created a <a href="/books" target="_blank">page</a> on my website to list the books I have read.
It is supposed to be like a bookshelf or library that we have in our homes.
I love to browse through the books people have in their homes.
I have always been fascinated by the books people read.
The display of books plays a vital role in sparking thoughtful conversations.
As books shape our thoughts and personality, it also helps to understand the person better.

Since we are in the digital age, I thought of creating a digital library for myself.
The idea had struck me while I was living in Delhi.
One of my friends had come to my home and he saw the books I had.
We had a great conversation about various coding practices after he saw <a href="https://amzn.to/495Liyv" target="_blank">“The Pragmatic Programmer”</a> book in my collection.
A couple of days later, he texted and asked me to send me the Amazon link to buy the book.
And that’s when I thought of creating the bookshelf.
I also had worked on a similar project during my college days with my friends.

So, I created a page on my website to list the books I have read.
Since I needed the book cover images, I explored a few options to do that.
And they were:
1. <a href="https://www.goodreads.com/api" target="_blank">Good reads API</a>
2. <a href="https://developers.google.com/books" target="_blank">Google books API</a>
3. <a href="https://affiliate-program.amazon.com/resource-center/how-to-build-amazon-affiliate-links?ac-ms-src=rc-home-card" target="_blank">Amazon associates links</a>

I tried the first two options but went with the third one.
There were a couple of reasons for that.
First, as expected, the APIs worked with an API key.
I didn’t want to deal with that in a static website.
Second, the good read API didn’t offer a convenient way to get the cover.
While Google Books API did, Google Books didn’t have an easily accessible way to buy them.
It does offer a link to search the book on various platforms, but they didn’t return reliable results.
For example, some search results only had Kindle editions while the paperback edition was available on Amazon.
The Amazon associates links didn’t look any promising at first glance either.
There was no API, but they offered a way to create a link to the book with a cover image.
They have to tool to create embeddable snippets of code that could be used to display the book cover.
All my requirements seemed to be met with this option.

So, I went ahead with Amazon associates links.
However, recently, I noticed that the images were not being rendered.
I checked and found that the image links were not working anymore.
I thought maybe Amazon had made some changes to the links.
Probably, they have changed the domain, path, or something.
So, I went to the Amazon associates page and tried to create a new link.
But, the tool didn’t offer any option to create a link with an image.
The only option was to create a text link.

<img class="img-with-border" src="/assets/media/broken-books-page.png" alt="Broken bookshelf" loading="lazy">
<div class="img-caption">Broken image thumbnails on Bookshelf</div>

I searched on the internet and found that Amazon has disabled the images for the associate links.
I couldn’t find the official announcement, but there were a few articles on the internet that mentioned this change.
Amazon probably had sent an email to the associates about this change.
Some opportunists have also created a tool to convert the old links to the new ones.
For example, <a href="https://www.blogfixer.com/fix-amazon-broken-image/" target="_blank">this one</a>

However, I had no limitation on using Amazon associates links.
So, I revisited the various options I had.
I tried the Google Books API again, but it still did not offer a way to buy the book.
So, I went the old way.
I retained the links from Amazon associates and used the Google Books API to get the book cover.

<img src="/assets/media/books-markdown.png" alt="Links in markdown" loading="lazy">
<div class="img-caption">Separate links for images and books in Markdown</div>

As mentioned earlier, I didn’t want to deal with the API key in a static website.
So, I wrote a small script to get the book cover from Google Books API.
At first, I thought of just getting the image links and updating the markdown files.
But, then I thought what if those links break as well in the future? So, I decided to download the images and store them in the repository.
I also wrote a small script to update the markdown files with the image links.

<img class="img-with-border" src="/assets/media/fixed-bookshelf.png" alt="Fixed Bookshelf" loading="lazy">
<div class="img-caption">Fixed Bookshelf</div>


Feel free to comment, get in touch if you have any interesting ideas involving books or like to have a conversation about the book that you love.


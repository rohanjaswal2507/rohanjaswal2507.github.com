---
layout: post
title: "Integration of BioJS components in IPython"
description: ""
category: 
tags: []
---
This summer I am working with <a href="https://biojsnet.herokuapp.com">*BioJS Foundation*</a> under <a href="https://summerofcode.withgoogle.com/">*Google Summer of Code programme*</a>.
My project is to create a specification that integrates BioJS visualisation components in IPython.
<a href="http://jupyter.org/">*Jupyter notebook*</a> is the best platform to practice interactive computing and is most used interactive computing platform used for IPython.


So, the approach to integrate all these components is to create jupyter widgets for each biojs component.
Jupyter widgets make the use of <a href="http://backbonejs.org/">*backbone.js*</a> which helps in creating a communication channel between Python and Javascript which helps Python code to execute some javascript in the browser.
The main challenge lies in programming the behaviour of all these widgets.
Visualisation of a component in jupyter notebook seems an easy task as backbone.js helps a lot in that by creating models and views that can be worked upon with both Python and JS.
But, real challenge is to program "How the widget and widget class object would react with user".
By this, I mean that people have been using all these components in javascript.
Now, the coding practices in javascript are little different from that in Python.
So, I have to take care that using these widgets in Python is very much similar to their usage in javascript.


One more challenge in the project is to handle and work with various data structures.
Luckily, <a href="https://github.com/ipython/traitlets">*traitlets*</a> help very much in this. But, still I have to work a lot in syncing that data between python and javascript.
For example, many biojs components use JSON in very complicated and complex way which makes it very difficult to deal with that data in Python.
So, some tweaks are required to use that data in Python and then work with it.
This happens in other direction also. Certain data in a python program has to be modified before it is provided to the javascript counterpart of the widget.


So far, I have been able to visualise two very popular BioJS components in IPython. Here is the link to github repo: <a href="https://github.com/rohanjaswal2507/biojsIPython">*biojsIPython*</a>

These are <a href="https://msa.biojs.net">*MSA*</a> and <a href="http://js.cytoscape.org/">*cytoscape.js*</a>.
The visualisation of these components in Ipython looks like this.
<center><img src="/assets/media/msa_import_from_url.png" width="100%">*MSA displaying a sequence*</img></center>
<center><img src="/assets/media/cytoscape_basic_drawing_example.png" width="100%">*Basic graph drawing using cytoscape.js*</img></center>

Now, I look to wrap up one more biojs component and then work on including more features of these components in the specification.

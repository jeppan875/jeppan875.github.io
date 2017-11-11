---
layout: post
title:  "Static site generators"
date:   2017-11-11 13:01:29 +0100
categories: static site generators
---

Is a teqnique to automatically generate a template for a site. It allows you to 
very quickly set up a site and have it running. A lot of code gets generated so 
the initial startup of a site runs much quicker. This site uses [jekyll](https://jekyll.com) 
and their standard template called minima. 

Static site generators have the benefit that they can take different file formats like markdown, 
html, and build a static site. For instance are all content on this site written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

Static site generators are very beneficial for smaller, content based sites where no databse is required. 
There are no realtime content. 

There are no user-interface for creating or changing content which will require the user to be more technical. 

### Partials
Just like css pre processors you can use partials or in this case "includes" which is reusable code that are 
isolated to a single file. For example you can have a single file for footer, header, navigation etc that are 
imported to each page. This way when you want to change something in the footer or header the changes will 
automatically apply to your whole site.


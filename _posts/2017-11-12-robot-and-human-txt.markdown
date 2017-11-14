---
layout: post
title:  "Robot and human text"
date:   2017-11-12 20:21:29 +0100
categories: Robot and human text
---

Robot.txt is a text file that is used by robots that traverses webpages. A robot can have different tasks. 
For instance google has a robot that index html documents that will be used in their search engine. 

There are different names for robots like spiders and crawlers. They are essentially the same. 

The main instructions given to the robots in the robot.txt is wether you want them inside your site. 
You can give instruction to allow specific robots and only allow them to visit certain areas of your site. 

A very important point to make is that the robots can ignore your robot.txt. 
Bad robots that searches websites for emails to spam would most likely ignore robot.txt. 

Robots you most likely want to visit your site are search engine robots. These will index your site in a
database so it can appear in searches through their search engines. 

The easiest way to make search engine robots visit your site is telling them directly you exist. 
With googles you can do it through https://www.google.com/webmasters/#?modal_active=none . 

Human.txt is a text file telling who created and contributed to the creation of a site. 
Its only purpose is to inform who created the site which doesnt have to be the same as a site owner. 

Both the robot and human txt file should be placed in the root directory of your site. Robots look at them by starting in the homepage, example: 
http://yourdomain.com/place-them-here .
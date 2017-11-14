---
layout: post
title:  "Making my site social"
date:   2017-11-12 21:21:29 +0100
categories: Making my site social
---

An easy way making your site more interseting for visitors is by letting 
them comment on the content you added. This might be on articles or blog posts 
for instance.

### Disqus
On this site I added an addon called disqus which allows users to make comments
on my blog posts. To add this to your site you need to visit [disqus homepage](https://disqus.com/) and 
become a member of disqus. Then you can choose different options on how to implement it. I simply choosed 
using the raw script code and added it to the end of the post.html file in the layouts folder. This way visitors 
can add a comment to my blog posts.

### Open graph
Open graph is a tool that allows you to share your site content on social media. For instance people can 
like your content on facebook by liking it. 

I added open graph to my site by inserting the following code in my head.html file in includes folder

{% highlight html %}
  <meta property="og:title" content="{% if page.title %}{{ page.title | escape }}{% else %}{{ site.title | escape }}{% endif %}" />
  <meta property="og:type" content="text" />
  <meta property="og:url" content="{{ page.url | replace:'index.html','' | prepend: site.baseurl | prepend: site.url }}" />
  <meta property="og:image" content="/img/caipi.jpg" />
{% endhighlight %}
---
layout: post
title:  "Pre compile css!"
date:   2017-11-10 13:01:29 +0100
categories: pre compile css
---

With the help of css pre-compiling we can expand the way we use the css language. 
The most significant benefit is that this allows for a more reusable code. 

This site uses *sass* as a css pre compiler. 

I will demonstrate two examples the benefits with using pre compiling with sass 
which I will refer two as scss.

### Variables

With variables we can finally store our values and reuse them wherever they are needed. On this 
site there is a main.scss file that stores variables that can be reused in other files. example: 

{% highlight scss %}
// main.scss, colors for links
$link-color:      #09a2d1;
$hover-color:      #3b17bd;
//_base.scss
a {
    color: $link-color;
    text-decoration: none;

    &:visited {
        color: darken($link-color, 15%);
    }

    &:hover {
        color: $hover-color;
        text-decoration: underline;
    }
}
{% endhighlight %}

### partials

This leads us into another feature called partials. Partials are files that are part of the sites css code. 
They are used to easier separate the code. A partial file starts with an underscore _. In our case _base.scss
is a partial file. Unlike other programming language were a base class would be inherited by other classes
the partials imports to a "main" scss file. On this site that is main.scss. They do this because they will compile 
into one single css file when the site launches. This is how it looks like in main.scss:   

{% highlight scss %}
// main.scss
@import
        "base",
        "layout",
        "syntax-highlighting"
;
{% endhighlight %}

You might have expected that _base.scss would import from main.scss but that is not the case with sass. 

### disadvantages
Even if the goal of using css pre compiling is to make code easier to read and less complex there are some 
things to be taken into consideration. Debugging might become a problem because the lines that your code are in
the browser will not match with the code you written since your written scss code compiles to a css file. However, 
there is a solution for this called source-mapping where a file is created when the project is built that have the 
extending .map. With the help of this you will find the corresponding lines in your code from the debugger. 

Another factor to take into account is that setting up the site requires more tools when using css pre compiling. 
I think this is something that is just hard the first few times for a beginner then it wont become an obstacle. With 
the help of css pre compilers you are allowed to write smarter code that are easier to change and maintain.

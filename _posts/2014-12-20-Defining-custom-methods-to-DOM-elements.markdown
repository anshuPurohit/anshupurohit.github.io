---
layout: post
title:  "Defining custom methods to DOM elements?"
date:   2014-12-20 17:45:10
categories: jekyll update
---

We can add custom methods to a dom element as per our needs. since dom elements are objects, methods can be added to their class and object of that class can access those methods. 

For example lets add custom method to DIV. <br>Methods are <br> 1. Visible <br> 2. Invisible

So we’ll add these methods to HTMLDivElement. All the div elements are objects of HTMLDivElement. custom methods can be added using prototype feature of Javascript.

JavaScript Code:
{% highlight js %}
//adding custom method to HTMLDivElement
HTMLDivElement.prototype.visible = function(){
	this.style.visibility = 'visible';
};

HTMLDivElement.prototype.invisble = function(){
	this.style.visibility = 'hidden';
}

//accessing custom defined methods
var section = document.getElementById('section');
section.invisible(); 
section.visible();
{% endhighlight %}

this whole concept is based on javaScript Protype functionality which allows us to incoparate OOPS concept in our 
code .

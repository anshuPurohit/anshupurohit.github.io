---
layout: post
title:  "How to center elments with CSS ?"
date:   2014-12-20 17:35:10
categories: jekyll update
---

<h3>INTRODUCTION</h3>
In this blog post we are going to cover techniques to center an element with css,Often i have seen that many developers some times find it difficult to center a element using css if it is not positioned static.so we are going to look at how to center an element that is positioned relative or absolute.

<h3>Horizontally centering an Static postioned element</h3>
To horizontally center an element we can take the help  of  css margin property.so what we need to do is to assign the below css property on the element we want to center horizontally.

CSS:

{% highlight css %}
div.block{
	width : 300px;
	height : 300px;
	margin : 0 auto;
}
{% endhighlight %}

so first of all we need to assign width to element we want to center ,height is optional you can leave it to default 
now assign margin: 0 auto; it will assign top and bottom margin to 0px and auto to left and right of the element,and it will center the element  according to the available space to its left and right. 


<h3>Horizontally & vartically centering an absolutely positioned element</h3>
The technique shown above to center an element goes out of context if element is not positioned static.In order to center an absolutely positioned element ,first we are going to look at the formula we are going to use ,i know its math but hold on its simple.

First lets consider a container div and box div inside that container.Dimensions of container are 500px X 500px,and of box are 100px X 100px; container's background color is gray and box's background color is white.

CSS:

{% highlight css %}
.container{
	width : 500px;
	height : 500px;
	background : #333;
	position : relative;
}
.box{
	width : 100px;
	height : 100px;
	position : absolute;
	background : #fff;
}
{% endhighlight %}

Formula used:

{% highlight js %}

X = parent width
Y = elements width
left = ( X - Y ) / 2 

A = parents height 
B = elements height
top = ( A - b ) / 2

{% endhighlight %}

So lets first horizontally center the Box ,according to formula left = 500-100/2 = 200px and top = 500-100/2 = 200px;
now apply top : 200px; and left : 200px; this will horizontally and vertically center the element.

CSS:

{% highlight css %}
#box{
	width : 100px;
	height : 100px;
	background : #fff;
	position : absolute;
	top : 200px;
	left : 200px;
}
{% endhighlight %}

<h3>Dead centering an absolutely positioned element</h3>
Lets pick the above example and tweak it for absolutely centering an element.In order to do so we are also going to assign left margin and top margin on the absolutely positioned element box. 

first assign negative left margin that is half of the width of Box Div  ( i.e -50px ) and then assign negative top margin that is half of the height of the box Div ( i.e -50px ).and this will dead center our element.

CSS:

{% highlight ruby %}
#box{
	width : 100px;
	height : 100px;
	background : #fff;
	position : absolute;
	top : 200px;
	left : 200px;
	margin-left : -50px;
	margin-top: -50px;
	margin-right : 0px;
	margin-bottom : 0px;
}
{% endhighlight %}

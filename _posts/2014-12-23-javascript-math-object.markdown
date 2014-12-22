---
layout: post
title:  "JavaScript window.Math object"
date:   2014-12-22 20:35:10
categories: jekyll update
---
In JavaScript multiple advance mathematical calculations can be performed by using an <br> object called `Math`.

<h3>Absolute Value<h3>
{% highlight js %}
Math.abs(21) //output: 21

{% endhighlight %}



<h3>Square Root</h3>

{% highlight js %}
Math.sqrt("25"); //output: 5

{% endhighlight %}

<h3>Rounding Numbers</h3>

{% highlight js %}
//Math.round(value): rounds the value to the nearest integer
Math.round("54.33"); //output: 54
Math.round("54.73"); //output: 55

//Math.floor(value): rounds down the value to the nearest integer
Math.floor("23.55"); //output: 24

//Math.ceil(value): rounds up the value to the nearest integer
Math.ceil("23.55"); //output: 24

{% endhighlight %}

<h3>Exponential Calculations</h3>

{% highlight js %}
Math.pow(6,4); //output: 1296

{% endhighlight %}

<h3>Maximum and Minimum Numbers</h3>
{% highlight js %}
//Math.min() returns the smallest value
Math.min(4,62,2,4.5); //output: 2

//Math.max() returns the largest value
Math.max(4,62,2,4.5); //output: 62

{% endhighlight %}

<h3>Sine function<h3>
{% highlight js %}
Math.sin("45"); //0.8509035245341184
{% endhighlight %}

<h3>Cosine function<h3>
{% highlight js %}
Math.cos("63") //0.9858965815825497

{% endhighlight %}

<h3>Random</h3>

{% highlight js %}
//Math.random() returns a random fractional number between 0 & 1
Math.random() // output: 0.7429756715428084

//Random number between 0 to 10
Math.floor( Math.random() * 11 ) //output: 3
{% endhighlight %}

<h3>Constant Values</h3>

{% highlight js %}
Math.PI //output: 3.141592653589793

Math.SQRT2 //output: 1.4142135623730951
{% endhighlight %}


---
layout: post
title:  "Introduction to CSS Media Queries"
date:   2015-04-19 20:34:10
categories: jekyll update
---
Media Queries allows us to define how a website or web-app will be presented on different
media or output devices like a mobile device or desktop screen. We can do this by defining conditions that tests the certain features of the output device and apply the css to the elements dynamically.

We can write `logical expressions` to test for `viewport width`, `resolution` or a `device width` and `height` etc.

Note: Smartphones uses a `virtual viewport` to fit the entire webpage on the small viewport. so for media queries to work we need to include a meta tag with name set to viewport and content set to device-width in our HTML doc HEAD section. 

{% highlight html %}
	<meta name="viewport" content="width=device-width">
{% endhighlight %}

<h3>There are few ways we can include media queries in our page:-<h3>

<h4>1) Using @media rule: </h4>
@media specifies the media type we want to target like screen, tv, handheld, projection & print etc and define the expression to check like max width, min-width etc.
{% highlight css %}
@media screen and (max-width: 768px) and (min-width: 481px){
	/*styles*/
}
{% endhighlight %}


<h4>2) Using Link Tag: </h4>
we can create different style sheets and link them to the HTML document using the link tag.

<strong>Disadvantages:-</strong>
<ul>
	<li>We need to include multiple link tags for queries.</li>
	<li>Multiple requests to the server can impact site performance.</li>
	<li>Media Queries style sheets are still downloaded even if the media queries return false.</li>
</ul>

{% highlight html %}
	<link rel="stylesheet" href="abc.css" media="screen and (max-width: 768px) and (min-width: 481px)">
{% endhighlight %}

<h4>3) Using Import Directive: </h4>
we can create different style sheets and link them to the HTML document using the link tag.
<br>
Imports can also be expensive to site performance because each import rule is a separate server request.
<br><br>
{% highlight css %}
	@import url("abc.css") screen and (max-width: 768px) and (min-width: 481px);
{% endhighlight %}


<h4>Examples of Media features and logical operators to adapt a layout to different viewport:</h4>
{% highlight css %}

/* targeting the device orientation */
@media only screen and (orientation:portrait){
	/*styles*/
}

@media only screen and (orientation:landscape){
	/*styles*/
}	

/* targeting the device width */
@media only screen and (max-device-width: 480px){
	/*styles*/
}

/* targeting the screens that are not b/w */
@media not screen and (monochrome){
	/*styles*/
}

/* print styles */
@media print{
	/*styles*/
}
{% endhighlight %}



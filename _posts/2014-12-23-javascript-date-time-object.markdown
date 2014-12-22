---
layout: post
title:  "JavaScript Date object"
date:   2014-12-22 20:35:10
categories: jekyll update
---
JavaScript provides `Date` object in order to work with date & time.

Getting the current Date:
{% highlight js %}
var currentDate1 = new Date();
//Tue Dec 23 2014 00:51:26 GMT+0530 (IST)

var currentDate2 = new Date(1419276181112); //Passing time stamp as argument
//Tue Dec 23 2014 00:53:01 GMT+0530 (IST)
{% endhighlight %}

Getting the old Date:
{% highlight js %}

var OldDate1 = new Date(1994,4,5); 
//Thu May 05 1994 00:00:00 GMT+0530 (IST)

var OldDate2 = new Date(1994,4,5,17,5);
//Thu May 05 1994 17:05:00 GMT+0530 (IST)
{% endhighlight %}

Getting the month, day, year etc & Setting the Date:
{% highlight js %}
var date = new Date();
// Tue Dec 23 2014 00:55:26 GMT+0530 (IST)

date.getFullYear() //2014
date.getDay() //2
date.getMonth() //11
date.getDate() //23
date.getTime() //1419276306824

date.setMonth(4)
//1400787055354
console.log(date)
//Fri May 23 2014 01:00:55 GMT+0530 (IST)
{% endhighlight %}

Comparison between Dates:
{% highlight js %}
var date1 = new Date(2003,2,7);
var date2 = new Date(2005,6,1);

//Checking which date is older
date1 < date2 //true

//Checking if two dates are same or not
date1.getTime() === date2.getTime() //false

{% endhighlight %}
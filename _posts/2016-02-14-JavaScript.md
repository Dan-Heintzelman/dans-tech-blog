---
layout: post
title:  "Ruby vs. JavaScript"
date:   2016-02-14
categories: ruby JavaScript
excerpt: "For this discussion, I am going to talk about Ruby Hashes vs Javascript
Objects."
---


### You say Tomatoes, I say Javascript

For this discussion, I am going to talk about Ruby Hashes vs Javascript
Objects. The reason I think it's important to discuss this is because
they LOOK very similar, but the way they are accessed is quite
different.

### Ruby Hashes

Ruby hashes can be written in many ways actually. Here are two common
ways.

**First Way - Using Hash Separator.**

{% highlight ruby %}
hash = {  :fname => "Dan", :lname => "Heintzelman",  }
{% endhighlight %}

**Second Way - Using just the symbol to separate key/value.**

{% highlight ruby %}
hash = {  fname: "Dan", lname: "Heintzelman",  }
{% endhighlight %}

To access the value of my first name, I have to use hash[:fname]. The
key goes between brackets.

### JavaScript Objets

Everything in Javascript is an object, so I think it is important to
demonstrate this.

{% highlight JavaScript %}
var objectDan = {      fname: "Dan",         lname: "Heintzelman",       height: 6      }
{% endhighlight %};

Notice how similar the object literal construction of both the hash in
ruby and the object in Javascript. However, instead of using brackets to
pull the value, in Javascript, you have to use dots. To access my
firstname, I would have to call `objectDan.fname` . This “fname” is a
property of the object Dan. One of the keys to understanding JS is that
every object has properties. If you don't make a property for it, it
doesn't mean they don't exist. Also, dot notation can be used to call a
function that lives within a property.Let's add a property that is a
function to the object objectDan.

{% highlight javascript %}
var objectDan = {      
	fname: "Dan",
	lname: "Heintzelman",       
	height: 6,          
	printName: function printName(){
		console.log(this.fname + ' ' + this.lname)    
		}   
	};

objectDan.printName();   // this prints to the console Dan Heintzelman `
{% endhighlight %}

See how that works? It's important to note that when I call a function
using the dot notation, I must put empty parenthesis after the function.
If it requires an argument value, then I can inlcude the values within
the parenthesis.

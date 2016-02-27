---
layout: post
title:  "Enumerable Methods and How They Act!"
date:   2016-01-31
categories: ruby enumerables
---

## Method Acting - Be the Method!

As most of you probably know, the art of method acting is about learning
to act like a role by become that role! When I first heard the concept
of an **Enumerable** method, I had no idea what it meant. I'm assuming
most of you reading this have just learned what it is, so I don't think
it will hurt you to get some resolidification (hopefully that's a word),
of the subject matter.

An enumerable is a module with a collection of methods that get *Mixed
in* with other classes. I think of this as being like a tool belt for a
superhero. A superhero may have innate abilities such as super strength
or laser vision, but the tool belt gives them added abilities.For
instance, both of the classes Array and Hash include the enumerable
module, so we know that methods such as `.map`, and `.collect` are able to
be called on objects with the class **Hash** or **Array**. Admiral Array and
Heroic Hash both make excellent heroes, but with their enumerable
methods, they are unstoppable! There are quite a few enumerable methods
out there, but I am going to choose one to discuss about in detail
today. Please check out your [Ruby docs
reference](http://ruby-doc.org/core-2.2.3/Enumerable.html) to read about
all of the enumerable methods currently out there.

### My Super Enumerable - .Select

A very useful enumerable method I'm going to teach you today is the
`.select` method. Select comes in both destructive! and not destructive
varieties. It's job is to run the code you specify between the code
block {code here} on every item in the object and return only items that
return true after running the code. I will demonstrate a commonly used,
but very helpful bit of code to return even numbers

{% highlight ruby %}
super_array = [1,2,3,4,5,6,7,8,9,10]
super_array.select { |num| num % 2 == 0 }
=> [2, 4, 6, 8, 10]
{% endhighlight %}

There you have it! One quick line of code and you can pull out thousands
of even numbers from an array. If you want to store them in a new array,
you can go ahead and assign the result to a variable. Otherwise, if you
prefer to change the value of super\_array to the newly returned even
numbers, you can use `.select!` instead!.

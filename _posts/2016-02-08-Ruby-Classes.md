---
layout: post
title:  "Ruby Classes"
date:   2016-02-08
categories: ruby classes
excerpt: "In order to understand the value of classes in Ruby, its important to
understand why we would use a class."
---

### School's out For Summer

If you have read my blog posts before, you know that I love to use
analogies to describe how things in the programming world work. As I was
pondering the yonder, I realized that my analogy for this blog post
would be quite simple! A ruby class can be compared to a class room of
students!

In order to understand the value of classes in Ruby, its important to
understand why we would use a class. Let's get back to the classroom,
shall we. Every class room in a school is going to have many of the same
different kinds of attributes. Chairs, Students, lab equipment,
teachers, etc. We know that it is inherent to a classroom, that we have
these things. However, the value of these things is likely to be
different between classrooms. (Unless the teachers and students are
being cloned of course.) I don't have to create a new variable for every
new teacher, or every new student, or every new piece of lab equipment.
With a class structure, I define a class that accepts these inputs and
allows them to be modified on many different instances (classrooms) in a
cinch! Let's get to the code, shall we.

#### Classes are Classy with Code

{% highlight ruby %}
class Classroom

def initialize(student_count, seats, teacher,microscope_count,frog_legs)
	@students = students
	@teacher = teacher_name
	@seats = seats
end

attr_accessor :student_count
attr_accessor :seats
attr_accessor :teacher_name
attr_accessor :microscope_acount
attr_accessor :frog_legs

def enough_seats
	if @seats >= @student_count
	puts "You have enough seat(s)!"
	else
	seat_req = @student_count - @seats
	puts "You need #{seat_req} extra seats!"
end
end

#Driver Code

# dans_class = Classroom.new(3,2,"Mr D", 5, 6000)
# dans_class.enough_seats
#output = You need 1 extra seat(s)!
#dan_class.seats += 1
# dan_class.enough_seats
#output = "You have enough seats!"

{% endhighlight %}


As you can see here, Mr D's classroom needs 1 extra seat. This can now
easily be tracked among many different classrooms. Think about what
other things can be done here. The attr\_accessor will allow the user to
change the values outside of the class. So if I need to fire Mr D, I can
do so, or if I need to add more chairs to the “inventory” of this
classroom, I now can easily, outside of the class. I hope thius helps to
solidify your understanding of classes!

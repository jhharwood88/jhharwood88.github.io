---
layout: post
title:      "Ruby, Self, and You."
date:       2019-12-17 18:58:18 +0000
permalink:  ruby_self_and_you
---

Every object in Ruby, regardless of type, is aware of iteself. These class based objects needed a way to reference the specific object in question, and thus we have the self. Self allows a function to access a specfic object and draw information or make modifications to it. 

While used in the global scope of the project self refers to the class as a whole, but while used inside of a function it can reference the specific instance of the object in question. Using the self keyword lets Ruby know that we are either speaking directly to the object in question or referenceing the class object in general. 

When you’re operating within the Class, you’re working with class variables and class methods.


```
Class example
   def test
	     @example = "heres an example"
	 end
	 
	 def run_test
	    puts "#{self.test}"
	 end
	 
end

```

Now with the method we created in this example class we have access to the variable inside of the class. Because the class variable of test is available to our full class, it can be called when invoking the run_test method. This allows instances of a variable to be used throughout a class, and called specifically without having to have the instantiation of the object occur within the method itself.


I hope this helps you to better understand the uses of self. The use of self is prevelent in Ruby, and similar concepts are used in almost every OO language. These methods and concepts are key building blocks as you continue to learn the Ruby language and have lasting effects on how succintly and effiecntly your code can be run. These principles are important to any developer, regardless of thier experience level. 

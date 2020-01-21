---
layout: post
title:      "Understanding Scope"
date:       2020-01-21 22:12:52 +0000
permalink:  understanding_scope
---


Scope is a key piece of understanding any given programming language, it determines how your variables interact with the rest of your code. In certain instances, this can be rather straight forward, but with languages like JS where anonymous functions and event handling features can come with their own unique set of complications. This can cause issues when dealing with scope when developing your applications. 

Scope is the ability to access certain varialbes, functions, or objects in specific areas of your code when being executed. Basically, scope covers the availability of variables and function in differing sections of your code.

There are many types of scope, some ones ill be covering in this blog are:

Global scope
Local scope


- Global Scope 

Variables defined outside any function, block, or module scope have global scope. Variables in global scope can be accessed from everywhere in the application.

Variables defined in the exterior of a function or block have global scope. Variables in global scope can be access from anywhere in the application. 

@@petName = "benji"


def function 
   *** inside this function, the global variable petName can be accessed
end

- Local Scope

Local variables have Function scope: They can only be accessed from within the function.
Local variables can only be accessed within the method they are being defined within. They can only be accessed within the functions they are called in. 

 * outside of the function, calling petName would return an error

def myFunction 
   petName = "benji
	 * the variable petName can only be accessed within its local method of myFunction
end


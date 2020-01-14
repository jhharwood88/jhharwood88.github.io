---
layout: post
title:      "Conditional Logic in UI"
date:       2020-01-14 23:38:40 +0000
permalink:  conditional_logic_in_ui
---


Conditional statements have long since been used to help determine what a users input will generate, moreso in the form of menus and selctors that the user will be able to choose from based on the UI. There are many applications in which conditional statements can be used to help improve the user experience. I personally have used a conditional statement when building out a UI to determine wether a user was logged in or viewing the page as a guest, if they were logged in as a recognized user a conditional statement built into the CSS identifier would change certain colors of certain icons and selectables to indicate that they could be accessed by a known user. 

While the previous example is rather specifc i will show how a generalized answer can be applicable in regards to helping improve the user experience. 


```
user_choice = gets.chomp

if user_choice == 1 

   do some stuff
	 
elsif user_choice == 2
   
	 do some other stuff
	 
end

```

This sort of conditonal logic allows the developer to adjust to the multiple selections a user might make from a text based input selection as well as a drop down based selection where the selectors were numbered. These allow for greater flexibility and user friendly interaction given that they will not be needed to call the action they specifcally were wanting, instead being able to choose from a list or menu for their desired function. 

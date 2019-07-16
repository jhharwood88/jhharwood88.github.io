---
layout: post
title:      "JS Project"
date:       2019-07-16 20:54:25 +0000
permalink:  js_project
---


    For my JavaScript project I changed the index and show of one of my classes to render the pages using JS instead of Rails. While this was probably one of the more straight forward projects out of the ones previously completed, there were still times i hit snags. 
		
		One of my most frustrating moments came from an error not based in the code i had supplied but in validations I had set in my previous project. I was returning a JSON object for the Item class, which should have had a couple values displayed and nothing else. Instead i was getting returned a full page of HTML, with no sign of the JSON object. This was especailly frustrating because I had gotten the JSON return working the previous day and had come back to make some minor changes to an unrelated section of the project only to have one of the main requirements break. It took me a couple hours of googling and looking at the return before i finally caught my mistake. When i was passing the JSON object back to the controller to create the new item, I hadnt considered that it had instanciated the object into my database. What this was doing was when trying to use the same object, without realising it had existed, i wasnt actaully returning the JSON because when trying to submit the values i was hitting a validation error which was then returning the whole HTML for the page with added error messages rather than the object. It wasnt until i read the HTML that i realized it had error codes included. 
		
		This just goes to show that even with a project that was previously working and a function that was previously working as planned its still important to read every return carefully - especailly those that dont make sense.

---
layout: post
title:      "The Benefits of Clean Code"
date:       2019-12-10 21:28:25 +0000
permalink:  the_benefits_of_clean_code
---


Recently, during a review of a technical code challenge I was presented with some new knowledge which I had never previously considered, and afterward gave me a new appreciation for and understanding of why we write our code as clean and concisely as possible. 

For the challenge, I was asked to write a basic text editor that could perform 4 different functions. At first, I simply wrote the code out to satisfy the problem without any extra context or functionality. After submitting my code for review, I was told that while this was done correctly, I needed to bring a more thoroughly flushed out and functional project back for the code challenge to be considered satisfied. 

After a couple days reworking and developing an interface I had my code submitted and ready for review. When I heard back, it was a bittersweet situation. While I had not provided enough of a solution to warrant progress in the hiring process I did at least leave with a better understanding and some technical knowledge I didn't possess before starting the challenge. 

The main flaw in my program, came with my CLI based user interaction. I had structured the interface around a while loop, continually looping back on itself until a specific entry would break that loop and allow the user to exit. The way I had allowed for multiple user inputs was by calling the method itself, after it had performed its intended operation. What I wasn't aware of, was how exactly the practice of recursion inside of my application would be cause for problems down the road. Based on the multiple calls, the buffer for the application would slowly start to fill and eventually cause a buffer overflow effectively crashing the application. I found that by removing the call back to the method itself and instead removing each function into an associated class would allow for the application to not only shorten its call stack but help improve the overall separation of concerns. With the addition of being their own instances of a class, each call to the main menu would then allow new functions to be added or modified without the need to find the specific method within the menu method. This would mean for any updates or additional features, no changes would need to be made to the menu but only new classes added to the application.

While I was aware of the need for separation of concerns, I had yet to encounter a reason to have such separation until then. It was a good experience all in all, a way of looking at a problem I wasn't even aware that I was causing down the road. 


---
layout: post
title:      "Git: Or how i learned to stop worrying and love the merge"
date:       2019-12-03 22:25:27 +0000
permalink:  git_or_how_i_learned_to_stop_worrying_and_love_the_merge
---


So im sure most anyone here is fimilar in some way with a content management system. They are the nice little applications that handle all of our versioning needs by allowing multiple people to collaborate remotely on a project, while still maintaining a singluar version of a code base. 

While there are many flavors to version management, such as github, gitlab, etc, they all have thier own unique values and special features. While my personal favorite has been github, there are plenty of options out there if you were looking to branch outside of the github universe. Despite thier differences their true power comes in how they are all alike, or even more so how they keep you and your fellow developers code bases all in line with each other. The ability for a team to be able to work atonomously on code, submit a pull request and have it reviewed by fellow developers before its then pushed off into production is incredibly important and valuable to both the developers and the platform its being implimented in. 

Some of these benefits include being able to test the code against preformed unit tests to determine if the code being implimented works correctly as well as will be able to be implimented without breaking anything in the current code base. It also help to allow fellow developers a chance to make suggested changes or correct flawed logic or operation before the code will become live. This can prove invaluable in the real world, as once things are implimented it can be a much more difficult job to take services offline to correct a serious flaw.

As much power as it gives us, it also comes with a signifigant responsibility. Those who are reviewing code have the commitment to provide expedious as well as succinct information and corrections where needed as to allow the developer to move onto more pressing matters. It also requires some amount of teamwork and coordination, especialyl in the real of working on a code base simulatneously. In this arena we encounter the much dreaded merge conflit, where two developers have made changes to a singluar file and neither one has the ability to merge their code into the maste codebase until the conflict is resolved. 

While this can be annoying it solves a major issue of a divergence from a unified codebase where in one persons code may directly reflect changes only to their local copy and therefore invalidate or even break code that is being developed by antoher collegue. These merge conflicts can sometimes be more difficult to resolve, but content managment systems have become better over the years at identifying the code that is causing the conflict and allowing developers to work together to resolve these merge conflicts. The true power of git, and its various repository managment systems is a cornerstone to any devlopment process and will continue to be in the future as far as I can tell.

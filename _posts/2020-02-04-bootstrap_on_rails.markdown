---
layout: post
title:      "Bootstrap on Rails"
date:       2020-02-04 21:57:03 +0000
permalink:  bootstrap_on_rails
---


Bootstrap is a framework that makes it easy for a developer to impliment their own designs on a website or web application. With predefined classes, styling your css choices for componensts such as lists, forms and widgets becomes much more simpler. The framework also allows JavaScript intigration, which makes creating things much easier than before. The bootstrap teams documentation is thorough, giving examples for most of the components Bootstrap provides.

Bootstrap comes with a detailed getting started guide, although its setup on a Rails environment differs from their website so a seperate guide would be needed to begin instalation.

When intigration bootstrap, its necessary to have a functional base rails application, which can be created using the scafforld function to quickly make the application. Once the application is created, migrate the data and seed in some dummy data to check that its displaying properly.

When you are using a framework such as Bootstrap, a CSS preprocessor is going to be involved. They enhance the vanilla CSS and add functionality such as use of variables, mixins and nesting of rules. Let’s look at two popular CSS preprocessors.

When using frameworks such as Bootstrap, CSS preprocessors are going to be used to enhance the base CSS and give added functionality to different aspects of the website/application. Bootstrap is written in LESS, but SASS can also be used when difinig CSS elements. The main differences are the particular way they are written, with SASS being less verbose and using whitespace to define its elements. SCSS can also be used, similar to SASS it will differ from LESS but will also have similarities versus regular SASS. While Bootstrap is written in LESS, it has been ported to SASS and is currently supported by the Bootstrap team. 

Now its time to add the Bootstrap Gem to your Rails project.

```
gem 'bootstrap-sass'
gem ' autoprefixer-rails'

```
Autoprefixer isnt required, but I found it to be helpful. It adds the correct vendor prefixes to your CSS code upon compilation. After the gems have been added, run 'bundle install' to complete the gem instalation. 

Its at this point we will rename our regular app/assets/stylesheets/application.css file to accomidate the SASS filetype by changing it to application.css.sass allowing us to import Bootstrap assets. By adding in 

```
@import "bootstrap-sprockets"
@import "bootstrap"
```
To our application.css.sass file, it will render imported assets where the @import statments are upon compiling. 

The final step will be to incorporate the JS bootstrap elements into the project, this can be done by modifying the app/assets/javascripts/application.js file as so:

```
//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require bootstrap-sprockets
//= require_tree .
```
Make sure the //= require_tree . is located on the last line of the application.js file, it is responsible for compiling the other JS files in the JS directory and subdirectories. If it requrires other files before hand, scripts may not ahve access to the Bootstrap functions.

At this point you have fully integrated Bootstrap into your working Rails application. 

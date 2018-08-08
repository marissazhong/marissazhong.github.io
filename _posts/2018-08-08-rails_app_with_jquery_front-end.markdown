---
layout: post
title:      "Rails App with JQuery Front-End"
date:       2018-08-08 21:50:23 +0000
permalink:  rails_app_with_jquery_front-end
---


To recap, my rails app was a Recipes Manager app that allowed users to create new recipes and store them in the database. They could also see other users' recipes and manage their virtual "pantry" which, when filled, showed which recipes they could make with those ingredients. 

For this project, I built upon the Rails work I had done previously to add more features. In fact, without realizing it I had already implemented some dynamic features in my recipes and pantry form, where I allowed the user to add an extra row (for ingredient or direction) without reloading the page. In reflection, I think these aspects of building the app are so relatable, as we are all users of very similar products and have a level of expectation for user interactions. 

I am happy to report that I was able to implement the following new features to improve the user experience:
* A "Show Your Recipes" button that rendered the user's recipes on the index page.
* A "More Info" button that rendered additional information about the recipe on the index page.
* The ability to see your new recipe immediately after submitting (rendered on the same page).

---
layout: post
title:      "Sinatra Portfolio Project"
date:       2018-07-24 18:53:54 +0000
permalink:  sinatra_portfolio_project
---


After surviving the NYC marathon last year with a severe lack of training, I decided that I should dedicate more effort to improving my running performance and give marathons another go (a very ill-advised order of events for any would-be marathoners). As part of this effort, I continue to try to reduce my addiction to added sugar and processed foods.

My Sinatra app is in the spirit of this effort. Aptly named "Five A Day", I built a simple online grocery store that includes a small database of items that would parallel any store's catalog of products. This app includes user features that require user creation and login. Each user can create, edit, or delete shopping carts. As users shop, they can choose from the items in the store and add them to the cart of their choosing. Of course, users are unable to see other users' carts. Items can be added to multiple carts. Each cart displays the list of items and the total price.

As I worked to implement the different features of the app, of course I saw certain shortcomings in how I had setup my app. For example, intially I had the app only include items and users models, with a many-to-many relationship between the two. This worked to an extent, however I quickly realized that this organization was insufficient for a store app. While in practice we probably only have one shopping cart at a time, I found working in the users controller to implement all the controller actions to be cumbersome and in violation of the principle of single responsibility of each controller and class. In addition, I thought that in the future to implement the ability to add multiple quantities of the same item, a separate class to hold any given user's items was necessary. As it stands, the cart class is equivalent to any type of list class, like if one wanted to have wishlists in addition to the shopping cart. 

As with any project, as I was implementing different functionalities I thought of various other features that would be necessary to work towards commercial release of such a product:
* Add multiple quantities of the same item
* Choose different sizes of types of same item (ie flour has white and whole wheat) (this comes down to just having a larger database of items)
* Name or partial name matching for certain items (so users can still find the correct item with slightly different phrasing)
* Improved CSS layout
* Of course, CHECKOUT! 

Stay tuned for future improvements... 

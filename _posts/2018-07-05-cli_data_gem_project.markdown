---
layout: post
title:      "CLI Data Gem Project"
date:       2018-07-05 22:52:04 -0400
permalink:  cli_data_gem_project
---


As I was brainstorming ideas for this project, I was in the middle of baking a batch of cupcakes for a 4th of July party. I've baked more cupcakes in my lifetime than I can count. What better idea then, I thought, than to aggregate cupcake recipes from different baking blogs? 

There's something about cupcakes that I find most fun to make... their size makes them the perfect candidate to bring to the office or gatherings to share, and also more significantly lends to an infinite number of variations to try making! There are various websites and blogs that I have scoured over the years for better and new recipes, from user-submitted websites like AllRecipes or Genius Kitchen, to professional websites like Martha Stewart and NYT Cooking. Scattered all over the internet are also blogs run by individual home bakers where I've found some of my favorite recipes. 

For this project, I decided to take three home baker blogs (Natasha's Kitchen, Sugar Spun Run, and Sally's Baking Addiction) and scrap their websites for cupcake recipes. To keep things relatively simple, I decided to contain the project to three basic categories - vanilla, chocolate, and 'other' cupcake recipes. This could easily be expanded to include other flavor categories such as fruit, carrot, etc. 

When starting this project, I relied on the Learn.co CLI Data Gem Walkthrough to inform me as to the file structure of a gem. From that framework, I first built a basic CLI that prompts the user to enter numbers of an ordered list and then I built a Cupcakes class that scrapes the blogs for the pertinent information and creates new cupcake objects to store that information.

By building the CLI first, I was able to map out the basic functionality that I wanted the gem to have. First, the user would be able to choose the category of cupcake recipe (vanilla, chocolate, or 'other') that they wanted to see. Then, the gem would display an alphabetized list of recipes of that flavor scraped from all three blogs. Next, the user could choose which recipe in particular from this list that they wanted to see. The gem would then display the ingredients and directions for the recipe, scraped from the appropriate page for that particular recipe. Finally, the user can choose whether to see another recipe or to exit the program. Then within the Cupcakes class, I built out scraper methods for both levels of scraping (list and detail) as well as a method to create a new Cupcake object for each scraped recipe. 

As I continued fleshing out the functionality of the gem, I realized areas for improvement and development that I worked to implement, such as:
* Initially I built the gem with the individual cupcake recipes as collections of hashes. Later on, I reimplemented these as objects. However, I kept the recipe attribute (ingredients and directions) as a hash. If the gem is expanded in the future to encompass more complex recipe parameters, I would also implement the recipes as objects.
* I noticed as I was working on the CLI that I was calling the scraping methods every time the user entered their desired category. This is less than ideal as that means if the user chooses to pull up multiple recipes the gem will scrape the page multiple times. I therefore split this call out to a separate method `scrape_recipes` that was called in the general `call` method - and therefore only once per program run.
* After initially implementing the scraper methods for the list view (list of recipes), I noticed a lot of repetitious code in creating each cupcake recipe object for the three baking blogs. Moreover, the CSS selectors were exactly the same between Natasha's Kitchen and Sugar Spun Run. Therefore, I implemented one joint scraper for recipe ingredients and directions for Natasha's Kitchen and Sugar Spun Run. I also created a `create_cupcake` class method which eliminated repetitious code between each individual food blog scraper method.

Looking forward, there are many areas in which I could implement enhanced functionality:
* Scraping more baking blogs
* Adding more flavor categories
* Adding additional parameters like yield, baking temperature, and baking time
* Implementing the ability to scale recipes to your desired quantity
* Building in grouping of similar recipes

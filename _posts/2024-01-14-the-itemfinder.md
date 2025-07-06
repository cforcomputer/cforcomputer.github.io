---
layout: post
title: The Itemfinder
slug: the-itemfinder
---

skills used:
- python
- apis
- sql
- sveltekit

*Project code is private (sorry)*

![Itemfinder tool picture](assets/images/projects/itemfinder.png)
*The original itemfinder tool built in Python*

### The problem

The company that I work manually searches Ebay for item listings, in order to source and restock inventory. Since listings are not the same on every ebay site (DE, US, IT, etc.), the sourcing team has to check every site. Furthermore, many of these items have different SKU codes, these slight variations are all the same item. However, they must search for each SKU code invdividually.

It can take days to search through all the sku codes for a set of items. It is labor intensive and an employee must click through every page to find the best deals.

### The solution

#### I present! The itemfinder!

[![itemfinder demo](assets/images/projects/itemfinder-svelte.png)](assets\videos\itemfinder\itemfinder.mp4)

Now instead of 5 hours, the average search takes less than 20 minutes. The time savings are approximately 74% for single SKU item searches, and over 93% for multi-SKU searches.

The Itemfinder started out as a barebones python application, but over time the purchase team continously asked for tweaks and updates. After installation and admin rights were restricted as a part of an IT update, I had visitors at my desk every few days asking for updates on when it would work again. The purchase team said that they didn't want to work anymore without it! 

The best solution that I found was porting the Python program into a webapp. I'd heard a lot of good things about Sveltekit, so I decided to learn how to use it for this project. This way nobody would have to download and install software, they could just access the tool from their browser, and all updates would be handled remotely.

The original python application would only use the Ebay API to retrieve live listings. With the API search it is very specific and sometimes is missing local listings, so in order to be absolutely sure all listings are retrieved, it combines the results from over a dozen different webscraping bots. The bots collect data from all major competitor websites.

The bots I've built up over my two years at JC-Electronics and the most important ones like Ebay run multiple times per day. These bots collections over 20 million different product listings PER DAY. The results are run through the scraper's parsers and the data is prepared inside multiple Alteryx workflows. The final data is uploaded to a central datawarehouse running MySQL.

The most valuable improvement that I made was the ability for the purchase team to make a combination search for products with multiple SKUs. They can create a list for a product, then click search, and if the title matches a "convert code" then it will search for every item in the convert code list and combine the results, filtering and sorting by price. Some items have over a hundred potential combinations (convert codes), and before this tool they would have to search each one individually, checking every competitor website and ebay site for the best prices. All of this now is done automatically.


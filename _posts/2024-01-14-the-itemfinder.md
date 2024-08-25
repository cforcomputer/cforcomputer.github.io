---
layout: post
title: The Itemfinder
slug: the-itemfinder
---

skills used:
- python
- apis
- sql

*Project code is private (sorry)*

![Itemfinder tool picture](assets/images/projects/itemfinder.png)

**The problem**

The company that I work manually searches Ebay for item listings, in order to source and restock inventory for refurbishment and resale. Since listings are not the same on every ebay site (DE, US, IT, etc.), the sourcing team has to check every site. Furthermore, many of these items have different SKU codes, these slight variations are all the same item. However, they must search for each on invdividually. On average, it takes about five hours to search for all combinations of SKU codes for an item. There is a better to do this!

**The Solution**

I present! The itemfinder! Using the Ebay browse API, we can grab the listings from every site. Then, using a database of codes for each item, we can run a search for every combination, aggregate them into a single list, remove duplicates, apply custom filters, and convert currency, and then sort by price :)

There are additional features, to search, and receive notifications for new listings only, and more are being requested and added.

Now instead of 5 hours, the average search takes less than 20 minutes. The time savings are approximately 74% for single SKU item searches, and over 93% for multi-SKU searches.
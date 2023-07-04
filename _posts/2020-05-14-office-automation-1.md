---
layout: post
title: automating an annoying work task
slug: office-automation-1
---

skills used:
- python
- html

[view project code](https://github.com/cforcomputer/work-auto-script-inthenews)

The problem
I was assigned a repetitive task as office work. It must be completed each day, but the level of importance of the task is low compared the duration of time required to complete it.

News articles about the university must be gathered from across the internet, then formatted in HTML line by line. On top of that, the articles must match the required sentence case structure, so each line must be checked for consistency. The result is several hours worth of wasted time every day.


**The Solution**

Using python, I built an application to automatically check every line for consistency using ReGex. The code is simple, using a for loop to run through each line. I used Kivy for the user interface and decided to call the program Newser.

The finally result is an application where you can paste in the data gathered by the crawler and immediately receive your fully checked and validated news articles to be pasted into the university website. Usually I wouldn’t have bothered to make a GUI with Kivy, but I decided to do so that other office employees with the same task could benefit from my work.

When I left my job during the pandemic, I was asked by my supervisor to show the staff how to use the application. Ultimately, much time was saved.


### photos
![newser-before](assets/images/projects/newser1.jpg)
![newser-after](assets/images/projects/newser2.jpg)
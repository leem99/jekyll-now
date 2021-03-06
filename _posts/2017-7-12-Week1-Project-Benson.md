---
layout: post
title: Metis Week 1
---

## Full Speed Ahead: Project Benson

#### About Metis

I am currently enrolled in a 12 week immersive data science boot camp operated by [Metis](https://www.thisismetis.com/faq) in San Francisco. Throughout the course of the bootcamp, students learn the fundamentals of data science, namely statistical inference and machine learning (supervised, unsupervised, natural language processing). Students also learn about data collection, data cleaning and storage, and data visualization. All of the course materials are taught in using Python. 

Our days start around 9:15 AM with a "paired program exercise". We work in randomly assigned pairs to complete brain teasers (usually revolving around statistics or computer programming), in order to reinforce the course material and get our brains firing on all cylinders. From about 10:30 until noon we got through a formal lecture. We then break for lunch from noon until 1:30. On some days there is another brief lecture in the afternoon. Otherwise we focus on our projects for the remainder afternoon, until about 6:00 PM. Throughout the boot camp there are four assigned projects, and a final, self-assigned, "passion project." For the final three weeks of the bootcamp, we will focus on exclusively on our final projects.

#### Project Objectives

As previously mentioned, Metis uses a project based curriculum. The first project is group based, and is completed during the first week of the program. This project, code named project Benson, revolves around New York City subway turnstile data. Once every four hours, each turnstile within the subway system records how many people entered and left the system through it. The data from all turnstiles are sent to a central database, and the records are made publicly available by the Metropolitan Transportation Authority (MTA) on a weekly basis.

The original problem statement was to use [MTA turnstile data](http://web.mta.info/developers/turnstile.html)
to help a fictitious non-profit  optimally place street canvassers for gathering signatures. In order to keep things interesting, each team was encouraged to tweak the problem statement and investigate a slightly different problem.  My team decided to help an imaginary food cart chain, The Brothers Falafel, optimally place food carts in order to maximize revenue. 

A goal of this project was to get us familiar with many of the tools that we will be using throughout the remainder of the boot camp, mainly the python packages pandas, numpy, and matplotlib. Another goal was to get us practicing exploratory data analysis. As a former NYC resident, proponent of both mass transit and falafel, and overall data geek, I had a lot of fun with this project. 


#### Data as Messy as the Subway Itself

When my team first sat down to analyze the MTA data set, it was a bit daunting. We felt like tourists trying to decipher garbled conductor announcements and weekend service changes, without ending up 20 stops away from our destination. Some of the biggest challenges we faced were the result of errant turnstile counts and the MTA’s haphazard labeling of data. We quickly learned that an important part of being a data scientist is being able to gather, clean, and interpret messy datasets. 

The turnstiles are sort of like a car odometer; however instead of counting miles traveled, they count total passengers. However, unlike an odometer which neatly rolls over at a million miles, or 100k if its really old, these meters can unpredictably jump up, or down. In order to counteract these outliers, we removed all negative passages counts. We also removed passenger throughputs that we deemed impossible. We said that the “theoretical maximum” throughput of a turnstile was one person every two seconds. While, by no means did this methodology remove all data outliers, it got us to a point where we could analyze the data and make meaningful observations regarding trends in usage. 

Nevertheless, the bigger issue ended up being the MTA's lack of consistency when labeling data. My team wanted to aggregate the turnstiles by station. However, there are many stations with duplicate names, for instance, I used to live near one of four stations called 125th Street. The MTA did not assign each subway station with a unique ID. In the end, we decided to aggregate our data by the field called “Remote Unit”. Smaller stations were comprised of a single remote unit; whereas, larger stations were comprised of many remote units. Functionally, this was the same as subdividing the largest stations into smaller substations. This seemed reasonable for our use case. Telling our customer to position their falafel carts need Grand Central station wouldn’t be particularly useful. However, identifying the busiest parts of that large sprawling station would be. 


#### Analysis

Given that our customer was an operator of food carts, we identified which stations (more accurately remote units) had the most traffic during lunch and dinner. We were also able to identify whether people were entering or exiting the station. In case The Brother Falafel wanted to place signage in the station directing people towards their carts, we were also able to identify the busiest turnstiles within the busiest stations.

Inspired by [*Seinfeld*](https://www.youtube.com/watch?v=IFE9C7BBkTY) , we also tried to identify the busiest platforms, just in case The Brother’s Falafel wanted to install track side food carts. We made the following assumptions: 1) each train line had its own platform, and 2) Traffic within each station was equally sub-divided amongst platforms. In doing so, we determined that many of the busiest platforms were in outer borough stations served by one train.

#### Final Thoughts

* I’m glad that the groups were encouraged to modify the original problem statement. This made the project more fun. It also resulted in each team dissecting the data a little differently, and enabled the various teams to learn from each other.

* Pandas in an incredibly powerful tool for exploratory data analysis. Once we got the hang of it, many of in the queries we had (such as aggregating to daily resolution and subsetting lunchtime and dinnertime data) could be made in a line or two of code.

* Once again, the boot camp has been very fast paced. We went from reviewing basic tools (such Python, Pandas, and git) to a finished project in less than a week.






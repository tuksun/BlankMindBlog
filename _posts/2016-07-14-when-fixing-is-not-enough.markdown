---
layout: post
title: When Fixing is not Enough
date: 2016-07-14 0:00:00
type: post
published: true
status: publish
categories: []
tags: []
description: It's thinner and lean but not buff yet
# 110 marker 1234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789
twitter-body: you write here and it goes on the share for twitter
featuredimg: polar-bear.jpg #if you put an image here it goes on twitter too

author: alex
---

### Crash Crash Crash Crash Crash

Today I tried to fix the query by reducing the amount of data used within the database. You can view it if your are in the Arup githup Repo. Essentially it is flipped around and attempts to reduce the amount of strained with repetitive searches in the beacon detection database (800k documents). 

Before, it used to find all the unique detections and apply a search for through the detection database. The proble with this is that it attempts to search each and every collection meaning that if it had 5 beacons in the database it would check 800,000 X 5. Therefore we find the right detections by using a `$match` `$sort` and `$group`, a simmilar methord but only displaying the correct detections. It then applies the check with the beacons database to assign the correct detections.

There are still a few bugs left that needs to be sorted out and check the quality when compared agaisnt the past. It also still breaks with the 800k database, so its probally the size since its about 12gigs.

![eww bugs]({{ site.baseurl }}/assets/when-fixing-is-not-enough/bugss.png) 

---
title: Weekend Task Searches
tags:
style: fill
color: primary
description: Question 5
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q6" text="👉 Next Question" %}

**Question 5:** *Let's say the CEO asks you if searches for tasks are up on the weekends year over year? You check the data and they are. What else do you look at before you communicate your findings?*

---
## What are we trying to learn?

My first step before checking any data would have been to ask Tim why this query is of importance to him and what specifically he’s trying to learn. That would help me understand what else I need to look at to answer his question. Digging deeper into his motivations for the query might reveal that what he’s trying to learn is much broader and he thinks the best way to learn it is seeing the increase in weekend task searches year over year, but there may be better ways to answer his question.  

## Significance of the increase

In terms of actually exploring the data, I'd first look at how significant the year on year increase is. Analytics aren’t always a binary outcome and if I were Tim, I’d react very differently if I heard searches for tasks on weekends were up by 10% over the last year compared to if they were up 200% year over year.

I would look at the absolute % increase for each year that we have been tracking events for task searches so Tim could see how we’ve been improving on the metric each year, and then I would calculate a compound annual growth rate since we’ve started collecting data to see the trend.

| Year        | Total weekend task searches | Change from previous year  |Average annual growth rate since inception |
| ------------- |-------------|-------------|-------------|
| 2012| 6000| n/a|n/a|
| 2013|25,000|⬆️ 316.67% |316.67%|
| 2014 | 95,540|⬆️ 282.16%|299.04%|
|2015|190,829|⬆️ 99.74%|216.83%|
|2016|450,007|⬆️ 135.82%|194.28%|
|2017|780,289|⬆️ 73.39%|164.74%|
|2018|991,565|⬆️ 27.08%|134.26%|
|2019|1,085,342|⬆️ 9.46%|110.13%|

<figcaption class="figure-caption text-center">The data could look something like this</figcaption>
<br>

## What's driving the growth?

This explains the what, but doesn’t explain the why. My next step would be to try attribute the percentage change in weekly task searches to a cause so that Tim has an understanding of why searches are up or down and what contributed to it.

I’d want to look at the growth in weekend task searches on a per user basis. This is a good way to see if the growth in searches are simply a result of a greater number of users, or because more of our existing users are searching for tasks on a weekend and are more engaged with the platform. If weekend task searches increased from 500,000 searches last year to 750,000 this year, suggesting 50% YOY growth, but number of users grew by 80%, the increase in search volume may actually be lower than I would expect given the user growth.

As an example, this is what I'd expect to see if the number of weekend task searches are being driven by new user growth:

<img src="https://i.ibb.co/JB3L52m/Screen-Shot-2019-12-29-at-9-16-01-am.png">
<figcaption class="figure-caption text-center">I'd want to compare YOY user growth to YOY weekend task search growth</figcaption>
<br>

<img src="https://i.ibb.co/4JRZpBL/Screen-Shot-2019-12-29-at-9-27-56-am.png" width="550" height="350">
<figcaption class="figure-caption text-center">I'd then want to look at average weekend task searches per user instead of just total volume</figcaption>
<br>

## Categorization

I'd want to get an understanding of what tasks users are predominantly searching for on weekends and how they are doing it. In terms of the 'what', I'd like to know if there is a Pareto  Principle consistent in the data. For example, are majority of users searching for a particular type of task on weekends? Since not all tasks are categorized by the Poster (e.g. users who click the '+' or 'Post a task' button on the web version of Airtasker aren't asked to put a category for their task) this might be a bit tricky and require us to string match certain search terms to attribute uncategorized posts to the correct category.

The next part of this is the 'how' - how are users searching for tasks on weekends? 'Search' is quite a broad term. This could comprise of several methods, so i'd be curious to see a breakdown of task search volume by method.

<img src="https://i.ibb.co/d66zb3Y/ezgif-com-video-to-gif-5.gif" width="550" height="350">
<figcaption class="figure-caption text-center">Logged in users searching for tasks directly via the search</figcaption>
<br>

<img src="https://i.ibb.co/K5PLjKX/ezgif-com-video-to-gif-6.gif" width="550" height="350">
<figcaption class="figure-caption text-center">Unregistered users searching for tasks via categories</figcaption>
<br>

## Weekend Distribution

With 52 weekends in a year, I'd want to know if task searches are evenly distributed across all of those or whether they peak in a select few weekends. This might help us understand what our most popular usage periods are and why. If there is some unequal distribution, perhaps it could also be attributed to seasonal factors like submitting tax returns at end of financial year, taskers having more time in their end of year holiday around Christmas and New Years or even New Years resolutions getting more people wanting to earn extra income through Airtasker.

<img src="https://i.ibb.co/J5KGd7G/Screen-Shot-2019-12-29-at-5-23-53-pm.png" width="550" height="350">
<figcaption class="figure-caption text-center">Some potential popular weekends for task searches (📝 🎄 🎉) </figcaption>
<br>

## User type

Since guest users (not logged in) are able to search for tasks on the platform, I'd be curious to know the split between weekend task searches by logged in users and guest users, especially considering the task search experience is significantly better as a guest user compared to a logged in one (I go into more detail on this in<a href="/essays/Airtasker-Challenge-Q4#ensure-a-healthy-offer-to-post-ratio-4">my response about growing active users</a>).

I'd also be interested in seeing if the task searches are from Taksers or Posters. My hypothesis is majority would be Taskers looking to make offers, but there may also be searches from Posters. They may wish to to know what similar task posts look like, have people done this type of task before and how they should price their task based on previous similar tasks.

## Weekends vs Weekday

Even though Tim wanted to know about weekends, I’d look at the same metrics for weekday task searches to understand if the data looks any different there. This could be a good opportunity to understand our users preferred timing of engaging with us. For example, if weekend task searches are higher than weekday task searches, perhaps our users find they have more time on the weekend to browse and search for tasks. In my original section where I mentioned I'd ask Tim what he's trying to learn by seeing if weekend task searches are up YOY, perhaps he wanted to know what is the most optimal time to post tasks. In that case, understanding the difference between weekend and weekday task search volumes, types of posts searched and user type would be extremely helpful to Tim.

<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q6" text="👉 Next Question" %}
</p>

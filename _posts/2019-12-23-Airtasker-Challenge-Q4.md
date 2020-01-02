---
title: Growing Active Users
tags:
style: fill
color: primary
description: Question 4
---
{% include elements/button.html link="/essays/Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q5" text="👉 Next Question" %}

**Question 4:** *Look at and explore www.airtasker.com . Feel free to download the mobile app too. What are 5 things you would do to grow active users? Include your math.*

---

{%- capture list_items -%}
Deconstructing 'Active'
Initiative 1 - More Efficient Tasker and Poster Activation
Initiative 2 - Reduce Likelihood of No-Shows
Initiative 3 - Improve Acceptance Rates for New Taskers
Initiative 4 - Ensure Assign Rates are at High Level
Initiative 5 - Tiered Progress Gamification OR Improve Trust and Integrity in Platform
{%- endcapture -%}

{% include elements/list.html title="Table of Contents" type="toc" %}

# Deconstructing 'Active'

It is important to clearly outline what the word “active” means. Whilst companies with similar characteristics may track the same metrics, there is no universal definition of an active user across marketplaces, or any software company for that matter, as every company has a different context. I do believe though, that there are two dimensions to define an 'Active' user:

**1) Frequency** - how frequently do we believe a user should be using our product? (e.g. daily, weekly, monthly etc)

**2) Activity** - what repeated user action constitutes a user being active? (e.g. simply opening the app? Manually triggering an analytics event like clicking on a menu icon? Performing a meaningful interaction?)

Although I believe these two elements are universal, I think it's important to consider how these factors would work for both sides of the Airtasker marketplace.

## Taskers ✏️ VS Posters 🏃‍
<br>

### Frequency

I'd like to see the user distribution based on number of posted and completed tasks (Posters) and number of offers and completed tasks (Taskers).

<img src="https://i.ibb.co/XJz26vR/Screen-Shot-2019-12-27-at-2-54-34-pm.png">
<figcaption class="figure-caption text-center">My assumption of Tasker and Poster Distributions based on number of tasks completed and posted respectively</figcaption>
<br>

This is purely an assumption in the absence of quantitative data, but my hunch is that of all the users who've posted a task, a significant majority have only posted one task. Inversely, I'd say of all the users who've completed a task, majority have completed 5 or more. Considering that a posters need to get a job done is less frequent than a Tasker's desire to bid on and complete tasks to earn money, I'd expect to see Taskers being far more active in returning to the platform on a regular basis than Posters if I were to look into the data.

Since Taskers can be interacting with many job posts at once, I'd expect Taskers to come back to the app on a weekly basis to browse new jobs, place offers and check on the status of pending offers. However, Posters only need to use the app when they need to get a job done. My personal belief is that any user who comes back to Airtasker to post a task whenever they have a job that needs to be done is considered 'active', whether that's once a month or once a year. I'd be very interested in slicing our Poster distribution data to know for users that have posted more than one task, what the time distribution of that was. E.g. do most of these users post quarterly, semi-annually, annually etc. I'd want to see this for users since Airtasker's inception as well as by cohorts to see users across different time periods (e.g. over the past year). For simplicity sake, I'm going to say quarterly active users for Posters. Even though that can be quite a long time-lag of measurement, I believe we would miss out on users who infrequently come to Airtasker to get a job done just because a shorter time span like 'monthly active users' is a more standard metric.

I’d also have very different usage expectations for Posters with an active task and those who don’t. I was using Airtasker multiple times a day when I had a task posted but not nearly as frequently when my task was completed. I'd say weekly active is an appropriate measure for Posters that currently have an active task which Taskers can bid on.

<br>
### Activity

It's critical we ask ourselves what threshold of activity a user needs to have to consider that session as valid for our active user metrics. In general, I think there are 3 options we can use as our benchmark for active users returning for a session:
1) User simply returns to the app or website (this means if a user opens the app then leaves instantly, they'd still be considered an active user)
2) User returns to app or website and fires at least 1 analytics event (eg. Changes tabs in mobile app, clicks a button etc.)
3) User returns to app or website and performs a meaningful interaction (e.g. searching for a job, clicking on a job post, placing an offer, clicking 'post a task' etc.

Obviously, the lower the threshold of activity required by us to attribute a user as ‘active’, the better our metrics look on paper. However it may not be indicative for a user coming back and getting value from the platform, so I generally prefer being quite “harsh” in our assessment of an active user. To some external stakeholders I think it's okay to use number of users returning to the site/app as the measure (as this is technically correct), but internally we need something more reliable to help us understand the true health of our marketplace.

To summarize how I would categorize our active users:

| | Frequency | Activity |
| ------------- |-------------| -----|
| **Taskers** | Weekly | Performs at least one meaningful Tasker event: e.g. search for a task, clicks on 'browse', clicks on a job post (in app or notification), places an offer|
| **Posters without an active task** | Quarterly |Posts a task |
| **Posters with an active task** | Weekly | Performs at least one meaningful Poster event: e.g. clicks on their job post (in app or notification), views a Tasker's profile, replies to a comment, accepts a tasker, sends a message etc |

## Important considerations I have omitted

Something to note, I’m not sure how exactly we can attribute a Tasker and a Poster as our user group for active user measurement. When users create an account, they are asked whether they are here to earn money (Tasker) or post tasks (Poster).

<img src="https://i.ibb.co/5smzNfk/IMG-4454.png" width="200" height="450">
<figcaption class="figure-caption text-center">Mobile App Onboarding</figcaption>
<br>

We could use this to determine what type of user this is in our marketplace. However, there is a major problem here: <strong><u>many users are both Taskers and Posters!</u></strong>

I'd love to know what percentage of our users have:
- only completed a job as a Tasker
- only posted a task  
- both completed a task and posted a task

But even from a cursory look on the platform, many users I come across do both. The issue here is that we may not capture this from the onboarding alone. A user might sign up as a Tasker but then later on become a Poster. Although users can change this setting in their user profile, I'd like to know from our data just how many users perform this action - my hunch is that it’s minimal.

<img src="https://i.ibb.co/dQb56Gy/IMG-829013-B14399-1.jpg" width="200" height="450">
<figcaption class="figure-caption text-center">Mobile App Account Settings (hidden deep within the app I/A)</figcaption>
<br>

As such, it might unreliable to use whatever the user has categorized themselves as for measurement. <strong><u>You can’t rely on what users say. We can only rely on what they do</u></strong>. We could determine whether someone is a Tasker or Poster (or both) by some actual user activity attributes. E.g.

- Tasker: has made an offer on a task in the last week
- Poster: has created a job posting in the last 3 months

# Initiative 1 - More Efficient Tasker and Poster Activation

<strong><u>One of the most critical steps to becoming an active user is ‘activating’ on their first session</u></strong>, which involves having a meaningful first experience which demonstrates enough value for the a Poster or Tasker to come back for a second session. If they have a poor first session and leave, they’re likely to go into Zombie mode and never return.

When looking at the two sides of the marketplace, I was thinking about what would be the goal we’d want each user to achieve in their first session.

| | Tasker | Poster |
| ------------- |-------------|-------------|
|**Job to Be Done** (why they signed up)|Make some extra cash| get a job done that they don’t want to do themselves|
|**First Session Goal**|place an offer on a task|post their task |

I'd love to see our data on this, but my assumption is <strong><u>if a user is not able do complete one of these goals in their first session, it's unlikely they will come back</u></strong>. And whilst they may not accomplish their job-to-be-done in their first use of our product, getting to the 'First Session Goal' mentioned above will help get them there with the least effort.

On the Airtasker web version, we have some form of tailored onboarding. If a user selects that they're here to **Post Tasks** then they get taken to the Dashboard page, which is very much designed to get the user to easily post a task, either from the selected categories or the 'Post a Task' button. Inversely, if they selects that they're here to **Earn Money** then they immediately get the modal to take them through the verification steps to be ready to make offers on tasks.

<img src="https://i.ibb.co/x6q6S0W/ezgif-com-video-to-gif-1.gif">
<figcaption class="figure-caption text-center">Onboarding flow if user says they signed up to post a task</figcaption>
<br>

<img src="https://i.ibb.co/bH23QnB/ezgif-com-video-to-gif-2.gif">
<figcaption class="figure-caption text-center">Onboarding flow if user says they signed up to earn money</figcaption>
<br>

Interestingly, I noticed that as long as the user selects they're here to 'Post Tasks' (even if they also select they want to earn money) they will be sent to the Dashboard where they can post their task. To me, this signifies that the higher value activity for Airtasker as a business is to get more tasks posted as opposed to have more taskers making offers.

This tailored onboarding is certainly a step in the right direction of increasing the probability of users activating in their first session. However, a core issue I noticed is that <strong><u>users who register directly from the mobile app do not get tailored onboarding</u></strong>.

<img src="https://i.ibb.co/w4XWYRM/ezgif-com-video-to-gif.gif" width="200" height="450">
<figcaption class="figure-caption text-center">Mobile app takes the user to the same screen whether they're a Tasker or Poster </figcaption>
<br>

I'd want to know % of our users create an account with the mobile app? I don't have the data but a cursory look at the Google Play store shows over 500k Android app downloads. I know from my conversation with Jerome that Airtasker has 4 million users (I assume this is registered users, not active Users). That means 12.5% of total registered users are on the Android app (excluding iPhone users). One thing I don't know is whether these users were cross device users who originally created an account on web and then downloaded the app, or created their account on the mobile app.

If the latter is significant, then this is a lost opportunity, considering that all users get dumped onto the 'Post a Task' page regardless of the reason they're here. I'd be curious to know if it is technical limitations of the native OS which prevent us from having tailored mobile app onboarding

(important note: I only have iPhone and did not download the app on Android. From my cursory research, I see Airtasker has native OS engineers, so the apps are tailored to iOS and Android operating systems. However, in the absence of seeing the Android app, my responses here are under the assumption that the mobile app experience is consistent across platform.)

## Improving Tasker Activation ⚡️
<br>
### Fast verification and Reconsider the modal on first land

I'm really curious to see some funnel data on how successful this verification onboarding modal is. What % users who see it for the first time close it vs complete the onboarding and click the 'Browse Tasks' CTA? And for users who do go through it, how far do they get through the slides?

If a significant majority complete that verification, then it's very effective. However, if they don't then they just get dropped straight to the dashboard to 'Post a Task', which is probably not the best onboarding location to set a Tasker up for success. I always thought it was a really nice touch when the verification process began when the user tries to place an offer. I felt it was more effective as the Tasker is already closer to the desired first session goal of placing an offer and would likely have higher motivation to complete the verification process at that point as opposed to straight after they have signed up. The latter makes getting started with the Airtasker feel a little more lengthy and process driven while the former seems a logical step to complete the action the user wants to take. This is just qualitative inference, so i'd need to test my hypothesis by looking at the following data:
- Breakdown % of Taskers who verify through the different verification methods (Is it 50/50 or is one significantly more used than the other? Note, I would also want to see how many Taskers verify their account via their user profile instead of the other 2 methods, but I assume it would be nominal)
- Like for like comparison of the conversion rate of the 2 methods (which has the highest completion rate?)

I also noticed that the verification steps differ between these two contexts:

<u>Onboarding Verification</u>

If a user only selects that they signed up to "Earn Money", they trigger a verification modal asking for the following:
- Upload profile picture
- Select if they'd like custom task alerts
- Provide mobile number
- Write a short description about themselves
- Provide bank account details

<img src="https://i.ibb.co/Y7gygwk/ezgif-com-video-to-gif-3.gif">
<figcaption class="figure-caption text-center">Verification modal after a Tasker signs up to Airtasker</figcaption>
<br>

<u>Task Offer Verification</u>

If a new Tasker tries to make an offer and has not yet verified their account, they trigger a verification modal asking them for the following:

- Upload profile picture
- Provide date of birth
- Provide mobile number
- Provide bank account details
- Enter their billing address

<img src="https://i.ibb.co/Y2FHzdh/ezgif-com-video-to-gif-4.gif">
<figcaption class="figure-caption text-center">Verification modal when a new Tasker attemps to make an offer on a task</figcaption>
<br>

As you can see, while the offer verification step asks the user for date of birth and billing address, the onboarding verification step asks if they'd like to receive custom alerts and to write a description about themselves. I'm curious to know why we ask different questions here? It's clear that the onboarding verification is trying to set the Tasker up for future success (e.g. build a better profile with a good description and get alerts on tasks) while the offer verification step is a bit more transactional. Since we're trying to optimize for the lowest effort the user needs to submit an offer, i'd opt for the quickest verification to ensure high completion rates.

This also involves removing any bottlenecks to speed up the verification process and make it seemless. One example is a UX nit I noticed while inputting my location in the app.

<img src="https://i.ibb.co/yNCQxbx/IMG-4455.png" width="200" height="450">
<figcaption class="figure-caption text-center">Error message after typing 'New South Wales' as my billing address State</figcaption>
<br>

A simple dropdown where the user can select from pre-filled options would have been far more efficient here and more standard convention for users.

### Remove any friction points

- better communicate what happens after

### Encourage them to submit more offers

- get them going when they're on a roll


## Poster Activation ⚡️

### Tailored flows for categories

There are some tasks where if the user chooses that particular category, it goes through a custom flow for that category. I think this is actually really effective and makes the platform feel much more bespoke. But more importantly, tailoring it to each individual posting helps guide the user to post correctly and set them up for success (especially for their first post).

Something i've noticed though is that there are inconsistencies across different use cases. E.g. mobile app, web, web logged out vs web logged in.... E.g. Removalist jobs when logged out are custom tailored while logged in it is just the normal poster flow. Why is that?  I understand that it probably makes sense for acquisition to get logged out users to go through a custom flow as they aren't yet used to the platform, but why not do it for both if it's more efficient and leads to better overall post rates??

### Remove bottlenecks

- e.g. show task day of week in mobile app!

### Clear commnunication

 - Was quite nervous when posting that I was going to be charged a fee. Wasn’t clear that I only have to pay once I accept

### Ensure post adheres to best practices and is mistake free

Ensure their post adheres to best practices

### Help them decide on a fair and accurate price


<br>

# Initiative 2 - Reduce Likelihood of No-Shows

# Initiative 3 - Improve Acceptance Rates for New Taskers

2 key components of this - 1) getting a healthy number of Tasker offers on a post (a good Offers:Post ratio), 2) Making it easy to accept the right Tasker
1. A few layers here:
    1. Ensure high offer rates - get more Taskers making offers on jobs and ensuring a solid offers per post ratio
    2. Better Task Search - Eg. Filtering, categorization
    3. Better awareness of tasks that the Tasker is interested in and a fit for (e.g. custom alerts - is this under-utilised feature? Very important to get people to return and continually come back to the app)
    4. Ensure high quality posts from posters (eg. Good description, right category, correct location)
    5. Ensure the poster can easily select the right Tasker to assign (eg. Marc feedback and my feedback about difficulty selecting from 20 offers. No ability to sort etc)

Kind of related to point 4 and 5 (and maybe a bit of a counter-argument to them) but when posting a task, I found myself not wanting to use people who were ‘new’ to Airtasker and hadn’t done any jobs yet. I’d be curious to know what data we have on this (and to interview new taskers to hear if they struggled with it) to actually know if they have difficulties getting jobs as new taskers. My hypothesis is that they do, and that first time posters don’t have the same issue. My first post got 25 offers in the first day. Taskers will make offers on any job they think is suitable for them, regardless of whether the poster has been on the platform for 5 years and posted 100 tasks or 5 minutes and posted one task.

**PHOTO OF LUIS G**

This is a photo of my job post. I’m very unlikely to pick Luis ^ when I’ve got 2 others offering the same price, but have completed hundreds of jobs at 5 star ratings.

How can we increase the likelihood of first time taskers getting selected for jobs? Any tips we can help them with? Eg. Maybe they should offer a lower amount than the Poster is offering. I know you can’t go below $5 but if I was offering $10 and Luis offered $5, that would be pretty compelling. I also think the default ordering by date offered descending is helpful in not getting to anchored in the people who have lots of experience - it keeps the list quite flat and neutral (although I do think sorting would be a very handy feature to help the poster better pick the right candidate)



Improve ability to select the right candidate

- I found myself struggling to pick the right person for my job because there were lots of good candidates
- I think it would help speed up the process by Airtasker being able to highlight the best candidates from the list. Eg. Based on reviews, number of tasks completed etc, 3 candidates get selected and get floated to the top in a “Recommended” section.

# Initiative 4 - Ensure Assign Rates are at High Level

### Ensuring there are offers on your post

KEY THING: Ensure high offer rates - get more Taskers making offers on jobs and ensuring a solid offers per post ratio

Components of this:
- Better Task Search - Eg. Filtering, categorization
- Better awareness of tasks that the Tasker is interested in and a fit for (e.g. custom alerts - is this under-utilised feature? Very important to get people to return and continually come back to the app)
- Ensure high quality posts from posters (eg. Good description, right category, correct location)
- Requesting offers from good Taskers (Marc said that for the latest task he put up to fix his blinds, he actually searched for similar tasks to find people who made offers or completed tasks for people that got accepted). He was trying to find high quality candidates that are suitable for his task - perhaps we should make this easier by recommending candidates to reach out to and request quotes from! 

when logged out, posters can go to task categories and actually find top rate taskers - e.g. https://www.airtasker.com/writing/cover-letters/. Might be interesting to turn the table and encourage posters to reach out to them to get quotes (I know this is currently possible already, but it is not heavily advertised to the user)

- mention improved search for taskers - as a Tasker looking for work, I found the search experience quite limited. Although it’s interesting for ‘browsing’, the only dimension I can really filter by is whether I want it done in task or in person (and if in person, the proximity to my current location) and price. Most of the tasks I was going through were not really a fit for me. Maybe one of our aims is to get people ‘browsing’ and spending more time in the app, but if we want people to complete meaningful interactions like getting taskers to make offers, it would be better if they are looking at job postings that are highly relevant to them  
- SEARCH: on desktop, users can browse for tasks by category but on mobile web and mobile app cannot. I think this is a lost opportunity and we should consider adding it to the filtering experience on mobile. (SHOW GIF OF TASK BROWSE ON DESKTOP AND THEN TASKE BROWSE ON MOBILE WEB). ACTUALLY, IT LOOKS AS THOUGH ONLY WHEN LOGGED OUT DO YOU SEE CATEGORIES. Overall, the search experience is so much more dynamic and has so much more functionality for guest users than logged in!!

- mention here that Posters should have high quality tasks:

E.g.: good content (high quality title and description), correct categorization (online/remote chosen correctly and then ensure that they are properly categorized - currently, not all users have their posts categorized. E.g. clicking 'post a task' on web version doesn't pick a category), correct pricing (help Posters choose the right price!)


### Finding the right candidate:

Ensure the poster can easily select the right Tasker to assign (eg. Marc feedback and my feedback about difficulty selecting from 20 offers. No ability to sort etc)


# Initiative 5 - Tiered Progress Gamification


<p class="text-center">
{% include elements/button.html link="/essays//Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q5" text="👉 Next Question" %}
</p>

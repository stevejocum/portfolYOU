---
title: Growing Active Users
tags:
style: fill
color: primary
description: Question 4
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q5" text="👉 Next Question" %}

**Question 4:** *Look at and explore www.airtasker.com . Feel free to download the mobile app too. What are 5 things you would do to grow active users? Include your math.*

---

{%- capture list_items -%}
Deconstructing 'Active'
More Efficient Tasker and Poster Activation (1)
Reduce No-Shows (2)
Improve Acceptance Rates for New Taskers (3)
Ensure a Healthy Offer to Post Ratio (4)
Pricing Strategy (5)
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

We could use this to determine what type of user this is in our marketplace. However, there is a major problem here:{% include elements/highlight.html text="many users are both Taskers and Posters." %}

I'd love to know what percentage of our users have:
- only completed a job as a Tasker
- only posted a task  
- both completed a task and posted a task

But even from a cursory look on the platform, many users I come across do both. The issue here is that we may not capture this from the onboarding alone. A user might sign up as a Tasker but then later on become a Poster. Although users can change this setting in their user profile, I'd like to know from our data just how many users perform this action - my hunch is that it’s minimal.

<img src="https://i.ibb.co/dQb56Gy/IMG-829013-B14399-1.jpg" width="200" height="450">
<figcaption class="figure-caption text-center">Mobile App Account Settings (hidden deep within the app I/A)</figcaption>
<br>

As such, it might unreliable to use whatever the user has categorized themselves as for measurement.{% include elements/highlight.html text="You can’t rely on what users say. We can only rely on what they do" %}We could determine whether someone is a Tasker or Poster (or both) by some actual user activity attributes. E.g.

- Tasker: has made an offer on a task in the last week
- Poster: has created a job posting in the last 3 months

---

When looking at how I'd increase active users, I am not thinking about growing the number of users we acquire at the top of the funnel (e.g. new marketing channels and partnership opportunities). This would only increase the quantity of active users. Instead, I'd want to{% include elements/highlight.html text="target further down in the funnel at how we can get a larger % of the users we acquire to become active users," %}which would have a much larger, sustainable impact on the business long term.

---

# More Efficient Tasker and Poster Activation (1)

One of the most{% include elements/highlight.html text="critical steps to becoming an active user is ‘activating’ on their first session," %}which involves having a meaningful first experience which demonstrates enough value for the a Poster or Tasker to come back for a second session. If they have a poor first session and leave, they’re likely to go into Zombie mode and never return.

When looking at the two sides of the marketplace, I was thinking about what would be the goal we’d want each user to achieve in their first session.

| | Tasker | Poster |
| ------------- |-------------|-------------|
|**Job to Be Done** (why they signed up)|Make some extra cash| get a job done that they don’t want to do themselves|
|**First Session Goal**|place an offer on a task|post their task |

I'd love to see our data on this, but my assumption is{% include elements/highlight.html text="if a user is not able do complete one of these goals in their first session, it's unlikely they will come back." %}Whilst they may not accomplish their job-to-be-done in their first use of our product, getting to the 'First Session Goal' mentioned above will help get them there with the least effort.

On the Airtasker web version, we have some form of tailored onboarding. If a user selects that they're here to **Post Tasks** then they get taken to the Dashboard page, which is very much designed to get the user to easily post a task, either from the selected categories or the 'Post a Task' button. Inversely, if they selects that they're here to **Earn Money** then they immediately get the modal to take them through the verification steps to be ready to make offers on tasks.

<img src="https://i.ibb.co/x6q6S0W/ezgif-com-video-to-gif-1.gif">
<figcaption class="figure-caption text-center">Onboarding flow if user says they signed up to post a task</figcaption>
<br>

<img src="https://i.ibb.co/bH23QnB/ezgif-com-video-to-gif-2.gif">
<figcaption class="figure-caption text-center">Onboarding flow if user says they signed up to earn money</figcaption>
<br>

Interestingly, I noticed that as long as the user selects they're here to 'Post Tasks' (even if they also select they want to earn money) they will be sent to the Dashboard where they can post their task. To me, this signifies that the higher value activity for Airtasker as a business is to get more tasks posted as opposed to have more taskers making offers.

This tailored onboarding is certainly a step in the right direction of increasing the probability of users activating in their first session. However, a core issue I noticed is that{% include elements/highlight.html text="users who register directly from the mobile app do not get tailored onboarding." %}

<img src="https://i.ibb.co/w4XWYRM/ezgif-com-video-to-gif.gif" width="200" height="450">
<figcaption class="figure-caption text-center">Mobile app takes the user to the same screen whether they're a Tasker or Poster </figcaption>
<br>

I'd want to know % of our users create an account with the mobile app? I don't have the data but a cursory look at the Google Play store shows over 500k Android app downloads. I know from my conversation with Jerome that Airtasker has 4 million users (I assume this is registered users, not active Users). That means 12.5% of total registered users are on the Android app (excluding iPhone users). One thing I don't know is whether these users were cross device users who originally created an account on web and then downloaded the app, or created their account on the mobile app.

If the latter is significant, then this is a lost opportunity, considering that all users get dumped onto the 'Post a Task' page regardless of the reason they're here. I'd be curious to know if it is technical limitations of the native OS which prevent us from having tailored mobile app onboarding.

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

### Straight to Search

For users who sign up and say they're here to earn money (Tasker), we should be driving them to make an offer. As mentioned, I think verification is best done once they're ready to make an offer. Although I'd want to see data to approve/disprove that hypothesis, if I am correct then it is best to get users straight to the core value of the app - browsing tasks. Currently, new users only go there automatically if they complete the onboarding and click 'browse tasks'. On the mobile app, no users get directed there, as all users get dumped on the 'Post a Task' page. This s not relevant for the Tasker, so at a minimum they should at least be sent to the Browse Tasks page on registration.

<img src="https://i.ibb.co/wwZVqSr/IMG-FD3-AEBF005-FD-1.jpg" width="200" height="450">
<figcaption class="figure-caption text-center">Browse Tasks page on mobile app</figcaption>
<br>

To go even further, we could{% include elements/highlight.html text="customize the Browse Tasks page on their first land to be tailored to them, as right now it is homogenous for every user" %}One way to do this would be to ask the Tasker what their skills are or what task categories they’d be interested in completing jobs for (a simple multi-select UI) and then show them a tailored search list with those tasks that are relevant for them.

This would require proper categorization, so either having all Posters assign a category to their posts when creating one (not all posting methods on the platform require categorization), or having a smarter, more robust category detection system without the user having to input a category.

### Remove any friction points

<u>Public Comments</u>
<br>
<img src="https://i.ibb.co/1sbdvrz/IMG-0-D1-A7187-FA8-D-1.jpg" width="200" height="450">
<figcaption class="figure-caption text-center">We require all users submitting offers to write a short description on why they should be picked for the task</figcaption>
<br>

When making my first offer, I was very{% include elements/highlight.html text="nervous about whether this message would be public or not." %}I only found out after I made my first offer that it does. I had a lot of apprehension around that because I didn't really want other Taskers to see my personal message to the Poster showcasing why I'm the best for the job. My hunch is other users feel embarrassed about this too. I think this becomes less of a problem once you submit more offers and get used to the way the platform workss, but for first time users I think it's a friction point that would be interesting to explore further.

I'm very curious why we keep these comments on the platform open from both sides? Public questions on a Task I understand, but for these comments users make when they're submitting their offer, I’d be interested to test whether keeping the comments hidden from other Taskers would encourage more first time taskers to make offers. I’d be keen to run a multivariate test:
- A) control
- B) comments by default hidden
- C) comment by default on but when user makes offer they have option to toggle it off and have their message be private


<u>Communication of Next Steps</u>

When submitting my first task, I found the{% include elements/highlight.html text="confirmation screen left me in the dark about what I should expect to happen now that I've submitted an offer." %}As first time users who who don't yet fully understand the mechanics of the platform, I think we can do a much better job at informing them of what they can expect after submitting their task.

<img src="https://i.ibb.co/TwMX64q/IMG-4696.png" width="200" height="450">
<figcaption class="figure-caption text-center">Confirmation screen after submitting an offer</figcaption>
<br>

Here's an example of some copy which would be much more helpful to first time users after submitting their offers:

```
Congratulations on submitting your first offer!

What's next?

1) Jake G. will review your offer
2) If they like you, they'll accept your offer and assign you to the task
3) You'll go to a private chat with just you and Jake G. to discuss any details for the task completion
```

I actually think this has the potential to{% include elements/highlight.html text="encourage users to submit more offers" %}as they have a clear understanding of what to do next and no longer are apprehensive. We could even optimize the `Close` button to say `Browse more tasks` which sends them straight back to the Browse page. Now that they've submitted their first offer, they're warm and on a roll. We should encourage them to submit as many offers as possible to increase their chances of getting assigned.


## Improving Poster Activation ⚡️
<br>

### Tailored flows for categories

There are some tasks where if the user chooses that particular category, it goes through a custom flow for that task post compared to the regular one.

<img src="https://i.ibb.co/fvYcLnG/ezgif-com-video-to-gif-8.gif" width="400" height="300">
<figcaption class="figure-caption text-center">Airtasker web Handyman custom post flow</figcaption>
<br>

I think this is actually really effective and makes the platform feel much more bespoke and tailored to the user's context. More importantly, however, tailoring it to each individual post helps guide the user to post correctly and set them up for success (especially for their first post).

There are two things i've noticed though:

<u>Not all task categories have a custom post flow</u>

Only a select few categories have a custom flow. My hunch is that we looked at the task categories which are most popular and tried to make a quicker, streamlined and bespoke user experience for those. I'm curious to know if that is the case, if they have higher completion rates than the default one and why we haven't done it for more categories.

<u>There are inconsistencies between web and mobile app</u>

On web, only the `Handyman` category has a unique flow, while all the rest are the default. On mobile however, `Cleaning` and `Removalists` are unique while the rest are default.

<img src="https://i.ibb.co/Vw8ccCW/ezgif-com-video-to-gif-9.gif" width="200" height="450">
<figcaption class="figure-caption text-center">Airtasker mobile app Cleaning task flow</figcaption>
<br>

As you can see here, when posting in a cleaning task on the mobile app, it has an{% include elements/highlight.html text="incredibly efficient UI which pre-populates the description page based on your selections." %}However, the web version does not have the same UI. I assume that from our analytics, cleaning tasks are one of our most commonly posted categories, but an overwhelming majority of them come from the mobile app, so we only changed the app UI, not the web.

I also noticed differences in the posting flow between Airtasker web for guest users and logged in users. For example, removalist jobs when logged out are custom tailored while logged in it is just the normal poster flow. I'd like to know why that is the case? I understand that it probably makes sense for acquisition to get logged out users to go through a custom flow as they aren't yet used to the platform, but why not do it for both if it's more efficient and leads to better overall post rates?

### Remove bottlenecks

Any potential friction points that could slow down or prevent a user from completing their post should be addressed. As an example, when I was posting my task, it was a bit annoying to not see the day of the week when I was selecting my date for the task. I had to exit the app and go to my calendar to check the day.

<img src="https://i.ibb.co/y4Dd9Mb/IMG-4473.png" width="200" height="450">
<figcaption class="figure-caption text-center">On mobile, we don't show day of the week while on desktop we do</figcaption>
<br>

### Clear Communication of Pricing

Having heard that Airtasker charges a fee to posters, I was quite{% include elements/highlight.html text="nervous when posting my task that I was going to be charged a fee." %}Especially considering I'd already verified my account, it wasn’t clear that I only have to pay once I assign a Tasker. I think communicating this would reduce friction of users completing their first posts.

### Help them decide on a fair and accurate price

{% include elements/highlight.html text="Knowing how to price your task is one of the most difficult things about posting a task" %}(especially for first timers). While on desktop we give a little bit of guidance but on mobile we don't, making it very tough for new users to know how to price their task correctly.

<img src="https://i.ibb.co/pP8Jp2J/Screen-Shot-2020-01-03-at-3-47-48-pm.png" width="350" height="350">
<figcaption class="figure-caption text-center">Hovering over 'Want Help?' on Airtasker web gives some basic pricing guidance</figcaption>
<br>

<img src="https://i.ibb.co/VgrDj53/IMG-C18-CB375-E176-1.jpg" width="200" height="450">
<figcaption class="figure-caption text-center">Users left in the dark on mobile app 🌑</figcaption>
<br>
<br>

Even the hover on web is very basic and feels like it has not had much consideration. We just show a generic `small = $25/hour`, `medium = $75/hour`, `large = $100/hour`. Our landing pages even have more accurate pricing data, and logged in users never come across it!

<img src="https://i.ibb.co/4SLBPPX/Screen-Shot-2020-01-03-at-4-18-54-pm.png" width="300" height="350">
<figcaption class="figure-caption text-center">Airtasker Gardening jobs landing page pricing data</figcaption>
<br>

Even if we showed users creating a post the same pricing data we show on those landing pages, it would be far more beneficial to users than the current generic one (or, for mobile app users, no help at all!)

I've spoken to a number of Posters who, when posting a task and are uncertain of pricing, manually look through similar posts to get a better gage of how they should price theirs. There's a lot we could do to remove the manual labour for them and make it quick and simple to pick a price for their task. I'll touch on this in my 4th initiative in a bit more detail.   

# Reduce No-Shows (2)

One of the most{% include elements/highlight.html text="vital ‘health’ metrics for Airtasker as a marketplace is the percentage of tasks completed" %}as that is the biggest measure of us providing a successful outcome for a Poster and a Tasker. A healthy marketplace isn’t a platform that has many jobs available, it’s one that has many jobs completed. So I'd first want to know from a quantitative standpoint if this is a problem by seeing{% include elements/highlight.html text="what % of tasks which get assigned do not get completed." %}

This would help explain the what, but not the why. I immediately thought that it would be imperative when a user cancels their task to ask them why they cancelled it (a simple survey with 1 multi-choice question). I noticed we don’t do this on a task before it is assigned (which I think we should, as the more user behavior we can understand, the better) but was very pleased to see we do this after a Tasker has been assigned.

<img src="https://i.ibb.co/NT1npNd/support-airtasker-com.png" width="300" height="350">
<figcaption class="figure-caption text-center">Task Cancellation Survey</figcaption>
<br>

One of the quickest ways for a Poster to never come back again is to experience one of the following:

**1) Tasker isn't responding to messages**

**2) Tasker didn't show up**

I'd want to know from our survey data{% include elements/highlight.html text="what % tasks get canceled because of these two reasons." %}. Without the hard data, I’d need to try and estimate roughly how many cancellations their are due to no shows by working back from known data and some assumptions:

```
- According the Airtasker website and my conversion with Jerome, there are $15.4 million
worth of jobs available each month on Airtasker.

- Looking at median pricing data for task categories, I’ll estimate the average task price
is $100, meaning roughly 150,000 jobs are available every month.

- I’m going to assume that of those, 75% get assigned, so 112,500.

- Of those which get assigned, I’m going to assume between 5-10% don’t get completed, meaning
that between 5,000 and 11,000 jobs a month are being cancelled.

- I’ll go further and say 70% of those are due to the two reasons mentioned above, meaning roughly
3,500-7,500 jobs a month are being cancelled due to no shows or not replying to messages
($350k-$750k given a $100 average task post assumption)
```

My basis for those assumptions is the{% include elements/highlight.html text="qualitative user research I gathered which demonstrated that no shows are a significant problem" %}on the platform. In my <a href="https://clyp.it/jh021dx0?token=08ab8fd76494a9977d0f6e9b4e70a7c4" target="_blank">user interview</a>, the participant mentioned this was by far the{% include elements/highlight.html text="worst part about being a Poster and completely discouraged her from wanting to post future tasks:" %}

> “It was for a seven o'clock start and I said to them 'I realized that you have a slightly lower rating at 87%. Please say that you will show up because it's always a disappointment'. They said 'Nah I'll be there. Absolutely. bells on'. 7:30 came. 8 o'clock came. Nine texts later, no answer. 10 texts later, no anwser. Never showed, never answered, never anything.”

> "I think in of all of the tasks I posted (>10), I've actually only had one turn up when they said they would"

I've read countless online reviews mentioning the exact same thing:

<img src="https://i.ibb.co/XtHzc9r/Screen-Shot-2020-01-03-at-5-12-48-pm.png" width="450" height="500">
<figcaption class="figure-caption text-center">One of many frustrated users experiencing no shows</figcaption>
<br>

You can see more of these reviews here:
- <a href="https://au.trustpilot.com/reviews/5cff87c2b055990650f67cdd‬" target="_blank">Review 1</a>
- <a href="https://au.trustpilot.com/reviews/5c5741b697afa10ac0871b08‬‬" target="_blank">Review 2</a>
- <a href="https://au.trustpilot.com/reviews/5c67b3b897afa10b687ca2f1‬" target="_blank">Review 3</a>
- <a href="https://au.trustpilot.com/reviews/5d67859af0186906181cc7d7‬‬" target="_blank">Review 4</a>

‪
In order to address this issue, I think there are two angles to look at it:
- **Before the fact:** what can be done proactively to ensure this doesn't happen
- **After the fact:** how can we better deal with the situation when it does occur

<br>

## Before the Fact

#### Clear Task Representation

In my user interview, the participant said she has completed many tasks where the Poster intentionally misrepresented the task to make it look easier than it was.

> "The tasks are horribly misrepresented. I went to one recently where it was 'Please sort my husband's wardrobe', and it was actually 6 double wardrobes"

> "You don't even know what you're bidding on. But they are meant to give an accurate indication of what it's meant to be. And they don't. They misrepresent it quite drastically, quite often.

If there are clear expectations between poster and Tasker, there is higher likelihood of a task being completed. Maybe the number of offers on a post would be reduced but it would likely be higher quality candidates who are willing to do the job.

#### Completion Rate deep dive

It would be useful to go deeper into a user's completion rate to see what tasks got cancelled, why, and if the Poster is able to leave a review for them. That way, the Poster can have total confidence in their decision when assigning a Tasker. You could even have sorting on the offers list to allow Posters to sort by completion rate descending (essentially, most reliable to least reliable).

#### Stricter Verification             

We could look at having better verification to weed out low quality Taskers, although this could hurt other metrics like number of active Taskers and average number of offers per post.

<br>

## After the Fact

#### Replace Tasker

If the Tasker doesn't show, currently users have to repost the task and re-accept offers all over again. It would be far more convenient for the Poster to replace the cancelled Tasker with someone else from their offers list. This would make a massive difference to the Poster experience (even though they've just had a no show) if they can quickly find a reliable replacement as opposed to having to repost the task again, get a refund for the previous task, or worse, choose not to post the task again or go to a competitor because of their poor experience!

#### Harsher Punishment for No-Show

Besides lower completion rate score, we could look at more severe repercussions to users who do not respond to messages or show up for their task. In one of our <a href="https://support.airtasker.com/hc/en-au/articles/360021358052-Everything-to-consider-when-cancelling-a-task#%E2%80%9Ccompletion_rate%E2%80%9D" target="_blank">support articles</a> we mention:

> Frequent cancellations can also lead to action against your Airtasker account. Depending on the situation, your account can be limited or in extreme cases, deactivated

I'd be curious to know the specifics here, and how many cancellations due to no show and no response lead to account deactivation. Even if there was a little symbol next to Tasker's names signalling they have been unreliable in the past, this would lead to less people hiring them and make the platform have a much higher quality base of taskers, which is critical for task completion rates, our most important marketplace metric.

#### Proper Cancellation Procedure

At the moment, when a user cancels and submits a reason, the other party has to accept it. I’m curious to know what % of cancellations get accepted by the other party? I'd assume Posters and Taskers don’t want their completion rates to be affected so I wonder if many just ignore it because they don’t want the repercussions. Should we not instead be a bit more hands on and have Airtasker deal with all cancellations instead of leaving it in the hands of the users?

This would only apply if users are currently unable to settle this themselves. So I'd want to speak to customer support to know how many customer support tickets do we get about a cancellation request not being accepted by other party? As you can see by this review, the Tasker obviously rejected the cancellation even though it sounds pretty convincing that they should have accepted:

<img src="https://i.ibb.co/ZHGRv9S/Overview.png" width="300" height="400">
<figcaption class="figure-caption text-center">Poster who cancelled a task and had the reason rejected by the Tasker</figcaption>
<br>

# Improve Acceptance Rates for New Taskers (3)

One of the biggest challenges for new Taskers is getting their experience up on the platform. I've seen feedback from users about the difficulty of getting started on the platform when you have no completed jobs and are competing with more experienced Taskers. I even experienced this myself as a Tasker, struggling to get assigned for jobs when the Poster could rather assign a tasker who has dozens or hundreds of completed projects.

<img src="https://i.ibb.co/ctC6ZQH/productreview-com-au.png" width="300" height="450">
<figcaption class="figure-caption text-center">One of many reviews about the difficulty of getting runs on the board as a Tasker 🏏</figcaption>
<br>

I also experienced this on the other side when I was a Poster and had to assign one Tasker from the 25+ offers I received. My immediate way to shortlist the best candidates was to ignore new Taskers in favour of more experienced ones with completed projects and great reviews.

<img src="https://i.ibb.co/Wy4cpTd/94-Completion-Rate.png" width="250" height="450">
<figcaption class="figure-caption text-center">Luis G. doesn't stand much chance next to the other 3 candidates... 😔</figcaption>
<br>

There's plenty other <a href="https://www.productreview.com.au/reviews/a25d3b16-3849-454b-990b-1710a8e5db6f" target="_blank">reviews</a> of users echoing the same problem. In the absence of quantitative data to validate my hypothesis, for the purposes of this task I think it is evident from qualitative user feedback that first time Taskers share this frustration and it is an issue. However, in a real scenario I’d want to validate this properly by:

- **Data:**Looking at our data to see what % of active Taskers have not been assigned to or completed any tasks
   - I'd also want to break this down by cohorts to see how long it takes on average for a new Tasker to get their first job. I'd also be interested in knowing from our data if there is a specific duration of time that a Tasker will churn after if they don’t get accepted for a task? (e.g. after 1 week of no tasks assigned)
   - Break down the data by number of offers made - e.g. average number of offers a user makes to get their first job
- **User Interviews:**
   - TASKER: If the data suggests this is an issue on a large scale, I'd query our database to get a list of users who've signed up within the last 7 days, placed more than 1 offer but have no assigned or completed tasks. I'd want to speak to them about their experience to better understand the problem
   - POSTER: I'd also want to speak with Posters who have recently had a task completed where they had offers from new Taskers to understand the mindset of Posters when looking at offers from inexperienced Taskers

## Strategies to address

#### Strong Tasker profile

We should encourage first time users to build up an excellent profile based on best practices and what will increase their chances of getting hired for jobs. This can include things like:
- Professional image and cover
- Detailed description behavior
- Skills
- ID Badge verification (digital ID, mobile, police check, LinkedIn etc)
- Relevant license badges (Electrical, Plumbing, WWCC etc)
- Portfolio (if relevant)

From my personal experience as a Poster, I looked through every profile of the Taskers who made offers to look through their reviews, profile descriptions and verifications to ensure they are trustworthy and reliable.

<img src="https://i.ibb.co/09j3sQS/Screen-Shot-2020-01-03-at-9-24-55-pm.png" width="550" height="700">
<figcaption class="figure-caption text-center">Disability worker platform HireUp does a great job of guiding the user to build a strong profile</figcaption>
<br>

#### Bid strategy

For new users who haven't been assigned to a task yet, we should advise them on best practices when making their offers. There are two components to an offer:

**1) Bid**

The Tasker needs to choose how much they are willing to complete the task for. From our data, I'm interested in seeing the average spread between original task price made by poster and accepted price from tasker to understand if on average the accepted price on a task is on par, above or below the original posted price. If it is on par or above, we can advise first time Taskers to submit offers that are below the Posters price to incentivise Posters selecting them. Depending on the nature of the task, if I had a new Tasker with no completed projects offer a lower price than the other Taskers with larger volume of completed tasks, I would be pretty compelled to select them.

I'd also be curious to know what percentage of offers have Afterpay since we launched it. If the uptake has been slow, we can A/B test different messaging around why a Tasker should offer Afterpay to see if we can improve the conversion from our current design. The current `Earn more by increasing your offer and turning on Afterpay payments for Posters` is quite good but I do have some ideas around how it can be improved. E.g. If we have data showing Taskers who offer Afterpay are more likely to be accepted, we could say something like `Taskers who offer Afterpay are X% more likely to get hired`.

<img src="https://i.ibb.co/HXdrKq6/Make-an-offer.png" width="250" height="450">
<figcaption class="figure-caption text-center">Make an Offer page</figcaption>
<br>

**2) Message**

All Taskers have to send a message along with their offer explaining why they should be chosen for the task. We should be providing as much guidance here for best practices. We currently have a small placeholder example, but I think we could give more support.  

<img src="https://i.ibb.co/vHMT0Zc/IMG-84357-C14-A5-AD-1.jpg" width="250" height="450">
<figcaption class="figure-caption text-center">Halloum made a much better impression on me than Luis</figcaption>
<br>

#### Be early

I think a viable strategy for getting runs on the board as a first time Tasker is to be the first person to place an offer on a new job. We can do this with some best practice tips (e.g. a help section or during onboarding) telling them that they should regularly monitor the browse page for new tasks and try be first to offer. We could also ensure that they have normal alerts set up so that they regularly receive notifications about new tasks and even nudge them to creating custom alerts.

#### Notifications for Tasks with no offers

During this answer I've mentioned a few times knowing about the percentage of posts which do not have offers (e.g. after 1 day, 2 days, 3 days etc). The longer the duration a post has not received offers, the better the chance a new Tasker has to get the job. We could set up notifications for new taskers with no completed posts about Tasks which have no offers. This can help fix 2 problems:
- getting first time Taskers assigned to jobs
- Ensure fewer tasks receive no bids

It might even be an interesting feature to add advanced filters on the browse page, allowing users to filter for tasks which have received no offers yet. I looked at a task that had 16 offers and felt very nervous to submit an offer because of the competition! I'd much prefer to hang around the low competition posts when getting started.


# Ensure a Healthy Offer to Post Ratio (4)

As a Poster, I cannot explain the visceral feeling of receiving my first offer on <a href="https://www.airtasker.com/my-tasks/10-minute-phone-call-17994016/" target="_blank">my job post</a>. It happened about 30 seconds after my post and they just started flying in - it was my Aha moment that immediately made me undestand the value of the app as a Poster. Experiencing this stressed to me the criticality of having ensuring posts receive a meaningful number of offers.

<img src="https://i.ibb.co/PMZZjgT/IMG-4482.png" width="250" height="450">
<figcaption class="figure-caption text-center">The offers flying in for my task. My AHA moment 😍</figcaption>
<br>

Of course I'd first want to validate that this is a problem by seeing the percentage of tasks on the platform which have no offers (I'd probably split this up by number of days since post so I can see how many tasks from 1 day, 2 days, 3 days ago etc still have no offers) and tieing that to the `post_id` to do an audit of those posts and understand why they received no offers.

I believe there are 2 components to ensuring this happens:

1) High quality posts

2) Posts being discovered by Taskers

## 1) High Quality Posts

High quality posts has a far higher likelihood of getting bids from Taskers. There are a few criteria of a good post:

#### Description

I've seen some posts with pretty lousy descriptions, and as a Tasker found it far more heplful to view posts which had a well explained description of the task, and even included pictures. We should guide posters on writing a good task description based on best practices. We currently provide a placeholder text on the web version of Airtasker (which could definitely be improved to be more guiding for the user) but not on the mobile app.

If anything, we should remove the need to manually create a description by doing it for them. Some tasks on the platform have a bespoke posting flow which pre-populates the description with the optimal content and details.

<img src="https://i.ibb.co/Vw8ccCW/ezgif-com-video-to-gif-9.gif" width="200" height="450">
<figcaption class="figure-caption text-center">Airtasker mobile app Cleaning task flow pre-populates the description</figcaption>
<br>

#### Categorization

I've come across dozens of in person tasks which were incorrectly categorized by the Poster as remote (and vice versa). This is problematic because Taskers might be searching for in-person tasks only (which you can filter for in the 'Browse' feature) and would therefore miss the in-person tasks which were incorrectly categorized.

We should also ensure that all posts are categorized (either by the user when creating it, which as I've mentioned not all users do because of the different UI based on device, or via Machine Learning) so that the Taskers are able to search for them (I'll touch on this in a moment).

#### Pricing

In my first initiative earlier in this post, I discussed the current issues around how we provide little guidance to Posters on setting a correct price. I think we could significantly improve the ability of posters to correctly and successfully post their task (and, Taskers having clear pricing as opposed to having to guess what to offer) if we assisted users in their pricing. This could range so many solutions, from simplest lowest hanging fruit, all the way to robust implementation
- Simply have an option for no pricing (eg. “?”) so that Taskers browsing jobs know that the Poster wants to see what people offer
- Based on the Post category, show the user similar jobs so they can get a rough price estimate (only problem here is that currently, not all users create posts with a category. If a user clicks the core CTA + icon in the top right of the nav bar, they bypass the categorization step and go straight to posting a task)
- Give the user price bounds based on their task category (e.g. we show a median, high and low price for task categories on our landing pages, yet don't actually show this to the Poster when they're setting their price)
- Based on the post category and attributes of the Post, recommend a price or a price range for the Task using Machine Learning. With $15.4M jobs a month and hundreds of thousands of jobs completed on the platform, we have an enormous volume of data to understand what is a fair price for a given task for a given category for a given set of requirements


## 2) Discovery by Taskers

#### Improved Search Experience

As a Tasker looking for work, I found the search experience quite limited. Although it’s interesting for ‘browsing’, the only dimension I can really filter by is whether I want remote or in-person (and if in person, the proximity to my current location) and price. Most of the tasks I was going through were not really a fit for me. Maybe one of our aims is to get people ‘browsing’ and spending more time in the app, but if we want people to complete meaningful interactions like getting Taskers to make offers, it would be better if they are looking at job postings that are highly relevant to them  

<img src="https://i.ibb.co/0F3R1qF/ezgif-com-video-to-gif-10.gif" width="500" height="700">
<figcaption class="figure-caption text-center">'Browse Tasks' feature with very baisc filters</figcaption>
<br>

<img src="https://i.ibb.co/VW1Qcqr/ezgif-com-video-to-gif-11.gif" width="500" height="700">
<figcaption class="figure-caption text-center">Categories feature for non-registered users</figcaption>
<br>

At the moment, the search functionality in the app is very limited and users aren't even able to filter for tasks in certain categories. I think there are a host of filters that we could add to the search which make it far more valuable to Taskers looking to hone in on specific types of tasks they're interested in, and therefore, get them to make offers.

#### Notifications

Besides getting a Tasker to put in the manual effort of searching for suitable jobs, an even more effective strategy is notifying them about jobs they're interested in. When creating an account, we ask users if they'd like to receive notifications for tasks, however I'm not sure how effective these are, as I did not receive any notifications.

<u>Custom Alerts</u>

I discovered we have a 'custom' alerts feature which is hidden deep within the user profile.

<img src="https://i.ibb.co/Zf5wCDd/Task-alerts.png" width="200" height="450">
<figcaption class="figure-caption text-center">Our custom alerts feature.... if users can find it 🙈</figcaption>
<br>

I tested it to see if i'd start receiving notifications quickly, and voila! Within a few minutes I started receiving notifications.

<img src="https://i.ibb.co/TcPJzT3/vodafone.png" width="200" height="450">
<figcaption class="figure-caption text-center">Success!</figcaption>
<br>

There are two major problems here:

**Firstly, the feature is very hidden**. I'd like to know our analytics on what percentage of taskers have custom alerts set up, and the distribution. Eg. Of those which do have, how many have 1 custom alert set up, 2, 3, 4 , 5-10, 10+ etc. My hunch is that very few have them set up, which I think is a big missed opportunity.

**Secondly, the feature is not user friendly**. I felt I was very much left in the dark when trying to add an alert and had no idea if what I was adding an alert for would even work! If I’m putting an alert for something, how likely is it that they will get picked up and I’ll be notified on it? We could tell the user how many notifications they would have received in the last 24 hours for that alert term. Again, I’m a believer in ‘Guide, but give freedom’. We should have options for popular custom alerts (eg. Task categories and then the option to add your own.)

<img src="https://i.ibb.co/GCVb2hB/Add-custom-task-alert.png" width="200" height="450">
<figcaption class="figure-caption text-center">Add custom task alert screen</figcaption>
<br>

<u>Smart alerts from onboarding</u>

In my first initiative, I mentioned changing the onboarding experience to ask Taskers what tasks they'd be interested in, then sending them to a search list specifically filtered for those tasks. If we did change that onboarding flow, we could save those preferences and ask them if they'd like to be notified on those tasks.

#### Helping when there are no offers

My brother recently posted a task to get someone to fix his blinds in his apartment. He posted the task and had no offers after about a day. So he manually searched for similar tasks and reached out to the Taskers who had either completed it or made offers on that post and then requested quotes from them. He was performing a very manual process to achieve the following:
- Get high quality candidates that he selects himself
- increase the speed at which he gets offers so he can complete his task faster

There is a lot we could do here to reduce the likelihood of a post receiving no bids, and also remove the hassle from the Poster in the event that it does occur:
- We could replicate something similar to the landing pages where Posters can see quality Taskers for their job type/category and encourage Posters to request quotes
   - This is already a possible feature in the app, but it is undersold. I'd be curious to see data around it's usage and how many Posters request quotes directly from a user profile.
- If it's been longer than the average time to receive 1 offer, we can send them a notification or an email to help them

```
Hey, looks like your Post hasn't received an offer yet. Here are some tips:
- reduce your price to make it more attractive to taskers
- request quotes from Taskers yourself: here's a list of reputable Taskers for [category X]
- struggling to get your post in front of eyeballs? Boost your post and have it featured
at the top of the search results
```

# Pricing Strategy (5)

The final thing I'd look at to grow active users is to adjust our pricing strategy. Based on my user research, there are a few areas I think could lead to an improvement in the number of Posters and Taskers who continue to use the platform.

## Pricing Strategy 1) Consider a pricing reduction

In my user interview, the participant mentioned her continued frustration at the excessive fees on the platform.

> "Their fees have gone from 7% to now almost 44% by the time they’ve gouged off of everybody"

Numerous online reviews have confirmed that other users share this frustration:

<img src="https://i.ibb.co/6Nn7MTR/Screen-Shot-2020-01-04-at-11-38-21-pm.png " width="600" height="300">
<figcaption class="figure-caption text-center">There are countless negative online reviews about our pricing </figcaption>
<br>

You can see more of these reviews here:
- <a href="https://www.productreview.com.au/reviews/6cc11684-a971-46fb-8d7a-6cc61d05ed29‬" target="_blank">Review 1</a>
- <a href="    8. https://www.productreview.com.au/reviews/f75ac90f-01a6-4caa-996e-88fc118c7a5e‬‬" target="_blank">Review 2</a>
- <a href="    10. https://www.productreview.com.au/reviews/56603e6f-7524-4453-b91b-48848d539861‬" target="_blank">Review 3</a>

It's important to consider the context of the question here is about increasing active users, not revenue. As a PM, it's extremely important to consider the pendulum swing affect that improving one metric may have on another. So for this strategy, i'd ensure that a pricing change would try meet the optimal point at which we grow active users whilst increasing revenue, or at least maintain the same level of revenue.

<u>Taskers</u>

I'd like to see from our analytics if the number of active Taskers (or, the percentage of new Taskers who become active) has decreased since as we have increased our fees over time, and whether they increased since we made the tiered pricing change. However, from my qualitative research I would think a number of Taskers no longer wish to continue completing tasks because of the huge fees (especially those who complete mostly small tasks, say, below $50, as they may think the value for their time, ROI, is not there).

Price testing is difficult, but we could conduct some sensitivity analysis and look at some testing to understand what the optimal pricing points are which would grow active users and lead to the most revenue. I am sure significant research and analysis went into the tiered pricing decision. I am purely going off user feedback and outrage about the fees that we charge.

We could even consider dropping the thresholds on the tiers to better incentivize smaller Taskers to reduce their fees (although we'd need to model out this impact on revenue). The participant in my interview mentioned a relevant quote about this:

> “There’s a company that has 14 people completing tasks on Airtasker and are on gold tier, but for me, it’s just one person. I’m never going to be on 10%. Why should somebody at the bottom who is doing a quirky task, which is what [Airtasker’s] original thing was, be up against an actual business with a professional model and nine different people going in. That's beyond an uneven playing field. The goal posts are in a completely different country. It's frustrating how much integrity they have lost.”

<u>Posters</u>

On the posters side, I assumed (and Jerome confirmed this) that you ran a test before implementing Poster fees and found that overall it had a net positive affect, so I imagine there wasn't a reduction in number of jobs posted on Airtasker (or at least, the loss of revenue from the reduction in post was counteracted by the increase in revenue from the poster fees)


## Pricing Strategy 2) Tiered progress gamification

I think we could improve the messaging around the tiered pricing to regularly remind users of what is required for them to receive a lower fee. We currently mention to them what tier they're on, but some level of gamification might incentivize the user to complete more jobs in order to reach their goal and reduce their fees.

<img src="https://i.ibb.co/xMBtnjd/IMG-E3-E7611-D77-BA-1.jpg" width="250" height="400">
<figcaption class="figure-caption text-center">There are countless negative online reviews about our pricing </figcaption>
<br>

The content we show in the <a href="https://support.airtasker.com/hc/en-au/articles/360022973151-What-is-tiered-pricing" target="_blank">Find out how your service fee is calculated</a> help centre article is really helpful, but I'd like to know what percentage of users who have submitted an offer have viewed that page, as I'd guess the number is nominal.

Bringing some of that content out of that page and into the 'Make an Offer' page could better 'gamify' the experience of being a Tasker and reducing your fees. We could simply amend the graphic at the bottom of the 'Make an Offer' page and add some copy along the lines of `$150 more to go this month to reach Silver Tier (3.7% lower fee)`

Not only could this gamification help drive more Tasker activity on the platform, but also improve our brand image by demonstrating to users that we want them to have a lower fee. I believe our brand image is being tarnished by online reviews about our 'greedy' pricing structure, which could be stunting active user growth.

## Pricing Strategy 3) Subscription model

I know this is something that we are looking at releasing this year, and I've touched on it in much detail <a href="/essays/Airtasker-Challenge-Q10" target="_blank">here</a>. Allowing posters to subscribe to a given service or set of services on the platform would allow them to save on commission and encourage them to post more tasks. This is especially true if the tasks are small tasks, as the smaller the task, the higher the fee as a percentage of the total task.

<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q5" text="👉 Next Question" %}
</p>

---
title: Subscription Model
tags:
style: fill
color: primary
description: Question 10
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q11-Q13-mission" text="👉 Next Question" %}

**Question 10:** *Your colleague is working on a new Subscriptions model that allows a Poster to subscribe to a given service (e.g. lawn mowing). They are not sure if the Poster would be willing to commit to a long-term Subscription from the get-go. They're also concerned that once the Poster and Tasker meet in person, the Poster would cancel the Subscription to shave off a few dollars of commission. How might your colleague's team resolve these problems?*

---
## Background and Context

I'd want to gage where my colleague's team is at in the product lifecycle for this product. From the question alone, I'd assume that the team have validated that a subscription model is the right direction for the business, and if implemented correctly could bring in an additional revenue stream for Airtasker, growing our top-line sales. This is inline with my conversion with Jerome where he mentioned Airtasker's shift in focus from rapid growth to rapid profitability!

I’d start off with some{% include elements/highlight.html text="clarifying questions to better understand the current landscape of the initiative:" %}

<u>Clarifying Questions</u>

- Why are we building this feature? Does it stem from a business goal like increase revenue for Airtasker or does it stem from a customer problem like `how can we save money for the user?` or `how can we make the Poster experience quicker and more convenient for frequently repeated tasks?`.
- What are our primary and secondary success metrics for shipping this subscription feature?
- What financial impact does a subscription have for Airtasker? Do we make more money than if the user posted the task as normal or less?
- What is the core value proposition for a user to use an Airtasker Subscription? What's the benefit(s) they accrue by using subscription over the normal one-off task?
- Who is the ideal target user of this subscription feature? What are their posting behaviours?
- What exactly does it mean to ‘subscribe’ to a service? Walk me through what that would look like for a Poster and how your team envisions it working?
- Does a subscription work as a 1:1 relationship (hire the same Tasker every time) or 1:Many (ability to hire different Taskers every time but as long as it is the same task category)
- Are Posters able to subscribe to multiple services/categories (e.g. cleaning, mowing, gardening) or just one? Why/why not?
- How do we determine the subscription charge?
- What financial impact (good or bad) does a subscription have for the Poster? For the Tasker?
- Does anything about the Tasker experience change when a Poster uses a subscription?
- For each period they pay, how many services or jobs are they entitled to with that subscription payment?
- You said you’re concerned whether poster’s willingness to commit to a long term subscription up front - how long is long term? Is the planned implementation that it’s a month to month subscription? Or is it a longer term subscription like 3, 6 or 12 months?

Whilst there's a fair few questions there, having this overview of what the feature looks like right now and how the team envisions it working will help me better understand how to address the concerns.

## Concerns

Whilst the team seem clear on the impact this product could have, it sounds like they're{% include elements/highlight.html text="unsure whether customers will actually use it and are concerned about users gaming the system." %}So there are clearly 2 major hypothesis which my colleague's team needs to validate to feel secure in launching this potentially very impactful new business model:

**1) Posters will pay for a subscription to a set of services up front that they haven’t received yet but will receive in the future**

**2) Posters will not abuse the service by initially opting into a subscription, then after the task has been completed cancelling their subscription to avoid the commission fee**

I’d want to ask my colleague{% include elements/highlight.html text="where did these concerns/assumptions came from?" %}Is this something that they or a team mate thought of internally? Or is this something that has come up during User Research (e.g. User Interviews)? If this is the latter, than we can start ideating solutions to overcome the problem as we would have already validated that this hypothesis is true because it came directly from users. If it is the former, then this is simply an assumption that we need to validate by going out to users and learning from them.

<img src="https://i.ibb.co/vJwLDht/Screen-Shot-2020-01-04-at-2-28-29-pm.png" width="500" height="600">
<figcaption class="figure-caption text-center">How I'd recommend my colleague solve these problems</figcaption>
<br>

### Team Concern

As mentioned, if these are simply concerns we have internally as a team, we need to go out there and validate with users whether it is true or false. It's futile to spend weeks of design and engineering time trying to fix a problem that doesn't exist.

Really, there are only two ways to validate with users whether a product assumption is true or false. You can look at:

{% include elements/highlight.html text="1) What users say" %}

{% include elements/highlight.html text="2) What users do" %}

A product principle of mine is that you {% include elements/highlight.html text="can't trust what users say, but you can trust what they do." %}I still believe there is value in both, but a person's actions is always the better barometer of truth than what they tell you. So let's look at how we can measure the concerns my colleague has.

<br>
#### What users say 🗣

I'd suggest two possible qualitative research approaches for this:

<u>Surveys</u>

We can send surveys out to some of our users, asking them{% include elements/highlight.html text="questions specifically targeted at our concerns" %}around users not willing to commit to a long term subscription from the get go and cancelling their subscription after completing the task. I'd sit down with my colleague to go through some good questions we could ask and how to write them to solicit the best responses. As a general rule though, I'd recommend{% include elements/highlight.html text="rooting the survey questions in past behaviour as much as possible as opposed to asking about behaviour." %}. For example:

❌ Would you pay for a 1 year Airtasker subscription upfront?
   - Yes
   - No

✅ How do you pay for your subscription services? (excluding any bills like phone, electricity, gas, water)
   - Weekly
   - Monthly
   - Quarterly
   - Semi-annually (every 6 months)
   - Yearly
   - Bi-yearly (once every 2 years)
   - I don't pay for any subscription services

❌ If you only needed one task done, would you pay for an Airtasker subscription and then cancel it once the task is completed?
   - Yes
   - No

✅ Have you ever paid for a subscription and then cancelled straight after the good or service was delivered?
   - Yes (Please provide details of the experience and why you cancelled)
   - No

We can do something akin to a{% include elements/highlight.html text="Concierge Test" %}where we have a 'Switch to Subscription’ button which just opens landing page telling them about the new idea and asks them to fill out a survey in exchange for $5 Airtasker credit. The main purpose here is to ensure the survey respondents are high quality candidates who are likely to be users of this subscription feature (as they were interested enough to click on it). The purposes of the concierge test would not be to validate demand, as I'm making the assumption that my colleagues team has already done that. If they haven't, a concierge test is a good way to gage demand of a potential feature, and we could alter the survey questions to be ones which validate whether users would want this feature.

<u>User Interviews</u>

For those who complete the survey, we could invite some for a user interview to dive deeper into their responses to better understanding{% include elements/highlight.html text="why they don't wish to pay upfront, what's holding them back and what would be their ideal experience to get them to pay." %}We could even get some mockups prepared to see them interact with the product, although the core focus of the session would be on exploring their concerns.  

<br>
#### What users do 🏃‍♂️

As mentioned, the best way to understand users is to watch what they do! So, I'd recommend two approaches here:

<u>Early Access program</u>

This is a really great strategy to release a new product the right way. I'd suggest to my colleague having a Beta Group (framing it as 'Early Access' makes it a lot more enticing to users to be a part of) with a number of Taskers and Posters (e.g. 30) who we get to{% include elements/highlight.html text="use the product as we are developing it" %}providing regular qualitative and usage feedback during the build process.

While I'd recommend having the ideal target user in this program (e.g. Posters which regularly post a certain type of job - e.g. apartment cleaning), one of our concerns was Taskers cancelling their subscription to save a few dollars of commission. These Posters are likely to be a different type to the ones formerly mentioned. They probably don't post frequent or recurring tasks, and would just post a one off task, say, every few months. So we'd want to have some of these users in their as well so we can see if our concern actually surfaces in user behaviour from these particular Posters.  

Although an early access program can help us see if these concerns appear during actual usage of the new product, there is one potential{% include elements/highlight.html text="drawback of this method which I call 'Big Brother'" %}Since users know that we are building the product iteratively with their feedback, there is a possibility that it is slightly moderated and that it's not a totally true reflection of how they'd use the product in real life with no one watching.

<u>Canary release</u>

This method can help overcome the Big Brother drawback of an early access program by seeing{% include elements/highlight.html text="raw, unmoderated usage of a feature out in the wild." %}This is where we launch the product to only a subset of users before rolling out to our entire user base.

Using an internal system, or any reliable feature flagging service like Launch Darkly, you can show the subscription feature to, say 20% of users or have a percentage of new signups go to a branch of the site which has that feature while the remainder go to the master branch. Some products (typically B2B Saas) also have a section of the user profile (e.g. 'Labs' or 'Beta') where the user can trial new features currently in Beta. Whatever the methodology, this is real users going to a real product out in the wild.

Whilst this gives us a totally objective way to see if our concerns play out in real life, the drawback is that it requires a functional product, or at least a working MVP. Depending on the complexity of the product, this can be a lot of development time to uncover a problem which we could have discovered through a survey or early access program. Considering the enabling of subscription payments might require a refactor of our Stripe billing API on the backend and substantial frontend changes too, this might be a{% include elements/highlight.html text="long way to go about learning what we want." %}

<img src="https://i.ibb.co/SBnZMXS/Screen-Shot-2020-01-04-at-4-18-27-pm.png" width="650" height="300">
<figcaption class="figure-caption text-center">I regularly review this chart, which perfectly sums up why we should validate early</figcaption>
<br>

### User Concern

If these concerns came from the user, or the team validated that they were an issue from further research, then they should look at ways to overcome them. I'd suggest organizing a{% include elements/highlight.html text="brainstorming session" %}with the team to discuss how they could prevent these two known concerns from happening by baking certain features into the product and business model. Giving everybody the opportunity to provide their ideas is extremely helpful in solving the problem, as each stakeholder has different lenses which can help us hone in on the right solution. Also, it may spark additional ideas we hadn't thought about before.

Besides the brainstorming session, there are a couple suggestions I think could help solve these problems:

##### Willingness to pay upfront

<u>Iterate the benefits</u>

Being very overt about the benefits to the poster of paying for the subscription upfront might help them overcome the hesitation of paying.

```
“This is your 3rd cleaning job post in a month. You would have saved $34 by switching
to an Airtasker Subscription. Switch to Subscription Now.
```

Note, that example copy is under the assumption that a user paying for a subscription would save money via this payment structure instead of posting tasks individually. If that's not the case, we can upsell other benefits like convenience and Tasker reliability.

We can also have a plans or info page which showcases all the benefits of the subscription model and why the Poster should pay for it upfront.

<u>Flexible subscription</u>

Offering flexible subscriptions like month to month cancel anytime could help overcome this problem of users not willing to commit to a subscription long term. We could even allow the user to choose different time periods, like quarterly or a 6 monthly subscription. The only drawback is that this solution might not help us with our second concern of one-off posters gaming the system. If there was a month to month subscription and I only had one task to post (e.g. remove a tree from my front yard) and I knew the subscription would save me money, I'd very likely pay for the month and then cancel it next month when I don't need it.

##### Gaming the system

<u>Upsell to target user</u>

Whilst we can allow any user who wants a subscription to pay for it, an idea could be to only up-sell the feature to our ideal target users - those who are posting a certain recurring task (e.g. house cleaning) or just regularly posting different tasks on the platform. If our concern is true, then we don't want to showcase the feature heavily to users we think will game the system. We could have some logic of who we showcase the feature to. For example, users who are posting at least their second task, and this current task is within a month of their previous one.

<u>Additional value</u>

People don't cancel subscriptions that are really valuable to them. While some very cost conscious Netflix users may only pay for a subscription for 1 month to binge watch the latest season of Peaky Blinders, majority keep their subscriptions (they have a 9% subscriber churn rate which is considerably low for a streaming service). The reason for such high retention is there's so much content, they're continually adding more, and the more you watch on Netflix the more personalized it becomes thanks to the recommendation algorithm.

We could add additional value for Posters who pay for a subscription, encouraging them to stay and keep their account, for example:
- Poster Features:
   - improved discoverability of posts (e.g. posts get featured at top of feed)
   - recommended Taskers based on their post
   - ability to assign multiple taskers to one task  
   - ability to repost a task if cancelled
- Loyalty reward scheme
- Partnership opportunities with complimentary brands (e.g. discounts to IKEA, Coles etc)


We'd need to look at our data and feedback channels (feature requests, customer support tickets, reviews etc) to understand what features would be most valuable for posters to continue using the service. We may even be able to justify a higher price for the subscription with all this value, which could {% include elements/highlight.html text="negate the impact of infrequent posters paying for a subscription and cancelling their account" %}because the subscription might be more profitable for us than a normal task.  


<u>Longer subscription period</u>

This is definitely contradictory to the other concern around unwillingness to pay long term and my suggestion of a month to month, cancel anytime subscription. However, I do think locking users in to a longer subscription period up front would avoid the problem of users cancelling their subscription after their task is completed to save on commission. I'd only pursue this if we disproved our first concern. Otherwise, we'd need to weigh up which of the concerns are greater and which we'd prioritize.

---
<br>

Something I think is important to note here is these two concerns my colleague has about the subscription model are heavily correlated. The users who aren't willing to commit to a long term subscription are likely the users who would cancel their subscription after the task is completed to save on commission. For example, if my colleague's team identified the target user of the feature is a poster who posts at leat 1 task a month, than it's likely that these users would commit to a long term subscription, while the ones who aren't willing to commit might not actually be our target user. If I had been posting 1 cleaning task a month for the past 6 months and felt confident I'd do it for the next year, I'd feel comfortable paying for a subscription up front. At my current workplace, our software can only be paid for via an annual subscription and this was tested against a monthly subscription and the former had better uptake.







<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q11-Q13-mission" text="👉 Next Question" %}
</p>

---
title: Growth has Plateaued
tags:
style: fill
color: primary
description: Question 3
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q4" text="👉 Next Question" %}

**Question 3:** *Given what you know about Airtasker, what would you do if our growth plateaus? Why?*

---
## Where is the plateau?

The first thing I'd need to understand is what dimension of growth we are talking about. To give some heuristic and structure here, I’d look at where ‘Growth’ for Airtasker in this specific context fits into, using the{% include elements/highlight.html text="Pirate Metrics" %}as a useful framework:

<img src="https://i.ibb.co/hWtPYKJ/Screen-Shot-2020-01-03-at-6-51-21-pm.png" width="300" height="450">
<figcaption class="figure-caption text-center">The AARRR metrics funnel 🏴‍☠️</figcaption>
<br>

**1. Acquisition:** are we struggling to acquire new users?

**2. Activation** - are we struggling to get new users to the core value of the product quickly enough?

**3. Retention** - are we struggling get users to repeatedly come back to use Airtasker?

**4. Referral** - are we struggling to get users to advocate about Airtasker to their friends?

**5. Revenue** - are we struggling to grow our sales revenue?

If 'growth' plateaus at Airtasker, the company would know about it, so I assume the team will be very clear on what specifically has plateaued and which of these 5 buckets it fits into.

## What is the plateau?

The next thing i'd want to know is{% include elements/highlight.html text="what do we consider a plateau" %}from a quantitative standpoint? This will give me some clarity on how severe the underperformance is and at what level of 'growth problems' we consider something worth fixing.

- **Is it a drop in our usual metrics?**
   - For example, say last year we were averaging $2 Million monthly revenue and it was growing by 8% month on month, but the last 6 months we've slowed down to 4% month on month growth.
- **Or is it completely flat?**
   - For example, say our number of active users is flat and has remained at the same level for the past 6 months

I'd also want to understand{% include elements/highlight.html text="over what time frame we are measuring the growth plateau." %}There's a difference in a metric underperformance compared to the previous month vs an inherent problem that has been occurring for 1 year and is evidently not improving.

## Why is there a plateau?

Now that we understand the 'what' (which area of growth has plateaued), the next step is to{% include elements/highlight.html text="understand why has it happened and what is the root cause." %}

I'd first start with seeing if there is a macro-change which is causing the underperformance as opposed to something specific within the product. For example cyclical issue due to external factors (e.g. we may have lower usage at the beginning of the year or during holiday periods which would hurt our metrics over those periods) or structural and something inherently wrong with the business or operations?

I'd also look if there were any{% include elements/highlight.html text="key business events which occurred at the start of the plateau period." %}For example, was there a key partnership which we discontinued from a certain date and we're now not acquiring the same volume of users?

If there's no contribution from those macro factors, I'd start looking deeper at each axis of growth to identify the real problem contributing to the plateau.

#### Acquisition 👷‍♂️👩‍💻

<u>Channel Breakdown</u>

If the number of users we acquire at the top of the funnel was stagnant, my first step would be to see if any acquisition channel in particular is underperforming. I'd start by {% include elements/highlight.html text="breaking down our new user growth by acquisition channel" %}to see how each contribute to our total number of users acquired. I'd then want to see the{% include elements/highlight.html text="trend of each channel over time." %}.The time period I look at would depend on the 'plateau' timeframe I would have clarified in my earlier steps, but I'd likely break it down by past 1 month, 3 months, 6 months, 1 year, 3 years. Is there one particular channel that is underperforming and others are still performing as normal?

I'd also want to look at our{% include elements/highlight.html text="conversion rates" %}across all of these channels (of users that come to us via those channels, what percentage sign up), which are the best and worst performers, and how the conversion rate of each channel has changed over time (we may find that the conversion rate of our biggest acquisition channel has decreased dramatically over the past year).

<u>Posters vs Taskers</u>

I'd also want to break this down, if possible, by Taskers and Posters to see if it's a particular type of user that we are struggling to acquire. For example, we may be getting lots of Taskers signing up to earn extra money but not many new Posters.

<u>Device Brekdown</u>

I'd check how our acquistion looks broken down by device type to see if it is a particular device where aquisition is plateauing.

- mobile web
- desktop web
- tablet
- iOS app
- Andorid app.

#### Activation 🏃‍♂️

If the growth issue is in the Activation step of the funnel, this means that we are struggling to turn new Posters and Taskers into active users. If this was what we saw in our analytics, I'd want to do some qualitative and quantitative research to better understand why it's happening:

<u>Quantitative</u>

I would look at data on first session usage for posters and Taskers. There would obviously be a reason they aren’t coming back for a second session, namely, that they aren’t getting to the core value of the app quick enough. This would also allow me to know if the activation problem is for Taskers or Posters, or both. I'd also be curious to understand from our data what actions for Posters and Taskers are correlated with activation. Do we have any leading indicators which we know will result in a user becoming active? E.g. Taskers who place an offer in their first session are 80% more likely to return for a second session compared to Taskers who don't.

I'd also look cross device to understand if users on mobile app have better activation rates than desktop users or vice verse.

<u>Qualitative</u>

I'd want to understand the experience of Taskers and Posters on their first session to understand where the pain points are and what is preventing them from having a meaningful first session. My research approach would include:
- **Hotjar recordings** for newly registered users to see their first session experience
- Surveys (e.g. in app, churned users)
- User Interviews:
   - I'd want to speak to active and recently churned users to see the differences in their experience and what caused the active users to return vs what caused the churn users to leave
   - I'd also want to speak to non-Airtasker users and get them to go through the experience of creating an account for the first time as a Poster and Tasker and watch their first Session

Activation is all about driving users to the core value of the product as quickly as possible. If the activation issue is on the Poster side, I’d look at optimizing the onboarding experience to get them to post a task in first session. If the issue is on the Tasker side, I’d look at driving them to verify their account and place offers in their first session.

I go into a lot more detail about strategies for activation <a href="/essays/Airtasker-Challenge-Q4#more-efficient-tasker-and-poster-activation-1" target="_blank">here</a>

#### Retention ↺

If the growth plateau is in the retention stage of the funnel, it means Posters aren't regularly coming back to post tasks and Taskers aren't coming back to make offers on them.

<u>Taskers</u>

If Tasker retention was an issue for us, I'd have a few assumptions in my head which I'd want to validate through quantitative data:

- They had a poor first experience as a Tasker
   - E.g. their task was misrepresented and there was much more involved than what was expected from the job description)
- They struggled to get accepted for jobs as a first time Tasker   
- They were put off returning because of the fees and the subsequent low take home pay
- Poor search experience for new jobs (e.g. users not being able to search for task in specific categories)
- Not getting notified about suitable jobs for them (e.g. user does not have notifications/alerts set up)
- Notification bugs (currently, when I click on notifications it doesn't take me to the right place)
   - There was a great website review task I got a notification about, clicked on it and then went to the previous page I was on last time I opened the app (my saved messages). I tried remembering the name of the task and searched for it but couldn’t find it
- Taskers use the platform as a lead gen and then take the business off-line to cut out Airtasker as the middle man to avoid paying fees

<u>Posters</u>

If Poster retention was an issue for us, I'd have a few assumptions in my head which I'd want to validate through quantitative data:

- Poster received no offers on their task
- They assigned a Tasker but the Tasker didn't respond to messages or didn't show up
- They had a poor experience with their Tasker (task not completed satisfactorily, Tasker didn't have the right skills etc)
- First experience was fine but they were put off returning because of the fees

#### Referral 📣

I would go ahead and make the assumption that our recent coupon referral T&Cs change to only apply a coupon to tasks over $100 would have lead to a significantly drop in the number of new tasks posted using a referral coupon. It seems pretty clear that given Airtasker’s new focus on profitability, it made sense to increase the constraints around using the coupon, as I’m sure there were many users abusing them and creating lots of fake accounts to generate new coupons. Additionally, you may have seen that the lifetime value (LTV) of customers who used a coupon for their first task was not significant enough to justify the cost of the referral program in its previous implementation method. Maybe the cost of acquisition (CAC) was higher than the LTV of new customers using coupons.

Having said that, we could test going back to the normal coupon structure, but ensuring verification by mobile for a users account, similar to Uber. That way, a coupon is not tied to an email address but instead a phone number. I know many users who will create dozens of fake email addresses to redeem coupon codes but not many who will use multiple phone numbers.

<img src="https://img.gadgethacks.com/img/31/71/63687868461652/0/add-2-step-verification-uber-for-stronger-overall-account-security.1280x600.jpg" width="450" height="650">
<figcaption class="figure-caption text-center">Uber's account verification makes it very hard to game the referral system</figcaption>
<br>

However, overall I think you guys did the right thing by modifying your T&Cs to reduce the number of people using coupons and never coming back, or abusing them repeatedly by creating new accounts. I don’t know the data around how important the referral program was to new user growth and volume of posts on the platform, but I think referral programs can be very hard to maintain and can significantly hurt other levers like revenue and profitability

This shows that it is important to consider why a particular growth dimension has plateued. We may have launched a particular feature, changed a business model or made a fundamental change in order to achieve a particular objective (e.g. profitability) at the intentional expense of growth of another, less critical area of the business (e.g. referral).

I would be curious to see the performance of our referral channel since making that change. E.g. How big was the drop in number of tasks posted with a referral coupon? And did it have a net positive impact on profitability?

#### Revenue/Profitability 💵

To improve profitability, there are really only two options:

- increase revenue
- lower costs

<u>Increase Revenue</u>

One dimension of increasing revenue is to extract more value from our current channels. For example, we could look at ways to increase the value of tasks on the platform to try and raise the average task price through proper categorization and task price recommendations for the poster. We could also look at enforcing minimum wages, although I know this is a hot topic that Airtasker has come under scrutiny for and Tim has <a href="http://theconversation.com/full-response-from-airtasker-ceo-tim-fung-77009" target="_blank">spoken about a lot</a>

The other dimension is to look at new business models and revenue streams. These could include:
- Charging a fee to the Poster when assigning a Tasker (which we've recently started doing)
- Advertising (e.g. Tasker ads, or even the ability of Posters to boost their listings and have it viewed by more Taskers)
- Subscription model for regular/recurring services

<u>Lower Costs</u>

Now this is something the Airtasker business knows very well given the recent changes to become a profitable company, such as reducing your headcount in the UK and a large redundancy of support staff in Sydney. All if these were obviously very effective, but cutting costs can be a tough thing to do from a personal level. Besides reducing staff, we can also look at projects/resources being allocated to low value projects and re-assign them to higher value activities. E.g. If we had a team on referrals but are no longer prioritizing that, we'd be better off looking for new business models and revenue streams.

---

As a final note, It's important to consider how{% include elements/highlight.html text="trying to grow one of these levers can impact other areas of growth." %}For example, a decision to improve revenue/profitability could reduce our referral growth. Therefore, when trying to solve the issue of a growth plateau in a particular area of the business, we need to consider the impact it would have on the other areas, not just in isolation.

<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q4" text="👉 Next Question" %}
</p>

---
title: A Failed Product Tactic
tags:
style: fill
color: primary
description: Question 2
---
{% include elements/button.html link="/essays/Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q3" text="👉 Next Question" %}

**Question 2:** *Say we tried product/growth tactic X and failed to generate the returns we’re looking for, how do you diagnose the issue?*

---

My favourite book on Product Management is <a href="https://www.amazon.com.au/Inspired-Create-Tech-Products-Customers/dp/1119387507/ref=pd_sbs_14_img_0/356-9437039-3119256?_encoding=UTF8&pd_rd_i=1119387507&pd_rd_r=67bbc32b-5e3a-464d-aafb-23d4753a6d7e&pd_rd_w=TCHd4&pd_rd_wg=QN83m&pf_rd_p=a7229bdc-4c52-476b-87a7-8cf10344d0a6&pf_rd_r=GZ9HH0HAJSH1DYS3WQBD&psc=1&refRID=GZ9HH0HAJSH1DYS3WQBD" target="_blank">Inspired by Marty Cagan</a>. Whilst there are too my nuggets of gold in that book to count, one thing which I regularly read again is his writing on how hard Product actually is. He mentions there are{% include elements/highlight.html text="2 inconvenient truths about product:" %}

#### 1) Most ideas aren't going to work

> "I promise you that at least half the ideas on your roadmap are not going to deliver what you hope. By the way, the really good teams assume that at least three quarters of the ideas won't perform like they hope."

<br>

#### 2) The ones that do work might take several iterations to get right

> "Even with the ideas that do prove to have potential, it typically takes several iterations to get the implementation of this idea to the point where it delivers the necessary business value."

<br>

I always remind myself that we may not succeed on our first attempt at solving a problem. And that’s exactly why Product Management is so rewarding, because when you do achieve the result you wanted, it’s intrinsically rewarding beyond explanation.

---

There are 3 layers I think through when trying to understand why something may not have worked as expected and achieved the results we were hoping for:

<img src="https://i.ibb.co/syGLPYC/Screen-Shot-2019-12-31-at-11-10-00-am.png"  width="430" height="500">
<figcaption class="figure-caption text-center">My diagnosis funnel</figcaption>

## 1) Technical or Measurement Issue

The first thing I look for if our tactic didn't generate our desired returns is if there were any{% include elements/highlight.html text="technical issues which prevented users from using what we built or getting value from it. I’d check if there were any bugs or site issues during the period of testing." %}This could be a bug in the feature we built or something adjacent in another part of the product which could have impacted the conversion flow and overall experience, negatively biasing results. I'd check this through a few avenues:

- Speaking to the engineering team
- Looking through error logs and crash reporting (e.g. Sentry, DataDog) over the period we collected results
- Qualitative audit of the feature to look for any bugs
- Going through our analytics to see how people used the feature and if there are any abnormal results (e.g. we may find 0 events triggered for clicks on our most important CTA, which may lead us to discover the element was hidden from users so no one saw it)
- Looking at overall platform metrics to see if usage stats look unusual for any of our leading indicators and key metrics during the time period we measured results for

Lastly, I'd{% include elements/highlight.html text="double check that our analytics tracking is all correct." %}For example, are we not including any tracking on a certain part of the feature which is understating our results?

If we did discover some issues in this step from those two areas which we know would have significantly impacted our results, I'd{% include elements/highlight.html text="organize a short sprint with my engineering team to fix the issues and then re-measure results." %}This has happened to a product I was working on, where the results were substantially worse than we anticipated but it was due to major bugs in the platform which impacted usability of the feature. We fixed them, re-measured and generated the returns we were expecting.

If we didn't discover any issues in this step, we move onto the next stage of the diagnosis funnel...


## 2) Right Idea but Needs Some Tweaking

As I mentioned earlier, even if we do launch the right thing it may take several iterations before we get it right. This situation summarizes my second diagnosis step well - we take the viewpoint that our solution is the right direction, but certain steps or aspects of the solution limited its efficacy.{% include elements/highlight.html text="The way we discover what the problems with our solution are is to look at feedback from real users using the feature." %}Whenever I launch a feature, there are 3 sources of feedback I try gather:

#### Event Tracking

I always make sure to{% include elements/highlight.html text="track every meaningful interaction a user can have with the feature" %}we’re launching, which helps us answer critical questions like:
- Which features did users interact with the most?
- Which features were *least* used?
- What percentage of users interacted with feature X?
- What percentage of users made it to the end goal of our funnel for the feature?
- Where in the funnel are users dropping off?

Digging through all this data on how users are using what we've built will help us understand where the problems lie. After that we can ideate ways to solve them and change the design and experience.

The way we set up event tracking may be different based on our tech stack and tracking implementation, but I like to use `page.subject.modifier->action` for the event names, plus any properties needed to gather more granular data beyond simple actions like clicking, toggling, closing, opening etc. For example:

- Event Name: `make_an_offer.your_offer.field->type`
- Properties: starting_price, user_input_price

<img src="https://i.ibb.co/r4Cmk2D/Screen-Shot-2019-12-31-at-2-44-16-pm.png"  width="400" height="400">
<figcaption class="figure-caption text-center">Using Chrome Inspect to make sure events are getting fired correctly</figcaption>
<br>

#### User Session Recordings

It is incredibly important to watch, observe and empathise with a user going through your product/feature. Whilst analytics are definitive and hard truth, you might miss things if you only looked at hard data alone.{% include elements/highlight.html text="You need to feel the user going through what you’ve built and see first hand what’s holding them back." %}You may see that many users clicked on something we wanted them to, started typing but then backspaced and didn't proceed because they were apprehensive. We'd want to know why they did that and what's holding them back.

I make sure to{% include elements/highlight.html text="set up Hotjar recordings for any new feature I ship to see how users are using it." %}This is still useful even if the feature did generate the desired returns, but is especially important when it didn't. I'd go through all the session recordings we have for the feature and see if I can draw additional insights on what is causing the problems.

<img src="https://i.ibb.co/mGXYxmb/Screen-Shot-2019-12-31-at-2-47-53-pm.png"  width="760" height="550">
<figcaption class="figure-caption text-center">Watching users using your product in the real world is one of my favourite things to do as a PM 👀</figcaption>
<br>

#### Qualitative Feedback

I like to incorporate some type of survey to gage qualitative user feedback on the feature when it's first released. The main purpose of this is to know:
- How valuable the feature is for users
- What users like and dislike
- What users would change
- What features are missing
- If we're improving satisfaction and providing more value to the user with every iteration we make

One of my <a href="/about#principles" target="_blank">Product Principles</a> is 'Don't Let the Dust Pile Up' - this means{% include elements/highlight.html text="don't ship a feature and never return to it again" %}(even if it did generate our desired returns). We should always look at how it can be changed, iterated on and improved.

<img src="https://i.ibb.co/qxm38TG/Screen-Shot-2019-12-31-at-2-37-21-pm.png"  width="450" height="350">
<figcaption class="figure-caption text-center">I typically begin the survey with this lightweight question to get users started</figcaption>
<br>

We can even{% include elements/highlight.html text="connect our user analytics to the survey results" %}(e.g. by passing through a unique analytics ID to the survey tool, like Typeform's hidden fields functionality) to understand{% include elements/highlight.html text="what user activity correlated with high/low satisfaction with the feature." %} Additionally, we can reach out to users with certain feedback and usage behaviour to do a short user interview and get a deeper understanding of why the feature didn't work for them and what happened when they experienced the feature for the first time.

## 3) Wrong Idea, Let's Move On

We need to prepare ourselves for the possibility that the product/growth tactic as a whole was not the right thing to move our desired metrics and have the impact we wanted. Essentially, we got the solution wrong 😔.

If after an iteration cycle or two we still couldn't achieve the desired impact on our metrics, it may become a resource drain to continue beating a dead horse. In this instance, one of two decisions need to be made:

**1) Move on to a new solution**

If we believe the problem we're solving is still important to our users and business, we will need to {% include elements/highlight.html text="go back to the drawing board, learn from what we've done this cycle and attempt a new solution to solving the problem." %}Whilst this can be incredibly disheartening for the team, if we are all regularly aware of the Inconvenient Truths about product mentioned earlier, we understand it's nothing personal and that this happens to the very best of teams. Let's re-do the product life-cycle again (now with learnings we never had the first time round) and have another crack!

**2) Ship if the results are acceptable**

Something important to note is that while a tactic or initiative might fail to generate the exact returns we were looking for, there are instances where {% include elements/highlight.html text="the tactic can still be considered enough to ship the feature." %}For example, say our goal was to halve the time it takes from a newly registered user to post a job from 2 days 1 day. We made some changes to the onboarding experience and it reduced it to 1 and a half days. Whilst it didn’t achieve the desired return, it was a significant directional improvement, and could very well still validate the experiment being successful enough to ship. There's no hard science to this, but on a case by case basis we need to consider what a 'good enough' solution is. E.g. we may have other very pressing priorities we need to work on and are willing to accept the result as it was still a directional improvement.

---
## Case Study
<br>
#### The Situation

There was actually a very recent example where my team launched something and failed to generate the returns we were hoping for. My team had recently launched a brand new 2.0 version of our platform, which we thought was far superior to our original platform. We measured our key metrics and they were at parity or better than the original platform, which was satisfactory. However, when we measured overall upgrade rates, users on the new platform were converting to paid customers at a far lower rate than the old platform (about 30% underperformance! We were gobsmacked 😱)

#### Step 1

As per my diagnosis process, our first step was to check if there was some error in our data. After looking at error logs, overall metrics and especially any bugs around payments and conversion flows, we found there were no issues. The data was in fact true and our new amazing platform was actually losing us money!

#### Step 2

I decided that we need to slice our data to get a better understanding of why this gap exists. There were three main areas I was interested in exploring:

<u>Breakdown of upgrade rates by trialing and post-trial users</u>

Automatically, every new users goes onto a 14-day trial of our premium plan. After the 14 days, they get downgraded to the free plan. I wanted to know if one of these are contributing to the underperformance more than the other.

<u>Breakdown of upgrade rates by mobile and desktop users</u>

I wanted to know if the conversion issue was more pronounced on a particular device, as there are certainly differences in features and experience between the two.

<u>Breakdown of upgrade routes</u>

There are numerous methods and scenarios how a user can upgrade to a premium account in our platform. Seeing how each are performing relative to our benchmarks on the old platform can help us spot the problems.

**There were a couple key findings from our analysis:**

- Mobile conversion was underperforming desktop

Looking at the main upgrade routes, we saw that majority of users were upgrading via a button in the top menu on desktop. However, this button didn't exist on the mobile version of the platform, so we decided to add it to mobile.

<img src="https://i.ibb.co/YZJB0ST/Screen-Shot-2019-12-31-at-3-13-09-pm.png" width="600" height="600">
<figcaption class="figure-caption text-center">Issue I wrote up in GitLab explaining the background and requirements for the engineer implementing our desired change</figcaption>
<br>

- Conversion rates were worse during a user's 14-day trial than they were post-trial

Learning this got us to see some pretty obvious reasons for why our conversion was suffering. We were very overt about the presence of our free plan on the platform. This mainly came from surveys I conducted with users who churned after their first session. Almost 20% of users said they didn't return because it was too expensive, and of those 75% didn't know we had a free plan. Given that 79% of our active users were on the free plan, and our company goal was active user growth, not profitability and revenue, I chose to prioritize being explicit about the free plan. So, the lowest hanging fruit for us was removing the messaging about the free plan.

<img src="https://i.ibb.co/cXcFCfG/Screen-Shot-2019-12-31-at-3-21-08-pm.png" width="650" height="400">
<figcaption class="figure-caption text-center">Gitlab Issue I wrote</figcaption>
<br>

We made those changes and re-measured results over a 3 week period to gather sufficient data.

#### Step 2 (again)

<img src="https://i.ibb.co/kxcXPxC/Screen-Shot-2019-12-31-at-4-07-47-pm.png" width="550" height="700">
<figcaption class="figure-caption text-center">We'd closed the gap for upgrade rates post-trial 🎉 but only reduced the gap for users during trial 😭</figcaption>
<br>

But this was positive! Our changes had the desired impact we wanted, but now we knew that there was something about the trial experience specifically which was causing users in that 14-day window to not convert.

Immediately, I started looking at the differences between the old site and the new site experience during a user's trial. I noticed 2:

**1) Presence of word 'Free'**

 We were still mentioning the words 'Free Plan' on the plan status button in the top bar menu during a user's trial on the new site, while the old site didn't. Our change from the first round was to decapitalize it (it used to say 'FREE plan' so we just toned it down to 'Free'). We decided to get rid of the word 'Free' completely.

 <img src="https://i.ibb.co/YPKzZfv/Screen-Shot-2019-12-31-at-4-50-10-pm.png" width="500" height="600">
 <figcaption class="figure-caption text-center">Gitlab Issue I wrote</figcaption>
 <br>

 **2) Dedicated Marketing Page vs User Profile**

 On the old site, when users clicked that button in the top menu bar, they were sent to a dedicated marketing page where they could upgrade from directly. This page was very well optimized to get user to pay (Reviews and Social Proof, Media, Product Features etc). On the new site, however, users who clicked the button were sent to their user profile to complete their upgrade, a dull page with no marketing. The reason for this was the implementation time to rebuild the marketing page in React, our new frontend framework that the new site was built with, was extensive and we didn't have the time. We chose the quickest solution which was to send users to the user profile instead.

Looking at the data, conversion rates on the marketing page were much higher than the user profile page. So even though the engineering estimate was steep, we decided to rebuild the marketing page in react so that users could upgrade from that page directly because we had strong evidence to suggest this change would work.

<img src="https://i.ibb.co/2gdPnSQ/Screen-Shot-2019-12-31-at-4-40-21-pm.png" width="700" height="650">
<figcaption class="figure-caption text-center">Gitlab Issue I wrote</figcaption>
<br>

We made those changes and re-measured results....

#### Step 3

No step 3 was needed thank goodness 😅. Our changes got us back to parity! We had officially closed the gap 🎊.

If our latest changes hadn't moved the needle, we would have had to regroup and explore some more abstract reasons why the app is underperforming. We were prepared for this and had a number of hypothesis in the backlog. E.g. some members of the team had a hypothesis that the updated Information Architecture on the new platform, whilst more efficient, made the app feel less powerful and feature-packed, which may cause fewer users to upgrade.


<p class="text-center">
{% include elements/button.html link="/essays//Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q3" text="👉 Next Question" %}
</p>

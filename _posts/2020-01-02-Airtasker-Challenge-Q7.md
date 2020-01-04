---
title: Tasker Ads
tags:
style: fill
color: primary
description: Question 7
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q8" text="👉 Next Question" %}

**Question 7:** *Airtasker's leadership team is considering an additional business model that allows taskers (people who work in the platform) to run ads in the marketplace. How do you determine its potential impact?*

---

This is a really interesting business model! Before tackling how I'd assess it's impact though, I'd want to clarify with the leadership team why we're considering this additional business model. Given the current business goals around profitability, sustainability and growing revenue streams, I’d say the{% include elements/highlight.html text="primary driver is to grow Airtasker's revenue," %}so its a{% include elements/highlight.html text="business problem we’re solving, not a customer problem." %}This could, however, have numerous benefits for both Posters and Taskers, which I will touch on in a moment.

I'd also want to{% include elements/highlight.html text="better understand the mechanics of the business model" %}and how it would work for the user and business. When we say “run ads in the marketplace”, does that mean ads running in the existing marketplace embedded in the current structure or a totally new feature? I see many ways this could be implemented:
- Would Posters post a task and then immediately receive ads for recommended Taskers?
- Would Posters be able to search and find specific individuals for a task?
   - Eg. A ‘Tasker Ads’ tab where you can search for Taskers in certain categories to find suitable people to offer services? (similar to some of our landing pages for non-registered users like <a href="https://www.airtasker.com/painting/house-painting/" target="_blank">House Painting</a>)
- Would Taskers make bids on jobs and the Tasker's who've paid for ads are floated to the top of the list as recommended?
- Would the Tasker be required to pay fixed pricing for the ads? Would there be a tiered structure where the more you pay, the more discoverability you get?
- Would the Tasker pay per impression?
- Would the Tasker have to bid for ads similar to Google Ads?
- Do Taskers bid for ads on individual job posts or just pay Airtasker and we showcase them to posters?

Since you said the leadership team is ***considering*** this business model, I assume the idea isn’t fully fleshed out in terms of its exact implementation. However, I'd still like to know what management is envisioning this looking like so I can have a better idea of how to assess its impact. Determining the 'impact' of a business model like this is not trivial. There are quite a few ways to break down what affect it would have on Airtasker, so I have broken it down by the impact to the business and the impact to users.

---

## Impact On Our Business 🏢
<br>

#### Success Metrics

<u>Financial</u>

As I mentioned, it seems clear that our primary driver for this change is to grow Revenue. Airtasker has always had its revenue stream from taskers, taking a 20% cut of Tasker's earnings (now in a tiered structure) and since <a href="https://support.airtasker.com/hc/en-au/articles/360031769372-What-is-the-booking-fee" target="_blank">a couple months ago</a>, taking a fee from posters once they accept an offer. Allowing Taskers to run ads in the market place would provide a 3rd and{% include elements/highlight.html text="diversified revenue stream" %}for Airtasker. Given our goal of becoming a more profitable, sustainable company, this additional revenue stream would help us towards that goal by{% include elements/highlight.html text="growing our top line sales." %}

To assess the full impact on revenue though a{% include elements/highlight.html text="detailed financial analysis" %}based on financial modelling will need to take place. Upon fully understanding the business model and our usage data, I would{% include elements/highlight.html text="model the impact with some assumptions" %}around costs, uptake of feature from Taskers and potential cannibalization of our existing business, and then forecast pessimistic, neutral and optimistic{% include elements/highlight.html text="P&L scenarios" %}

Revenue is not the only financial impact an ads business model can have on the business. There are also{% include elements/highlight.html text="costs involved which could impact our bottom line" %}such as:
- **Technical**
   - There may be significant engineering costs involved in building the and maintaining the ads platform (e.g. we may leverage existing libraries and paid SaaS services, build a new payments structure from scratch)
- **People Cost**
    - We may need to hire a product team to look after the 'Ads' product and that is a substantial ongoing cost

<u>Product</u>

There are a number of important metrics we would have which determine the overall health of our marketplace. Introducing an ads platform could impact those as well. For example, this could lead to an{% include elements/highlight.html text="increase in average number of quotes per job, reduced average time to receive a quote, and higher overall assign rates." %}

#### Technical

An ads business model is a pretty significant technical undertaking, so I'd want to assess the impact of this platform change from an engineering standpoint. Some things i'd consider:

- There would also likely be a substantial development cost. This is not a trivial change, as it requires significant backend work, data pipeline and analytics set up, design/UI work and significant investment on actually implementing this on the frontend (+ native mobile and and android apps).
- Do we have the technical capability to build a sophisticated matching algorithm? Are we able to use third party software to assist us in building this?
- Can we reuse any of our existing codebase? For example, we currently have a notification system to alert Taskers on jobs we think are relevant to them
- Our current use of the Stripe API is for transactional revenue. We’re taking a clip from taskers and posters. Depending on the exact implementation of the business model, it may require a refactor of our billing infrastructure to enable this additional payment channel
   - In my current workplace, we wanted to add an additional plan tier and even that required a complete refactor of our Billing API, which consisted of an entire re-write of the Billing system on the backend, and then implementation on the frontend

#### Brand and Community Perception

Something that currently concerns me is the recent{% include elements/highlight.html text="brand perception around Airtasker prioritizing profit over users." %}In my <a href="https://clyp.it/jh021dx0?token=08ab8fd76494a9977d0f6e9b4e70a7c4" target="_blank">user interview</a> with a Tasker/Poster on the platform, she raised this point repeatedly:

> “There’s a company that has 14 people completing tasks on Airtasker and are on gold tier, but for me, it’s just one person. I’m never going to be on 10%. Why should somebody at the bottom who is doing a quirky task, which is what [Airtasker’s] original thing was, be up against an actual business with a professional model and nine different people going in. That's beyond an uneven playing field. The goal posts are in a completely different country. It's frustrating how much integrity they have lost.”

> They're chasing the dollar. They've lost all focus on what they used to be

> Their fees have gone from 7% to now almost 44% by the time they've gouged off of everybody

Additionally, there are countless online reviews of frustrated users who believe the platform fees are unreasonable:

<img src="https://i.ibb.co/M2RCKrt/Screen-Shot-2020-01-02-at-7-37-38-pm.png" width="650" height="175">
<figcaption class="figure-caption text-center">One of many negative reviews about our fees 💵</figcaption>
<br>

There's excellent advice I once learnt from a mentor which is{% include elements/highlight.html text="not all business is good business." %}I would heavily encourage us to consider how this new business model might affect perception of our brand and potentially lead to higher churn rates and a decline in acquisition.

I would conduct{% include elements/highlight.html text="surveys and qualitative user interviews with our community members" %}(both Posters and Taskers) to gage perception of the Airtasker brand and the impact on their user behaviour of launching ads on the platform.

#### Alignment to our Mission

We really need to ask ourselves if implementing this new business model would enable more people to realize the full value of their skills. It might allow some people to do so if ads improve their discoverability and result in more jobs for them, but what about the users that don't have the propensity to spend money on ads? We may{% include elements/highlight.html text="unintentionally alienate a large portion of current users from realizing the full value of their skills" %}by prioritizing the few who pay for ads.
<br>

## Impact On Our Users 👷‍👩🏻‍💼
<br>

#### Tasker

<u>Positive Impacts</u> ✅

**Greater Discoverability**

The key positive impact on Taskers is being more visible to Posters and therefore an increase in the number of jobs they are assigned to. I see this being of particular{% include elements/highlight.html text="benefit to first time Taskers who can often struggle to get jobs." %}I've seen feedback from users about the difficulty of getting started on the platform when you have no completed jobs and are competing with more experienced Taskers. I even experienced this myself as a Tasker, struggling to get assigned for jobs when the Poster could rather assign a tasker who has 100 completed projects.

<img src="https://i.ibb.co/ctC6ZQH/productreview-com-au.png" width="300" height="450">
<figcaption class="figure-caption text-center">One of many reviews about the difficulty of getting runs on the board as a Tasker 🏏</figcaption>
<br>

I also experienced this on the other side when I was a Poster and had to assign one Tasker from the 25+ offers I received. My immediate way to shortlist the best candidates was to ignore new Taskers in favour of more experienced ones with completed projects and great reviews.

<img src="https://i.ibb.co/Wy4cpTd/94-Completion-Rate.png" width="250" height="450">
<figcaption class="figure-caption text-center">Luis G. doesn't stand much chance next to the other 3 candidates... 😔</figcaption>
<br>

Ads could be a viable way for first time Taskers to increase their chances of getting assigned to tasks and start completing some jobs to build up their experience on the platform.

**Lead Generation**

A lot of businesses use Airtasker as a method to generate new leads, so this is another channel for them to advertise their services. As businesses have a propensity to pay for acquiring customers, I'd think it's a pretty attractive strategy for them to grow their customer base.

<br>
<u>Negative Impacts</u> ❌

**Affordability and Competitiveness**

Whilst there are businesses that operate on Airtasker, my assumption is that majority of Taskers are individuals. Platforms with ads are generally paid for by businesses which have a higher propensity to pay (e.g. Google Ads) or by the supply side in a marketplace (e.g. Carsales upselling you on packages to increase discoverability of your listing). With the fees we currently take from Taskers, which from my user interview and online reviews I can see is a major frustration point for users, it might be unreasonable to expect users to pay for ads and take it out of their overall earnings, of which we already take a significant cut.

An ads business model has the potential to{% include elements/highlight.html text="crowd out a large percentage of Taskers who can't afford to advertise." %}The model may favour the 20% of people who do take it up and not the 80% who don’t. Those who can’t afford to advertise might experience dissatisfaction and distrust in the platform and no longer want to put offers on jobs because they are too small to compete and the costs are too high. This could turn them off the platform and lead to higher Tasker churn.

<img src="https://media.giphy.com/media/xT5LMESHbV1KLGMsq4/source.gif" width="350" height="350">
<figcaption class="figure-caption text-center">Airtasker is already a competitive platform. Ads may add fuel to the fire...</figcaption>
<br>


**ROI for the Tasker**

The Return on Investment needs to be there for the Tasker to make it worth their while to pay for ads. For a platform that already takes a lot of fees, having additional costs of paying for ads to get jobs might actually lead to a net neutral or negative outcome for them if they aren't able to generate more income from jobs than the cost of their ads.

**Risk of Poor Uptake by Posters**

Posters may have a{% include elements/highlight.html text="negative perception about ads" %}and would prefer to choose the best and most suitable applicant for the task (which very likely will be someone who hasn't paid for ads). They may be averse to clicking an add and requesting a quote from those users, instead opting to wait for organic Taskers to submit offers.

If Posters do adopt this mindset when we launch the feature and there is little uptake from them in actually choosing Taskers who use ads, Taskers will not want to continue paying for ads as it would not lead to any ROI for them. The nature of a marketplace means{% include elements/highlight.html text="both demand and supply need to use this feature for it to have value to either party." %}

In my user research, I'd try{% include elements/highlight.html text="validate the risk of low uptake from Posters through value testing with prototypes." %}I'd put the Poster in scenarios where they're required to pick a Tasker for their job and see how they respond to ads vs organic situations. I'd also ensure that if we did release the new model, we would have a{% include elements/highlight.html text="closed beta group and then a canary release" %}before a full rollout to assess real usage and whether my hypothesis plays out or not.

<br>
#### Poster

<u>Positive Impacts</u> ✅

**Quicker Assign Rates**

If one of the implementation methods is surfacing candidates to the Poster after they post their job, this would be a{% include elements/highlight.html text="change in ownership and decision making from Tasker to Poster." %}Rather than passively waiting for offers, Posters can actively choose from candidates straight after posting. The ads could therefore help posters more quickly fill their jobs. This would provide more choice for the Poster and increase the speed of task completion.

**Suitable, High Quality Candidates**

Another value proposition for the Poster is not just the ability to fill their task with a candidate quickly, but to assign it to the ***right*** candidate. I’d love to look at our data to know what percentage of tasks posted receive zero offers, but my assumption is the figure is low and that the{% include elements/highlight.html text="biggest problem on the platform is not getting offers on tasks, but getting high quality offers." %}If our ads matching algorithm can surface relevant Taskers, not just simply anyone who pays, then this can lead to higher quality task completion for the Poster.

<br>
<u>Negative Impacts</u> ❌

**Relevance and Neutrality**

Placing ads on a site serves two audiences with conflicting interests. From a user experience standpoint, ads are often a hindrance and users would generally be happier without them. As I alluded to earlier, the introduction of ads may make the platform feel less organic, whereby the{% include elements/highlight.html text="results we show are no longer determined by what is most relevant and neutral but by who pays the most" %}This could cause aversion from Posters to accept Taskers from Ads, instead opting to wait for offers and hand-select the right candidate organically.

---

Overall, I think a business model which allows Taskers to run ads in the marketplace could have a{% include elements/highlight.html text="positive impact on our top and bottom line," %}but I believe there are a{% include elements/highlight.html text="number of key risks" %}which I'd need to validate through user research. Conducting{% include elements/highlight.html text="qualitative research with Poster and Taskers" %}to understand their response to this platform change will be critical to understanding whether these risks are likely to eventuate if the feature were to go live. If we got through initial research and felt that we could overcome the risks, I'd still want to ensure we see{% include elements/highlight.html text="live usage of the feature in a early access program or canary release" %}to understand how users in wild actually use what we've built and whether it would have the desired business impact if rolled out to all users.

---

## Charging Posters? 🤔

Advertising is a common business model for marketplaces (especially as an additional revenue stream on top of other business models like commission fees, listing fees, subscription/membership fees etc). However, it's{% include elements/highlight.html text="more common that the advertising is on the supply side, not the demand." %}Marketplaces like Seek, CarSales, Gumtree, Facebook Marketplace and many others offer the person creating the listing the opportunity to 'boost' their post and have it viewed by more people.

<img src="https://i.ibb.co/T1KXYqF/Screen-Shot-2020-01-02-at-4-36-49-pm.png" width="250" height="450">
<figcaption class="figure-caption text-center">Facebook Marketplace have started allowing sellers to boost their listing to get more eyeballs 👀</figcaption>
<br>

<img src="https://i.ibb.co/09nvxrp/Screen-Shot-2020-01-02-at-4-38-42-pm.png" width="550" height="450">
<figcaption class="figure-caption text-center">Carsales by default shows you 'featured' listings. Users can choose a Standard, Premium or Ultimate listing package when paying for their listing 🚗</figcaption>
<br>

For this to even be worth our time, I'd first want to know our data on what % of tasks posted receive no offers. If an extremely low % of posts do, then this revenue model might not be viable since there is no incentive for Posters to pay for something they don't need. Maybe the only benefit would be to receive offers quicker, but again i'd want to see the average time of an accepted task on the platform to know whether this is actually an issue. Looking at your marketing landing pages (like <a href="https://www.airtasker.com/gardening/" target="_blank">Gardening</a>), most categories of job have a pretty speedy average time to receive an offer (a few hours).

However, if the % of posts that don't receive an offer is significant, I'd then want to dig further to see if we have impression data on the platform like number of listings seen by Taskers (not necessarily viewing the actual listing, but just coming across it in the browse feature). If we track event properties like `post_id` then we can see if the posts which did not receive any offers were because of receiving below average impressions, or because of some other qualitative factors (e.g. poor post description and inaccurate pricing). If it is the former, than there's{% include elements/highlight.html text="preliminary evidence to suggest that allowing users to pay to boost their posts could be a viable business model." %}

<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q8" text="👉 Next Question" %}
</p>

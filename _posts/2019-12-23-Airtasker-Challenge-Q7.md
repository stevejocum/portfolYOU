---
title: Tasker Ads
tags:
style: fill
color: primary
description: Question 7
---
{% include elements/button.html link="/essays/Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q8" text="👉 Next Question" %}

**Question 7:** *Airtasker's leadership team is considering an additional business model that allows taskers (people who work in the platform) to run ads in the marketplace. How do you determine its potential impact?*

---

This is a really interesting business model! Before tackling how I'd assess it's impact though, I'd want to clarify with the leadership team why we're considering this additional business model. Given the current business goals around profitability, sustainability and growing revenue streams, I’d say the primary driver is to grow Airtasker's revenue, so its a business problem we’re solving, not a customer problem. This could, however, have numerous benefits for both Posters and Taskers, which I will touch on in a moment.

I'd also want to better understand the mechanics of the business model and how it would work for the user and business. When we say “run ads in the marketplace”, does that mean ads running in the existing marketplace embedded in the current structure or a totally new feature? I see many ways this could be implemented:
- Would Posters post a task and then immediately receive ads for recommended Taskers?
- Would Posters be able to search and find specific individuals for a task?
   - Eg. A ‘Tasker Ads’ tab where you can search for Taskers in certain categories to find suitable people to offer services? (similar to some of our landing pages for non-registered users like <a href="https://www.airtasker.com/painting/house-painting/" target="_blank">House Painting</a>)
- Would Taskers make bids on jobs and the Tasker's who've paid for ads are floated to the top of the list as recommended?
- Would the Tasker be required to pay fixed pricing for the ads? Would there be a tiered structure where the more you pay, the more discoverability you get
- Would the Tasker pay per impression?
- Would the Tasker have to bid for ads similar to Google Ads?
- Do Taskers bid for ads on individual job posts or just pay Airtasker and we showcase them to posters?

Since you said the leadership team is ***considering*** this business model, I assume the idea isn’t fully fleshed out in terms of its exact implementation. However, I'd still like to know what management is envisioning this looking like so I can have a better idea of how to assess its impact. Determining the 'impact' of a business model like this is not trivial. There are quite a few ways to break down what affect it would have on Airtasker, so I have broken it down by the impact to the business and the impact to users.

## Impact On Our Business 🏢

<u>Success Metrics</u>

#### Financial

As I mentioned, it seems clear that our primary driver for this change is to grow Revenue. Airtasker has always had its revenue stream from taskers, taking a 20% cut of the Tasker revenue (now in a tiered structure) and since X months ago, taking a fee from posters. Allowing taskers to run ads in the market place would provide a 3rd and diversified revenue stream for Airtasker. Given our goal of becoming a more profitable, sustainable company this additional revenue stream would help us towards that goal.

* I’d imagine there is a success metric (primary, and perhaps secondary too) which will determine whether this idea is successful or not. Eg. Grow revenue by 10%. Increase acceptance rates by 25%.
* Further research would need to be taken into this based on certain financial assumptions - costs, uptake from taskers, pessimistic, neutral and optimistic scenarios etc
* Cannibalization - advertising might take the bulk of the jobs and cannibalise existing business
* To assess the full impact on revenue, a detailed financial analysis based on financial modelling will need to take place based on further research

Revenue is not the only financial impact this ads business model can have on the business. There are also costs involved which could impact our bottom line. E.g. engineering costs maintain adds platform, new payments infrastructure, costs of monitoring the actual ads marketplace and ensuring it is used correctly (e.g. additional staff, or is this baked into the software and we are very hands off)

- Revenue

### Product

Other important product metrics

<u>Technical</u>
- do we have the technical capability to build sophistocated matching algorithms?
- Can we reuse any existing codebase? For example, we currently have a notification system to alert taskers on things we think are relevant to them
- Our current use of the Stripe API is for transactional revenue. We’re taking a clip from taskers and posters. If we move to an ad model it may require a refactor of our billing infrastructure to enable this additional payment channel.
   - In my current workplace, we wanted to add an additional plan tier and even that required a complete refactor of our Billing API, which consisted of an entire re-write of the Billing system on the backend, and then implementation on the frontend
- There would also likely be a substantial development cost. This is not a trivial change (depending on implementation method) - significant backend, data engineering and pipeline, and frontend

<u>Brand and Community Perception</u>
- being too money greedy. People already getting concerned about how much money we're already taking from users (mention Pam quote and images of reviews)

<u>Alignment to our Mission</u>
- Would doing this enable more people to realize the full value of their skills? It might allow some people to if ads help them get discovered but what about the ones that don't have the propensity to spend? Do we actually alienate a large portion of people from realizing the full value of their skills?

## Impact On Our Users 👷‍👩🏻‍💼

<u>Tasker</u>

#### Positive Impacts

- Could help posters more quickly fill their jobs (quicker assign rates). The decision making is changed from the tasker to the poster - a change in ownership and decision making. Rather than waiting for offers, they can actively choose. So this would provide more choice and the ability to fill jobs faster for posters.
        - Overall, I don’t think the biggest problem on the platform is getting offers on tasks (I’d love to look at our data to know what percentage of tasks posted do not get offers, but my assumption is that this figure is very low). So I don’t think this benefit would be incredibly huge. The main thing is ensuring high quality offers. If this ad model can do that then it will be very beneficial to posters.

#### Negative Impacts

- Making the platform less organic.
- Not showing the most ‘relevant’, neutral results, just the people that pay the most

when you’re placing ads on your site, you’re serving two audiences with conflicting interests: from a user experience point of view, ads are almost always a hindrance, and your users would generally be happier without ads.

<u>Poster</u>

#### Positive Impacts

#### Negative Impacts

---

## Charging Posters? 🤔

Advertising is a common business model for marketplaces (especially as an additional revenu stream on top of other business models like commission fees, listing fees, subscription/membership fees etc). However, it's more common that the advertising is on the supply side, not the demand. Marketplaces like Seek, CarSales, Gumtree, Facebook Marketplace and many others offer the person creating the listing the opportunity to 'boost' their post and have it viewed by more people.

<img src="https://i.ibb.co/T1KXYqF/Screen-Shot-2020-01-02-at-4-36-49-pm.png" width="250" height="450">
<figcaption class="figure-caption text-center">This is not an ideal situation for a product team to be in 🎯</figcaption>
<br>

<img src="https://i.ibb.co/09nvxrp/Screen-Shot-2020-01-02-at-4-38-42-pm.png" width="450" height="300">
<figcaption class="figure-caption text-center">Carsales by default shows you 'featured' listings, those which users have paid more</figcaption>
<br>

<p class="text-center">
{% include elements/button.html link="/essays//Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q8" text="👉 Next Question" %}
</p>

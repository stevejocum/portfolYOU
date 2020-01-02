---
title: 10 Random Features
tags:
style: fill
color: primary
description: Question 1
---
{% include elements/button.html link="/essays/Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q2" text="👉 Next Question" %}

**Question 1:** *Given a choice of 10 random product/growth features, how do you determine which ones to execute?*

---

I think there are 3 possible scenarios here:

## 1) The team has a general list of ideas in the backlog which aren’t rooted in a customer or business problem

If I had a list of 10 features in front of me, I could use all the prioritisation frameworks in the world, but it would still be very difficult to select the right one if I don’t understand why we’re choosing one of these to work on in the first place.

<img src="https://media.giphy.com/media/Q62cWrGZqzsYw/source.gif" width="450" height="250">
<figcaption class="figure-caption text-center">This is not an ideal situation for a product team to be in 🎯</figcaption>
<br>

So the first thing I would do is strip it back and ensure our team{% include elements/highlight.html text="understand why we want to release one of these initiatives." %}I’d ask our team and senior leaders:

- What is our biggest company objective for the next quarter? For the next year? For the next 3 years?
- What is the most immediate objective for my product team? Are there any OKRs we have for the next quarter?
- What business problem do we want to solve with this next feature release? What area of the business are we trying to improve?
    - **Example:** stagnating revenue, poor user retention, improve average offer to post ratio
- What customer problem do we want to solve with this next release? What area of the current user experience are we trying to improve?
    - **Example:** Help Posters to select the right candidate from the offers they receive, reduce the number of Posters who experience Taskers not showing up for a job
- What are our success criteria for this release so that we objectively know if we succeeded or not?
    - **Example:** Increase monthly revenue by 10%, increase the number of Posters who post a task in their first session by 20%.

Answering these questions will give me a clear picture of what my team should be trying to achieve, and therefore, what we should build. I should now be able to quickly cut down the list of 10 initiatives to a one or two features that we think could actually solve the problem at hand. However, I wouldn’t want to restrict ourselves to this existing list of random features, many of which may have been targeted at a totally different objective to what we actually care about right now. I’d want our team to{% include elements/highlight.html text="ideate new potential solutions to solve the problem that we now have clarity over." %}

## 2) The problem we’re solving and the desired outcome are known, and we have ideated a number of solutions to solve the problem

This second scenario (the ideal one!) is where my{% include elements/highlight.html text="team has total clarity on what problem we’re trying to solve and how we will know if we succeeded." %}My assumption is that we would have had some formalised brainstorming of solutions to solve the problem and these 10 product/growth features are the result of that.

|Problem to solve | Leading success indicator | Lagging success indicator |
| ------------- |-------------| -----|
| Reduce the number of users who churn after their first session | Increase number of Taskers submitting an offer on their first session by 20%, Increase number of Posters posting a task on their first session by 20% | Increase the number of Taskers returning for a second session by 15%, Increase the number of Posters returning for a second session by 15%|

<figcaption class="figure-caption text-center">Example of a well considered initiative before deciding what solution to build</figcaption>
<br>

Now, this becomes an exercise of prioritizing which potential solution to execute. For me, the aim of this exercise is{%include elements/highlight.html text="not to pick the one idea we're going to execute, but the 2 or 3 we have the highest conviction will achieve the result we want."%}After that, I like to actually validate with users which of our high conviction solutions are the best, as our{% include elements/highlight.html text="users are the best judge of whether a solution we've built solves their problems." %}I tend to do that with concept and value testing in a qualitative user interview format, or an A/B test with MVPs of our solutions to get some more statistical significance.

While we could qualitatively look at our potential solutions and make a decision on the ones we think are the best candidates, I like using some more quantitative measure to remain objective. I like to use Intercom's{% include elements/highlight.html text="RICE Score" %}(Reach, Impact, Confidence, Effort) to determine the quality and fit of a solution to our problem at hand. Whilst there are so many factors to consider when prioritizing which solution to build, I find this score encompasses majority of those things and does a pretty good 'filtering' job to give some direction to the product team as to which select few ideas we should pursue further.  
<br>

### Breaking Down the  RICE Score
<br>
#### Reach

**How many users will this feature impact?**

For this, I'd look at each solution and estimate how many users will be interacting with it over a certain period (e.g. monthly). Based on the particular success metric and problem we're solving, this 'Reach' metric might change but will usually follow a consistent format of number of people or events over a time period - e.g. customers per month, completed transactions per month from Airtasker pay to Tasker).

There may be times we have to pull a number from a hat, but where possible it's crucial to use real data from our analytics to estimate the reach of a feature. E.g. if we know this feature will be seen by every Poster who accepts a Tasker for a Job in a given month, we can very easily look the average number of accepted tasks per month to gage the reach of the feature.

*For our final calculation, we use the number of users or events per time period for our variable `R`.*

#### Impact

**How much will this feature impact each user we reach?**

Here we look at how likely the feature will lead to the customer outcome we intend when each user encounters it. This dimension is a bit more 'gut feel'. We typically need to do some user research to get a better gage of a feature's potential impact.  

*For our final calculation our we use the following criteria to get our variable `I`:*

- Massive impact = 3x
- High impact = 2x
- Medium impact = 1x
- Low impact = 0.5x
- Minimal impact = 0.25x

#### Confidence

**How confident are we in our estimates of Reach, Impact and Effort?**

This is a really good dimension as it allows us to account for poor estimation. For example, say we think a project will have huge impact but we don't really have the data to back it up, the confidence score allows us to take that into consideration.

*For our final calculation our we use the following criteria to get our variable `C`:*

- High confidence= 100%
- Medium confidence= 80%
- Low confidence= 50%

#### Effort

**How many 'person-months' will this project take to ship?**

This is where it's good to get some input from engineering and design to roughly estimate how much people-power is needed for a particular feature. E.g. 2 weeks planning, 1 week design, 3 weeks build is 1.5 person months. From a technical standpoint, it's important to consider our current tech stack, capabilities and what enabling this new feature would entail. Does this require building entire new functionality we don't have from scratch? Are there existing libraries we can use for the solution to cut engineering time and still achieve a quality solution? Same here for design - this solution may have a very thin UI layer while most of the complexity lies on the backend. Or inversely, there may be no or minimal architectural, data pipeline and infrastructure changes but the design and frontend UI component of the feature is very complex.  

For the first three variables, the higher the score the better. Here, it's the opposite - the lower the effort the more attractive the project if it can achieve the result we want.

*For our final calculation our we use the number of person-months get our variable `E`:*

#### Calculation

`RICE SCORE = (R x I x C)/E`


|Feature| Reach | Impact |Confidence |Ease |RICE Score |
| ------------- |-------------| -----| -----| -----|
| 1|4,500|3|100% |2|6750|
| 2|15000|1|80%|3.5|3429|
| 3|7000|2|50%|1|7000|
| 4|10000|1|50%|1.5|3333|
| 5|...|...|...|...|...|
| 6|...|...|...|...|...|
| 7|...|...|...|...|...|
| 8|...|...|...|...|...|
| 9|...|...|...|...|...|
| 10|...|...|...|...|...|

<figcaption class="figure-caption">Putting all our features side by side lets us see which have the greatest potential</figcaption>
<br>

---

There are some additional factors I think are important to consider when deciding which feature to execute which don't get encompassed by a qualitative scoring method like RICE:

<u>Reversibility of decision</u>

I like to look at whether certain product decisions are one way or two way doors. If we make a decision and it doesn't work, how easy is it to go back? Based on the circumstances and context around what we’re working on, I’d decide that if it is a non-reversible change we might need to conduct further research on a number of ideas to be more confident on our estimates of reach, solution impact and effort before we move on. However, if it is a very reversible decision and we have many time pressures, I’d feel much more comfortable picking one option from a selection of high potential candidates.

<u>Fit with the current product</u>

Every new feature added to a product has a risk of:
- **Feature bloating**
   - While Enterprise Software is in some instances acceptable to have many features and capabilities, mass consumer platforms like Airtasker rely on simplicity to be accessible to a broad range of users. The more features we add, the greater the complexity of the product.
- **Adversely impacting other parts of the product and user experience**
   - Introducing a new feature might change the usage patterns of other features. This is okay, but it's important to consider the follow on affect of changed user behvaiour. E.g. A new feature to instantly match supply and demand might negatively impact ability of new taskers to get a job.
- **Adversely impacting other product metrics**
   - There have been times where I prioritized a feature based on our current business goals and it improved our targeted business metric but negatively impacted another critical one. So it's simportant to ask if this feature could negatively impact adjacent but important metrics that matter to the health of our business - revenue, retention, conversion etc

<u>Stakeholder impact</u>

We'd need to consider what impact this has on all areas of the business besides just product, engineering and design. Some examples could be:
- Do we need to train support and sales in understanding the new feature and business model to be ready to handle customer inquiries or pitch for business respectively?
- Does this new feature change our value propisition and require us to reconsider our product messaging, marketing material and go to market strategy?
- Are there legal hurdles which would prevent us from launching this?


## 3) The 10 random features are scoped projects which are planned in our roadmap that need to be prioritised

The third scenario I can draw from this question is that we have a roadmap with these 10 projects and need to prioritise them and decide it's sequence. Overall, I believe{% include elements/highlight.html text="roadmaps should not go out beyond 6 months" %}because it{% include elements/highlight.html text="anchors you into building things which might not be relevant to the business context at that point in time." %}We can plan a year out, but we can’t tell the future, so it’s important to have that flexibility.
- The next 6-8 weeks should be very known
- The following few months can be planned with high level briefs
- Anything after that are loose product initiatives aligned with the mission


I’d ask similar questions to scenario 1 mentioned at the beginning of my answer to understand our most important business goals and what problems are most critical for our business. The RICE framework can also be applied to this scenario as it works just as well for comparing apples to apples as it does apples to oranges, since you end up with a quantitative score to assess which initiative would have the largest positive impact on our business. In many ways, it's actually a lot easier to estimate impact, confidence and effort for projects on the roadmap which have already been scoped.

However, there are a couple other frameworks I think apply specifically to this roadmap prioritization scenario:

### 1) Kano Model

There are three types of features a company can ship to users:

#### Basic Expectations 😤

These are features that a user expects to be there (generally based on their experience with similar products). Users tend not to talk about these or ask for them, but will complain if they're not there. If you asked someone to design their ideal hotel experience, they may talk about a big bed, a private jacuzzi, big TV with Netflix, free room service, but they’ll never talk about having a toilet in the room and having hot water available in the shower at 2am when they come back from a big night out.

While these features don't score high on satisfaction, they're critical to retaining users and ensuring they don't get frustrated by a lack of something they consider essential.  

#### Satisfiers or Performance Features 😊

These are features which users want but don't necessarily need. They could live without it, but the presence of these features makes them satisfied. Most feature requests fall into this category - e.g. more advanced search filters for tasks, or ability to sort offers on your task.

#### Delighters 😲

These are features that 'wow' the user. Users don't ask for these features, but are usually blown away when they see them. This could range from Apple's 'share wifi' feature to a restaurant giving you a complimentary desert at the end of your meal.

---

I find this a great framework to understand what fits into a release cycle. A good shipping cadence will ensure that we have a sprinkle of each type of feature in a release (all 3 are important to satisfying users). However, I would tend to{% include elements/highlight.html text="prioritize a project targeted at meeting a basic expectation over one aimed at delighting users." %}

For example, say 3 of the 10 projects in our roadmap were:
1. A new tasker vetting system to reduce the likelihood of a Tasker not showing up for a job after they've been accepted by the Poster
2. The ability for Posters to Sort task offers to find the best candidate
3. Instant matching of a Tasker to a Post


|Basic Expectation | Satisfier | Delighter |
| ------------- |-------------| -----|
|Vetting System to Reduce No Shows | Sorting Task Offers|Instant Matching |

<figcaption class="figure-caption">Categorizing these by the Kano Model would look like this</figcaption>
<br>


While sorting task offers would satisfy a lot of users and instant matching of supply and demand on the platform could be the most amazing user experience for each party, if a Poster accepts an offer and then that Tasker doesn't answer their messages or show up for the job, that user will almost certainly complain to us and likely never use us again. It's a basic expectation of a Poster on our platform that if they accept someone for the job, the person will complete the job.

<img src="https://i.ibb.co/MN2P4mP/Overview.png" width="200" height="450">
<figcaption class="figure-caption text-center">What happens when we fail to meet basic expectations</figcaption>
<br>

### 2) Urgency x Importance Matrix

This is actually something I picked up from Stephen Covey's 7 Habits of Highly Effective People, my favourite personal development book i've read. He had this fantastic time management framework to apply to your own personal goals. I think it's extremely fitting to PMs making prioritization decisions for the roadmap.

<img src="https://i.ibb.co/2qYBKWL/Screen-Shot-2019-12-30-at-10-13-55-pm.png" width="550" height="350">
<figcaption class="figure-caption text-center">Urgency x Importance prioritization matrix</figcaption>
<br>

The matrix involves plotting any feature/initiative based on how urgent it is needed and how important it would be for the business to have it.

|Urgent, Important| Not Urgent, Important | Urgent, Not Important |Not Urgent, Not Important |
| ------------- |-------------| -----| -----|
|These are usually crisis situations or things which if we don't address right now will cause significant business problems. These should be prioritized above others | These are things which aren't pressing matters, but we know will be important longer term. Whilst the urgent and important matters should be prioritized, if all we did was work on those we'd never be working on projects that drive business growth and add new value for customers, so these are in many ways just as important. I'd prioritize these alongside the urgent and important projects, or at a bare minimum ensure resources are dedicated to any further planning and scoping needed for that project so they are in a good position to work on next.|These are time wasters which although may need to be done are impeding our ability to focus on the high impact projects which will drive business results. I'd de-prioritize these until they become urgent and important, or allocate a minimal set of resources to them|These are distractions that should be avoided at all costs, as they are time wasters not adding value to the business.|

---

On a final note, I think it's important to consider the definition of 'execute' mentioned in the question. For the purposes of the question, I assumed we meant 'deciding what to work on', but execution can also mean delivery. So in terms of actually delivering a solution, I like to use a{% include elements/highlight.html text="canary release" %}methodology to roll out a new feature to a subset of users and{% include elements/highlight.html text="measure whether the feature actually achieves our primary and secondary success metrics before a full roll-out." %}

<p class="text-center">
{% include elements/button.html link="/essays//Airtasker-Challenge" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q2" text="👉 Next Question" %}
</p>

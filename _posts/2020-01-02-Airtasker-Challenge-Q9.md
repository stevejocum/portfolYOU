---
title: Instant Matching
tags:
style: fill
color: primary
description: Question 9
---
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q10" text="👉 Next Question" %}

**Question 9:** *A teammate suggests we build a product that helps instantly match demand and supply. But another thinks this cannot be done because unlike transportation, the jobs being done on Airtasker are too complex and we can never fully scope every one of them upfront. How would you approach such a problem?*

---

## Why would we build this?

It is firstly extremely critical to assess{% include elements/highlight.html text="why instantly matching demand and supply is an initiative that is important to the business." %}What exactly would instantly matching demand and supply achieve for the user and for Airtasker? So I’d start with trying to narrow my understanding of:
- What problem we believe the solution of ‘Instant Match’ would help solve
- Whether this is actually a priority for the company given:
   - Our broader company goals (short, medium, long term)
   - The critical metrics (leading and lagging indicators) that my team and other product teams are focused on moving
   - Current initiatives we are already working on
   - Existing product roadmap

## How would it work?

It's hard to have an effective discussion if both parties are on different wavelengths of what the product will look like. Whilst it is best to start with problems than identify the solution, at a minimum I'd want to understand how my team-mate envisions Instant Matching working for the user. I'd ask them:

- How do you define 'Instant Matching' in this context for Airtasker?
- How do you envision this working? What would the experience look like for a Tasker and Poster that gets instantly matched?
   - Do we automatically assign the task to the most suitable?
   - Or is it like Uber where we notify the most suitable Tasker about the job and they have a limited time to accept it?
- Is this an optional feature that Posters and Taskers get to choose whether they want it? Or would this be a global change?

This now gets me on the same page as my colleague in terms of what this might look like in the real world. Now I can start digging a bid deeper.

## Praise and dig into source

I'd say to my colleague:

> Instant Matching is a really interesting idea! What made you think of it?

#### Reason for question

Ideas are amazing and I constantly encourage people from all disciplines and departments to share whatever ideas they they think could improve the Airtasker experience for our stakeholders. So I would first{% include elements/highlight.html text="praise my team mate" %}for providing a really interesting idea and knowing that{% include elements/highlight.html text="their contributions are acknowledged and valued." %}

This question also{% include elements/highlight.html text="allows me to understand the root of the idea and what sparked it." %}This idea wouldn’t have just appeared out of thin air and was likely a solution to some problem this person believed was important in the business (or perhaps not, in which case I would certainly want to know!)

That leads to my next question…

## Customer/Business problem

I'd then ask my colleague:

> What problem do you believe instantly matching demand and supply would help solve?

#### Reason for question

{% include elements/highlight.html text="I don’t believe products should ever start with a solution and then try find the problem to match it." %}We always need to start with the problem at hand and have a very narrow understanding of that. From there, we have a much clearer idea for how we can solve it, and perhaps instantly matching demand and supply is not the right solution to it.

<img src="https://media.giphy.com/media/G2MPcSmq0DZcs/source.gif" width="300" height="500">
<figcaption class="figure-caption text-center">What happens when you start with the solution before the problem </figcaption>
<br>

For example, framing it as a problem, is this about:
- Reduce the number of tasks which do not receive an offer? (improve Bid:Post ratio)
- Reduce the number of tasks that don't get assigned? (improve average assign rates)
- Reduce the average assign time per post? (how long it takes for a task to get assigned once it's been posted)
- Reduce the time it takes for a Poster to select the right Tasker for their job once they've received offers?
- Reduce the time and effort involved for a Tasker to get a job that matches their skills?  

Now we can understand what problem we're trying to solve and whether 'Instant Matching' is actually an effective solution for it.

## Business outcome

I'd then ask my colleague:

> If it works in the way you anticipate, how do you think this idea would positively impact our company?

Everything we build at Airtasker needs to be:
- **Valuable:** users want it and it solves their problems or improves their lives
- **Usable:** it is understandable and users can get to the value
- **Feasible:** we are actually able to build it within our constraints
- **Viable:** it works for the business and achieves a positive business result

It’s this last one, `Viability`, that I am trying to answer here. Whilst there's a place for features that add value to users but don’t have a substantial business impact (eg. Nice to haves and delighter features), a company like Airtasker whose core goal is to become a profitable, sustainable entity on its own, should very much be thinking about how what we build impacts the profitability and revenue making potential of our company.

For whatever I build, it's always critical to understand{% include elements/highlight.html text="what our success metrics are and what business outcome we are hoping to achieve:" %}
- What **financial** impact do we intend to have on the company by solving this problem? (e.g. increase revenue by 15%)
- What **non-financial** impact do we believe solving this problem would have on the business? (e.g. product metrics like task assign and completion rates)

### Value of product

Before jumping in to the concern my colleague has about the complexity of scoping each job for Instant Matching, I think there is a critical risk here besides simply the technical complexities of matching the kind of tasks on Airtasker, and that is{% include elements/highlight.html text="Value Risk - Do users actually want this?" %}

{% include elements/highlight.html text="Most products fail not because teams didn't have the technical capabilities to build it, but because it doesn't solve a problem and add value to users." %}

<u>Posters</u>

Do posters actually want to instantly have their post matched? Or do they prefer having the control of selecting their candidate themselves to feel secure and confident in our platform?

<u>Taskers</u>

Do Taskers actually want to be instantly assigned to a task they don’t know about or do they prefer manually posting offers on the tasks they feel they are a fit for?

<img src="https://img.icliniq.com/qa/my-child-is-refusing-food-what-can-be-the-reason.jpg" width="600" height="400">
<figcaption class="figure-caption text-center">We need to validate that this is something users want before we give it to them</figcaption>
<br>

I would encourage the team to get{% include elements/highlight.html text="rapid learning with the least effort to validate this hypothesis." %}I'd suggest building some quick prototypes and conduct some user testing to see user behaviour with the feature, how valuable they think it is and whether they’d use it. This can be super lightweight - Eg. Simple toggle button at end of task post (Poster) or during onboarding (Tasker) and maybe 1-2 slides explanation on the value. I'd also combine this with a qualitative interview to understand the Tasker and Poster experience and whether the problems we're trying to solve with this product exist in their use of Airtasker.

---

If after asking these questions to myself and my colleagues I believe this idea is grounded in sound foundations (solves an important problem, is relevant to our current business goals and could have a large positive impact on the business), I’d then want to address the concerns of the other team mate and what assumptions they have.



## Complexities of scoping each task

Product risk can be split up into the four factors I mentioned earlier:
- **Value Risk:** The risk that users will not want the product and that the problem it solves is not meaningful enough for them
- **Usability Risk:** The risk that users will not be able to understand and use what we've built
- **Feasibility Risk:** The risk that we won't be able to build the solution and actually solve the problem
- **Viability Risk:** The risk that the solution doesn't work for our business and achieve a business result

I have already addressed value and viability risk. Usability risk I believe can always be solved, as a UI can always be tested with users and iterated on until it is understandable and usable.{% include elements/highlight.html text="This concern from my colleague clearly falls into the feasbility risk column." %}

The biggest concern of my colleague is their belief that jobs being done on Airtasker are too complex and we can never fully scope every one of them upfront. I understand where my colleague is coming from - although Uber has variations of their service, they really provides only 1 service (get me from point A to B via a car). We have many different task types - house cleaning, resume writing, removalist, market research, website development. The key though, is to{% include elements/highlight.html text="break down 'complexity' to understand why we think it would be difficult, and whether these are actually solvable:" %}

<br>
#### What's complex?

I'd ask my colleague:

> What do you mean by 'scope'? What would scoping a task consist of?

I'd want to clarify what is actually involved in scoping a task, and what elements need to be extracted to make a match.

> Why could we never scope every one of the tasks up front?

> What exactly do you think is too complex about the jobs posted on Air Tasker?

I want to know exactly what the source of concern is around 'complexity of scoping a task' so we can understand whether it's valid and how we may go about solving it.

<br>
#### Category breakdown  

I'd ask my colleague:

> Which specific jobs and scenarios concern you?

> What jobs do you think instant matching would be most beneficial for? What jobs do you think instant matching would be counter-productive for?

> Are there jobs being done on Airtasker right now that you think are not complex and we’d be able to instantly match people with a greater degree of ease?

I'm curious to know if it is a certain type of job which are concerning us. We may uncover that a number of jobs are standardized and simple enough to have instant matching for while others might be unsuitable.

If that is the case, I'd also want to understand whether those which we do think can be a match are actually important categories for Airtasker. I'd want to look at our data to see a breakdown of job posts by category to see which tasks are our most commonly posted on the platform.

We may be able to uncover an 80/20 solution where our most popular tasks are able to be feasibly scoped for instant matching.

<br>

#### Matching Algorithm

I believe there are two components to a matching algorithm for Airtasker Instant Match:

{% include elements/highlight.html text="Relevance:" %}- the Tasker is suitable for the job

{% include elements/highlight.html text="Proximity:" %}- the Tasker is close to the task location

I'd also want to have an engineer present to discuss their understanding of building a matching algorithm and what other considerations need to be made.

<br>
##### Relevance

<u>Suitability of Tasker</u>

If I received an instant match for a task about graphic design, I'd certainly not be able to complete it to the satisfactory standard of the Poster. That's why we need to ensure the Tasker matched to the post is suitable. We'd need to match users based on several factors, such as:
- Skills
- Number of jobs completed
- Category/type of jobs completed
- Completion Rate

One are of concern I'd have is whether the relevance factor of our matching algorithm could favor Taskers who have already completed many jobs and alienate first time Taskers. This could have an adverse impact on number of active Taskers and lead to higher Tasker churn.

<u>Desirability from Takser</u>

On Uber, it's very easy to know which drivers are currently in the car working and looking for jobs. Our case is a little different. This is primarily because we don't necessarily know what tasks a Tasker wants to complete. Our algorithm may be able to infer the relevance of a Tasker to a job for those who have already completed a certain number of jobs. However, for new Taskers we may need to ask them during onboarding what types of tasks they're interested in so we can effectively match first time Taskers.


##### Proximity

The location of the task can impact our ability to instantly match the Poster and Tasker.

<u>Remote</u>

If it's an online task, physical location is not a matching factor at all. It would simply be finding the most suitable tasker based on the relevance factor.

<u>Physical</u>

If it's a physical task we're instantly matching, the algorithm would need to take into account proximity of the users location to the task location. However, this would not be the only factor as it would also need to consider relevance of the Tasker. There may need to be some weights applied to determine which is most important - e.g. who would our algorithm choose first between the following 2 users:
- **User 1:** 500m away from the task location but hasn't completed any tasks yet
- **User 2:** 5km away from the task location and has completed 2 previous tasks, 1 of which matches the category of this particular post

---

<br>

Peeling back the layers to understand what Instant Matching would achieve for the user and the business is critical to getting us on the right track before getting stuck in the weeds of solutions. Similarly, diving deeper into the complexities of the solution which concerned my colleague like I have shown will allow us to break down what those complexities really are, whether they are actually problems or not, and how we would go about solving them.

<p class="text-center">
{% include elements/button.html link="/essays/Airtasker-Challenge#challenge-questions" text="🏠 Back to Home" %}
{% include elements/button.html link="/essays/Airtasker-Challenge-Q10" text="👉 Next Question" %}
</p>

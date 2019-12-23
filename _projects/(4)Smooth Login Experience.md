---
name: Smooth Login UX
tools: [Simply Wall St]
image: https://i.ibb.co/w43qtcy/Screen-Shot-2019-12-07-at-3-12-28-pm.png
description: A simple, tightly scoped solution to helping users log in to the app correctly and seamlessly
---

Be sure to mention:
- problem, user feedback and data on duplicate accounts
- best solution was to unify duplicate accounts, but this required significant backend work so we scoped the solution tightly to be completed with 1-2 days development work
- Decided to ignore existing duplicate accounts, but just prevent it for new users. We can deal with the existing user issues later
- Figma designs
- Implementation - backend amended our login/registration API to return the provider source tied to the email address once the email was validated. Frontend was therefore very simple - allowed us to display to the user which provider is tied to that login method and let them with 1 click login.
- Results

## Improving our Activation

{%- capture list_items -%}
My Role in this Project
The Problem
Hypothesis
Discovery research
Solution Ideation
Solution Validation
Implementation
Pre-launch validation
Go to market strategy
Launch
{%- endcapture -%}

{% include elements/list.html title="Table of Contents" type="toc" %}

## My Role in this Project

I was the lead product manager on this project. I was responsible for the entire end to end product lifecycle, from identification of the problem, problem scoping, discovery research through to delivery, launch and post launch validation.

## The Problem

Our primary acquisition strategy was content marketing. We had 2 parts of our business - the Simply Wall St application (a freemium SaaS product) and Simply Wall St News (a free News site providing analysis on individual stocks world-wide).

Our news site receives over 1 Million unique monthly readers. We partnered with Apple, Google and Yahoo to syndicate our news articles. A typical user would:
- Search Google for a stock
- Click on our article
- Read our article
- Click a link in the article which took them to our website
- Scroll through our website and receive a prompt to register
- Create an account and automatically begin a free trial

**PROVIDE A GIF OF THE FLOW!**

Whilst this was an extremely efficient funnel, leading to over 17,000 new accounts a week, a very low proportion of them stuck around after their first session.

According to the [Pirate Metrics]([https://www.slideshare.net/dmc500hats/startup-metrics-for-pirates-long-version]) (of which I believe any feature a PM is working on can be tied to at least one of those outcomes) we were amazing at Acquisition, but very poor at Activation and Retention.

{%- capture carousel_images -%}
https://bit.ly/2BBbVhc
https://bit.ly/2DOtxXB
{%- endcapture -%}

{% include elements/carousel.html %}



## Hypothesis

## Discovery Research
- Interviews in Tyro (existing users and non-users)

## Solution Ideation

## Solution Validation

## Implementation

## Pre-launch validation

## Go to Market Strategy

## Launch

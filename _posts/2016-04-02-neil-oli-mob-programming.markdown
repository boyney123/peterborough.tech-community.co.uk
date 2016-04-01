---
layout: post
title:  "Mob Programming: Put down the pitchforks and pick up a keyboard"
cover: http://i.imgur.com/a1kaZPc.jpg
date:   2016-04-02 08:00:00 +0000
categories: tech
subtitle: Mob Programming
blurb: How mobbing can help you to produce high-quality code, built to do the right thing, which is understood by everybody within the team.

author: Neil Studd
---

Together with my colleague [Oli Wennell](https://twitter.com/owennell), I recently gave a talk at the BGL Technology Conference in Shoreditch, to communicate our team's love of mob programming. [The slides are available online](http://www.slideshare.net/NeilStudd1/mob-programming-put-down-the-pitchforks-and-pick-up-a-keyboard) but there's not a lot of context on there, so I've written this article to bring its message to a wider audience!

## The challenges that we all face

When I'm working within agile teams, or talking to those who do, I often hear many of the same issues being raised repeatedly at retrospectives. Common recurring issues include:

* **Information silos:** Specialist knowledge is known by only a few members of the team. We often express our desire to break down these silos by pairing and sharing, but inevitably when we're up against tight deadlines (when are we not?), we fall-back to giving tasks to the person who knows the code best.
* **Too many meetings:** Even when we're calling ourselves agile, we're often drowning in meetings and ceremonies. There are story kick-off and review meetings, which often involve complex discussions around requirements and architecture, which everyone forgets as soon as they leave the room. The answer? More meetings!
* **Waiting for questions to be answered:** Once we've started to work on a task, inevitably we'll reach a point where we need clarification from a key stakeholder. Depending on who this is, and which office (or timezone!) they're working in, it may take hours (or even days) to get an answer. So we switch to a different task, and then switch back again once we get an answer, incurring context-switching penalties along the way. Wouldn't it be nice if we could remove the need to have a long wait for answers?
* **Testing and reviewing too late:** Many agile teams are actually working in a series of mini-waterfalls. Story kick-offs are the requirements-gathering session; then the developers implement the feature; then they throw it "over the wall" to the testers for verification. One of the key goals of agile is to have people of all disciplines working together at the same time, so it's frustrating when a team devolves back to a production-line mentality.
* **Inconsistent coding practices:** Have you ever looked at a piece of code, and you've known who's written it without even looking at the history or comments? Everybody has their own style, which creates inconsistency in the codebase, adding to the pile of technical debt that you'll never have time to fix.

From my experiences at [Compare The Market](http://www.comparethemarket.com), I've found that all of these pain-points can be reduced greatly if you're willing to embrace the power of mob programming.

## What is mob programming?

[Mob programming](http://mobprogramming.org/) (often called mobbing for short) was invented by Woody Zuill, and has been described as "All the brilliant people working on the same thing, at the same time, in the same space, and on the same computer". The first three parts of that sentence are already part of the core tenets of Agile; the addition of having everybody (e.g. developers, testers and business analysts) working on the same computer is its most noticeable difference.

If you're familiar with [pair programming](https://en.wikipedia.org/wiki/Pair_programming) then you'll already know about the roles of the **driver** (writing code at the keyboard) and the **navigator** (offering guidance and review). Mobbing is basically the same, except there are many navigators, and you regularly rotate the person who's the driver (for instance, every 15 minutes).

![One of our mobs in action](http://i.imgur.com/LoHGqfi.jpg)

It's essential to have a centrally-located monitor which anybody is capable of plugging-into or projecting onto. Ideally, everybody should have a similar setup: for example, equivalent Visual Studio / Resharper settings, the same keyboard shortcuts and environment settings, so that anybody can drive from anybody's machine and have much the same experience.

Critics of mob programming say that it's inefficient and wasteful - with only one person writing code at a time, how can this possibly offer value? Well, there's much more to programming than actually writing code:

* Analysing and clarifying requirements
* Deciding how you're going to solve a problem
* Making architectural decisions
* Creating examples/scenarios to drive a TDD approach
* Implementing a simple "walking skeleton" version
* Deciding on whether your first approach is fit-for-purpose
* Agreeing what should be refactored
* Reviewing the solution with stakeholders

These activities require very little writing of code; however, they all require a lot of discussions between people of different disciplines. When you're working in a mob environment, all of those people are already in the same place, allowing for faster decision-making and developing a group consensus in the moment.

## How does mobbing help?

There are a number of notable benefits to adopting a mob programming approach. In no particular order, here's a few of them - each person will probably have their own favourite, depending on which is causing them the most pain at the moment!

Mobbing removes the pain and stress of code reviews, as all of the code is being reviewed as it's written. You'll also experience an equivalent boost in code consistency, as the group gradually adopts a common approach on often-contentious subjects such as indentations and linebreaks.

It's not just code quality which improves; the constant review process means that discussion and debate occurs at the moment when the work is fresh in the group's mind, rather than those annoying "What were we thinking?" conversations which might otherwise happen weeks later.

With everybody working on the same code at the same time, knowledge sharing becomes a natural by-product of the mobbing process. This makes mobbing particularly useful for "spikes" and other work which will be the foundation of future user stories, because it means that anybody can pick up the next user story and already have a grounding in what's been done.

Mob programming is also an incredibly inclusive process, open to people of varying disciplines. It's a great learning environment - "learning by doing" is often the most efficient way to gain knowledge, and for would-be developers (like myself, a tester by trade) it's allowed me to write production code in a safe environment with the support of my colleagues, and I've picked up more skills than I would've done by reading textbooks.

## Watch out for potential pitfalls

Before you run off to try mob programming for yourself, here are a few lessons that we've learned through our mobbing activities. Arm yourselves with these, and you'll have a very good chance of success!

* **Not every task is suited to mobbing:** You don't need a large group of navigators to help you with your timesheet, or to complete mundane, prescriptive tasks. That's OK - we're not saying that mob programming is the only way of working. When we start a user story, we evaluate whether it might be appropriate to mob on it. If it's not, then we don't!
* **Don't be afraid to split the mob:** Once you've started mobbing, don't feel that you're locked-in to this way of working. If it turns out that the task isn't going anywhere, break away until you feel ready to progress. Speaking of which...
* **Beware of rabbit holes:** If you're working on your own, burning 10 minutes on an unrelated investigation might not be a big deal, but if you've got 6-7 people in that rabbit hole with you, that investigation has effectively burned over an hour of the team's time. Try keeping a sidebar or a "To Do" list, to allow you to stay focused on the current activity.
* **Don't make one person drive for too long:** Just like in a car, driving is an intense activity which requires immense concentration, and if you try to do it for too long then you're going to become prone to mistakes and headaches! Rotate the driver regularly, by either using a timer or rotating whenever you get to a natural changeover point (e.g. all of the tests are passing).
* **Support the driver:** Just because the driver is front and centre, it doesn't mean that the navigators get to switch off. They are the eyes and ears of the group, staying heads-up to guide the driver, and doing whatever is necessary to allow them to stay focused on the keyboard. It's not a time for going off to meetings, or to get into a lengthy email discussion. You might be missing an important bit of discussion, and before you know it, you're going to be at the keyboard again.
* **Mobbing requires trust:** Having somebody watching you code can be a stressful experience. How many more mistakes or typos do you make when there's someone looking over your shoulder? Scale that up to multiple navigators watching you, and you'll need to ensure that you have a safe, trusting environment which allows every team member to be in the limelight without fear of reproach.
* **You can't force a team to work like this:** Everything we've discussed above - trust, openness and freedom of communication - comes with time. Newly-formed teams, or new employees being dropped into an existing team, will need to learn each other's boundaries, so that they are comfortable discussing and debating with each other. Don't throw the entire team in at the deep end: run smaller mobbing experiments to begin with, and run frequent retrospectives, to learn what is (or isn't) working for you.

## What's stopping you?

It's easy to get started with mob programming. All you need is a large enough desk, with a good-sized monitor that everybody can see. Then it's just a case of trying it, and finding out whether it works for you.

We've seen that it can be more productive, in the right situations - maybe it will work for you too. Contact myself or Oli if you'd like any tips or assistance on your mobbing adventure!

[Contact Neil via Twitter](https://twitter.com/neilstudd)

[Contact Oli via Twitter](https://twitter.com/owennell)
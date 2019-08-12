_note: this is the mostly unedited RFC that is cited in [my talk](https://speakerdeck.com/buritica/increasing-engineering-tempo-at-splice). a few parts assume knowledge in the organization, but if you have questions about this [send me a tweet](https://twitter.com/buritica) and I'm happy to give you more context on how we were organized at the time or what challenges we had._


# ⚡️ Increasing Engineering Tempo ⚡️

*Authors*:
* juan@splice.com

*Contributors:*
* [email redacted]
* [email redacted]
* [email redacted]

## 1 Summary

Our ability to succeed as a business depends on whether we can learn faster than the market moves. This proposal outlines a strategy to drastically improve how we deliver software so that we can enable faster learning across the board.

To fully realize Splice's vision we must become an organization that is excellent in delivering high-quality software. We can't state enough importance and urgency of the successful execution of this strategy.  We will use this document to guide our approach, and it will serve as the north star for our implementation over the next six months.

🕶 our vision:

> A future where shipping working code is one of the fastest, safest and, most effective ways to learn and to test new ideas.


## 2 Motivation

The objective of this proposal is to set a strategy that organizes and communicates process changes and cultural transformations we want to drive, to improve our ability to deliver working software. Our motivation is to enable Splice to fulfill its mission, so we must aspire and iterate towards becoming excellent in producing working software.

The fast-paced growth of our Engineering Organization (5 ~ 50 in 18 months) has rendered functioning delivery practices ineffective, and our process patching has barely kept us afloat. To get out of this state, we must take a new approach towards improvement.

The strategy outlined below aims to enable the Technology Organization to fuel fast learning for Splice as a whole, and it should have a direct impact on our capacity to scale and fulfill our mission.

Given the cross-functional nature of our team and the different maturity stages of the infrastructure across our products, this strategy will require input and participation from the entire Technology Organization.

In addition to this, Technology Executive team must be decisive in the approach, enable the rest of the organization to execute, and assist in measurement and adaptation of tactics to accomplish our goal of improving delivery. Empower and not dictate.

## 3 Detailed Design

**🔥 a year ago, all we could see were fires**

![fire](https://user-images.githubusercontent.com/228120/42862236-a4726bb4-8a2c-11e8-9a4b-64d581aed382.gif)

The awareness of challenges in our developer toolchain is not new. As we can see in the image below, our desire to improve delivery has been present in our *TODO* list for quite a while. Unfortunately, we found out the hard way that we wouldn't be able to focus on fixing these parts of our process until we resolved enough critical issues.

![image](https://user-images.githubusercontent.com/228120/42861976-7f206330-8a2b-11e8-93a9-9155df0861f3.png)

Today, and thanks to a monumental effort by the entire Tech Org, we can say that we have made significant progress towards understanding and stabilizing parts of our product and infrastructure, so we are ready to fulfill higher level needs.

> “ ~~Human~~ Splice's Technology Team's needs arrange themselves in hierarchies of prepotency. That is to say, the appearance of one need usually rests on the prior satisfaction of another, more pre-potent need.”
> - Abraham H. Maslow. “A Theory of Human Motivation.”

If we consider our organization as an organism that aspires towards [self-actualization](https://en.wikipedia.org/wiki/Self-actualization), we can use [Maslow's Theory of Human Motivation](https://psychclassics.yorku.ca/Maslow/motivation.htm)  as inspiration and say that we have been able to satisfy our *basic needs* enough to start considering the next level, *safety*.

**The Q3 Pursuit of Safety**

Imagine a not too distant future where:

💪 Every engineer is empowered by tools and processes, willing and able to take more significant risks.

🚀 Engineers are confident that the code they're delivering won't break Splice and when it does, they can fix it quickly.

🎉 Everyone in the Technology Organization, or outside of it, feels comfortable and welcome contributing code to any part of our codebase, including End to End tests.

⚡️We continuously expose all Splice employees to new functionality and learnings.

The first step towards this future is to remove delivery roadblocks while also increasing our confidence in the changes we are making.  Without a foundation where quick change is "safe," we won't be able to focus on satisfying the next level of needs <sup>[4](#social-belonging)</sup>


### 3.1 Plan For The Plan

Our plan for the plan is pretty straightforward:

1. Define metrics that can help us gauge obstacles in our delivery process so that we can have an impact through our improvements.
2. Form a Delivery Working Group
3. Start measuring.
4. Communicate strategy to Tech, Splice, Exec, and Board
5. Survey the delivery challenges we have in Frontend, Backend, Application and Quality SIGs.
6. Propose tactics that may help in removing those obstacles.
7. Identify the right places to incubate short-term wins, get to work.
8. Observe impact on metrics.
9. Iterate, learn, iterate.

### 3.2 Execution Period

The execution period for this strategy is *6 months.*

👶 Month one, *crawl*: In a growing organization of our size, one month is not sufficient to cause impactful process and tooling changes, so we must accept this and instead set ourselves up for change acceleration.

🚶‍♀️Q3, walk: we should be walking towards the future we envision, and delivery should be measurably better.

🏃‍♀️ H2, run: by the end of the year, we should be well on our way towards fulfilling higher level needs and delivering constant learning to our entire organization.


### 3.3 Metrics

Being mindful of [Measurement Myopia](http://www.druckerinstitute.com/2013/07/measurement-myopia/), the initial step towards a successful delivery improvement strategy is the definition of metrics that we can use as proxies for the evaluation of progress. With these metrics in place, we can formulate theories on how to move them and evaluate whether our execution is having the desired impact.

> It can be proven that most claimed research findings are false <sup>[1](#false-research)</sup>

To account for the decay of our knowledge, we will set the half-life of our metrics as three months. They should be fully realized by then, and have good candidates for replacement metrics that will guide us towards our future of continuous learning.

ℹ️ *The metrics below are the outcome of our Tech Exec offsite that took place in June, and rose as viable candidates from a healthy discussion and exploration of other metrics.*

#### 3.3.1 Time to Merge

Defined as the time it takes a Pull Request to be merged into a deployable branch 

🎯 By the end of Q3, we are merging 100% of Pull Requests within 36 hours.

By choosing this metric, we'd like to enable a future where pull requests (PRs) are small and short-lived. Small pull requests are [easier to review](https://www.ibm.com/developerworks/rational/library/11-proven-practices-for-peer-review/index.html), and by keeping them short, we can start moving towards splitting our work into small, shippable units that allow to faster feedback cycles.

🗝 To enable incremental development by getting higher quality work into users' hands faster. This process improvement will reduce the time it takes to learn about product decisions or fixing problems.

**Measurement:**
Since we don't have a baseline, we have initially set the target for this metric by the very scientific method of *gut-feeling*.  We will adjust it as time goes by to account for factors that add noise, like weekends or prototypal branches.

A proof of concept dashboard for this metric is already available in Data Studio. Thanks to @mattetti and @mariagandica for putting it together, and Data Coven + GrowFace for laying the foundations for this work to easily happen today.

#### 3.3.2 Deploy Frequency

Defined as the times in a day a team (vertical or otherwise) deploys to a production-like environment. <sup>[2](#production-like)</sup>

🎯 By the end of Q3, all product verticals are deploying at least once a day.

By choosing this metric, we aim to focus process improvements towards removing bottlenecks in our deployment procedures. For example,  cross-team dependencies, testing challenges, acceptance delays, competition for staging environments, infrastructure limitations, and deploy time.

🗝 To enable Splice employees to interact with working software sooner, drastically reducing how long it takes us to learn about our changes and resulting in faster feedback cycles.

**Measurement:**
Today it's not easy for us to associate deploys to Verticals since many of our repositories have shared ownership. We do know who is on which team, so for the sake of prototyping measurement we can assume that any deploy an engineer triggers can be associated with their team.

We don't have a dashboard for this metric since it requires some deployment instrumentation. A hacky way to measure this could be by asking engineers to self-report deploys in a global spreadsheet we feed into our dashboard. We could look at Clubhouse data or state changes for tickets, but it may not be a great alternative since all teams use different processes. We're also not yet consistent with keeping our tickets up to date 🧐.

#### 3.3.3 New End to End (E2E) Test Coverage

Defined as the degree to which we cover new product behaviors or bug fixes with automated Black Box Integration Tests <sup>[3](#blackbox)</sup>, written by behavior authors.

🎯 By the end of Q3, 100% of Engineers have written an End to End Test in an improved testing environment.

By choosing this metric, we aim to remove obstacles engineers have that prevent them from adequately testing their work. Some examples of obstacles are the CI infrastructure capacity, the difficulty of booting a full-fledged development environment locally, or painful test data setup.

Low or unknown End to End Test Coverage, has lead us to have little confidence in the work we ship since we never know what unrelated functionality will break (shoutout to Google Analytics 😭). Our Quality Team has made a monumental effort in supporting our confidence, but they can only do so much and operating at scale requires a different approach.

We're also hoping to mitigate the adverse effects that this improvement strategy may bring.  Releasing more ~~bugs~~ opportunities faster is not a desirable outcome.

Finally, we're explicit about the distributed responsibility of Quality and Testing in Engineering.

🗝 To increase the confidence in the new work we're delivering, so we can set ourselves up for delivery acceleration.

*ℹ️ During the metric definition process, we found that easily measuring confidence in what we ship may not be something achievable during Q3. We still aspire towards higher confidence in our work and believe it is crucial to decrase Time To Learn. Despite the measurement challenge, we consider we should attempt something while being explicit about our intent.  What we're trying to drive here is a process change by maturing our testing infrastructure and distributing authorship, so that we can make progress towards a higher standard of quality and confidence during in Q4.*

### 3.4 Associated process changes

**Deployable Branches.**

For this strategy to succeed, it is essential that the outcome of merged Pull Requests be available for all Splice employees to test or try. Ideally, a PR is auto-deployed "somewhere" (behind a feature flag, a branch deployment or a canary desktop build), allowing for stakeholders, and other Splice employees get nearly instant access to the work so that we can learn about it faster.

**Pull Requests Authors Merge Pull Requests:**

We have places in our process where QA Engineers have unintentionally ended with the responsibility of merging Pull Requests and acting as air traffic controllers for Staging. By the end of the quarter, we should have transferred the merging responsibility back to the authors, and coordinating staging environments should be a tale from the past.

The responsibility transition will only be possible if we can successfully decouple deployment (all Splice employees can interact with this work) from release (this code is available to end users) while increasing the confidence in our changes.

### 3.4 Change Management

As we have established above,  improving our delivery 📦 is urgent and essential for enabling our company to fulfill its mission.

> We empower musicians to realize their creative potential and unleash it on the world.

Executing on this plan will not be easy. We're going to cause process and cultural change on a 70+ Technology Organization in a company that is "a different company" every six months, so we must be patient, deliberate and perseverant.

#### 3.4.1 Responsibility and accountability.

We will treat this plan as a Technology Organization OKR to highlight its importance to the rest of the company. Measured in a public dashboard and graded like everyone else's. The VPE will be responsible for the communication and accountable for execution of this strategy.

#### 3.4.2 Delivery Working Group

Staffing this work, like many of our cross-cutting projects will be a challenge. Since we're leaders in the space, we can't afford a pit-stop. This limitation restricts us to something closer to aerial refueling as the approach we will attempt.

![fuel](https://user-images.githubusercontent.com/228120/42862280-d56ab53c-8a2c-11e8-90bd-846f30c89668.gif)

We will need to form a cross-vertical Working Group responsible for executing on this plan so that we can guarantee some dedicated attention to this effort for an estimated six month period.

Even though Tech Leadership has been given insight into this approach early, Verticals should not expect their Q3 Plans to be negatively affected by this work. All engineers are encouraged to volunteer any free cycles towards supporting this work, as advisors or active contributors.

Like many parts of our organization, the Delivery WG should be considered Work In Progress and its full membership is pending discussion with managers of all teams so that we can minimize the impact on mission-critical initiatives.

For now, this group is composed by:

* The entire Infrastructure team
* Nicolás Hock, on as Infrastructure Intern
* Advisors from all SIGs & Disciplines
* Michael Gorsuch, as WG Lead
* VPE, starring as Corporate Credit-card Holder, Overhead & Motivational Guide

#### 3.4.3 Project Management

Visibility into our decision making and progress is vital for our success. For this reason, we will track our OKR progress publicly and will manage all initiatives that belong to this project in a public Asana board, so the entire company can access all details and participate in the discussion. We will also make all documents available to the company, and open our meetings so that everyone can observe.

VPE will play a dual role of meeting facilitator, Strategy Project Manager, and will empower individuals to lead and manage different initiatives.

## 4 Drawbacks
* We don't yet know the amount of effort, or cross-cutting impact that this approach will have on our other business objectives and by making infrastructural & process changes we risk delaying initiatives that depend on the status quo.
* Our testing toolchain and CI/CD environments are fragile; we may very well begin shipping bugs faster by removing roadblocks without first adding sufficient coverage to critical paths of our product
* We don't yet have an excellent track record of delivering on long-running projects on time ( some teams have, but we are one big organization). Failure will further erode the trust in our ability to deliver successfully, making it harder to get on track.

## 5 Alternatives
In addition to the proposed metrics, we also evaluated:

* Time to Implement
* Time to Deploy
* Deploy Confidence
* Support Time / Frequency
* Uptime & Stability (quality)

## 6 Potential Impact and Dependencies

This plan directly impacts all of Technology, and indirectly the entire company.  For this reason, we will give access to everyone to all the artifacts we produce.

As far as dependencies, we primarily depend on our ability to form a team that can work mostly uninterrupted while creating short-term wins, while minimizing or eliminating the impact to our Q3 plans. Initiatives also have cascading dependencies, that we are not fully aware of yet so we must be diligent in surveying our team to surface their knowledge.

This document is *required reading for everyone in Technology* so that we can all individually support and contribute towards the success of our plan.

## 7 Unresolved questions
* Who are all the members of the Delivery Working Group?
* How can we accurately measure our Key Results
    * some progress towards measurement Time To Merge has been made thanks to Maria, Matt A & enabled by GrowFace.
* What are the best projects to incubate and experiment with process change?

## 8 Conclusion

Making substantial progress towards improving how fast our organization can learn, enabled by our ability to deliver high-quality working software is a goal we must accomplish in the next six months. By reducing our Time To Merge, increasing our Deployment Frequency and working towards covering all new work with End to End Tests during Q3 we will be well on our way towards a future where shipping working code is one of the fastest and most effective ways to learn and to test new ideas at Splice. This goal won't be an easy one to achieve, but it's required for us to empower musicians to realize their creative potential and unleash it on the world.

---

<a name="false-research">1</a>: Ioannidis JPA (2005) Why Most Published Research Findings Are False. PLoS Med 2(8): e124. https://doi.org/10.1371/journal.pmed.0020124

<a name="production-like">2</a>: a place where Splice population other than those in the Technology Organization can interact with software without Engineering assistance. For example, behind a feature flag that can be self-managed, or a staging environment that is accessible to anyone with [redacted].

<a name="blackbox">3</a>: Tests that determine whether many separately developed modules work together as expected, and don't "know or care" about the internal implementation of said modules.

<a name="social-belonging">4</a>: Challenges like role definition, responsibilities, PM<>Design<>Eng partnerships, on-boarding, documentation, dist work performance management are starting to poke more frequently as new needs.

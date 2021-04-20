(this is an old example that illustrates how I introduced a a team to the process of RFCs, my understanding of how to deploy this process well has evolved since then)

# RFC on RFCs

- **Main Author:** @buritica
- **Backers:** n/a


## 1 Summary

This proposal aims to structure the way the [redacted] team makes technical decisions.

## 2 Motivation
By formalizing a technical decision process we become a more effective and efficient team by enabling the following:

- Adding a light early stage of technical design, that helps us understand our goals and evaluate decisions before writing heavy implementations
- Creating an opportunity to raise risks or concerns by our shared experience. One of us may have solved a similar problem before, but belong to a different team. This process gives us the ability to share our expertise and past mistakes.
- Sharing institutional knowledge, by exposing the entire team to different domain problems which will improve the shared understanding of our platform.
- Centralizing initial design documentation
- Facilitating future on-boarding of new members, since they'll be able to dive into the context on how we made several decisions in the past.
- Updated documentation by treating RFCs as live documents when past decisions need to be updated due to new information or features
- Shared sense of belonging, by including our team into the process of important decisions
- Diminished fear of failure, by having a process where critical business risks are identified, we can allow ourselves to make bolder approaches as a team
- Clear ownership, by allowing individuals and teams to propose and make critical decisions we can take calculated risks, make mistakes and enable continuous improvement
- Constant learning, by allowing members of diverse backgrounds provide input
- Clarity in decision making process, by guaranteeing that those responsible for the decision are leading the process, preventing bike-shedding and reducing design by committee and brainstorming sessions

## 3 Detailed design

#### 3.1 When to RFC

The distinction on when to create an RFC is not clear cut. Engineers are expected to use good judgement when determining whether an RFC is necessary. Minor updates to endpoints may not require an RFC, but when in doubt ask [redacted] whether certain work requires a proposal.

Below are some guidelines that may be used to determine whether a proposal may be needed:
_note: the cases below do not always mandate a proposal_

- Will a new feature require a new endpoint?
- Are you starting a new project?
- Will your changes have architectural impact?
- Are you proposing the use of a new tool, library, technology or process?

RFCs may not only be part of the initial process. In some cases, teammates may request a proposal to justify or argument modifications in an existing Pull Request. For example, when a new dependency is added to a system or a proposed system modification has a a wider system impact than what originally expected..

#### 3.2 How to RFC

##### New proposals
1. Clone and fill [RFC Template][template] in a new branch of this repository
    - rename `_template.md` by prefixing a numbered `000X` so we can keep folder organized
    - You may send an early Pull Request but label `[wip]` tag in the title while in progress
2. When ready for comments, send a Pull Request on `master`
    - Use descriptive labels on pull-request for future organization
3. Send a calendar invitation to [redacted]
	- title: `[RFC] 000X Deadline`
	- all day event: `true`
	- alert: `on the day of`
	- description: `link to RFC`
4. All members of [redacted] are expected to read and add comments to Pull Request within expected timeframe
    - members may indicate they've read the document and have no comments with a 👀, votes are not required
5. Author and backers should resolve comments they consider necessary and indicate which suggestions will not be addressed according to their judgement
6. [redacted] will approve by merging pull request, veto, or may delegate someone for approval
7. [redacted] will generate readable version and upload to Shared Read Only Google Drive so entire company gets access

##### Modifications to existing, previously approved proposals
1. Clone and make modifications to existing RFC
2. Same process as above

#### 3.3 Additional Notes
- If confidence of acceptance is high (architectural change, new technology use), early work can be done while RFC is under review so time is not wasted
- High priority RFCs may have less than 24 hr review cycle, as long as they are brief and easy to understand. It'll be the author's responsibility to communicate the urgency of the proposal.
- Minimum time for an RFC to be reviewed should be enough to allow for timezone differences and reviewers day to day work and responsibility. Use your judgement so that teammates may review proposals without having their own goals / deadlines affected. Make sure you plan ahead, and bear in mind that you don't have to wait for approval to start work if confidence in acceptance is high. When in doubt, check with [redacted].
- Time may be extended by modifying the date and the attached calendar invite by Author if comments or questions are unresolved

## 4 Drawbacks
Adding RFCs as an initial step to our engineering process will have increase the time we take to `ship` something. This will improve as we completely incorporate RFCs into the way we build software.

## 5 Alternatives

**What other designs have been considered?**

- Another option not detailed could be a forum-like platform, like [Discourse][discourse]


**What is the impact of not doing this?**

Not having a clear way of making technical decisions will reduce our ability to grow as a team and handle more complex problems under pressure, in addition to limiting the shared knowledge in our team and a loss of institutional knowledge by having implicit undocumented processes and decisions.

## 6 Unresolved questions

**What parts of the proposal are still TBD?**

- How can we include folks outside of engineering into our RFC process if it resides in Git?

[//]: # (Links below)

[template]: ../rfc_template.md
[discourse]: http://www.discourse.org/

# Managing Distributed Teams: Two Tenets

*if you're interested in tools, take a look at the [list of tools](https://github.com/tomrijntjes/distributed-teams) I maintain.*

When running a remote team, there are some key differences with running a colocated team:

- you have access to a global talent marketplace
- your team members have access to a global job marketplace
- you can't bond over beers

I tried to capture my personal experience with working in two very different remote software teams for two years each in two simple tenets. Here they are:

- You're not going to be friends. Prioritize effectiveness over team cohesion
- Write it down. Emphasize transparency in the form of written documentation.

## We Are Not Going to be Friends

I've been a part of two software teams that took opposite approaches. Team A took the office-based model and implemented it online. The overhead in terms of alignment meetings somehow increased: a large part of consensus building could no longer take place at the coffee machine so people felt that this is a good reason to meet more often.

Team B took a different approach: hold the minimal amount of recurring meetings (roughly 6 hours per week) and do absolutely nothing to 'build' the team. All other communication took place asynchronously. If the need for alignment, knowledge-sharing or collaborative problem solving arises, an ad-hoc call would be arranged.

On all relevant metrics, team B outperformed team A, particularly:
- high velocity
- low churn
- work-life balance

Was it horrible to work in team B?
When people reliably tackle hard problems together, relationships deepen based on respect for what the other can do. It's an entirely different type of connection to bonding over team activities, shared aspects of personal lives and non-professional interests.

## Everything as Version-Controlled Markdown

Due to difficulties with timezones and general unpleasantness of being in a conference call, emphasize asynchronous written communication through instant messaging and version-controlled markdown.

1. Capture technical details close to the code in module-level READMEs.
1. Large decisions that are expensive to revert must be captured in [ADRs](https://adr.github.io/).
1. Operational failures can be captured in [blameless postmortems](https://github.com/dastergon/postmortem-templates).

Having a temporal dimension to documentation is critical, because it allows future readers to put the current state of the project into context. For example, a new engineer may ask themselves why framework A is used over framework B. The relevant ADR should:
- answer that question,
- describe how that choice was made,
- describe the context in which that choice was made.

If the constraints have changed from the moment that the decision was made, perhaps it is possible to reconsider the choice. If not, that saves you an unproductive discussion.

Another example:
An engineer wants to invest considerable resources in a certain category of tech debt. The collection of post-mortems immediately tells you whether that investment is justified. Which incidents would the change have prevented? If so, what would have been the business impact of avoiding those issues?

There is an interesting connection to the other tenet. Transparency and merit-based collaboration are two sides of the same coin. Good documentation makes it absolutely clear which ideas are contributed by whom. No longer shall the loudest in the room get the credit. Expect a tyranny of the expert writer.
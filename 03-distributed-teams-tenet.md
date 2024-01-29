# Managing Distributed Teams

*if you're interested in tools, take a look at the [list of tools](https://github.com/tomrijntjes/distributed-teams) I maintain.*

When running a remote team, there are some key differences with running a colocated team:

- you have access to a global talent marketplace
- your team members have access to a global job marketplace
- you can't bond over beers

I tried to capture my personal experience with working in two very different remote software teams for two years each in one simple tenet: **build capabilities, not teams**. 

## Start Building Capabilities

If you accept a relatively high turnover, priorities change. 
Your processes should focus on building capabilities. 

By that I mean knowing how to do stuff on a team level. You do that by 
- making onboarding as smooth and informative as possible, 
- agressively sharing knowledge and 
- avoiding loss of knowledge when someone leaves

### Onboarding

To be honest, I don't know how to do this well because *every single company* I worked for in the remote era bungled it. 

The good news is, standards are so low it's not that hard to stand out as an employer.

The following tips are all reversals of what I've seen going wrong:
- provide hardware on time, or support bringing your own device.
- give people a basic sense of where they sit in the organization, especially if you work for a large enterprise.
- prepare entry-level task, even for senior staff.
- assign someone to pair program with on a task.
- have a clear entrypoint to the documentation, at least containing functional/commercial objectives, architecture diagrams, and a map of the rest of the documentation.

### Everything as Version Controlled Markdown

A large part of building team capabilties is having high standards for documentation.

Especially given difficulties with timezones, emphasize asynchronous written communication through instant messaging and version-controlled markdown.

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

## Stop Building Teams

### Reduce Overhead Agressively

I've been a part of two software teams that took opposite approaches. Team A took the office-based model and implemented it online. The overhead in terms of alignment meetings somehow increased: a large part of consensus building could no longer take place at the coffee machine so people felt that this is a good reason to meet more often.

Team B took a different approach: hold the minimal amount of recurring meetings (roughly 6 hours per week) and do absolutely nothing to 'build' the team. All other communication took place asynchronously. If the need for alignment, knowledge-sharing or collaborative problem solving arises, an ad-hoc call would be arranged.

On all relevant metrics, team B outperformed team A, particularly:
- high velocity
- low churn
- good work-life balance

Was it horrible to work in team B?
When people reliably tackle hard problems together, relationships deepen based on respect for what the other can do. 
It's an entirely different type of connection to bonding over team activities, shared aspects of personal lives and non-professional interests.

### Cultural Affinity (still) matters

A contentious standpoint perhaps, but I think it's too important not to mention. 
It's not impossible to work closely together with people from incompatible cultural backgrounds, but it takes longer to build the trust you need for a high performing team.
You don't always have that time, especially if you assume relatively high turnover.

Does that mean you should discriminate based on the color of someone's skin or a person's sexual preference? Absolutely not.
Does that mean that if you know in your bones this person will not gel well in the team, whatever that means, it's sufficient reason to pick another candidate? I think that can be justified.


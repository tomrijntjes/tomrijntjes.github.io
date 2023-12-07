# Bootstrap Engineering Standards

Congratulations, you have know what you want to build and which people you need to do it.

How do you avoid building an unsustainable mess? The next legacy codebase?

Top teams set engineering standards early without bogging down engineers in bureaucracy when the project is at its most fragile.

To keep momentum with stakeholders, the key idea is to start delivering value now without setting yourself up for failure later.

## Decide Fast, on Record

Do not wait for all key stakeholders to become available. Instead, draft a decision and send it around for review. 
This is better for a number of reasons:
- give people time to research all options, leading to higher quality choices
- asynchronous communication is more flexible and often faster
- help future joiners understand why you went in a certain direction, and if there's space to come back to that choice

It's tempting to draw in all engineers for every consequential choice, especially when you start with a small team. 
Resist this temptation. Write an [ADR](https://github.com/joelparkerhenderson/architecture-decision-record#what-is-an-architecture-decision-record).

> ADR: architecture decision record

## Establish a Technical Foundation

To keep velocity high and creativity flowing, avoid standardising everything from the start. Focus on use, not reuse.

However, some modern practices are hard to install once the product organization is up and running, for example:
- infrastructure as code
- continuous integration/continuous delivery 
- centralized master data and reference data

## Focus on code in production

Especially in the early phases when everything is unclear, make sure to build **operational excellence** by rewarding working code in production over slideware. 

> slideware: software that only exists in powerpoint form

If you build it, you run it. This is the best way to avoid an unmaintainable codebase.

### Infra as Code

Take a moment to set up Terraform. It's not hard and will save you many headaches.
Make sure every engineer is authorised to provision cloud resources, but keep track of cost. 

### Continuous Integration

Establish this practice from the start.
Avoid situations where only some guys know how to deploy code. 
Every engineer must be able to ship a change, automatically.

### Centralized MRD

If you want interoperability between a suite of applications, they'll have to speak the same language.
Create a shared data model and update it as the product suite evolves.

## Hire Short Term

If you think you know which capabilities you will need three years down the road, you are probably mistaken. 
Priorities will change, new insights will crush expectations and open up possibilities beyond imagining. 
If you want to build an agile product team, you have to hire for agility. 

To be specific:
- hire senior individual contributors first. They can help with setting hiring standards.
- contractors are used to delivering value quickly, and are happy to move on when your needs change.
- prioritise generalists over specialists at first
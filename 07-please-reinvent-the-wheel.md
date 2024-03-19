# Reinventing The Wheel

It's a common trope in software development that too little standardization is Bad and too much standardization is Also Bad.
Opinions on where an organization stands on the spectrum are divided and it seems like there is no useful framework for finding the optimal middle ground.

This is my attempt to introduce a degree of rigor to the question: should you standardize the software development process more, or less?

## Success Stories and Stumbles

Let's zoom all the way out and look at global scale efforts beyond the realm of software.
There have been many standardization efforts with varying degrees of success.

| Effort | Start Year | Completion/Current Status (Year) | Timespan (Years) | Success Rating |
|---|---|---|---|---|
| Shipping Containers | 1950s (Concept) | Late 1960s (ISO Standards) | ~15-20 | Revolutionary Success |
| Internet Protocol Suite (TCP/IP) | 1970s | Ongoing Development | 50+ (Ongoing) | Revolutionary Success |
| International Time Zones | 1884 | 1929 (Majority Adoption) | 45 | Significant Success |
| Metric System | 1795 (French Revolution) | Ongoing Adoption | 229+ (Ongoing) | Significant Success |
| Power Plugs and Outlets | 1904 (NEMA foundation) |  - | 120+ (Ongoing) | Moderate Success |
| International Driving Permits (IDPs) | 1921 (International Convention) | 1949 (Geneva Convention on Road Traffic) | 28 | Moderate Success |
| Keyboard Layouts | 1868 (Sholes & Glidden Typewriter) | Ongoing | 156+ (Ongoing) | Limited Success |
| Betamax vs. VHS | 1975 (Betamax) | Mid-1980s (VHS Dominates) | 10-15 | Catastrophic Failure |
| Coded Character Set for Text Interchange (CCITT) | 1960s | 1990s (Superseded by Unicode) | 30-40 | Catastrophic Failure |
| Esperanto | 1887 | Ongoing Development | 137+ (Ongoing) | Limited Success |

What does this list tell us, if any generalization can be made at all?

- Standards of this scale can take literal centuries to take hold!
- It does seem to help if there's a significant economical driver (shipping containers).
- It helps if there are no incumbent systems (TCP/IP)
- It doesn't help if some market players benefit from a segregated market (power plugs and outlets)
- You need to align with interests of the dominant political power, ie. the USA (Esperanto, Metric System)

It may hint at the relevant questions that can be asked about a standardization effort.

1. is there a strong economic driver?
1. what does it cost?
1. who benefits from the status quo?
1. who benefits from standardization?
1. how lies the balance of power between those stakeholder groups?

## Enterprise Software

Let's try to apply these questions to a number of typical standardization efforts in the enterprise software landscape.

### Programming Languages

This may be a somewhat fabricated example but I'm sure there a companies out there that identify as a Java shop.
Let's assume for a moment that even though you can't do everything with Java, you can build a Java-centric ecosystem. Should you pursue this?

#### Economic Driver

Hiring becomes simpler. You need only one interview protocol. You can develop CI/CD assets and use them across the board.
There is little friction to rotating employees between teams.

#### Cost

There are significant costs to rewriting everything to a single language.
Employees that specialize in the obsolete programming language will have to adapt and not everyone is interested in that. People will leave.
There are opportunity costs: adopting emerging languages will be even more costly, because it's no longer possible to experiment at a small scale.

#### Stakeholders

Programmers will be generally indifferent or against. It limits them with no clear benefit. They have significant power by being able to leave or go on strike.
Architects, cyber security engineers and hiring managers will benefit. Hiring managers have the power to hire & fire, but ultimately they need people to build stuff.

#### Verdict

Don't.












I've been interviewing for a new role lately and in enterprise land there seem to be two themes:
1. everybody in our sprawling organization is reinventing the wheel. We're trying to bring some standardization to their efforts.
2. software development in our organization is stifled by bureaucracy. We'd like to decentralize so it becomes possible to innovate.

Paraphrasing:
1. we want a more homogeneous software landscape
2. we want a more heterogeneous software landscape

This tension field is ubiquitous and I'm still trying to make sense of it.

Here are a couple of lenses:

## Engineers versus Managers

homogeneous software landscapes are good for governance and management. It makes hiring efficient because you only need to source from a highly focused talent pool

However, the prescribed tools are an unwanted constraint for solving the engineering problem at hand. Innovation is much less rewarding.

## Language

Reinventing the wheel is so obviously stupid it is a powerful cognitive stop. OF COURSE we want people to build of each other's work, avoid double work, leverage progress, etcetera.
However, software products are often superficially similar in reality and do not benefit much from standardization at all. One-size-fits-nobody.

I like this explanation because during interviews the hiring manager so completely embodies one of the two perspectives it's impossible to ask critical questions.
When I ask what kind of pains come from the excessively heterogeneous software landscape I get no real answer.
When I ask the same for an overly centralized landscape, the pain is often clear: we can't get anything done on time because of bureaucracy. Maybe I'm biased because this perspective favors engineers.

I realize I use the words centralized and homogeneous interchangeable. Can I define them more precisely?

|              | centralized            | federated        |
|--------------|------------------------|------------------|
| homogeneous   | design by committee    | software factory |
| heterogeneous | innovation and quality | creative chaos   |



## Maturity

Organizations go from startup to enterprise, where innovation is important at first but quality becomes more important later.
Most of my clients are not digital native so I'm not entirely sure about this angle.


## Disentangling Centralization

Standardizing everything is bad. Standardizing nothing is also bad. Which elements of the enterprise software stack are good candidates for standardization?

1. cyber security auditing
1. identity and access management
1. quality assurance auditing
1. master data and reference data

bad:
1. cyber security implementation
1. quality assurance implementation
1. transactional data
1. basically any technology choice
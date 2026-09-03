## Why software projects fail

A common scenario: developers talk to customers, write requirements, then build the product, but the result doesn't meet expectations. This usually happens for one of two reasons. Either the requirements never really matched what people needed, or the needs changed while the product was being built.

A big part of the problem is stakeholders. A stakeholder is anyone with a stake in the project, whether internal (developers, managers, marketers) or external (customers, users, operations, management). Products often fail because some stakeholders were missing from the process entirely (think of a kids' app designed only by talking to adults), or because what a user says they want differs from what they actually do and feel. Business goals, technology, and competitors also keep shifting underneath a project.

The Netflix recommender example is a good illustration: customers asked for maximum choice and comprehensive search, but what actually worked was a handful of good recommendations, simply presented. Steve Jobs made a similar point about not just relying on market research since people often don't know what they want until it's shown to them. None of this means skipping user research, it just means treating stated needs critically.

## Why software is complex

Complexity here means anything that's hard to understand or modify. It helps to split this into two types:

Accidental (or incidental) complexity comes from implementation choices and can be removed by cleaning up code, switching languages or frameworks, or paying down technical debt. Technical debt is essentially the cost of cleaning up a "quick fix" later.

Intrinsic complexity is the complexity that remains even after all the accidental complexity is gone. It can't be removed, only managed, mainly by designing modular systems with independent parts and more predictable runtime behavior.

Software engineering exists to reduce both kinds of complexity through systematic application of engineering approaches to building software.

## When do you actually need software engineering?

Not every coding task needs a formal process. It matters when you're collaborating with others on a software project, building something for a customer or stakeholders other than yourself, or building something meant to grow and change over time.

Software engineering is described as more than just coding. It draws on computer science but also borrows structure from other engineering fields: measurement, decision-making, tooling, reusable components, secure coding standards, and soft skills like communication and teamwork. A "code-only" approach tends to cause problems down the line with modularity, reuse, and testing, and the cost of fixing an error grows sharply the later it's caught in the lifecycle (planning is cheap, fixing bugs after release is expensive). One estimate has maintenance eating up roughly two thirds of total software cost.

## Purpose of the course

The course aims to build a better understanding of the software development process itself, including coordination, communication, and abstraction mechanisms, with a particular focus on agile development. It also aims to teach the "language" developers use to talk about design: UML diagrams (especially state machines), workflow diagrams, design patterns, and architectural principles.

## Development processes, generally

A development process defines what must be done, when, by whom, and how. Common models include:

**Waterfall**: requirements, design, implementation, testing, and maintenance happen in strict sequence. Good for projects where requirements are well known upfront (common in critical software), but poor at handling change, since new requirements tend to surface only once customers start interacting with the software.

**Incremental and iterative development**: incremental means delivering the system in small chunks with user involvement along the way, iterative means continuously refining through repeated cycles. Both handle change better than waterfall, but each added iteration increases complexity and cost.

**Spiral model**: combines risk analysis, prototyping, and planning in repeated loops, useful when risk needs to be managed carefully across versions.

**Reuse-oriented development**: a "Lego" approach where you assemble existing components (APIs, web services) rather than building everything from scratch. Saves development time but adds cost in integration, configuration, and testing.

**Agile / Scrum**: organizes work around a prioritized product backlog, short sprints (1 to 4 weeks), and a daily standup. A product owner and team select backlog items to build within a sprint, then review and reflect at the end.

A useful way to compare waterfall and agile is by what's fixed versus flexible. In waterfall, scope is fixed and cost/schedule flex to meet it. In agile, cost and schedule are fixed and scope is what flexes.

Choice of method matters a lot depending on risk. Pacemaker software failing could cost lives and carries legal liability, so it demands a much more rigorous process than something like a calorie counter app, even though both are "software."

## Core software engineering activities

**Specification**: figuring out what the customer actually wants and making sure the development team understands it the same way. This is genuinely hard, as the classic comic about vague client requests illustrates. Requirements engineering is the formal process of defining, documenting, and maintaining requirements, and it involves checking two things: is the domain knowledge itself clear (through interviews, ethnographic study, shadowing), and is your interpretation of the problem clear to both the customer and your own team.

**Design**: once requirements are understood, code needs to be structured for loose coupling, reuse, and extensibility. Design activities typically include architecture, interface design, database design, and component selection.

**Validation and verification**: compiling isn't enough. You need to check the code was built according to requirements and that new changes don't break existing components. A common cycle here is: write a test, watch it fail, write code to pass it, confirm all tests pass, then refactor.

**Testing strategies** form a pyramid, going from cheapest/most numerous at the bottom to most expensive/broadest at the top:

- Unit tests check a single component's output against an expected result
- Integration tests check units interacting with things you don't fully control (databases, networks, threads)
- Functional tests treat the system as a black box and check it against functional specs
- Acceptance tests check whether the system meets business/contract requirements, usually done with actual domain specialists or customers

An important caveat: passing tests only proves the software behaves correctly for the cases you tested. It doesn't prove the absence of bugs. If you need stronger guarantees (as in safety-critical systems), you need something like formal verification, which checks properties across the whole input space rather than just sampled data points.
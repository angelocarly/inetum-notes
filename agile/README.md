# Scrum and Agile

## Waterfall
1. What do we want? (in x months)
2. Proven technology (in x months)
3. Planning & Budget? (in x months)
4. Emerging changes? (in x months)
5. What do we want? (x months)

- Voordeel:
  - Alles is al voorgekauwd in het begin
- Nadeel:
  - Veel informatie/essentie gaat verloren

## Agile
**Agile manifesto**
- Individuals and interactions *over* Process and tools
- Working software *over* Comprehensive documentation
- Customer collaboration *over* Contract negotiation
- Responding to change *over* Following a plan

**Overview**  
Lean ( Agile ( Scrum/Kanban ( XP ) ) )
- Lean: Mindset
- Agile: Approach/method
- Scrum/Kanban: Frameworks
- XP: Technique

- MVP: Minimum Viable product
  - Learning vehicle
  - Risk reduction tool
- MMP: Minimum Marketable product
  - Less is more
    - Smallest possible feature
	- Add most value
  - Reduce time-to-market

## Scrum
- Low prescriptive framework for incremental software development
- Continuous improvement via empirical process control
- No technological constraints
- It's all in the [Scrum Guide](http://www.scrum.org/scrumguides)

### People
- Role 1: scrum master
  - facilitator of scrum events

- Role 2: Product Owner
  - Mandated business representative
  - Accountable for the vision and product backlog management
  - Expresses and orders Product Backlog Items (PBI's)
  - Tracks progress, value, ROI and TCO
  - Inspects working software
  - Authority over the requirements, not over the estimates or the people

- Role 3: Development Team
  - 3-9 people
  - Cross-functional
  - Collective accountability to turn PBI's into increments of potentially shippable software
    - Within engineering standards
	- Against 'Definition of Done'
  - Empowered and self-organizing for the technical realization
  - Collective Ownership of the code
  - Authority over the PBI estimates, the Spring Backlog and the People

### Scrum framework
- Event 1: **Spring planning**
  - Time-boxed: 8 hours for 4 weeks Sprint, or proportionally shorter
  - Scrum Team
  - Part 1: What?
    - Product Owner presents ordered PBI's
	- Development Team pulls top-ordered items from Product Backlog
	  - Past performance (Velocity) + Projected capacity
	- Sprint Goal is crafted upon forecasted functionality
  - Part 2: How?
    - Development Team discusses, decomposes, designs and identifies tangible work
	- Development Team plans Sprint Backlog for building a "Done" product increment
  - Right-time planning
- Event 2: **Daily Standup**
  - Time-boxed, 15 minutes max
  - Development Team present, Scrum Master and Product Owner optional
  - Each Team member answers 3 questions
    - What have I accomplished since previous Daily Scrum?
	- What is my forecasted work until next Daily Scrum?
	- What impediments are in the way?
  - The Development Team self-inspects & adapts
    - Sprint Backlog & Progress (remaining work)
  - Right-time planning
  - It's about sharing information, not about status reporting
  - After-Scrum's for detailed discussions
- Event 3: **Sprint review**
  - Time-boxed
  - Scrum Team
  - Part 1: Sprint Review: *4 hours for 4 weeks Sprint, or proportionally shorter*
    - Collaborative working session with stakeholders
	- Release plan, anticipated functionality and date are inspected
	- No undone work, potentially shippable increment of functionality
  - Part 2: Sprint retrospective: *3 hours for 4 weeks Sprint, or pororionally shorter*
    - Inspect & adapt for pepole, relationships, joy, process and tools
	- Review Product quality and Definition of Done
	- Identify next Sprint improvements

#### Artefacts
- Artefacts 1: **Product Backlog**
  - An inventory of the requirements for on Product *PBI's*
    - Commonly understood Product features, alternatives and non-functional requirements
	- Ordered upon attributes like Value, effort, dependencies and risk
	- Higher-order PBI's are more decomposed and fine-grained
  - Single source of (emerging) requirements
  - Remove PBI's that remain low-ordered
  - Estimates are just estimates (days, Points, Gummy Bears, Ping pong balls)
    - Reflect Team capacity, not the company desire
  - Transparent (visible, understandable)
  - Visualize cumulative work remaining
    - Trend line reflects progress
	- Scrum Classic = Burndown chart
- Artefacts 2: **Sprint Backlog**
  - Forecasted funcitonality and work to turn it into a 'Done' increment
  - Estimated in hours 5-24
  - Development Team signs up for work
    - No work is assigned
	- Development Team can add, delete and change Sprint Backlog at any time
	  - Emerging work
	- Development Team re-estimates and updates work remaining at least daily
  - Visualize cumulative work remaining
    - Trend line reflects progress
	- Scrum Classic = Burndown chart
- Artefacts 3: **Definition of Done**
  - No work remaining for Release in production
    - Include infrastructure, performance and non-functionals
	- Hand dependencies by using stubs, mock-ups, etc.
  - Prevent undone work because:
    - Incomplete work cumulates beyond control
	- Technical debt requires 
	- Demonstrated increment is not shippable
	- The rythm of development gets broken
	- Velocity can not be tracked
	- Predictability decreases
	- Information is not trustworthy and transparency disappears
	- Trust from stakeholders is lost

### Principles of scrum
- **Shared visual workspace**
  - Prefer co-location without physical barriers
  - Visual Management Techniques
    - Post all artefacts, agreements and standards for high visibility and transparency
  - Face-to-face communication
- **Self-organizing**
  - Empowered teams
    - Cross-functional
	- Feature Teams
  - Inspect & adapt
    - Daily Scrum
	- Sprint Backlog
	- Sprint Retrospective
- **Empiricism**
  - Scrum theory is grounded in closed-loop feedback process control
    - Knowledge comes from experience
	- Predictions must be frequently verified against measurements
  - Transparency
    - Visibility of significant aspects of the process
	- Common standards
  - Inspection
    - Detect variances on anticipated outcome
	- Skilled inspectors inspect at right frequency
	- Scrum artefacts
  - Adaptation
    - Adjust the process or materials to eliminate variances
	- Adjust soon to prevent acuumulation of variances
	- Scrum events
- **Scrum has no explicit rule (for/against)**
  - Co-location
  - Part-time work
  - Multi-tasking
  - Onshore, nearshore, offshore
- **The Scrum Values**
  - Address the human side of Scrum
  - A framework for how we can interact effectively as a team, on a human level

## User stories
**3C's**
- Card
  - High level description
- Conversation
  - What make it become your holiday picture
  - Wat maakt het duidelijk voor jullie
- Confirmation
  - That's the way we'll be able to test it
If you replace conversations with documents, you've stopped using user story!

**Connextra format**
- As a [type of user]
- I want to [perform some task] (when?)
- So that I can [reach some goal]

- A user story describes the value you want to be delivered to the user
- A user story can be formulated on different levels
- A user story describes a need, not a solution
- Is not always one to one to technical implementation

**Gherkin**
- Given [context]
- When [event occurs]
- Then [outcome]

- Given [a shopper is not logged in]
- When [they proceed to checkout]
- Then [They are prompted to create an account]

### Lifecycle of user story
- They are alive, they:
  - Are born
  - Grow
  - Reproduce
  - Die
- They evolve in your backlog

### Good user story
INVEST
- Independent - Encourage loosly coupled design
- Negotiable - A promise tot talk rather to sick to a specification
- Valuable - Everyone get into client's shoes. Ask why, why and why
- Estimable - You can manage what you measure
- Small - Small enought to plan for short production releases
- Testable - Done means tested and ready to deploy

### User stories are not enough
- User stories are not enough
- User stories lack
  - preconditions
  - actor actions
  - system responses
  - business rules

### Structured conversation: 7 product dimensions
1. User
   - People, system, devices that interact with the product
2. Interface
   - How users connect to the product
3. Action
   - Capabilities offered to the users
4. Data
   - Data and information the product retains
5. Control
   - Policies, rules, and/or any regulations the product enforces
6. Environment
   - The technology platforms and in some cases the physical properties of the product
7. Quality Attribute
   - Poperties that describe the product operation and development, security, usability, reliability, response time and testability

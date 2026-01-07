Washizaki, H. (Ed.). (2025). SWEBOK: Guide to the software engineering body of knowledge (Version 4.0a). IEEE Computer Society. https://computer.org/swebok

<small>\* The notes focus on practical advice not glossary terms.</small>

# 1 Software Requirements

## I

> If not detected and repaired early, missing, misinterpreted and incorrect requirements can induce exponentially cascading rework to correct them ... the project, the product or both are likely to suffer from added costs, delays, cancellations and defects.<small>[Merged quotes]</small>

> The role of requirements documentation throughout the service life of the software is to capture and communicate intent for software engineers who maintain the code but might not have been its original authors.

## 1.4

> Functional requirements specify observable behaviors that the software is to provide — policies to be enforced and processes to be carried out.

## 1.5

> Nonfunctional requirements ... constrain the technologies to be used in the implementation ...

## 2.1

> Many projects benefit from performing a stakeholder analysis to identify as many important stakeholder classes as possible. This reduces the possibility that the requirements are biased toward better-represented stake holders and away from less well-represented stakeholders.

## 2.2

> Elicitation is not a passive activity. Even if cooperative and articulate stakeholders are available, the software engineer must work hard to elicit the right information.

## 3.1

> Each requirement should:
>
> - be unambiguous (interpretable in only one way);
>
> - be testable (quantified), meaning that compliance or noncompliance can be clearly demonstrated;
>
> - be binding, meaning that clients are willing to pay for it and unwilling not to have it;
>
> - atomic, represent a single decision
>
> - represent true, actual stakeholder needs;
>
> - use stakeholder vocabulary;
>
> - be acceptable to all stakeholders.

## 3.4

> When a project has more — and more diverse — stakeholders, conflicts among the requirements are more likely.
>
> ... project scope management ... balancing what’s desired in the stated software product requirements with what can be accomplished given the project requirements of cost, schedule, staffing and other project-level constraints.
>
> ... product family development (e.g., [20]). This involves separating requirements into two categories ... invariant requirements ... that all stakeholders agree on ... variant requirements, where conflict exists ... The software can be designed using design to invariants to accommodate the invariant requirements and design for change to incorporate customization points to configure an instance of the system ...

## 4.2

> Use case: ![Use Case Example](Use-Case-Example.png)

> ... user story ... “As a \<role\> I want \<capability\> so that \<benefit\> ...

## 4.3

> [Test case:] ... “Given \<some context\> [and \<possibly more context\>], when \<stimulus\> then \<outcome\> [and \<possibly more outcomes\>].”

## 4.5

> ... documenting additional attributes for some or all requirements can be useful.
>
> - tag to support requirements tracing;
>
> - description (additional details about the requirement);
>
> - rationale (why the requirement is important);
>
> - source (role or name of the stakeholder who imposed this requirement);
>
> - use case or relevant triggering event;
>
> - type (classification or category of the requirement — e.g., functional, quality of service);
>
> - dependencies;
>
> - conflicts;
>
> - acceptance criteria;
>
> - priority (see Requirements Prioritization later in this KA);
>
> - stability (see Requirements Stability and Volatility later in this KA);
>
> - whether the requirement is common or a variant for product family development (e.g., [20]);
>
> - supporting materials;
>
> - the requirement’s change history.

## 5.3

> ... prototype that concretely demonstrates some important dimension of an implementation. Prototypes can help expose ... assumptions and, where needed, give useful feedback on why they are wrong.

## 6.2

> All stakeholders must understand and agree that accepting a change means accepting its impact on schedule, resources and/or commensurate change in scope elsewhere in the project.

## 7.2

> Prioritizing requirements is useful ... because it helps focus ... on delivering the most valuable functionality soonest.

> What factors are relevant in determining the priority of one requirement over another?” ...
>
> - value; desirability; client, customer and user satisfaction;
>
> - undesirability; client, customer and user dissatisfaction (Kano model, below);
>
> - cost to deliver;
>
> - cost to maintain over the software’s service life;
>
> - technical risk of implementation;
>
> - risk that users will not use it even if implemented.

> - enumerated scale (e.g., must have, should have, nice to have);

> Effective requirement prioritization focuses on finding groups of requirements with similar priorities rather than creating overly rigorous measurement scales or debating small differences.

# 2 Software Architecture

## 1.2

> ... concerns evolve over the life cycle of a system and as technologies, policies and other influences evolve.

## 1.3

> A principal use of a software system’s architecture is to give those working with it a shared understanding of the system to guide its design and construction.

## 2.1

> An architecture view represents one or more aspects of an architecture to address one or more concerns [38*] ...
>
> - a logical view (depicts how the system will satisfy the functional requirements);
>
> - a process view (depicts how the system will use concurrency);
>
> - a physical view (depicts how the system is to be deployed and distributed) ...
>
> - a development view (depicts how the top-level design is broken down into implementation units, the dependencies among those units and how the implementation is to be constructed).

> Separating concerns by view allows interested stakeholders to focus on a few things at a time ...

## 3.2

> ... fundamentals of the system are decided, but other aspects, such as the internal details of major components are deferred.

> Typical concerns in architectural design ...
>
> - Overall architecture styles and computing paradigms
>
> - Large-scale refinement of the system into key components
>
> - Communication and interaction among components
>
> - Allocation of concerns and design responsibilities to components
>
> - Component interfaces
>
> - Understanding and analysis of scaling and performance properties, resource consumption properties, and reliability properties
>
> - Large-scale/system-wide approaches to dominating concerns (such as safety and security, where applicable)

# 3 Software Design

## 1.1

> ... design thinking appropriate to software: ...
>
> (1) crystallize a purpose or objective;
>
> (2) formulate a concept for how the purpose can be achieved;
>
> (3) devise a mechanism that implements the conceptual structure;
>
> (4) introduce a notation for expressing the capabilities of the mechanism and invoking its use;
>
> (5) describe the usage of the notation in a specific problem context to invoke the mechanism so the purpose is achieved. [20]

## 1.4

> Software design principles ...
>
> - Abstraction is “a view of an object that focuses on the information relevant to a particular purpose and ignores the remainder of the information” ...
>
> - Separation of concerns (SoC) ... By identifying and separating concerns, the designer can focus on each concern for the system in isolation ...
>
> - Modularization ... structures large software as comprising smaller components or units. Each component is named and has well-defined interfaces for its interactions with other components. Smaller components are easier to understand and, therefore, to maintain. ... each module in a system should have a single responsibility ...
>
> - Encapsulation ... nonessential information is less accessible, allowing users of the module to focus on the essential elements at the interface.
>
> - Separation of interface and implementation is an application of encapsulation that involves defining a component by specifying its public interfaces, which are known to and accessible to clients; isolating the use of a component from the details of how that component is built ...
>
> - Coupling is defined as “a measure of the interdependence among modules in a computer program” [11]. Most design methods advocate that modules should be loosely or weakly coupled.
>
> - Cohesion ... is defined as “a measure of the strength of association of the elements within a module” [11]. Cohesion highlights organizing a module’s constituents based on their relatedness. Most design methods advocate that modules should maximize their cohesion/locality.
>
> - Uniformity is a principle of consistency across software components — common solutions should be produced to address common or recurring problems. These include naming schemes, notations and syntax, interfaces that define access to services and mechanisms, and ordering of elements and parameters. This can be achieved through conventions such as rules, formats and styles.
>
> - Completeness ... means ensuring that a software component captures the important characteristics of an abstraction and leaves nothing out ... design completeness against requirements: a design should be sufficient for designers to demonstrate how requirements will be met and how subsequent work will satisfy those requirements ...
>
> - Verifiability means that information needed to verify the design against its requirements and other constraints is available ...

## 2

> Software design ... multistage ...
>
> - The architectural design stage addresses the fundamentals of the system as a whole and in relation to its environment ...
>
> - The high-level design stage is outward-facing — developing the top-level structure and organization of the software, identifying its various components and how that software system and its components interact with the environment and its elements.
>
> - The detailed design stage is inward-facing — specifying each component in sufficient detail to facilitate its construction and to meet its outside obligations, including how software components are further refined into modules and units.

## 4

> Work products of software design capture
>
> (1) aspects of the problems to be solved, using the vocabulary of the domain;
>
> (2) a solution vocabulary for solving the design problems (see section 1.1 Design Thinking);
>
> (3) the major decisions that have been taken; ...
>
> (4) explanations of the rationale for each nontrivial decision ...

> A fundamental aspect of software design is communication about the design among designers, and to customers, implementers and other stakeholders ... The communication will vary depending upon the target audience, the level of detail ..., and relevance ...

> The Unified Modeling Language (UML) is a widely used family of notations addressing both structural and behavioral concerns ...

## 4.6

> Design rationale captures why a design decision was made. This includes prior assumptions made, alternatives considered, and trade-offs and criteria ana lyzed to select one approach and reject others. Although the reasons for decisions are likely to be obvious to the current design team, they can be less obvious to those who modify or maintain the system after deployment. Recording the rationale enhances the software product’s long term maintainability.

## 5.1

> ... general strategies useful in the design process include divide-andconquer and stepwise refinement strategies; topdown vs. bottom-up strategies; strategies using heuristics, patterns and pattern languages; and iterative and incremental approaches.

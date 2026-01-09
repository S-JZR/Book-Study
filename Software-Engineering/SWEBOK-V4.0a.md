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

> Design rationale captures why a design decision was made. This includes prior assumptions made, alternatives considered, and trade-offs and criteria analyzed to select one approach and reject others. Although the reasons for decisions are likely to be obvious to the current design team, they can be less obvious to those who modify or maintain the system after deployment. Recording the rationale enhances the software product’s long term maintainability.

## 5.1

> ... general strategies useful in the design process include divide-andconquer and stepwise refinement strategies; topdown vs. bottom-up strategies; strategies using heuristics, patterns and pattern languages; and iterative and incremental approaches.

# 4 Software Construction

## 1.1

> - ... reduced complexity is achieved by creating simple and readable code rather than clever code.

## 1.2

> - Anticipating change helps software engineers build extensible software, enhancing a software product without disrupting the underlying structure.

## 1.3

> - Constructing for verification builds software in such a way that faults can be readily found ... Specific techniques ... include following coding standards to support code reviews and unit testing, organizing code to support automated testing, restricting the use of complex or difficult-to-understand language structures, and recording software behaviors with logs.

## 1.4

> - Reuse ... existing assets to solve different problems ... typical assets that are reused include frameworks, libraries, modules, components, source code and commercial off-the-shelf (COTS) assets.

## 1.5

> - Applying external or internal development standards during construction helps achieve a project’s efficiency, quality and cost objectives.

## 2.4

> Unnecessary dependencies should be avoided to improve build efficiency.

## 3.3

> The following considerations apply to the software construction coding activity:
>
> - Techniques for creating understandable source code, including naming conventions and source code layout
>
> - Use of classes, enumerated types, variables, named constants and other similar entities
>
> - Use of control structures
>
> - Handling of error conditions — both anticipated and exceptional (e.g., input of bad data)
>
> - Prevention of code-level security breaches (e.g., buffer overflows or array index bounds)
>
> - Resource use through use of exclusion mechanisms and discipline in accessing serially reusable resources, including threads and database locks
>
> - Source code organization into statements, routines, classes, packages or other structures
>
> - Code documentation
>
> - Code tuning

## 3.6

> ... techniques ... to ensure construction quality ...:
>
> - Unit testing and integration testing (see section 3.4, Construction Testing)
>
> - Test-first development (see section 6.1.2 in the Software Testing KA)
>
> - Use of assertions and defensive programming
>
> - Debugging
>
> - Inspections
>
> - Technical reviews, including security-oriented reviews (see section 2.3 in the Software Quality KA)
>
> - Static analysis (see section 2.2.1 of the Software Quality KA)

## 4.4

> Design by contract is a development approach in which preconditions and postconditions are included for each routine ... specifies the semantics of a routine and thus helps clarify its behavior.

> Defensive programming means to protect a routine from being broken by invalid inputs ... checking the values of all the input parameters and deciding how to handle bad inputs ...

## 4.5

> ... errors ... handled ...
>
> Assertions ... returning a neutral value, substituting the next piece of valid data, logging a warning message, returning an error code or shutting down the software ... Exceptions ... detect and process errors or exceptional events.

> Exception-handling policies ... including in the exception message all information that led to the exception, avoiding empty catch blocks, knowing the exceptions the library code throws, perhaps building a centralized exception reporter, and standardizing the program’s use of exceptions.

> ... fault tolerance strategies include backing up and retrying, using auxiliary code and voting algorithms, and replacing an erroneous value with a phony value that will have a benign effect.

## 4.14

> Code efficiency — determined by architecture, detailed design decisions, and data structure and algorithm selection — influences execution speed and size.

# 5 Software Testing

## I

> ... expected behaviors on a finite set of test cases ...
>
> - Finite: ... Testing always implies a trade-off between limited resources and schedules on the one hand and inherently unlimited test requirements on the other.
>
> - Selected: ... different selection criteria might yield vastly different degrees of effectiveness.
>
> - Expected: For each executed test case, it must be possible ... to decide whether the observed SUT outcomes match the expected ones ... observed behavior may be checked against user needs ( ... testing for validation), against a specification (testing for verification), or ... implicit requirements or expectations.

## 1.2.8

> ... "program testing can be used to show the presence of bugs, but never to show their absence” [3].

## 2

> Software testing is usually performed at different levels throughout development and maintenance. Levels can be distinguished based on the object of testing, the target, or on the purpose or objective (of the test level).

## 2.1

> ... target of the test ... unit, integration, system, and acceptance.

## 2.2

> ... objectives of testing ... check that the functional specifications are correctly implemented ... non-functional properties may be tested as well ... test objectives vary with the test target; different purposes are addressed at different levels of testing.

## 2.2.4

> Before the SUT is released, it is sometimes given to a small, selected group of potential users for trial use (alpha testing) and/or to a larger set of representative users (beta testing) ...

## 3

> ... degree of information about the SUT ... black-box techniques ... SUT’s input/ output behavior ... white-box ... techniques ... how the SUT has been designed or coded.

## 3.1

> ... specification-based techniques ... select a few test cases from the input domain that can detect specific categories of faults (also called domain errors). These techniques check whether the SUT can manage inputs within a certain range and return the required output.

## 3.1.2

> Boundary Value Analysis ... Test cases are chosen on or near the boundaries of the input domain of variables, with the underlying rationale that many faults tend to concentrate near the extreme values of inputs.
>
> ... robustness testing, wherein test cases are also chosen outside the input domain of variables to test program robustness in processing unexpected or erroneous inputs.

## 3.1.4

> The Combinatorial Test Techniques systematically derive the test cases that cover specific parameters of values or conditions.

## 3.1.5

> Decision tables ... represent logical relationships between conditions (roughly, inputs) and actions (roughly, outputs) ... Test cases are systematically derived by considering every possible combination of conditions and their corresponding resultant actions.

## 3.1.8

> Scenario-Based Testing ... represent the sequence of activities performed by humans and/or software applications ... ensure that both typical and alternate work flows are also tested.

## 3.1.11

> Forcing Exception ... Test cases are specifically conceived for checking whether the SUT can manage a predefined set of exceptions/errors, such as data exception, operation exception, overflow exception, protection exception or underflow exception.

## 3.2

> Structure-Based Test Techniques can be performed at different levels (such as code development, code inspection, or unit testing) and can include static testing (such as code inspection, code walkthrough, and code review), dynamic testing (like statement coverage, branch coverage, and path coverage), or code complexity measurement (e.g., using techniques like cyclomatic complexity [12]).

## 3.2.1

> Control flow testing covers all the statements, branches, decisions, branch conditions, mod ified condition decision coverage (MC/DC), blocks of statements, or specific combinations of statements in a SUT.

## 3.5.2

> Specialized heuristics ... systematically observe system use under controlled conditions to determine how well people can use the system and its interfaces ... include cognitive walkthroughs, claims analysis, field observations, thinking aloud, ... user questionnaires and interviews.

## 3.7

> Combining different testing techniques has always been a well-grounded means to assure the required level of SUT quality.

## 5.2.1

> Test Planning ... levels: ...
>
> (1) process management (i.e., identification of test policies, strategies, processes, and procedures),
>
> (2) organizational management (i.e., definition of the test phase, test type and test objective), ...
>
> (3) design and implementation (i.e., definition of the test environment, the test execution process and monitoring, the completion process, and reporting).

## 5.2.4

> ... everything done during testing should be performed and documented specificall and clearly enough that another person could replicate the results.

## 6.1.2

> ... shift-left testing movement ... testing in the early stages of software development to detect and remove faults as early as possible to increase overall SUT quality and reduce the cost and risks of testing activities.

# 6 Software Engineering Operations

## 2.2

> The overall software process requires the use of different environments at different stages ... the development environment, the testing or quality assurance (QA) environment, the preproduction environment, and the production environment.
>
> ... all environments need to be built from the same code source (single source of truth) to ensure that all the environments are synchronized with the production environment in which the software is released.

## 3.1

> ... execute software verification as early as possible, using test-driven development (TDD) ...

## 3.2

> Environment-based release strategies use a staging environment to support the release of a new version of an application.

> Application-based release strategies are based on the use of toggles (e.g., feature toggles) that make it possible to enable or disable specific sections of the code (e.g., a feature) using configuration parameters.

## 6

> ... “[t]he biggest risk to any software effort is that you end up building something that isn’t useful. The earlier and more frequently you get working software in front of real users, the quicker you get feedback to find out how valuable it really is.”

# 7 Software Maintenance

## 1.3

> Software maintenance is typically performed to do the following:
>
> - Correct faults and latent defects
>
> - Improve the design or performance of operational software
>
> - Implement enhancements
>
> - Help users understand the software’s functionality
>
> - Adapt to changes in interfaced systems or infrastructure
>
> - Prevent security threats
>
> - Remediate technical obsolescence of system or software elements
>
> - Retire the software

## 1.4

> ... the relative cost of error fixing increases in later phases of the software life cycle. Maintenance also uses a significant portion of the total financial resources attributed throughout the life of a software ... most software maintenance — over 80% — is used for enhancing and adapting the software [3].

## 1.5

> ... eight laws of software evolution:
>
> - Continuing Change — Software must be continually adapted, or it becomes progressively less satisfactory.
>
> - Increasing Complexity — As software evolves, its complexity increases unless work is done to maintain or reduce that complexity.
>
> - Self-Regulation — The program evolution process is self regulating with close to normal distribution of measures of product and process attributes.
>
> - Invariant Work Rate — The average effective global activity rate in an evolving software package is invariant over the product’s lifetime.
>
> - Conservation of Familiarity — As software evolves, all associated with it (e.g., developers, sales personnel and users) must maintain mastery of its content and behavior to achieve satisfactory evolution. Excessive growth diminishes that mastery ...
>
> - Continuing Growth — Functional content of a program must be continually increased to maintain user satisfaction over its lifetime.
>
> - Declining Quality — The quality of software will appear to be declining unless it is rigorously maintained and adapted to changes in the operational environment.
>
> - Feedback System — Software evolution processes constitute multilevel, multiloop, multi-agent feedback systems and must be treated as such to achieve significant improvement over any reasonable base.

## 2.1.1

> ... a significant portion of total maintenance effort is devoted to understanding the software to be modified ... Comprehension is more difficult in text-oriented representation (e.g., in source code), where it is often difficult to trace the evolution of software through its releases or versions if changes are not documented and the developers are not available to explain them.
>
> Various techniques can help engineers understand existing software, such as visualization and reverse engineering using tool-based graphical representations of the code.

## 2.1.4

> Technical debt often accumulates when the need to quickly address corrective, emergency, and additive maintenance tasks, constrained by limited time and understanding of the software, leads to compromises ... will take additional time and effort to address during maintenance.

> ... when addressing technical debt:
>
> 1. Code quality versus relevance: Not all technical debt is urgent.
>
> 2. Alignment with organizational objectives: The software architecture should reflect the organization’s goals.
>
> 3. Process loss: Ensure complementary skills of software engineers involved.

## 2.3.1

> ... improving maintainability, including: ensuring legibility, pursuing structured code, reducing code complexity, provide accurate code comments, using identation and white space, eliminating language weaknesses and compiler dependent constructs, facilitate error-tracing, ensure traceability of code to design, conduct inspections and code reviews.

## 4.2

> Refactoring ... aims to reorganize a program without changing its behavior ... to improve the internal structure and the maintainability of software.

# 8 Software Configuration Management

## 1.3

> ... branch ... set of evolving source file versions [1]. Merging consists of combining different changes to the same file [1] ...

## 2.3

> A software baseline is a formally approved version of a CI (regardless of media type) that is formally designated and fixed at a specific time during the CI’s life cycle ...

## 2.5

> CIs ... Common types of relationships ...
>
> - Dependencies: CI-1 and CI-2 depend mutually on each other ...
>
> - Derivation: One CI derives from another, typically in a sequential relationship ... for instance, CI-1 is completed before CI-2 is developed ...
>
> - Succession: Software items evolve as a software project proceeds ... state of an evolving item ... relationship with itself ...

## 3.2

> Changes may be supported by source code version control tools ... to track and document changes to the source code. These tools provide a single repository for storing the source code, so they can prevent more than one software engineer from editing the same module at the same time, and they record all changes made to the source code. Software engineers check modules out of the repository, make changes, document the changes, and then save the edited modules in the repository. If needed, changes can also be discarded, restoring a previous baseline.

# 9 Software Engineering Management

## I

> Other issues can complicate effective management ...
>
> - Clients often do not know what is needed or what is feasible.
>
> - Increased understanding and changing conditions will likely generate new or changed software requirements.
>
> - Clients often do not appreciate the complexities inherent in software engineering, particularly regarding the impact of changing requirements.
>
> - As a result of changing requirements and software malleability, software is often built iteratively rather than as a linear sequence of phases.
>
> ...
>
> - Typically, the underlying technology has a high rate of change.
>
> ...
>
> - A significant number of software projects failed due to human issues ...
>
> - Software rework to remove faults and respond to change.
>
> - Speed and cycle time are important metrics for managing software. Software capabilities are often delivered at increasing speed to satisfy business and mission needs [13].

> The deliverables, and hence the phases, are part of a generally sequential process designed to ensure proper control of the project and to attain the desired product or service, which is the project’s objective.

> ... project ... phases
>
> - Initiation and Scope Definition, which deals with the decision to embark on a software engineering project
>
> - Software Project Planning, which addresses the activities undertaken to prepare for a successful software engineering project from the management perspective
>
> - Software Project Enactment, which deals with generally accepted SEM activities that occur during a software engineering project’s execution
>
> - Review and Evaluation, which deals with ensuring that technical, schedule, cost and quality engineering activities are satisfactory
>
> - Closure, which addresses the activities accomplished to complete a project

## 1.2

> ... feasibility analysis is to develop a clear description of project objectives and to evaluate alternative approaches to determine whether the proposed project solution is the best approach, given the constraints of technology, resources, finances and changes to ethical, environmental, and socio-technical considerations. An initial project and product scope statement, project deliverables, project duration constraints, and an estimation of resources needed should be prepared.

> ... work breakdown structure (WBS) and context diagram ... Breaking work into smaller tasks is a common productivity technique that makes the work more manageable and approachable.

## 2.3

> The estimation of effort, schedule and cost is an iterative activity that should be negotiated and revised among affected stakeholders until consensus is reached on resources and time available for project completion.

> ... constantly monitor stakeholder requirements and changes as they evolve to analyze their impact on the project cost and schedule.

## 2.4

> Equipment, facilities and people should be allocated to the identified tasks, including allocating responsibilities for completing various project elements and the overall project.

## 2.5

> Risk is effect of uncertainty on objectives that has negative (threats) or positive (opportunities) consequences on objectives.

> ... risk register ... repository for all risks identified and for additional information about each risk [2].

## 2.6

> ... quality attributes that are important for software users (e.g., efficiency, safety, security, reliability, availability) and ... software developers and maintainers (e.g., maintainability is important to those who provide sustainment services)

## 3.6

> Progress to date should be reported at specified and agreed-upon times both within the organization (e.g., to a project steering committee) and to external stakeholders (e.g., clients or users). Reports should focus on the information needs of the target audience as opposed to the detailed status reporting within the project team.

## 4.1

> ... Progress should be assessed upon achieving a major project milestone ... or ... a product increment.

## 5.2

> A project, phase or iteration retrospective analysis should be undertaken so that issues, problems, risks and opportunities encountered can be analyzed. (See Topic 4, Review and Evaluation.) Lessons learned should be drawn from the project and fed into organizational learning and improvement endeavors.

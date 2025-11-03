# Software Design Description
## For {{project name}}

Version 0.1  
Prepared by {{author}}  
{{organization}}  
{{date_modified}}

## Table of Contents
<!-- TOC -->
* [1. Introduction](#1-introduction)
  * [1.1 Document Purpose](#11-document-purpose)
  * [1.2 Subject Scope](#12-subject-scope)
  * [1.3 Definitions, Acronyms, and Abbreviations](#13-definitions-acronyms-and-abbreviations)
  * [1.4 References](#14-references)
  * [1.5 Document Overview](#15-document-overview)
* [2. Design Overview](#2-design-overview)
  * [2.1 Stakeholder Concerns](#21-stakeholder-concerns)
  * [2.2 Selected Viewpoints](#22-selected-viewpoints)
* [3. Design Views](#3-design-views)
* [4. Decisions](#4-decisions)
* [5. Appendixes](#5-appendixes)
<!-- TOC -->

## Revision History

| Name | Date | Reason For Changes | Version |
|------|------|--------------------|---------|
|      |      |                    |         |
|      |      |                    |         |

## 1. Introduction
💬 _Provides an overview of the document and orients the reader to the system being designed._

### 1.1 Document Purpose
💬 _Clarifies why this SDD exists, what it describes, and who should use it._

➥ State the purpose of this SDD in 2–4 sentences. Identify its intended audiences (e.g., developers, architects, maintainers, operators) and how they use it across the lifecycle.

💡 Tips: 
- Mention related documents (vision/scope, BRD, SRS, roadmap, contracts) if relevant.

### 1.2 Subject Scope
💬 _Defines the scope, purpose, and boundaries of the design._

➥ Identify the system being designed by name and version/release. In 3–5 sentences, describe its primary purpose, key capabilities, and intended outcomes. Clearly list inclusions and exclusions when this SDD covers part of a larger system.

💡 Tips:
- Connect capabilities to business objectives and reference a separate vision/scope document if relevant.
- Include a simple diagram if it clarifies boundaries within a larger system.

### 1.3 Definitions, Acronyms, and Abbreviations
➥ Help readers understand specialized terms and notation by providing a glossary of domain terms, acronyms, and abbreviations used in the SDD.

💡 Tips:
- Keep entries alphabetized and consistent across the document set.

| Term | Definition                                                                                                               |
|------|--------------------------------------------------------------------------------------------------------------------------|
| API  | Application Programming Interface - A set of definitions and protocols for building and integrating application software |
| SDD  | Software Design Document - A document that describes the intended purpose, requirements, and nature of a software        |

### 1.4 References
💬 _Lists external sources that are normative or informative for this SDD._

➥ Cite standards, contracts, policies, interface specs, UX style guides, use-case docs, architectural decisions, or a vision/scope document. For each reference, include title, author/owner, version, date, and location/URL. Indicate whether each reference is normative (binding) or informative (guidance).

💡 Tips:
- Prefer stable links or repository paths over volatile URLs.

### 1.5 Document Overview
💬 _Brief guide to the structure of the SDD so readers can quickly find what they need._

➥ Summarize what each major section covers (Design, Decisions, Appendixes), note any document conventions, and mention how updates and revision history are managed.

💡 Tips:
- Keep to 3–5 sentences focusing on navigation and conventions.

## 2. Design Overview
💬 _Describes the nature and approach of the system architecture and design._

### 2.1 Stakeholder Concerns
💬 _Defines key stakeholders and their design-related interests._

➥ Identify stakeholder types (e.g., users, developers, operators), their main concerns (e.g., availability, maintainability, risk mitigation) and the viewpoints or design elements of this document that address them.

### 2.2 Selected Viewpoints
💬 _Defines the perspectives used to represent and reason about the system’s design._

➥ Identify and describe the viewpoints that were selected to address the stakeholders' concerns identified in Section 2.1. Each viewpoint addresses specific stakeholder concerns and utilizes visualization languages (e.g., UML, C4, sequence diagrams). Note which concerns each viewpoint addresses.

#### 2.2.1 Context
💬 _Defines the system as a black box, identifying its boundaries and its environment._

**Addresses:** System boundaries, environment actors (users, external systems) and offered services (use cases).
**Typical Languages:** UML Use Case Diagram, C4 Context Diagram.

#### 2.2.2 Composition
💬 _Describes how the system is recursively assembled from major constituent parts (subsystems, components, or modules), and how those are organized and relate to one another_

**Addresses:** Identify the major design elements; allocation of responsibilities, and localization of functionality; modularity (reuse, buy-vs-build) and integration.
**Typical Languages:** UML Component Diagram, Hierarchical Decomposition Diagram, UML Package (functional), Deployment (runtime) Diagram.

💡 Tips:
- Focus on how components fit together and where external, reused, or third-party components integrate.
- Consider organizing into subcategories for clarity: Functional (logical) decomposition and Runtime (physical) decomposition.

#### 2.2.3 Logical
💬 _Captures the static design structure of the system in terms of types and their implementation (class, interface) and their relationships._

**Addresses:** Development and reuse of appropriate abstractions and their implementations; encapsulation and dependencies among entities.
**Typical Languages:** UML Class Diagram, UML Object Diagram.

💡 Tips: 
- Focus on the static and stable abstractions that collaborate to fulfill system goals. 
- Complements Composition (assembly) by clarifying the abstractions that underlie it.

#### 2.2.4 Physical
💬 _Depicts the tangible system infrastructure._

**Addresses:** Hardware configuration, physical topology, and physical constraints.
**Typical Languages:** Hardware Block Diagram, Network Topology Diagram, Rack Layout, Cloud Infrastructure Diagram.

💡 Tips:
- Complements Deployment by showing the platform topology on which software is mapped.

#### 2.2.5 Structure
💬 _Documents internal organization of components and their parts, ports, and connectors_.

**Addresses:** Internal composition of complex entities; reusability of fine-grained components.
**Typical Languages:** UML composite structure diagram, UML class diagram, UML package diagram, C4 Container diagram.

💡 Tips: 
- Complements Composition by focusing on interfaces and connectors.

#### 2.2.6 Dependency
💬 _Shows how design elements interconnect and access each other, illustrating import, service, or build-time relationships._

**Addresses:** Integration needs and prioritization; coupling and dependencies; root cause and change impact analysis.
**Typical Languages:** UML Package Diagram, Dependency Graph, UML Component Diagram

💡 Tips: 
- Draw dependencies directionally (“uses”, “requires”, “provides”).

#### 2.2.7 Information
💬 _Models the persistent data structure, its relationships, and the mechanisms for access and management._

**Addresses:** Data structure and semantics; persistence; metadata; data integrity; data management and access schemes.
**Typical Languages:** Entity-Relationship Diagram, UML Class Diagram, Logical Data Model.

💡 Tips: 
- Use consistent naming with the Logical viewpoint to maintain type alignment.

#### 2.2.8 Interface
💬 _Specifies the externally visible interfaces among components, subsystems, or with external systems._

**Addresses:** Interoperability through contract definition; encapsulation, and integration risks.
**Typical Languages:** API specifications, IDLs, function/method signature, UML Component Diagram

#### 2.2.9 Interaction
💬 _Illustrates how entities collaborate at runtime via messages: who talks to whom, in what order, and under which conditions._

**Addresses:** Allocation of responsibilities; message sequencing, timing, and synchronization; error propagation; distributed components state transition logic and concurrency.
**Typical Languages:** UML Sequence Diagram, UML Collaboration Diagram, BPMN Process Flows.

💡 Tips:
- Provide representative “happy-path” and “failure-path” scenarios.
- If concurrency affects ordering, annotate lifelines/regions and reference the Concurrency viewpoint.

#### 2.2.10 Algorithm
💬 _Details the internal processing logic of an operation: steps, decisions, loops, and error handling, emphasizing critical or novel algorithms within the design._

**Addresses:** Computational complexity; time-space processing logic; performance, determinism, and reproducibility.
**Typical Languages:** Pseudocode, flowchart, Decision Table mathematical formulation.

💡 Tips: 
- Tie each algorithm to its owning class/component.
- Consider referencing Interface contracts to link invariants and pre/postconditions.
- Consider referencing Resource impacts if performance or space is critical.

#### 2.2.11 State Dynamics
💬 _Details how system or component states evolve in response to events or stimuli over time._

**Addresses:** Modes/states, transitions, events/triggers, guards, entry/exit effects, concurrency regions, synchronization.
**Typical Languages:** UML State Machine Diagram, State Transition Table, Automata, Petri Net.

💡 Tips: 
- Complements Interaction/Algorithm when behavior differs by state.

#### 2.2.12 Concurrency
💬 _Describes how the design handles parallelism, synchronization, and coordination among concurrent entities._

**Addresses:** Thread/process structure; synchronization and locking; concurrency control; event ordering; parallel execution and race conditions.
**Typical Languages:** UML Activity Diagram, UML Sequence and State Diagram, actor model.

💡 Tips:
- Complements other dynamic viewpoints when parallelism, synchronization, or ordering guarantees are first-class concerns that would clutter those views.

#### 2.2.13 Patterns
💬 _Identifies reusable design ideas and collaborations—design patterns, architectural styles, or framework templates—that guide or constrain the system’s structure and behavior._

**Addresses:** Reuse of proven solutions; consistency of architectural style; collaboration roles and connectors; template-based component structures.
**Typical Languages:** UML Composite Structure Diagram, UML Package/Class Diagram, Architecture Description Language.

💡 Tips: 
- Record which patterns are applied and where.

#### 2.2.14 Deployment
💬 _Describes how software entities are mapped onto the physical execution environment, what runs where and how nodes are connected_

**Addresses:** Component-to-node allocation; deployment topology; communication mechanisms; distribution, replication, and scaling; operational constraints.
**Typical Languages:** UML Deployment Diagram, Infrastructure-as-Code topology, Network Diagram, CI/CD pipeline diagrams.

💡 Tips: 
- Include environment tiers and deployment sequencing if relevant.

#### 2.2.15 Resources
💬 _Specifies use and management of shared or limited resources, such as memory, bandwidth, threads, or file handles._

**Addresses:** Resource utilization and allocation; contention and availability; performance bottlenecks; locks and priorities; resource management strategies. 
**Typical Languages:** UML Class Diagram (for resource entities), UML Real-Time Profile, UML Object Constraint Language (OCL), Resource Allocation Table.

💡 Tips: 
- Cross-reference with Concurrency (timing) and Deployment (placement) views for a full runtime picture..

## 3. Design Views
💬 _Documents the main architectural and design elements that define the system._

➥ Define design views to a level of detail sufficient to implement the system (prescriptive architecture) or to understand how to operate or maintain the existing product (descriptive architecture). Use unique identifiers, keep elements concise and modular, and include diagrams or links where applicable. Reference relevant design decisions from Section 4 that this view represents. Include applicable SRS requirement IDs that this element implements when available.

📃 Template:
```markdown
- ID: [NNN]-{title}
- Title: Short, descriptive name of the view.
- Viewpoint: The viewpoint of which this view is an instance.
- Representation: The design view representation per the viewpoint and language selected, e.g., natural language description or a diagram or a combination thereof.
- More Information: Additional context. Links to related artifacts.
```

💡 Tips:
- This section should contain enough information to implement the system (prescriptive architecture) or to understand how to operate or maintain the existing product (descriptive architecture).
- If available, include references to the SRS requirement IDs that the design view implements. This demonstrates how requirements are addressed by the design.
- Reference relevant design decisions from Section 4 that influenced or resulted from this design element.

## 4. Decisions
💬 Captures significant architectural or design decisions and their rationale.

➥ Document significant architectural decisions that have substantial long-term impact on the system's structure,
behavior, or quality attributes.

```markdown
- ID: [NNN]-{title}
- Title: short title, representative of solved problem and found solution.
- Context: Describe the context and problem statement.
- Options: Enumerate considered alternatives.
- Outcome: Chosen option: "{title of option 1}", because {justification}.
- More Information: Additional context. Links to related artifacts.
```

💡 Tips:
- Keep one decision per record.
- Consider adopting MADR (Markdown Architecture Decision Record) pattern directly to document decisions. 

## 5. Appendixes
💬 _Optional supporting material that aids understanding without being normative._

➥ Include glossaries, data dictionaries, models/diagrams, sample datasets, or change-impact analyses that support the main sections. Reference rather than duplicate content when possible.

💡 Tips:
- Keep appendixes organized and referenced from the main text.


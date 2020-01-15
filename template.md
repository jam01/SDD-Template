# Software Design Description
## For <project name>

Version 0.1
Prepared by <author>  
<organization>  
<date created>  

Table of Contents
=================
* [Revision History](#revision-history)
* 1 [Introduction](#1-introduction)
  * 1.1 [Document Purpose](#11-document-purpose)
  * 1.2 [Product Scope](#12-product-scope)
  * 1.3 [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
  * 1.4 [References](#14-references)
  * 1.5 [Document Overview](#15-document-overview)
* 2 [Design](#2-overall-description)
  * 2.1 [Stakeholder concerns](#21-stakeholder-concerns)
  * 2.2 [Selected Viewpoints](#22-selected-viewpoints)
    * 2.2.1 [Context](#221-context)
    * 2.2.2 [Composition](#222-composition)
    * 2.2.3 [Logical](#223-logical)
    * 2.2.4 [Dependency](#224-dependency)
    * 2.2.5 [Information](#225-information)
    * 2.2.6 [Patterns](#226-patterns)
    * 2.2.7 [Interface](#227-interface)
    * 2.2.8 [Structure](#228-structure)
    * 2.2.9 [Interaction](#229-interaction)
    * 2.2.10 [State dynamics](#2210-state-dynamics)
    * 2.2.11 [Algorithm](#2211-algorithm)
    * 2.2.12 [Resources](#2212-resources)
    * 2.2.13 [Physical](#2213-physical)
    * 2.2.14 [Deployment](#2214-deployment)
    * 2.2.15 [Concurrency](#2215-concurrency)
    * 2.2.16 [Behavioral](#2216-behavioral)
  * 2.3 [Design Views](#23-design-views)
* 3 [Appendixes](#3-appendixes)

## Revision History
| Name | Date    | Reason For Changes  | Version   |
| ---- | ------- | ------------------- | --------- |
|      |         |                     |           |
|      |         |                     |           |
|      |         |                     |           |

## 1. Introduction
> This section should provide an overview of the entire document

### 1.1 Document Purpose
Describe the purpose of the SDD and its intended audience.

### 1.2 Subject Scope
<!-- TODO -->

### 1.3 Definitions, Acronyms and Abbreviations

### 1.4 References
List any other documents or Web addresses to which this SDD refers. Provide enough information so that the reader could access a copy of each reference, including title, author, version number, date, and source or location.

### 1.5 Document Overview
Describe what the rest of the document contains and how it is organized.

## 2. Design
> This section is the body of the SDD and should detail the nature and approach of the design.

### 2.1 Stakeholder Concerns
> Identify the different type of stakeholders to whom the SDD will be of interest and their concerns on the design subject. For example, on a prescriptive design, software developers are one of the main stakeholders and their concerns could be functionality and software interoperability, whereas operators may be more concerned with configurability and deployment options.

> Usual design stakeholders include users, developers, operators, software designers, system integrators, maintainers, acquirers, and project managers. Design concerns are usually aligned with functional or non-functional properties like functionality, reliability, performance, or maintainability. Concerns can also be more specific or abstract like the feasibility of constructing and deploying the system, or e potential risks and impacts of the system to its stakeholders throughout its life cycle.

> The specific stakeholders entries should:
* Be identifiable.
* State their design concerns.
* Reference the design views that address such concerns.

### 2.2 Selected Viewpoints
> Identify and describe the viewpoints that were selected in order to address the stakeholders' concern identified in section 2.1. A viewpoint defines the perspective from which a design view is taken. Each selected viewpoint should state what concerns it addresses and identify the visualization language(s) it uses to do so.

> For example in order to address interoperability concerns an SDD author may choose to utilize an Interface viewpoint. The author must then also choose which visualization languages are appropriate for that viewpoint and the design subject, some options may be UML Component diagrams, Interface Definition Language (IDL), or OpenAPI specification.

> See IEEE 1016-1998

#### 2.2.1 Context
Helps describe the design subject as a black box. It can depict the subject in terms of offered services, actors, system boundaries, and design subject's scope. Example visualization languages include UML use case diagram.

#### 2.2.2 Composition
Describes the way the design subject is (recursively) structured into constituent subsystems and (pluggable) components, buy vs. build, reuse of components. Can be broken down into Logical and Physical composition viewpoints. Example visualization languages include UML package diagram, UML component diagram, UML deployment diagram.

#### 2.2.3 Logical
Describes static structure such as classes, interfaces, and their relationships. Example visualization languages include UML class diagram, and UML object diagram.

#### 2.2.4 Dependency
Interconnection, sharing, and parameterization

#### 2.2.5 Information
<!-- TODO -->
#### 2.2.6 Patterns
<!-- TODO -->
#### 2.2.7 Interface
<!-- TODO -->
#### 2.2.8 Structure
<!-- TODO -->
#### 2.2.9 Interaction
<!-- TODO -->
#### 2.2.10 State dynamics
<!-- TODO -->
#### 2.2.11 Algorithm
<!-- TODO -->
#### 2.2.12 Resources
<!-- TODO -->
#### 2.2.13 Physical
<!-- TODO -->
#### 2.2.14 Deployment
<!-- TODO -->
#### 2.2.15 Concurrency
<!-- TODO -->
#### 2.2.16 Behavioral
<!-- TODO -->

### 2.3 Views
> This sub-section, depending on the nature of the design activity, should contain enough information to implement the product (prescriptive architecture) or enough information for others to understand how to maintain or adapt the existing product (descriptive architecture).

> The specific views should:
* Be uniquely identifiable
* Identify the viewpoint of which it is an instance
* Provide the view representation according to the viewpoint languages
* Record the relevant design decisions made as they relate to the presented view's elements, see IEEE 42010:2011 5.8.2

## 3. Appendixes

# Requirements Engineering

**Requirements engineering (RE)** is the process of establishing the services a customer requires from a system and the constraints under which it operates and is developed.

- System requirements are descriptions of system services and constraints generated during the RE process

## What is a Requirement?

- Ranges from a high-level abstract statement of a service or system constraint to a detailed mathematical functional specification
- Serves a dual function:
  - Basis for a **bid for a contract** — must be open to interpretation
  - Basis for the **contract itself** — must be defined in detail
  - Both may be called requirements

### Requirements Abstraction (Davis)

- "If a company wishes to let a contract for a large software development project, it must define its needs in a sufficiently abstract way that a solution is not pre-defined"
- Requirements must allow several contractors to bid, offering different ways of meeting needs
- After contract award, the contractor writes a detailed system definition for client validation
- Both documents may be called the requirements document

## Types of Requirement

- **User requirements** — natural language + diagrams of services and operational constraints; written for customers
- **System requirements** — structured document with detailed descriptions of functions, services, and operational constraints; defines what should be implemented; may be part of a contract between client and contractor

### Readers of Different Requirement Specifications

- User requirements: read by end-users, managers, customers (non-technical)
- System requirements: read by developers, testers, project managers (technical)

## System Stakeholders

Any person or organisation affected by the system who has a legitimate interest:

- **End users**
- **System managers**
- **System owners**
- **External stakeholders**

### Stakeholders in the Mentcare System

- Patients whose information is recorded in the system
- Doctors responsible for assessing and treating patients
- Nurses who coordinate consultations and administer treatments
- Medical receptionists who manage appointments
- IT staff responsible for installing and maintaining the system
- Medical ethics manager who ensures the system meets ethical guidelines
- Health care managers who obtain management information
- Medical records staff who ensure information is maintained, preserved, and record-keeping procedures are implemented

## Agile Methods and Requirements

- Producing detailed system requirements is seen as a waste of time — requirements change too quickly
- The requirements document is always out of date
- Agile uses **incremental requirements engineering** and expresses requirements as **user stories**
- Practical for business systems; problematic for systems requiring pre-delivery analysis (critical systems) or systems developed by several teams

## Functional and Non-functional Requirements

### Functional Requirements

- Statements of services the system should provide
- How the system should react to particular inputs
- How the system should behave in particular situations
- May state what the system should **not** do
- Depend on the type of software, expected users, and type of system
- Functional **user** requirements may be high-level statements
- Functional **system** requirements should describe services in detail

### Mentcare System: Functional Requirements Example

- A user shall be able to **search the appointments lists** for all clinics
- The system shall **generate each day, for each clinic**, a list of patients expected to attend appointments that day
- Each staff member shall be **uniquely identified** by his or her 8-digit employee number

### Requirements Imprecision

- Problems arise when functional requirements are not precisely stated
- Ambiguous requirements may be interpreted differently by developers and users
- Example — the term **search** in requirement 1:
  - **User intention** — search for a patient name across all appointments in all clinics
  - **Developer interpretation** — search for a patient name in an individual clinic (user chooses clinic then searches)

### Requirements Completeness and Consistency

- In principle, requirements should be both complete and consistent
- **Complete** — include descriptions of all facilities required
- **Consistent** — no conflicts or contradictions in descriptions
- In practice, system and environmental complexity makes a complete and consistent requirements document impossible

### Non-functional Requirements

- Define system properties and constraints (reliability, response time, storage requirements)
- Constraints: I/O device capability, system representations
- **Process requirements** may mandate a particular IDE, programming language, or development method
- May be more critical than functional requirements — if unmet, the system may be useless
- May affect the overall architecture rather than individual components (e.g. minimising communications between components for performance)
- A single security requirement may generate multiple related functional requirements and restrict existing requirements

### Domain Requirements

- Constraints on the system from the domain of operation

## Non-functional Requirements Classifications

### Product Requirements

- Specify the delivered product must behave in a particular way (execution speed, reliability)

### Organisational Requirements

- Consequence of organisational policies and procedures (process standards, implementation requirements)

### External Requirements

- Factors external to the system and its development process (interoperability, legislative requirements)

### Examples from the Mentcare System

| Type | Example |
|---|---|
| **Product** | The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 0830–17.30). Downtime within normal working hours shall not exceed five seconds in any one day |
| **Organisational** | Users of the Mentcare system shall authenticate themselves using their health authority identity card |
| **External** | The system shall implement patient privacy provisions as set out in HStan-03-2006-priv |

## Goals vs Verifiable Requirements

- Non-functional requirements are difficult to state precisely; imprecise requirements are difficult to verify
- **Goal** — a general intention of the user (e.g. ease of use)
- **Verifiable non-functional requirement** — a statement using some measure that can be objectively tested
- Goals are helpful to developers as they convey the intentions of system users

### Usability Requirements Example

| Type | Statement |
|---|---|
| **Goal** | The system should be easy to use by medical staff and organised so user errors are minimised |
| **Testable NFR** | Medical staff shall use all system functions after 4 hours of training; after training, avg errors by experienced users ≤ 2 per hour of system use |

## Metrics for Specifying Non-functional Requirements

| Property | Measure |
|---|---|
| **Speed** | Processed transactions/second, user/event response time, screen refresh time |
| **Size** | Mbytes, number of ROM chips |
| **Ease of use** | Training time, number of help frames |
| **Reliability** | Mean time to failure, probability of unavailability, rate of failure occurrence, availability |
| **Robustness** | Time to restart after failure, % events causing failure, probability of data corruption on failure |
| **Portability** | % target-dependent statements, number of target systems |

## Requirements Engineering Processes

- Vary by application domain, people involved, and organisation
- Generic activities common to all processes:
  - **Requirements elicitation**
  - **Requirements analysis**
  - **Requirements validation**
  - **Requirements management**
- RE is an iterative activity in which processes are interleaved — a spiral view

## Requirements Elicitation

- Technical staff work with customers to discover the application domain, services, and operational constraints
- Involves end-users, managers, engineers, domain experts, trade unions — collectively called **stakeholders**

### Stages of Elicitation

1. **Requirements discovery** — interacting with stakeholders to discover requirements; domain requirements are also discovered
2. **Requirements classification and organisation** — grouping related requirements into coherent clusters
3. **Prioritisation and negotiation** — prioritising requirements and resolving conflicts
4. **Requirements specification** — documenting requirements for the next spiral iteration

### Problems of Requirements Elicitation

- Stakeholders don't know what they really want
- Stakeholders express requirements in their own terms
- Different stakeholders may have conflicting requirements
- Organisational and political factors may influence system requirements
- Requirements change during analysis; new stakeholders emerge; business environment changes

### Interviewing

- Formal or informal interviews with stakeholders are part of most RE processes
- **Closed interviews** — based on pre-determined list of questions
- **Open interviews** — various issues explored with stakeholders

#### Effective Interviewing

- Be open-minded, avoid pre-conceived ideas about requirements, and listen to stakeholders
- Prompt interviewees using:
  - **Springboard question** — a starting question to begin discussion
  - **Requirements proposal** — suggest a possible requirement for reaction
  - **Prototype system** — work together on a prototype
- Normally a mix of closed and open-ended interviewing

#### Problems with Interviews

- Application specialists use domain language that is hard for requirements engineers to understand
- Interviews are not good for understanding domain requirements:
  - Engineers cannot understand specific domain terminology
  - Some domain knowledge is so familiar that people find it hard to articulate or think it isn't worth articulating

### Ethnography

- A social scientist spends considerable time observing and analysing how people actually work
- People do not have to explain or articulate their work
- Social and organisational factors of importance may be observed
- Work is usually richer and more complex than simple system models suggest

#### Scope of Ethnography

- Requirements derived from how people actually work, not how process definitions suggest they ought to work
- Requirements derived from cooperation and awareness of other peoples activities
- Effective for understanding **existing processes** but cannot identify new features that should be added

### Focused Ethnography

- Developed in a project studying air traffic control
- Combines ethnography with **prototyping**
- Unanswered questions from prototype development focus the ethnographic analysis
- Problem: ethnography studies existing practices that may have historical basis no longer relevant

### Stories and Scenarios

- Real-life examples of how a system can be used
- Stakeholders can relate to them and comment on their situation

#### Example: Photo Sharing in the Classroom (iLearn)

- Jack is a primary school teacher in Ullapool, Scotland
- He decides a class project focused around the fishing industry (history, development, economic impact)
- Pupils gather reminiscences from relatives, use newspaper archives, collect old photographs
- Pupils use an **iLearn wiki** to gather stories and **SCRAN** (history resources site) for archives/photos
- Jack needs a **photo sharing site** so pupils can take and comment on each other's photos and upload scans
- Emails a primary school teachers group; two teachers suggest **KidsTakePics** (a photo sharing site allowing teachers to moderate content)
- KidsTakePics is not integrated with iLearn authentication, so Jack sets up teacher and class accounts
- Uses iLearn setup service to add KidsTakePics to services seen by pupils; when they log in they can immediately upload photos

#### Scenario Structure

Scenarios are a structured form of user story that should include:

- Description of the **starting situation**
- Description of the **normal flow of events**
- Description of **what can go wrong**
- Information about **other concurrent activities**
- Description of the **state when the scenario finishes**

#### Example: Uploading Photos (iLearn / KidsTakePics)

**Starting situation:**

- User or group of users have digital photos saved on a tablet or laptop
- They have successfully logged on to KidsTakePics

**Normal flow:**

- User chooses Upload Photos; prompted to select photos and project name
- Option to input keywords for each photo
- Uploaded photos named by combining username with local filename
- System emails the project moderator to check new content
- On-screen message confirms the action

**What can go wrong:**

- **No moderator** associated with the project — email generated to school administrator to nominate one; users informed of possible delay
- **Duplicate filenames** — user asked to re-upload (overwrite), rename (auto-add number), or cancel

**Other activities:**

- Moderator may be logged on and approve photos as they are uploaded

**System state on completion:**

- User is logged on
- Selected photos uploaded with status **awaiting moderation**
- Photos visible to moderator and the uploading user

## Requirements Specification

- Process of writing user and system requirements in a requirements document
- **User requirements** — understandable by end-users and customers (non-technical background)
- **System requirements** — more detailed, may include technical information
- May be part of a contract — must be as complete as possible

### Ways of Writing System Requirements

| Notation | Description |
|---|---|
| **Natural language** | Numbered sentences in natural language; each expresses one requirement |
| **Structured natural language** | Standard form or template with fields for each aspect of the requirement |
| **Design description languages** | Programming-like language with abstract features (rarely used now, useful for interface specifications) |
| **Graphical notations** | UML use case and sequence diagrams with text annotations |
| **Mathematical specifications** | Based on finite-state machines or sets — unambiguous but most customers cannot check what it represents |

### Requirements and Design

- In principle, requirements state **what** the system should do; design describes **how**
- In practice, requirements and design are inseparable:
  - System architecture may be designed to structure the requirements
  - System may inter-operate with other systems generating design requirements
  - Use of specific architecture for non-functional requirements may be a domain requirement
  - May be consequence of a regulatory requirement

### Natural Language Specification

- Requirements written as natural language sentences supplemented by diagrams and tables
- Expressive, intuitive, and universal — understandable by users and customers

#### Guidelines

- Invent a standard format and use it for all requirements
- Use language consistently — **shall** for mandatory, **should** for desirable
- Use text highlighting to identify key parts
- Avoid computer jargon
- Include rationale explaining why the requirement is necessary

#### Problems

- **Lack of clarity** — precision is difficult without making the document hard to read
- **Requirements confusion** — functional and non-functional tend to be mixed
- **Requirements amalgamation** — several different requirements expressed together

### Example Requirements for the Insulin Pump

- **3.2** The system shall measure the blood sugar and deliver insulin, if required, every 10 minutes (rationale: blood sugar changes are slow; more frequent measurement unnecessary; less frequent could lead to high sugar levels)
- **3.6** The system shall run a self-test routine every minute with conditions and actions defined in Table 1 (rationale: self-test can discover hardware/software problems and alert the user)

### Structured Specifications

- Limits writer freedom; requirements written in a standard way
- Works well for embedded control systems; may be too rigid for business systems

### Form-based Specifications

Components of a form-based specification:

- Definition of the **function or entity**
- Description of **inputs** and where they come from
- Description of **outputs** and where they go to
- Information needed for the **computation** and other entities used
- Description of the **action** to be taken
- **Pre and post conditions** (if appropriate)
- **Side effects** (if any)

### Tabular Specification

- Supplements natural language
- Useful when defining multiple possible alternative courses of action
- Example: insulin pump computes dose based on rate of change of blood sugar level

Insulin pump computation table:

| Condition | Action |
|---|---|
| Sugar level falling (r2 < r1) | CompDose = 0 |
| Sugar level stable (r2 = r1) | CompDose = 0 |
| Sugar level increasing, rate of increase decreasing ((r2 - r1) < (r1 - r0)) | CompDose = 0 |
| Sugar level increasing, rate of increase stable or increasing ((r2 - r1) >= (r1 - r0)) | CompDose = round((r2 - r1) / 4); if rounded result = 0 then CompDose = MinimumDose |

### Use Cases

- UML-based scenarios
- Identify **actors** in an interaction and describe the interaction itself
- A set of use cases should describe all possible interactions with the system
- High-level graphical model supplemented by more detailed tabular description
- UML sequence diagrams add detail showing sequence of event processing

## The Software Requirements Document

- Official statement of what is required of system developers
- Includes both user requirements definition and system requirements specification
- **NOT a design document** — describes **what**, not **how**
- Content varies by system type and development approach

### Users of the Requirements Document

- **Customers** — specify requirements and read them for validation
- **Managers** — use to plan and schedule development
- **System engineers** — use to understand what to build
- **Test engineers** — use to develop test cases
- **Maintenance engineers** — use to understand the system for changes

### Requirements Document Variability

- Information depends on type of system and development approach
- Systems developed incrementally have less detail
- IEEE standard exists for large systems engineering projects

### Structure of a Requirements Document

| Chapter | Description |
|---|---|
| **Preface** | Expected readership, version history, rationale for new versions, summary of changes |
| **Introduction** | Need for the system, brief function description, how it works with other systems, alignment with business objectives |
| **Glossary** | Technical terms used in the document |
| **User requirements definition** | Services for the user, non-functional requirements described in understandable language, product and process standards |
| **System architecture** | High-level overview, distribution of functions across modules, reused components highlighted |
| **System requirements specification** | Functional and non-functional in detail; interfaces to other systems |
| **System models** | Graphical models (object models, data-flow models, semantic data models) showing relationships between components |
| **System evolution** | Fundamental assumptions, anticipated changes (hardware evolution, changing user needs), helps designers avoid constraining future changes |
| **Appendices** | Detailed specific information — hardware descriptions (minimal/optimal config), database descriptions (logical organisation, data relationships) |
| **Index** | Normal alphabetic index, index of diagrams, index of functions |

## Requirements Validation

- Concerned with demonstrating that requirements define the system the customer really wants
- Requirements error costs are high — fixing after delivery may cost up to **100 times** the cost of fixing an implementation error

### Requirements Checking

- **Validity** — does the system provide the functions that best support the customer's needs?
- **Consistency** — are there any requirements conflicts?
- **Completeness** — are all functions required by the customer included?
- **Realism** — can requirements be implemented given available budget and technology?
- **Verifiability** — can the requirements be checked?

### Validation Techniques

- **Requirements reviews** — systematic manual analysis of the requirements
- **Prototyping** — using an executable model to check requirements
- **Test-case generation** — developing tests for requirements to check testability

### Requirements Reviews

- Regular reviews while requirements definition is being formulated
- Both client and contractor staff involved
- Reviews may be **formal** (with completed documents) or **informal**
- Good communication between developers, customers, and users resolves problems early

### Review Checks

- **Verifiability** — is the requirement realistically testable?
- **Comprehensibility** — is the requirement properly understood?
- **Traceability** — is the origin of the requirement clearly stated?
- **Adaptability** — can the requirement be changed without large impact on other requirements?

## Requirements Change

### Why Requirements Change

- Business and technical environment always changes after installation:
  - New hardware introduced
  - Need to interface with other systems
  - Business priorities change
  - New legislation and regulations introduced
- Customers and users are rarely the same people — conflicting requirements
- Large systems have diverse user communities with different, often conflicting priorities — final requirements are inevitably a compromise

### Requirements Evolution

- Requirements evolve continuously as systems are developed and used
- New requirements emerge during development and after deployment

### Requirements Management

- Process of managing changing requirements during RE and system development
- Track individual requirements and maintain links between dependent requirements
- Establish formal process for change proposals and link them to system requirements

### Requirements Management Planning

- **Requirements identification** — each requirement uniquely identified for cross-referencing
- **Change management process** — activities that assess impact and cost of changes
- **Traceability policies** — relationships between requirements and between requirements and system design
- **Tool support** — from specialist requirements management systems to spreadsheets and databases

### Requirements Change Management Process

1. **Problem analysis and change specification**
   - Problem or change proposal is analysed for validity
   - Analysis fed back to requestor who may respond with more specific proposal or withdraw

2. **Change analysis and costing**
   - Effect of proposed change assessed using traceability information and knowledge of requirements
   - Decision made whether to proceed

3. **Change implementation**
   - Requirements document, system design, and implementation modified
   - Document should be organised so changes can be easily implemented

---

# System Modeling

**System modeling** is the process of developing abstract models of a system, each presenting a different view or perspective.

- Uses graphical notation, almost always based on **Unified Modeling Language (UML)**
- Helps analysts understand system functionality
- Models are used to communicate with customers

## Existing and Planned System Models

- **Existing system models** — used during RE to clarify what the current system does; basis for discussing strengths and weaknesses
- **New system models** — used to explain proposed requirements to stakeholders, discuss design proposals, and document for implementation
- **Model-driven engineering** — generates complete or partial implementation from system models

## System Perspectives

- **External perspective** — models the context or environment of the system
- **Interaction perspective** — models interactions between the system and its environment, or between system components
- **Structural perspective** — models the organisation of a system or the structure of data processed
- **Behavioral perspective** — models dynamic behaviour and how the system responds to events

## UML Diagram Types

| Diagram | Purpose |
|---|---|
| **Activity diagrams** | Show activities in a process or data processing |
| **Use case diagrams** | Show interactions between a system and its environment |
| **Sequence diagrams** | Show interactions between actors and the system and between components |
| **Class diagrams** | Show object classes and associations between them |
| **State diagrams** | Show how the system reacts to internal and external events |

## Use of Graphical Models

- **Facilitate discussion** about existing or proposed systems — incomplete and incorrect models are OK as their role is to support discussion
- **Document existing system** — accurate representation but need not be complete
- **Generate system implementation** — models must be correct and complete

## Context Models

- Illustrate the operational context of a system — what lies outside system boundaries
- Social and organisational concerns affect boundary decisions
- **Architectural models** show the system and its relationship with other systems

### System Boundaries

- Define what is inside and outside the system
- Show other systems that are used or depend on the system being developed
- Position of boundary profoundly affects system requirements
- Defining a system boundary is a **political judgment** — pressures to increase/decrease influence of different parts of an organisation

### The Context of the Mentcare System

- The Mentcare system sits within a broader health care environment
- Interacts with: patient records system, hospital administration, pharmacy systems, etc.

### Process Perspective

- Context models only show other systems, not how the system is used in that environment
- **Process models** reveal how the system is used in broader business processes
- UML activity diagrams are used to define business process models
- Example: **Process model of involuntary detention** (Mentcare) — activity diagram showing steps from assessment through detention

## Interaction Models

- **User interaction** — helps identify user requirements
- **System-to-system interaction** — highlights communication problems
- **Component interaction** — assesses if proposed structure delivers required performance and dependability
- Modelled using **use case diagrams** and **sequence diagrams**

### Use Case Modeling

- Originally developed to support requirements elicitation, now part of UML
- Each use case represents a discrete task involving external interaction with a system
- **Actors** may be people or other systems
- Represented diagrammatically (overview) and textually (detailed)

#### Transfer-Data Use Case (Mentcare System)

**MHC-PMS: Transfer data**

| Field | Value |
|---|---|
| **Actors** | Medical receptionist, patient records system (PRS) |
| **Description** | A receptionist may transfer data from the Mentcare system to a general patient record database maintained by health authority |
| **Data** | Updated personal information (address, phone number) or summary of patient's diagnosis and treatment |
| **Stimulus** | User command issued by medical receptionist |
| **Response** | Confirmation that PRS has been updated |
| **Comments** | Receptionist must have appropriate security permissions to access patient info and PRS |

#### Use Cases Involving Medical Receptionist (Mentcare)

- Includes: Transfer data, View patient information, Manage appointments, etc.

### Sequence Diagrams

- Part of UML; model interactions between actors and objects within a system
- Show the sequence of interactions during a particular use case
- Objects and actors listed along the top with a dotted line drawn vertically
- Interactions between objects indicated by annotated arrows

#### Sequence Diagram for View Patient Information

- Actor: Medical receptionist
- Objects: User interface, Patient record, Database
- Steps: Receptionist requests patient info → UI sends query → Database retrieves → Response displayed

#### Sequence Diagram for Transfer Data

- Actor: Medical receptionist
- Objects: UI, Local data, PRS (Patient Records System)
- Steps: Receptionist initiates transfer → system reads local data → sends to PRS → PRS confirms

## Structural Models

- Display organisation in terms of components and their relationships
- **Static models** — structure of system design
- **Dynamic models** — organisation during execution
- Created when discussing and designing system architecture

### Class Diagrams

- Used in object-oriented system modeling to show classes and associations
- An **object class** is a general definition of one kind of system object
- An **association** is a link between classes indicating some relationship
- During early stages, objects represent real-world entities (patient, prescription, doctor)

#### UML Classes and Association

- Represented as boxes (classes) with lines (associations) between them
- Associations labelled with names (e.g. "prescribes", "undergoes")
- Multiplicity indicators (1, *, 0..1) show how many objects participate

#### Classes and Associations in the MHC-PMS (Mentcare)

- **Patient** class — attributes: name, address, date of birth, registration date
- **Doctor** class — attributes: name, employee number, speciality
- **Consultation** class — links Patient and Doctor with date, time, notes
- **Prescription** class — links Consultation with drug, dosage, quantity
- **Treatment** class — describes treatment plan for a patient

#### The Consultation Class

- Central class connecting patient, doctor, date, and treatment details
- Attributes: consultationDate, consultationTime, notes, patientID, doctorID
- Operations (methods): getPatientHistory, prescribeDrug, recordNotes

### Generalization

- Everyday technique used to manage complexity
- Instead of learning detailed characteristics of every entity, place them in more general classes
- Allows inference that different members of a class have common characteristics

#### Generalization in System Modeling

- Examine classes for scope of generalization — if changes proposed, you don't need to check all classes
- In object-oriented languages (Java), implemented using **class inheritance**
- **Superclasses** (higher-level) define attributes and operations inherited by **subclasses** (lower-level)
- Subclasses add more specific attributes and operations
- Example: **HealthProfessional** superclass with **Doctor**, **Nurse**, **Receptionist** subclasses

### Aggregation Models

- Show how classes that are collections are composed of other classes
- Similar to **part-of** relationships in semantic data models
- Example: A **Clinic** aggregates **ConsultationRoom**, **WaitingArea**, **ReceptionDesk**

## Behavioral Models

- Models of dynamic behaviour as the system executes
- Show what happens (or is supposed to happen) when a system responds to a stimulus

### Types of Stimuli

- **Data** — some data arrives that has to be processed by the system
- **Events** — some event happens that triggers system processing (may have associated data)

### Data-driven Modeling

- Many business systems are data-processing systems driven by data input
- Controlled by data input with relatively little external event processing
- Show sequence of actions for processing input data and generating output
- Particularly useful during requirements analysis for end-to-end processing

#### Example: Activity Model of the Insulin Pump's Operation

- Blood sugar sensor reading → compute required insulin → check safety limits → deliver insulin → update display → log data

#### Example: Order Processing

- Receive order → validate → check inventory → calculate price → process payment → confirm → dispatch

### Event-driven Modeling

- Real-time systems are often event-driven with minimal data processing
- Example: landline phone switching system responds to events like **receiver off hook** by generating dial tone
- Shows how a system responds to external and internal events
- Based on assumption that a system has a finite number of states
- Events (stimuli) may cause a transition from one state to another

### State Machine Models

- Model system behaviour in response to external and internal events
- Often used for modelling real-time systems
- States as **nodes**, events as **arcs** between nodes
- When an event occurs, the system moves from one state to another
- **Statecharts** are part of UML

#### Example: Microwave Oven States

| State | Description |
|---|---|
| **Waiting** | Oven waiting for input; display shows current time |
| **Half power** | Power set to 300 watts; display shows "Half power" |
| **Full power** | Power set to 600 watts; display shows "Full power" |
| **Set time** | Cooking time set to user's input; display shows selected time |
| **Disabled** | Operation disabled for safety; interior light on; display shows "Not ready" |
| **Enabled** | Operation enabled; interior light off; display shows "Ready to cook" |
| **Operation** | Oven in operation; interior light on; timer countdown; at completion, buzzer for 5 seconds, light on, display shows "Cooking complete" |

#### Microwave Oven Stimuli

| Stimulus | Description |
|---|---|
| **Half power** | User pressed half-power button |
| **Full power** | User pressed full-power button |
| **Timer** | User pressed one of the timer buttons |
| **Number** | User pressed a numeric key |
| **Door open** | Oven door switch is not closed |
| **Door closed** | Oven door switch is closed |
| **Start** | User pressed Start button |
| **Cancel** | User pressed Cancel button |

## Model-Driven Engineering (MDE)

- Approach where **models** (not programs) are the principal outputs of development
- Programs that execute on hardware/software platform are generated automatically from models
- Raises the level of abstraction — engineers no longer concerned with programming language details or platform specifics

### Usage of MDE

- Still at an early stage of development; unclear if it will significantly affect practice
- **Pros:**
  - Systems considered at higher levels of abstraction
  - Automatic code generation makes it cheaper to adapt systems to new platforms
- **Cons:**
  - Models for abstraction may not be right for implementation
  - Savings from code generation may be outweighed by costs of developing translators for new platforms

### Model-Driven Architecture (MDA)

- Precursor of more general MDE
- Model-focused approach using a subset of UML models
- Models at different levels of abstraction created; from a high-level platform-independent model, a working program can (in principle) be generated without manual intervention

### Types of Model in MDA

- **Computation Independent Model (CIM)** — models important domain abstractions; sometimes called **domain models**
- **Platform Independent Model (PIM)** — models operation of the system without reference to implementation; uses UML to show static structure and event responses
- **Platform Specific Models (PSM)** — transformations of the PIM for each application platform; may have layers adding more detail

### MDA Transformations

- Transformations are applied to convert CIM → PIM → PSM → code
- May require specialised tools for each level of transformation

### Multiple Platform-Specific Models

- A single PIM can generate multiple PSMs for different platforms (Java, .NET, etc.)
- Each PSM adds platform-specific detail

### Agile Methods and MDA

- MDA claims to support iterative development for agile methods
- Extensive up-front modelling contradicts agile manifesto principles
- However, if transformations are fully automated and code generated from PIM, MDA could work in agile — no separate coding required

### Adoption Limitations of MDA/MDE

- Specialised tool support required to convert models between levels
- Limited tool availability; organisations may require adaptation and customisation
- Companies reluctant to develop their own tools or rely on small vendors for long-lifetime systems
- Abstractions useful for discussion may not be the right abstractions for implementation
- For most complex systems, implementation is not the major problem — RE, security, dependability, integration with legacy systems, and testing are more significant
- Platform-independence arguments only valid for large, long-lifetime systems
- For software products and information systems, MDA savings likely outweighed by introduction and tooling costs
- Widespread adoption of agile methods has diverted attention from model-driven approaches

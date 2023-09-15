# Architecture description

## Introduction and Goals

## Business context and goal

In the ever-evolving landscape of travel, we as new player comes – a dynamic startup that stands apart from the affiliations of traditional travel agencies.

### Vision

Our mission? To pioneer the next generation of online trip management dashboard, empowering travelers to take charge of their journeys like never before. We envision a world where your travel experiences are seamlessly organized, accessible at your fingertips, and tailored to your preferences.

Introducing the Road Warrior Dashboard – a user-friendly interface designed to revolutionize the way you manage your trips. Whether you're at your computer or on the go with your mobile device, we've got you covered.

### Key Features

Seamless Trip Organization: Say goodbye to the chaos of scattered reservations. With our dashboard, all your travel arrangements are neatly organized by trip, allowing you to have a clear overview of your entire journey.

Web and Mobile Accessibility: Your travel plans should be accessible wherever you are. Our platform is optimized for both web browsers and mobile devices, ensuring that you have the information you need at your fingertips, whether you're at your desk or on the move.

Route Change Tracking: We understand that travel plans can be subject to unexpected changes. Our dashboard keeps you informed about any alterations to your routes, ensuring that you're always up to date and prepared for any adjustments.

Integration with Airlines, Hotels, and Car Rentals: The Road Warrior Dashboard isn't just an isolated tool – it's your gateway to the travel ecosystem. We're seamlessly integrated with most major airlines, hotel chains, and car rental agencies, making it effortless to manage all aspects of your journey in one place.


## Requirements Overview

### Functional Requiremens

Functional requirements are derived from input given by the stakeholders documented there [input](input.md).

| # | Requirement |
|---|-------------|
| FR1   | Road Warrior is system built and managed by a start up                                                                                                       |
| FR2   | Poll email looking for travel-related emails                                                                                                                 |
| FR3   | Filter and whitelist certain emails                                                                                                                          |
| FR4   | The system must interface with the agency’s existing airline, hotel, and car rental interface system to update travel details (delays, cancellations, etc.) |
| FR5   | Customers should be able to add, update, or delete existing reservations manually as well                                                                    |
| FR6   | Items in the dashboard should be able to be grouped by trip, and once the trip is complete, the items should automatically be removed from the dashboard     |
| FR7   | Users should also be able to share their trip information by interfacing with standard social media sites or allowing targeted people to view your trip      |
| FR8   | Richest user interface possible across all deployment platforms                                                                                              |
| FR9   | Provide end-of-year summary reports for users with a wide range of metrics about their travel usage                                                         |
| FR10  | Road Warrior gathers analytical data from users trips for various purposes - travel trends, locations, airline and hotel vendor preferences, etc.           |
| FR11  | Customers must be able to use the system through web and mobile apps                                                                                         |
| FR12  | Must integrate with preferred travel agency for quick problem resolution (help me!)                                                                         |

### Technical requirements

Technical requirements are derived from input given by the stakeholders documented there [input](input.md)

| #     | Technical Requirement                                                                                          |
|-------|---------------------------------------------------------------------------------------------------------------|
| TR1   | Must integrate seamlessly with existing travel systems (i.e, SABRE, APOLLO)                                    |
| TR2   | 2 million active users/week                                                                                    |
| TR3   | Total users: 15 million (user accounts)                                                                       |
| TR4   | Users must be able to access the system at all times (max 5 minutes per month of unplanned downtime)          |
| TR5   | Travel updates must be presented in the app within 5 minutes of generation by the source                       |
| TR6   | Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec)                           |
| TR7   | Must work internationally                                                                                      |

### Non Functional

Non functional requirements are derived from functional and technical requirements

- **[NFR1]** Availability
  - 99.99% ("four nines") 4.38 minutes/month <- **[TR4]**
- **[NFR2]** Scalability/Elasticity  
  - 2 million active users/week <- **[TR2]**
  - total users: 15 million (user accounts) <- **[TR3]**
- **[NFR3]** Performance
  - Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec) <- **[TR6]**
  - Travel updates must be presented in the app within 5 minutes of generation by the source <- **[TR5]**
- **[NFR4]** Consistency
  - Travel updates must be presented in the app within 5 minutes of generation by the source <- **[TR5]**
  - Once the trip is complete, the items should automatically be removed from the dashboard <- **[FR5],[FR6]**
  - End Year report must be consistent with active and inactive trips <- **[FR9]**
  - Analytical data must be consistent with operational data <- **[FR10]**
- **[NFR5]** Cost
  - system must by cost efficient <- **[FR1]**
- **[NFR6]** Evolvability
  - adding an new integration must be efficient <- **[TR1],[FR4],[FR12]**
  - adding new region must be efficient <- **[TR7]**
  - adding new features to ui must be efficient <- **[FR1],[FR8],[FR11]**
  - adding new import source for trips or trip parts must be efficient <- **[FR2],[FR3]** //we do not believe that the majority of the users will accept access to their emails, and assume that this requirement will evolve
  - adding new social media sharing functionality must be efficient <- **[FR7]**
  - changing data structure of the analytical data should be efficient <- **[FR10]**
- **[NFR7]** Useability
  - all capabilities of a device should be useable for best user experience <- **[FR8]**

### Requirements matrix

| FR/TR  | Availability | Scalability | Performance | Consistency | Cost | Evolvability | Useability |
| ------ | ------------ | ----------- | ----------- | ----------- | ---- | ------------ | ---------- |
| [FR1]  |              |             |             |             | x    | x            |            |
| [FR2]  |              |             |             |             |      | x            |            |
| [FR3]  |              |             |             |             |      | x            |            |
| [FR4]  |              |             |             |             |      | x            |            |
| [FR5]  |              |             |             | x           |      |              |            |
| [FR6]  |              |             |             | x           |      |              |            |
| [FR7]  |              |             |             |             |      | x            |            |
| [FR8]  |              |             |             |             |      | x            | x          |
| [FR9]  |              |             |             | x           |      |              |            |
| [FR10] |              |             |             | x           |      | x            |            |
| [FR11] |              |             |             |             |      | x            |            |
| [FR12] |              |             |             |             |      | x            |            |
| [TR1]  |              |             |             |             |      | x            |            |
| [TR2]  |              | x           |             |             |      |              |            |
| [TR3]  |              | x           |             |             |      |              |            |
| [TR4]  | x            |             |             |             |      |              |            |
| [TR5]  |              |             |             | x           |      |              |            |
| [TR6]  |              |             | x           |             |      |              |            |
| [TR7]  |              |             |             |             |      | x            |            |

## Quality Goals

## Stakeholders

 | Name            | Role                               |
 | --------------- | ---------------------------------- |
 | *Neal Ford*     | Architecture Kata 2023 Jury Member |
 | *Mark Richards* | Architecture Kata 2023 Jury Member |
 | *Jacqui Read*   | Architecture Kata 2023 Jury Member |
 | *Clare Sudbery* | Architecture Kata 2023 Jury Member |
 | *Robin Losey*   | Architecture Kata 2023 Jury Member |

## Architecture Constraints

For a startup in a greenfield development scenario, there are minimal limitations on technology choices. However, the solution space is constrained by the specific [Technical Requirements](#technical-requirements) outlined by the stakeholders. These technical requirements serve as the primary guiding constraints for the project's architecture and technology decisions.

## System Scope and Context

### Business Context

The Road Warrior platform serves various actors, including Travellers, External Persons, Analysts, Travel Systems, and the System itself. Travellers can log in, register, view their dashboard, manage reservations and trips, share trips on social media, provide access to external people, view end-of-year reports, configure email settings, and contact the "HelpMe!" agency for support. External Persons can access shared trip information, while Analysts access analytical reports. Travel Systems update travel data, and the System performs tasks such as polling emails, sending notifications, and collecting analytical data for end-of-year reports and analysis.

#### Actors overview

| Actor           | Description                                                                                                                                                     | Use Case Reference                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Traveller       | Private or Business user using Road Warrior to manage his trips.                                                                                                | UC01, UC02, UC03, UC04, UC05, UC06, UC07, UC08, UC09, UC10 |
| External Person | A person having access to a trip, which is shared by Traveller.                                                                                                 | UC11                                                       |
| Anaylst         | Business user accessing analytical data.                                                                                                                        | UC01, UC12                                                 |
| Travel System   | System Actor to deliver information on changes on reservations. It includes Travel systems like APOLLO as well as dedicated Airline/Hotels/Car rental agencies. | U14                                                        |
| Supporting agency| User selected agency for support and resolve issues. ("HelpMe! agency)                                                           													    | U10, U19                                                   |
| System          | Some activities are initiated by the system.                                                                                                                    | UC15, UC16, UC18                                           |

#### Use case overview

| #    | Use Case                                | Short Description                                                                                                     | Actor              | Requirement |
| ---- | --------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------ | ----------- |
| UC01 | Login in system                         | User logs into the system.                                                                                            | Traveller, Analyst |             |
| UC02 | Register in system                      | Traveller registers as a new user to system.                                                                          | Traveller          |             |
| UC03 | View dashboard                          | Traveller gets an overview of his trips.                                                                              | Traveller          | FR6         |
| UC04 | Manage reservations                     | Traveller add, edit removes reservations manually.                                                                    | Traveller          | FR6         |
| UC05 | Manage trip                             | Traveller creates trips, add new reservation to it, etc.                                                              | Traveller          | FR6         |
| UC06 | Share trip via social networks          | Traveller transfers his trip to social media.                                                                         | Traveller          | FR7         |
| UC07 | Provide access to external people       | Traveller gives a direct link to a person to view his trip.                                                           | Traveller          | FR7         |
| UC08 | Access end-of-year report               | Traveller view the result of the yearly report on his trips.                                                          | Traveller          | FR9         |
| UC09 | Define filter and whitelist for email   | Traveller configures the email poll, including the filter and whitelisting.                                           | Traveller          | FR3         |
| UC10 | Contact with "HelpMe!" Agency           | Traveller contact with agency for resoving issues.                                                                    | Traveller, Supporting agency          | FR12        |
| UC11 | Access to shared trip information       | External Person view a trip of a Traveller.                                                                           | External Person    | FR7         |
| UC12 | Access to analytic reports              | Analyst views analytic reports from the system.                                                                       | Analyst            | FR10        |
| UC14 | Update travel data                      | System updates the received data for a reservation.                                                                   | Travel System      | FR4         |
| UC15 | Poll emails                             | System polls email system of traveller.                                                                               | System             | FR2         |
| UC16 | Push notification about changes in trip | System pushes the information received from email, Travel system, etc. towards the traveller.                         | System             | FR4         |
| UC18 | Collect analytical data                 | System collect information from all Travellers for later analytical work on it and for preparation end-of-year report | System             | FR10        |
| UC19 | Configure "HelpMe!" Agency              | Traveller able to choose agency for support him in issues                                                             | Traveller          | FR12        |

### Technical Context (C4-Level1)

This chapter corresponds to C4 Model Level 1 [System Context diagram](https://c4model.com/#SystemContextDiagram). 
It describes the system as a blackbox concentrating on the external dependencies.

![Context Diagram](diagrams/Context.drawio.svg)

## Solution Strategy

The solution strategy for the Road Warrior Travel Management Dashboard focuses on simplifying integration with external systems, prioritizing core features for the MVP, and leveraging cloud services for cost-effectiveness. By adopting Agile development methodologies, the project aims to ensure iterative progress, flexibility, and improved collaboration between the team and stakeholders. This approach balances efficient development with adaptability, allowing the platform to deliver a seamless and user-friendly experience for managing travel plans.

1. **Implement email forwarding functionality** instead of direct integration with Email Providers. Users can forward their travel-related emails to a specific email address provided by the platform. This will simplify the initial development and reduce the complexity of integrating with various email providers.

2. **Utilize public Identity Providers (IDPs) for user authentication** (as per ADR2). This will allow users to log in using popular services like Google or Facebook, reducing the need for a custom authentication system and simplifying the onboarding process.

3. **Exclude analytics and reporting features from the MVP scope**. Focus on the core functionality of trip organization and management, which will allow for faster development and testing of the essential features of the platform.

4. **Integrate only with Travel Systems** (such as SABRE, APOLLO) for retrieving travel information, and skip direct integration with hotels, car rentals, and airlines. This will streamline the development process and allow the platform to focus on a single integration point for travel data.

5. **Leverage native services in the public cloud (XaaS)** instead of building custom solutions. Utilize cloud-based infrastructure, databases, and other services to reduce development time, maintenance efforts, and costs.

6. **Research and adopt industry standards and best practices** for each component of the platform. This will ensure a high level of interoperability, reliability, and maintainability of the system.

7. **Adopt Agile development methodologies** to ensure iterative progress, flexibility, and better collaboration between the development team and stakeholders. Implement practices such as product backlog management, sprints, daily stand-ups, continuous integration, code reviews, testing, and sprint retrospectives to continuously refine the project based on feedback and learnings from each sprint.

## Building Block View

## Whitebox Overall System (C4-Level2)

This aligns with Level 2 of the C4 Model, specifically the [Container diagram](https://c4model.com/#ContainerDiagram). This diagram provides an internal view of the system, focusing on its components and their interactions with external systems. In our system, we equate containers with domains, and both terms are used interchangeably.

![Container Diagram](diagrams/Container.drawio.svg)

### Motivation

In the context of our architecture, the decision to split our solution into several domains stems from a fundamental understanding of the necessary functionality and a keen consideration of various non-functional requirements. By dissecting our system into distinct domains and components, we embark on a journey to achieve greater flexibility and efficiency in our development process.

### Function analyses

In our pursuit of an optimized and well-structured solution, we turn our attention to the deliberate division of functionality, specifically the distribution of Use Cases across our distinct domains.

By meticulously organizing an independent set of Use Cases within each domain, we not only foster a more agile and self-contained development process but also reduce the inherent complexities associated with interdependencies

In more formal terminology, this strategic approach directly contributes to the enhancement of 'Loose coupling' and 'Cohesion' within our system, reinforcing the foundational principles that guide our architectural choices
| Domain               | Use Case Reference                                                                                                | Use Cases name                                                                                                                                                                                                                                                                                                                                                                 |
| -------------------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Analytic domain      | UC08 <br> UC12 <br> UC18 <br>                                                                                        | Access end-of-year report <br> Access to analytic reports <br> Collect analytical data                                                                                                                                                                                                                                                                                         |
| User settings domain | UC09 <br> UC19                                                                                                    | Define filter and whitelist for email <br>   Configure "HelpMe!" Agency                                                                                                                                                                                                                                                                                                                                       |
| Channel              | UC01 <br> UC02 <br> UC03 <br> UC04 <br> UC05 <br> UC06 <br> UC07 <br> UC08 <br> UC09<br> UC10<br> UC11 <br> UC12 <br> UC16 | Login in system <br> Register in system <br> View dashboard <br> Manage reservations <br> Manage trip	<br> Share trip via social networks <br> Provide access to external people <br> Access end-of-year report  <br>  Define filter and whitelist for email <br> Contact with "HelpMe!" Agency <br> Access to shared trip information <br> Access to analytic reports	<br> Push notification about changes in trip |
| Trip organizer       | UC03 <br> UC04 <br> UC05 <br> UC14 <br> UC16                                                                      | View dashboard <br> Manage reservations	<br> Manage trip	<br> Push notification about changes in trip                                                                                                                                                                                                                                                                          |
| IAM domain           | UC01 <br> UC02                                                                                                    | Login in system<br> Register in system                                                                                                                                                                                                                                                                                                                                         |
| Integration domain   | UC14 <br> UC15 <br> UC16                                                                                          | Update travel data	<br> Poll emails	<br> Push notification about changes in trip                                                                                                                                                                                                                                                                                               |

*Remark: In "Channel domain" we mentioned list of Use cases, but only UI part of these US is related to Channel domain._

Usecase vs domains tracebility:
| #    | Use Case                                | Analytic | User settings | Channel | Trip organizer | IAM | Integration |
| ---- | --------------------------------------- | -------- | ------------- | ------- | -------------- | --- | ----------- |
| UC01 | Login in system                         |          |               | X       |                | X   |
| UC02 | Register in system                      |          |               | X       |                | X   |
| UC03 | View dashboard                          |          |               | X       | X              |     |
| UC04 | Manage reservations                     |          |               | X       | X              |     |
| UC05 | Manage trip                             |          |               | X       | X              |     |
| UC06 | Share trip via social networks          |          |               | X       |                |     |
| UC07 | Provide access to external people       |          |               | X       |                |     |
| UC08 | Access end-of-year report               | X        |               | X       |                |     |
| UC09 | Define filter and whitelist for email   |          | X             | X       |                |     |
| UC10 | Contact with "HelpMe!" Agency           |          |               | X       |                |     |
| UC11 | Access to shared trip information       |          |               | X       |                |     |
| UC12 | Access to analytic reports              | X        |               |         |                |     |
| UC14 | Update travel data                      |          |               |         | X              |     | X
| UC15 | Poll emails                             |          |               |         |                |     | X
| UC16 | Push notification about changes in trip |          |               | X       | X              |     | X
| UC18 | Collect analytical data                 | X        |               |         |                |     |
| UC19 | Configure "HelpMe!" Agency              |          |  X            | X       |                |     |

As you can see in table: we have very high independent domains.

*Remark: In "Channel domain" we mentioned list of Use cases, but only UI part of these US is related to Channel domain._

### Architecture characteristics

Even all Architecture characteristics should be taking in account when we design and implement domains, some of Architecture characteristics played more important role and influence significantly on component design and deployment.

| Architecture characteristics | Analytic | User settings | Channel | Trip organizer | IAM    | Integration |
| ------------------ | -------- | ------------- | ------- | -------------- | ------ | ----------- |
| availability       | medium   | medium        | high    | high           | high   | high        |
| compatibility      | high     | low           | low     | low            | high   | high        |
| evolvability       | high     | low           | High    | high           | low    | medium      |
| localizability     | low      | low           | high    | high           | low    | medium      |
| testability        | low      | low           | high    | high           | medium | medium      |
| traceability       | high     | low           | low     | medium         | high   | high        |

Based on this analyses we can see that all domains has different Architecture characteristics and as result we are not able to combine them.

### Strategic Design

Category    | Domain                   | Explanation
--------    | ------------------------------------ | -----------
Core        | Channel <br> Trip organizer <br> Integration domain  | A core domain makes an organization unique and different from others. An organization cannot succeed (or even exist) without being exceptionally good in its core domain. Because the core domain is so important, it should receive the highest priority, the biggest effort, and the best developers. 
Generic     | Analytic domain <br> Integration domain           | Generic domain is a domain that does not contain anything special to the organization but is still needed for the overall solution to work.We can tryi to use off-the-shelf software for your generic subdomains in order to save of time and work.
Supportive  | User Settings 			            | A supporting domain is a domain that is necessary for succeed, but it does not fall into the core domain category. It is not generic either because it still requires some level of specialization for the organization in question. We can start with an existing solution and tweak it or extend it to your specific needs.

### Contained Building Blocks

This chapter provides an overview of the different domains that compose the Road Warrior system. Each subchapter describes a domain, its responsibilities, interfaces with other domains, and the rationale behind its existence.

#### Analytics domain

**What the domain does:**

The Analytic domain is responsible for collecting data for reports, creating reports, and providing access to reports. This domain handles persistent data like raw analytical data and generated reports.

**Interfaces:**

- Delivers end-of-year reports by dashboard (Like FE the Dashboard is API driven as well and allows further automation on behalf of the end customer)
- Receives notifications directly from the Trip Organizer domain
- Extracts data from the Trip Organizer domain to collect information about trips and reservations over time

**Why we have the domain:**

This domain is separated from others because it serves for a data driven business model. Non-functional requirements for this domain are unclear at the beginning of the project. Espicially information needs might evolve and requires additional Analytical and ML capabilities.

**Information needs:**

Currently there are no clear requirments on information needs for this domain. Ideation: [First scetch of information model](analytic-information-model.md).

#### User Settings domain

**What the domain does:**

The User settings domain manages the configuration of mailboxes for polling, as well as filter and whitelist definitions.

**Interfaces:**

- Users can change configuration for whitelists, filters, and mailboxes via the Channel domain
- The Integration domain uses the configuration from the Configuration domain

**Why we have the domain:**

This domain is relatively simple and does not require high performance or many changes during project evolution.

#### Trip Organizer Domain

**What the domain does:**

The Trip Organizer domain allows users to manage their trips, create new ones, delete trips, and add reservations. Data is ingested from the Integration domain.

**Interfaces:**

- The Integration domain sends all notifications about changes in reservations to the Trip Organizer to maintain up-to-date information in the trip repository
- The Trip Organizer sends notifications about changes in reservations to the Channel domain for delivery to end-users
- The Trip Organizer domain provides an API for client applications (Channel domain) to access information about trips and reservations
- The Trip Organizer reads detailed data about reservations via the Integration domain from Travel systems and Agencies
- The Trip Organizer provides data to the Analytic domain about trips and reservations

**Why we have the domain:**

This domain is the core of the business and differentiates the platform from competitors. It requires high evolvability and dedicated security due to the storage of customer data.

#### Channels Domain

**What the domain does:**

The Channel domain is responsible for providing user interfaces, such as web applications and mobile applications.

**Interfaces:**

- Receives all notifications about changes in reservations from the Trip Organizer and updates content in user interfaces
- Uses the API of the Trip Organizer to access information about trips and reservations
- Uses IAM for user registration and login (token exchange)
- Receives end-of-year reports from the Analytic domain
- Provides configuration to the User Settings domain

**Why we have the domain:**

This domain represents the "face" of the platform to end-users and requires high quality (testability) and evolvability. It is critical from a UX perspective and is expected to undergo many changes that need to be delivered to users quickly.

#### IAM Domain

**What the domain does:**

The IAM domain covers all aspects of user registration, authentication, and authorization.

**Interfaces:**

- Manages registration and login processes for the Channel domain (token exchange)
- Validates tokens for Channel, Analytic, and Trip Organizer domains (not shown in the diagram)

**Why we have the domain:**

It is a standard pattern to have IAM as a separate domain since it is well-developed and independent of the project's business specifics. It typically allows for the reuse of existing out-of-the-box solutions with minimal customization and configuration.

#### Integration Domain

**What the domain does:**

The Integration domain provides capabilities for collecting information from external sources like email inboxes, external travel systems, and agencies.

**Interfaces:**

- Sends notifications directly to the Analytic domain for updated information and analysis of agency behavior
- Uses configuration from the Configuration domain
- Provides detailed data about reservations from Travel systems and agencies to the Trip Organizer domain
- Sends notifications directly to the Trip Organizer domain to update reservations and inform users

**Why we have the domain:**

This domain serves as the gateway to the external travel world, organizing all integrations in a similar way to reduce data model alignment in other domains. It is expected to experience high loads due to the addition of new reservations and the need to request details about these reservations from external partners. Additionally, all active reservations (in active trips) can receive updates via Travel systems, emails, or from agencies.

## Whitebox view on each Domain (C4-Level3)

This corresponds to C4 Model Level 3 [Component diagram](https://c4model.com/#ComponentDiagram). 
It describes each container/domain as a whitebox concentrating on the components inside container/domain and their dependencies to other containers/domains.

### Channels Domain (C4-Level3)

In our system, the user interface (UI) serves as one of the channels to interact with users. As per the requirements, we have identified three explicit channels for this interface:

- **Web**
- **iOS**
- **Android**

Importantly, we've designed our system to be flexible and modular. Adding a new channel, such as car entertainment, should be a local change within this domain and does not impact other domains.

To ensure the effectiveness of our UI channels and to maintain architectural coherence, we've made three significant architecture decisions with a primary focus on this domain:

1. [**ADR 2 User Onboarding and Authentication Strategy**](adrs/adrs02-authentication.md): This decision addresses the strategy for user onboarding and authentication within our UI channels.

2. [**ADR 3 How to share trips**](adrs/adr03-SharingTrip.md): This decision outlines how trip-sharing functionality is implemented and integrated into our UI.

3. [**ADR 4 Frontend Technology**](adrs/adr04-FrontendTechnology): This decision pertains to the selection of frontend technologies to be used in developing our UI channels.

These decisions should reduce costs and time to market by following best ptractices as "stateful web url", "3rd party login" and open protocols as OpenID connect.

<img src="diagrams/Component-Channels.drawio.svg">

### IAM Domain (C4-Level3)

The Identity and Access Management (IAM) domain plays a pivotal role in our architecture, serving as a foundational and supportive element relevant to all other domains. Due to its high degree of harmonization and well-established principles, IAM becomes an invaluable resource that can be harnessed by public providers.

One notable addition to our IAM framework is the integration of Zero Trust principles. Zero Trust represents a paradigm shift in authorization, moving from a perimeter-based model to a more granular approach. In this model, authorization is extended to each individual component within the system.

Our implementation of Zero Trust is bolstered by the presence of an internal Identity Provider (IDP). This IDP serves as a crucial mechanism, enabling us to decouple each component from potential changes made by third-party Identity Providers (IDPs). 

For further details on our security concept, including the Zero Trust implementation, please refer to the [Security Concept](architecture.md#security) chapter.

The following architectural decision is particularly relevant to the IAM domain:

- [**ADR 2 User Onboarding and Authentication Strategy**](adrs/adrs02-authentication.md)

This decision forms a key component of our strategy within the IAM domain, addressing user onboarding and authentication, which are fundamental aspects of identity and access management.

<img src="diagrams/Component-IAM.drawio.svg">

### Trip Organizer Domain (C4-Level3)

The Trip Organizer domain allows users to manage their trips, create new ones, delete trips, and add reservations. Data is ingested from the Integration domain.
Following diagram represent components which involved in this domain.

<img src="diagrams/Component-TripOrganizer.drawio.svg">

**Purpose/Responsibility**:

Reservation Manager component - Reservation Manager received notifications are from Travel Systems/Agencies or email inboxes, 
which are subsequently used to update the internal database with the latest reservation information. 
If these updates are deemed significant for the user, notifications are then dispatched via the Channel Notification component. 
In cases where reservations are manually created or generated via email, the Reservation Manager has the capability to request 
supplementary reservation details from Travel Systems or Agencies. Additionally, channels have the ability to request reservation information via REST API.

Trip Manager component - The Trip Manager facilitates users in performing Create, Read, Update, and Delete (CRUD) operations on trip entities and establishes associations between trips and reservations.

Channel notification - Technical component which distribute notification from Reservation manager to Channel domain.

**Interface(s)**:

Trip organizer provide following interfaces:

- REST interface for Channel domain for manage reservations
- REST interface for Channel domain for manage trips
- Message interface for Channel domain for inform user about reservation changes
- DB access for Analytic domain for collection metrics

Trip organizer consume following interfaces:

- REST interface form Integration domain for reading details about reservation
- Message interface from Integration domain to recive changes in reservation

**Quality/Performance Characteristics**

Following quality attributes are important for components in this domain:

- availability - 99.99
- evolvability - because we need to change our system very fast if our hypotises are wrong
- security - this component has user personal data (as a part of reservations) and need follow regulator rules (GDRP for exmaple)
- testability - as we expect a lot of changes in these components then we should have good test automatization and transparency on test coverage.
- localizability - as we work intenationally we need to support different localization for users and for reservations

**This domain covers following Use Cases**:

- UC03 View dashboard
- UC04 Manage reservations
- UC05 Manage trip
- UC14 Update travel data
- UC16 Push notification about changes in trip

### Integration Domain (C4-Level3)

<img src="diagrams/Component-Integration.drawio.svg">

**Purpose/Responsibility**:

Notification - The technical component receives data pushes from integration components and generates notifications for the Analytic and Trip Organizer domains.

Integration router - This component supports the logic for determining the appropriate integration method to obtain detailed reservation information and harmonizes the data model across various data sources.

Travel system integration - This component facilitates the integration with Travel Systems. During the detailed design phase, it is anticipated that this component will be subdivided to accommodate each specific Travel System, such as APOLLO and SABRE.

Airlines integrations - This component is designed to facilitate integration with multiple airline systems through the utilization of standard APIs

Car rental integrations - This component is designed to facilitate integration with multiple Car rental systems through the utilization of standard APIs

Hotel integrations - This component is designed to facilitate integration with multiple Hotel (PMS) systems through the utilization of standard APIs

Email reader - This component possesses the capability to access user mailboxes through standard protocols, notably SMTP. It undertakes the task of filtering incoming emails and extracting reservation-related information. It is envisaged that, in the detailed design phase, this component will be further subdivided into 'Mailbox Reader' and 'Email Parser' components.

**Interface(s)**:

Integration domain consume one interface from User Setting domain - configuration for user mailboxes, filters and whitelists.

Integration domain provide following interfaces:

- Message interface for notify Analytic and Travel Organizer domains about reservation changes.
- JSON interface for collect detailed information about reservations.

**Quality/Performance Characteristics**:

Following quality attributes are important for components in this domain:

- availability - 99.99%
- compatibility - we need to follow SABRE, Appolo and standard agency interfaces.
- tracebility - we need to be able to understand which message and when goes from which source.

**This domain covers following Use Cases**:

- UC14 Update travel data
- UC15 Poll emails
- UC16 Push notification about changes in trip

### User Settings (C4-Level3)

<img src="diagrams/Component-UserSetting.drawio.svg">

**Purpose/Responsibility**

Mailbox setting, Filters and Whitelists settings, Supporting agency settings - allow to manage user specific settings.

**Interface(s)**

User Settings domain provide one interface which user by 
* Channels domain - CRUD operations on settings
* Integration domain - reading configuration for mailboxes, filters and whitelists.

**This domain covers following Use Cases**
* UC09 Define filter and whitelist for email
* UC19 Configure "HelpMe!" Agency (Supporting agency)

### Aanlytics Domain (C4-Level3)

The analytical domain is responsible for collecting data for reports, creating reports, and providing access to reports. This domain handles persistent data like raw analytical data and generated reports.

![Component Overview](diagrams/Analytics-logical.drawio.svg)

In order to focus on business development and fast time to market, we decided to start with a lean serverless approach that reduces the effort for infrastructure management and maintenance to a minimum (see [Rationale for Analytics components](adrs/adr05-analytics-make-or-buy.md)). In essence, a serverless data warehouse abstracts away the complexities of infrastructure and management, allowing Road warrior to focus on deriving insights from their data. It offers a combination of flexibility, scalability, and cost-effectiveness that is start of the art in the market. This approach allows us to focus on the core business and to scale the system easily.  

Separatoin of concern: User will have access to reports through Dashboard Frontend (Looker), which an optional API acces ([Looker API](https://developers.looker.com/api/overview/)).

For the sake of security and consitency users do no have direct access to the storgage layer (GCS). All data handling is done by the serverless components which are authorized by Service Users only.

Uploads from the Trip Organizer domain are done via File upload to GCS. The data is then processed and upladed by a serverless dockerized Knative component (Cloud Run) and stored in BigQuery. Automated scheduling and orchestration is done by Cloud Scheduler or DataFlow (based upon APACHE Airflow).

Interface(s) for the start:

- Federated Query from BigQuery: can directly query data stored in Cloud SQL using federated queries. The queries can be scheduled for periodical updates.
- File Interface: Data which are acquired by Trip organizer are pushed on GCS object store. 

**This domain covers following Use Cases**:

- UC08 Access end-of-year report
- UC12 Access to analytic reports
- UC18 Collect analytical data

## Runtime View

### \<Runtime Scenario authentication >

Following flow describes the authentication process with 3rd party Identity Provider (IDP)
Corresponding architecture decision record is [ADR 2 User Onboarding and Authentication Strategy](adrs/adrs02-authentication.md)

![Authentication Flow](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/wschaef/architecture-kata-2023/main/diagrams/authentication.puml)

## Deployment View

<img src="diagrams/Deployment.drawio.svg">

## Cross-cutting Concepts

### *Security*

In our security strategy for the "Road Warrior" system, we implement multiple layers of defense to ensure a robust and secure operation.

#### First Level of Defense

At the first level of defense, we rely on cloud-native offerings to enhance the security of our system:

- **Cloud Armor**: We use Cloud Armor as a web application firewall (WAF) to defend against Distributed Denial of Service (DDOS) attacks and reduce the risk associated with the OWASP Top Ten vulnerabilities.

- **Virtual Private Cloud (VPC)**: We leverage VPC to create a private network environment and implement network firewalls that require explicit configuration for each external connection. This approach enhances control and security.

#### Second Level of Defense

Building upon the first level of defense, we introduce custom security measures:

- **Internal Identity Provider (IDP)**: We implement an internal IDP to convert every token received from third-party IDPs into an internal token format. All internal servers are required to verify these internal tokens, rejecting any that are not valid.

#### Zero Trust Concept

Our security strategy aligns with the "Zero Trust" concept by:

- Designing trust explicitly: We do not assume trust by default but establish trust through verified mechanisms.

- Reducing the risk of lateral movement: With our internal IDP and token verification, we limit the potential for unauthorized access and lateral movement within the system.

In the diagram below, you can see a high-level view of the explicit trust relationships within our system:

<img src="diagrams/Security.drawio.svg">

This multi-layered approach to security ensures the protection of our "Road Warrior" system from various threats and vulnerabilities.

## Architecture Decisions

- [ADR 1 Architecture Style](adrs/adr01-ArchitectureStyle.md)
- [ADR 2 User Onboarding and Authentication Strategy](adrs/adrs02-authentication.md)
- [ADR 3 How to share share trips](adrs/adr03-SharingTrip.md)
- [ADR 4 Frontend technology](adrs/adr04-FrontendTechnology)
- [ADR 5 Backend technology](adrs/adr05-analytics-make-or-buy.md)

## Risks and Technical Debts

We see following risks:

**Risk: Requesting Email Access**

Requesting access to users' emails, whether granted to all or none, poses significant data privacy challenges. This can potentially lead to unintended exposure of sensitive information and raise concerns about user privacy.

**Risk: Diversity in Interface Integration**

Integrating interfaces from various entities like hotels, car agencies, and airlines directly can introduce complexities and costs. This approach may hinder system evolution and maintenance, potentially leading to increased expenses and limited adaptability.

## Glossary

| Term             | Definition                                                                                                                                                       |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| *Trip*           | *\<definition-1>*                                                                                                                                                |
| *Reservation*    | *\<definition-2>*                                                                                                                                                |
| *Booking*        | *\<definition-2>*                                                                                                                                                |
| *Travel angency* | *\<definition-2>*                                                                                                                                                |
| *ADR*            | *ADR stands for "Architecture Decision Record." It is a document that captures important architectural decisions made during the software development process.* |
| *NFR*            | *NFR stands for non functional requirements, derived from input given by the stakeholders*                                                                       |
| *IDP*            | *Identity Provider is a system managing identities of users and provides authentication through protocol like OpenId Connect*                                    |
| *BFF*            | *Backend for Frontend is a server responsible to provide data for a frontend line a mobile app or web app*                                                       |

## References

- Arc42 Template Created, maintained and © by Dr. Peter Hruschka, Dr. Gernot Starke and
contributors. See <https://arc42.org>.

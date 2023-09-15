# Introduction and Goals

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

Functional requirements are derived from input given by the stakeholders documented there [input](input.md)

- **[FR1]** - Road Warrior is system built and managed by a start up
- **[FR2]** - Poll email looking for travel-related emails
- **[FR3]** - Filter and whitelist certain emails
- **[FR4]** - The system must interface with the agency’s existing airline, hotel, and car rental interface system to update travel details (delays, cancellations, updates, gate changes, etc.).
- **[FR5]** - Customers should be able to add, update, or delete existing reservations manually as well.
- **[FR6]** - Items in the dashboard should be able to be grouped by trip, and once the trip is complete, the items should automatically be removed from the dashboard.
- **[FR7]** - Users should also be able to share their trip information by interfacing with standard social media sites or allowing targeted people to view your trip.
- **[FR8]** - Richest user interface possible across all deployment platforms
- **[FR9]** - Provide end-of-year summary reports for users with a wide range of metrics about their travel usage
- **[FR10]** - Road Warrior gathers analytical data from users trips for various purposes - travel trends, locations, airline and hotel vendor preferences, cancellation and update frequency, and so on.
- **[FR11]** - Customers must be able to use the system through web and mobile apps
- **[FR12]** - Must integrate with preferred travel agency for quick problem resolution (help me!)

### Technical requirements

Technical requirements are derived from input given by the stakeholders documented there [input](input.md)

- **[TR1]** - must integrate seamlessly with existing travel systems (i.e, SABRE, APOLLO)
- **[TR2]** - 2 million active users/week
- **[TR3]** - total users: 15 million (user accounts)
- **[TR4]** - Users must be able to access the system at all times (max 5 minutes per month of unplanned downtime)
- **[TR5]** - Travel updates must be presented in the app within 5 minutes of generation by the source
- **[TR6]** - Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec)
- **[TR7]** - Must work internationally
  
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

| Role/Name                          | Contact         |
| ---------------------------------- | --------------- |
| Architecture Kata 2023 Jury Member | *Neal Ford*     |
| Architecture Kata 2023 Jury Member | *Mark Richards* |
| Architecture Kata 2023 Jury Member | *Jacqui Read*   |
| Architecture Kata 2023 Jury Member | *Clare Sudbery* |
| Architecture Kata 2023 Jury Member | *Robin Losey*   |

## Architecture Constraints

For a startup in a greenfield development scenario, there are minimal limitations on technology choices. However, the solution space is constrained by the specific [Technical Requirements](#technical-requirements) outlined by the stakeholders. These technical requirements serve as the primary guiding constraints for the project's architecture and technology decisions.

## System Scope and Context

## Business Context

The Road Warrior platform serves various actors, including Travellers, External Persons, Analysts, Travel Systems, and the System itself. Travellers can log in, register, view their dashboard, manage reservations and trips, share trips on social media, provide access to external people, view end-of-year reports, configure email settings, and contact the "HelpMe!" agency for support. External Persons can access shared trip information, while Analysts access analytical reports. Travel Systems update travel data, and the System performs tasks such as polling emails, sending notifications, and collecting analytical data for end-of-year reports and analysis.

### Actors overview

| Actor           | Description                                                                                                                                                     | Use Case Reference                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Traveller       | Private or Business user using Road Warrior to manage his trips.                                                                                                | UC01, UC02, UC03, UC04, UC05, UC06, UC07, UC08, UC09, UC10 |
| External Person | A person having access to a trip, which is shared by Traveller.                                                                                                 | UC11                                                       |
| Anaylst         | Business user accessing analytical data.                                                                                                                        | UC01, UC12                                                 |
| Travel System   | System Actor to deliver information on changes on reservations. It includes Travel systems like APOLLO as well as dedicated Airline/Hotels/Car rental agencies. | U14                                                        |
| Supporting agency| User selected agency for support and resolve issues													    | U10, U19                                                   |
| System          | Some activities are initiated by the system.                                                                                                                    | UC15, UC16, UC18                                           |

### Use case overview

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

*\<optionally: Explanation of external domain interfaces>**

## Technical Context

![Context Diagram](diagrams/Context.drawio.svg)

**\<Diagram or Table>**

**\<optionally: Explanation of technical interfaces>**

**\<Mapping Input/Output to Channels>**

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

## Whitebox Overall System

***\<Overview Diagram>***
![Container Diagram](diagrams/Container.drawio.svg)

***\<Component Diagram>***
![Component Overview](diagrams/Component-overview.drawio.svg)

***\<Aanlytics Diagram>***
![Component Overview](diagrams/Analytics-logical.drawio.svg)

### Motivation

In the context of our architecture, the decision to split our solution into several domains stems from a fundamental understanding of the necessary functionality and a keen consideration of various non-functional requirements. By dissecting our system into distinct domains and components, we embark on a journey to achieve greater flexibility and efficiency in our development process.

### Function analyses

In our pursuit of an optimized and well-structured solution, we turn our attention to the deliberate division of functionality, specifically the distribution of Use Cases across our distinct domains.

By meticulously organizing an independent set of Use Cases within each domain, we not only foster a more agile and self-contained development process but also reduce the inherent complexities associated with interdependencies

In more formal terminology, this strategic approach directly contributes to the enhancement of 'Loose coupling' and 'Cohesion' within our system, reinforcing the foundational principles that guide our architectural choices
| Domain               | Use Case Reference                                                                                                | Use Cases name                                                                                                                                                                                                                                                                                                                                                                 |
| -------------------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Analytic domain      | UC08 <br> UC12 <br> UC18 <br>                                                                                        | Access end-of-year report <br> Access to analytic reports <br> Collect analytical data                                                                                                                                                                                                                                                                                         |
| Configuration domain | UC09 <br> UC19                                                                                                    | Define filter and whitelist for email <br>   Configure "HelpMe!" Agency                                                                                                                                                                                                                                                                                                                                       |
| Channel              | UC01 <br> UC02 <br> UC03 <br> UC04 <br> UC05 <br> UC06 <br> UC07 <br> UC08 <br> UC09<br> UC10<br> UC11 <br> UC12 <br> UC16 | Login in system <br> Register in system <br> View dashboard <br> Manage reservations <br> Manage trip	<br> Share trip via social networks <br> Provide access to external people <br> Access end-of-year report  <br>  Define filter and whitelist for email <br> Contact with "HelpMe!" Agency <br> Access to shared trip information <br> Access to analytic reports	<br> Push notification about changes in trip |
| Trip organizer       | UC03 <br> UC04 <br> UC05 <br> UC14 <br> UC16                                                                      | View dashboard <br> Manage reservations	<br> Manage trip	<br> Push notification about changes in trip                                                                                                                                                                                                                                                                          |
| IAM domain           | UC01 <br> UC02                                                                                                    | Login in system<br> Register in system                                                                                                                                                                                                                                                                                                                                         |
| Integration domain   | UC14 <br> UC15 <br> UC16                                                                                          | Update travel data	<br> Poll emails	<br> Push notification about changes in trip                                                                                                                                                                                                                                                                                               |

*Remark: In "Channel domain" we mentioned list of Use cases, but only UI part of these US is related to Channel domain._

Usecase vs domains tracebility:
| #    | Use Case                                | Analytic | Configuration | Channel | Trip organizer | IAM | Integration |
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

_Remark: In "Channel domain" we mentioned list of Use cases, but only UI part of these US is related to Channel domain._

### Architecture characteristics

Even all Architecture characteristics should be taking in account when we design and implement domains, some of Architecture characteristics played more important role and influence significantly on component design and deployment.

| Architecture characteristics | Analytic | Configuration | Channel | Trip organizer | IAM    | Integration |
| ------------------ | -------- | ------------- | ------- | -------------- | ------ | ----------- |
| availability       | medium   | medium        | high    | high           | high   | high        |
| compatibility      | high     | low           | low     | low            | high   | high        |
| evolvability       | high     | low           | High    | high           | low    | medium      |
| localizability     | low      | low           | high    | high           | low    | medium      |
| testability        | low      | low           | high    | high           | medium | medium      |
| traceability       | high     | low           | low     | medium         | high   | high        |

Based on this analyses we can see that all domains has different Architecture characteristics and as result we are not able to combine them.

### Contained Building Blocks

This chapter provides an overview of the different domains that compose the Road Warrior system. Each subchapter describes a domain, its responsibilities, interfaces with other domains, and the rationale behind its existence.

#### Analytic domain

**What the domain does:**

The Analytic domain is responsible for collecting data for reports, creating reports, and providing access to reports. This domain handles persistent data like raw analytical data and generated reports.

**Interfaces:**

- Delivers end-of-year reports to the Channel domain
- Receives notifications directly from the Integration domain for updated information and analysis of agency behavior
- Reads data from the Trip Organizer domain to collect information about trips and reservations

**Why we have the domain:**

This domain is separated from others because it can be purchased from a third party. Non-functional requirements for this domain are unclear at the beginning of the project, but generating "end-of-year" reports requires high elasticity at the end of the calendar year.

#### User Settings

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

#### Channel Domain

**What the domain does:**

The Channel domain is responsible for providing user interfaces, such as web applications and mobile applications.

**Interfaces:**

- Receives all notifications about changes in reservations from the Trip Organizer and updates content in user interfaces
- Uses the API of the Trip Organizer to access information about trips and reservations
- Uses IAM for user registration and login (token exchange)
- Receives end-of-year reports from the Analytic domain
- Provides configuration to the Configuration domain

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

Important Interfaces  
*\<Description of important interfaces>*

### Channels

<img src="diagrams/Component-Channels.drawio.svg">

*\<Purpose/Responsibility>*

*\<Interface(s)>*

*\<(Optional) Quality/Performance Characteristics>*

*\<(Optional) Directory/File Location>*

*\<(Optional) Fulfilled Requirements>*

*\<(optional) Open Issues/Problems/Risks>*

### IAM

<img src="diagrams/Component-IAM.drawio.svg">

### Trip Organizer

<img src="diagrams/Component-TripOrganizer.drawio.svg">

*\<Purpose/Responsibility>*

*\<Interface(s)>*

*\<(Optional) Quality/Performance Characteristics>*

*\<(Optional) Directory/File Location>*

*\<(Optional) Fulfilled Requirements>*

*\<(optional) Open Issues/Problems/Risks>*


### \<Name black box n>

*\<black box template>*

### \<Name interface 1>

…

### \<Name interface m>

## Level 2

### White Box *\<building block 1>*

*\<white box template>*

### White Box *\<building block 2>*

*\<white box template>*

…

### White Box *\<building block m>*

*\<white box template>*

## Level 3

### White Box \<\_building block x.1\_\>

*\<white box template>*

### White Box \<\_building block x.2\_\>

*\<white box template>*

### White Box \<\_building block y.1\_\>

*\<white box template>*

# Runtime View

## \<Runtime Scenario authentication >

Following flow describes the authentication process with 3rd party Identity Provider (IDP)
Corresponding architecture decision record is adr02-authentication

![Authentication Flow](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/wschaef/architecture-kata-2023/main/diagrams/authentication.puml)

## \<Runtime Scenario 2>

## …

## \<Runtime Scenario n>

# Deployment View

## Infrastructure Level 1

***\<Overview Diagram>***

Motivation  
*\<explanation in text form>*

Quality and/or Performance Features  
*\<explanation in text form>*

Mapping of Building Blocks to Infrastructure  
*\<description of the mapping>*

## Infrastructure Level 2

### *\<Infrastructure Element 1>*

*\<diagram + explanation>*

### *\<Infrastructure Element 2>*

*\<diagram + explanation>*

…

### *\<Infrastructure Element n>*

*\<diagram + explanation>*

# Cross-cutting Concepts

## *\<Concept 1>*

*\<explanation>*

## *\<Concept 2>*

*\<explanation>*

…

## *\<Concept n>*

*\<explanation>*

# Architecture Decisions

[ADR 1 Architecture Style](adrs/adr01-ArchitectureStyle.md)
[ADR 2 User Onboarding and Authentication Strategy](adrs/adr01-ArchitectureStyle.md)
[ADR 3 How to share share trips](adr03-SharingTrip.md)
[ADR 4 Frontend technology](adr04-FrontendTechnology)

# Quality Requirements

## Quality Tree

## Quality Scenarios

# Risks and Technical Debts

We see following risks:

**Risk: Requesting Email Access**

Requesting access to users' emails, whether granted to all or none, poses significant data privacy challenges. This can potentially lead to unintended exposure of sensitive information and raise concerns about user privacy.

**Risk: Diversity in Interface Integration**

Integrating interfaces from various entities like hotels, car agencies, and airlines directly can introduce complexities and costs. This approach may hinder system evolution and maintenance, potentially leading to increased expenses and limited adaptability.

# Glossary

| Term             | Definition                                                                                                                                                       |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| *Trip*           | *\<definition-1>*                                                                                                                                                |
| *Reservation*    | *\<definition-2>*                                                                                                                                                |
| *Booking*        | *\<definition-2>*                                                                                                                                                |
| *Travel angency* | *\<definition-2>*                                                                                                                                                |
| *ADR*            | *ADR stands for "Architecture Decision Record." It is a document that captures important architectural decisions made during the software development process. * |
| *NFR*            | *NFR stands for non functional requirements, derived from input given by the stakeholders*                                                                       |
| *IDP*            | *Identity Provider is a system managing identities of users and provides authentication through protocol like OpenId Connect*                                    |
| *BFF*            | *Backend for Frontend is a server responsible to provide data for a frontend line a mobile app or web app*                                                       |

# References
* Arc42 Template Created, maintained and © by Dr. Peter Hruschka, Dr. Gernot Starke and
contributors. See <https://arc42.org>.

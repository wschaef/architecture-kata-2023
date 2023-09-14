# Introduction and Goals

## Business context and goal
The Road Warrior Travel Management Dashboard

In the ever-evolving landscape of travel, we as new player comes  – a dynamic startup that stands apart from the affiliations of traditional travel agencies. 

### Vision
Our mission? To pioneer the next generation of online trip management dashboard, empowering travelers to take charge of their journeys like never before. We envision a world where your travel experiences are seamlessly organized, accessible at your fingertips, and tailored to your preferences.

Introducing the Road Warrior Dashboard – a user-friendly interface designed to revolutionize the way you manage your trips. Whether you're at your computer or on the go with your mobile device, we've got you covered.

### Key Features:

Seamless Trip Organization: Say goodbye to the chaos of scattered reservations. With our dashboard, all your travel arrangements are neatly organized by trip, allowing you to have a clear overview of your entire journey.

Web and Mobile Accessibility: Your travel plans should be accessible wherever you are. Our platform is optimized for both web browsers and mobile devices, ensuring that you have the information you need at your fingertips, whether you're at your desk or on the move.

Route Change Tracking: We understand that travel plans can be subject to unexpected changes. Our dashboard keeps you informed about any alterations to your routes, ensuring that you're always up to date and prepared for any adjustments.

Integration with Airlines, Hotels, and Car Rentals: The Road Warrior Dashboard isn't just an isolated tool – it's your gateway to the travel ecosystem. We're seamlessly integrated with most major airlines, hotel chains, and car rental agencies, making it effortless to manage all aspects of your journey in one place.

## Requirements Overview

[List of functional, technical and non functional requirements](requirements.md)

## Quality Goals

## Stakeholders

| Role/Name   | Contact        | Expectations       |
| ----------- | -------------- | ------------------ |
| *\<Role-1>* | *\<Contact-1>* | *\<Expectation-1>* |
| *\<Role-2>* | *\<Contact-2>* | *\<Expectation-2>* |

# Architecture Constraints

# System Scope and Context

## Business Context

### Actors overview

| Actor | Description | Use Case Reference |
| ------ | ----------- | ------------------ |
| Traveller   | Private or Business user using Road Warrior to manage his trips. | UC01,UC02, UC03, UC04, UC05, UC06, UC07, UC08, UC09, UC10 |
| External Person | A person having access to a trip, which is shared by Traveller. | UC11 |
| Anaylst | Business user accessing analytical data. | UC01, UC12, UC13 |
| Travel System | System Actor to deliver information on changes on reservations. It includes Travel systems like APOLLO as well as dedicated Airline/Hotels/Car rental agencies.  | U14 |
| System | Some activities are initiated by the system. | UC15, UC16, UC17, UC18 |

### Use case overview

| # | Use Case | Short Description | Actor | Requirement |
| - | -------- | ----------------- | ----- | ----------- |
| UC01 | Login in system | User logs into the system. | Traveller, Analyst |  |
| UC02 | Register in system | Traveller registers as a new user to system. | Traveller |  |
| UC03 | View dashboard | Traveller gets an overview of his trips. | Traveller | FR6 |
| UC04 | Manage reservations | Traveller add, edit removes reservations manually. | Traveller | FR6 |
| UC05 | Manage trip | Traveller creates trips, add new reservation to it, etc. | Traveller | FR6 |
| UC06 | Share trip via social networks | Traveller transfers his trip to social media.  | Traveller | FR7 |
| UC07 | Provide access to external people | Traveller gives a direct link to a person to view his trip. | Traveller | FR7 |
| UC08 | Access end-of-year report | Traveller view the result of the yearly report on his trips. | Traveller | FR9 |
| UC09 | Define filter and whitelist for email | Traveller configures the email poll, including the filter and whitelisting. | Traveller | FR3 |
| UC11 | Access to shared trip information | External Person view a trip of a Traveller. | External Person | FR7 |
| UC12 | Access to analytic reports | Analyst views analytic reports from the system. | Analyst | FR10 |
| UC13 | Analyse trends | is this redundant and not needed? | Analyst | FR10 |
| UC14 | Update travel data | System updates the received data for a reservation. | Travel System | FR4 |
| UC15 | Poll emails  | System polls email system of traveller. | System | FR2 |
| UC16 | Push notification about changes in trip | System pushes the information received from email, Travel system, etc. towards the traveller. | System | FR4 |
| UC17 | Remove finished trip | Do we really need this use case? | System | FR6 |
| UC18 | Collect analytical data | System collect information from all Travellers for later analytical work on it and for preparation end-of-year report | System | FR10 |


*\<optionally: Explanation of external domain interfaces>**

## Technical Context

<img src="diagrams/Context.drawio.svg">

**\<Diagram or Table>**

**\<optionally: Explanation of technical interfaces>**

**\<Mapping Input/Output to Channels>**

# Solution Strategy

# Building Block View

## Whitebox Overall System

***\<Overview Diagram>***
<img src="diagrams/Container.drawio.svg">

***\<Detailed Component Diagram>***
<img src="diagrams/Component overview.drawio.svg">

Motivation  
*\<text explanation>*

Contained Building Blocks  
*\<Description of contained building block (black boxes)>*

**Reporting domain** - responsible for collect data for reports, create reports and provide access to reports. This domain has persistent data like raw analytical data and generated reports. Reporting domain includes folloing components:
* Data Collector - recive notification from external systems and store them
* Data Viewer - provide access to raw analytic data.
* End-Of-Year report creation and caching - report generation engine and storage for generated reports.
  
**Integration domain** - provide capabilities for collect information from external sources like emailboxes, external travel systems and agancies. Several components included in domain:
* Notification - component which reicve updated from external systems via integration layer and notify other domains about changes.
* EMail processing - engine for reading emails from user mailboxes. Also apply filters and whitelist rules and parse email for get information about reservation.
* Airlines/Hotel/Car rental integrations - Integration with several Agencies via standard APIs.
* Travel system integraion - integrate with APPOLO, SABRE system in order to collect information about reservation and recieve updates regarding these reservations.

**Trip organizer domain** - allow use to manage his trips, create new one, delete and add reservations to this trips.
Data ingested from integration domain.

**Authorization and Authentication domain** - covers all aspect of registration, authentication and authorization user.




Important Interfaces  
*\<Description of important interfaces>*

### \<Name black box 1>

*\<Purpose/Responsibility>*

*\<Interface(s)>*

*\<(Optional) Quality/Performance Characteristics>*

*\<(Optional) Directory/File Location>*

*\<(Optional) Fulfilled Requirements>*

*\<(optional) Open Issues/Problems/Risks>*

### \<Name black box 2>

*\<black box template>*

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

# Quality Requirements

## Quality Tree

## Quality Scenarios

# Risks and Technical Debts

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

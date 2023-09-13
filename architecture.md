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
|-------------|----------------|--------------------|
| *\<Role-1>* | *\<Contact-1>* | *\<Expectation-1>* |
| *\<Role-2>* | *\<Contact-2>* | *\<Expectation-2>* |

# Architecture Constraints

# System Scope and Context

## Business Context

**\<Diagram or Table>**
[use case overview](usecases.md)

[actor overview](actors.md)
**\<optionally: Explanation of external domain interfaces>**

## Technical Context

![system overview](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/wschaef/architecture-kata-2023/main/diagrams/context.puml)

**\<Diagram or Table>**

**\<optionally: Explanation of technical interfaces>**

**\<Mapping Input/Output to Channels>**

# Solution Strategy

# Building Block View

## Whitebox Overall System

***\<Overview Diagram>***
<img src="diagrams/Container.drawio.svg">

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

## \<Runtime Scenario 1>

-   *\<insert runtime diagram or textual description of the scenario>*

-   *\<insert description of the notable aspects of the interactions
    between the building block instances depicted in this diagram.>*

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

# Quality Requirements

## Quality Tree

## Quality Scenarios

# Risks and Technical Debts

# Glossary

| Term        | Definition        |
|-------------|-------------------|
| *\<Term-1>* | *\<definition-1>* |
| *\<Term-2>* | *\<definition-2>* |

# References
* Arc42 Template Created, maintained and © by Dr. Peter Hruschka, Dr. Gernot Starke and
contributors. See <https://arc42.org>.

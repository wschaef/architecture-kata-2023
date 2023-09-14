## Requirements Overview

### Functional Requiremens

Functional requirements are derived from input given by the stakeholders documented there [input](input.md)|

 #     | Requirement                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
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
#### NFR1 - Availability

Requirement Reference: TR4

Availability is set at 99.99% ("four nines"), which translates to 4.38 minutes/month of allowed downtime.

#### NFR2 - Scalability/Elasticity

Requirement Reference: TR2, TR3

The system must accommodate 2 million active users/week and a total of 15 million user accounts.

#### NFR3 - Performance

Requirement Reference: TR6, TR5

The system must meet the following performance criteria:

- Response time from web: 800ms
- Mobile: First-contentful paint of under 1.4 sec
- Travel updates must be presented in the app within 5 minutes of generation by the source

#### NFR4 - Consistency

Requirement Reference: TR5, FR5, FR6, FR9, FR10

The system should ensure consistency in the following aspects:

- Travel updates must be presented in the app within 5 minutes of generation by the source
- Once the trip is complete, the items should automatically be removed from the dashboard
- End Year report must be consistent with active and inactive trips
- Analytical data must be consistent with operational data

#### NFR5 - Cost

Requirement Reference: FR1

The system must be cost-efficient.

#### NFR6 - Evolvability

Requirement Reference: TR1, FR4, FR12

The system should allow for efficient integration and feature addition, including:

- Adding new integrations with travel systems
- Adding new features to the user interface
- Adding new import sources for trips or trip parts

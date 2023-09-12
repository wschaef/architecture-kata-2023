# Requirements

## Functional Requiremens

Functional requirements are derived from input given by the stakeholders documented there [input](input.md)

- **[FR1]** - Road Warrior is system built and managed by a start up
- **[FR2]** - Poll email looking for travel-related emails
- **[FR3]** - Filter and whitelist certain emails
- **[FR4]** - The system must interface with the agency’s existing airline, hotel, and car rental interface system to update travel details (delays, cancellations, updates, gate changes, etc.). Updates must be in the app within 5 minutes of an update (better than the competition)
- **[FR5]** - Customers should be able to add, update, or delete existing reservations manually as well.
- **[FR6]** - Items in the dashboard should be able to be grouped by trip, and once the trip is complete, the items should automatically be removed from the dashboard.
- **[FR7]** - Users should also be able to share their trip information by interfacing with standard social media sites or allowing targeted people to view your trip.
- **[FR8]** - Richest user interface possible across all deployment platforms
- **[FR9]** - Provide end-of-year summary reports for users with a wide range of metrics about their travel usage
- **[FR10]** - Road Warrior gathers analytical data from users trips for various purposes - travel trends, locations, airline and hotel vendor preferences, cancellation and update frequency, and so on.
- **[FR11]** - Customers must be able to use the system through web and mobile apps
- **[FR12]** - Must integrate with preferred travel agency for quick problem resolution (help me!)
- **[FR13]** - Must work internationally
  
## Technical requirements

Technical requirements are derived from input given by the stakeholders documented there [input](input.md)

- **[TR1]** - must integrate seamlessly with existing travel systems (i.e, SABRE, APOLLO)
- **[TR2]** - 2 million active users/week
- **[TR3]** - total users: 15 million (user accounts)
- **[TR4]** - Users must be able to access the system at all times (max 5 minutes per month of unplanned downtime)
- **[TR5]** - Travel updates must be presented in the app within 5 minutes of generation by the source
- **[TR6]** - Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec)
  
## Non Functional

Non functional requirements are derived from functional and technical requirements

- **[NFR1]** Availability
  - 99.99% ("four nines") 4.38 minutes/month <- **[TR4]**
- **[NFR2]** Scalability  
  -  2 million active users/week <- **[TR2]**
  -  total users: 15 million (user accounts) <- **[TR3]**
- **[NFR3]** Performance
  -  Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec) <- **[TR6]**
- **[NFR4]** Consistency
  -  Travel updates must be presented in the app within 5 minutes of generation by the source <- **[TR5]**
  -  Once the trip is complete, the items should automatically be removed from the dashboard <- **[FR5][FR6]**
- **[NFR5]** Cost
  - system must by cost efficient <- **[FR1]** 
- **[NFR6]** Evolvability
  -  adding an new integration must be efficient <- **[TR1],[FR4],[FR12]**
  -  adding new region must be efficient <- **[FR13]**
  -  adding new features to ui must be efficient <- **[FR1][FR8][FR11]**
  -  adding new import source for trips or trip parts must be efficient <- **[FR2],[FR3]** //we do not believe that the majority of the users will accept access to their emails, and assume that this requirement will evolve
  -  adding new social media sharing functionality must be efficient <- **[FR7]**

# Requirements overview

| FR/TR   | Availability | Scalability | Performance | Consistency | Cost | Evolvability |
| ------- | -----------  | ----------- | ----------- | ------- | ---- | ------------ |
|FR0      |             |             |             |         |      |              |
|FR1      |             |             |             |         |      |              |
|FR2      |             |             |             |         |      |              |
|FR3      |             |             |             |         |      |              |
|FR4      |             |             |             |         |      |              |
|FR5      |             |             |             |         |      |              |
|FR6      |             |             |             |         |      |              |
|FR7      |             |             |             |         |      |              |
|FR8      |             |             |             |         |      |              |
|FR9      |             |             |             |         |      |              |
|FR10     |             |             |             |         |      |              |
|FR11     |             |             |             |         |      |              |
|FR12     |             |             |             |         |      |              |
|FR1      |             |             |             |         |      |              |
|TR1      |             |             |             |         |      |              |
|TR2      |             |             |             |         |      |              |
|TR3      |             |             |             |         |      |              |
|TR4      |             |             |             |         |      |              |
|TR5      |             |             |             |         |      |              |
|TR6      |             |             |             |         |      |              |

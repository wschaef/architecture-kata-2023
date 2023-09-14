# ADR Analytics make of buy

**Status** : proposed / accepted / superseded

**Date** : 11.09.2023

**Stakeholders**

- [ ] @wschaef
- [ ] @uweTelco
- [ ] @slookin
- [x] @mauermbq

## Context

In consideration of the following requirements:

- **[FR9]** - Provide end-of-year summary reports for users with a wide range of metrics about their travel usage
- **[FR10]** - Road Warrior gathers analytical data from users trips for various purposes - travel trends, locations, airline and hotel vendor preferences, cancellation and update frequency, and so on.

We assume that the business model relies on the analytical domain by offering E2E travel data to travel agencies and other potential B2B customers.

The objective is to provide a flexible approach for data warehousing which allows to scale and has inbuild security.

The critical decision criteria include:
    - flexibility
    - Infrastructure as Code
    - security
    - scalability
    - low TCO
    - Serverless or fullly managed platform as a service

**Scope**: This decision pertains on the analytical domains.

**Assumption**: We follow a cloud native approach based on Google GCP just as an example. The decision is not limited to this cloud provider. The only core assumption is, that the start-up decides for one cloud provider for the whole architecture. Lift and shift between cloud providers is not cost efficient and therefore not advised.

## Decision

- Use serverless Data warehouse technologies for analytical purposes (Big Query)
- Use Availab Frontend technologies for analytical purposes (Looker), as long as not already one exists in the company
- Data Upload is on Google Cloud Storage (GCS)

## Concequences

Each warehouse technology has its own pros and cons and requires learning curve.

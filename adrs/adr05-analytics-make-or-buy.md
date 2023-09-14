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
- Handle external data as objects: Data Upload is on Google Cloud Storage (GCS)
- Use Google Cloud Dataflow to create a data pipeline that reads from Cloud SQL and writes to BigQuery. This method is particularly useful if you need to perform transformations on the data before it gets to BigQuery. (to be clarified)

### Ratioanle for Serverless Data Warehouse

By reducing the overhead associated with infrastructure management and offering powerful tools and integrations out-of-the-box, serverless data warehouses like BigQuery enable businesses to focus on data analytics and insights rather than the intricacies of data storage and management.

Advantages in detail - especially start-up needs to reduce ops effort and focus on business value:

- **Ease of Use**:
  - **Zero Infrastructure Management:** Users don't need to worry about the underlying infrastructure, including the provisioning, configuration, and scaling of resources.
  - **No Indexing**: In traditional databases, proper indexing is crucial for performance. With BigQuery, there's no need to manually manage indexes.
- **Inbuild Scalability:**
  - Automatic Scaling: The serverless architecture scales automatically to handle large datasets and complex queries if startup growa.
  - Concurrency: Handle multiple queries simultaneously without degradation in performance.
- **Cost Efficiency:**
  - **Pay-as-you-go Pricing**: With BigQuery, you pay for the amount of data processed by your queries, not for storage or pre-allocated resources.
  - **Automatic Storage Optimization:** Data storage is optimized automatically, with the first terabyte of data processed per month being free.
- **Integrated Machine Learning (ML)**:
  - **BigQuery ML:** Enables users to create and execute machine learning models in BigQuery using SQL commands, eliminating the need to move data to specialized tools or platforms. This might be relevant for NLP processing of Email content.
- **Security:**
  - **Encryption:** Data is encrypted at rest and in transit.
  - **Access Management:** Integrates with identity and access management tools, allowing fine-grained control over who can access and modify data and datasets. Additionally there is no additional tooling necessary for data access management (no separate access manegement capabilities needed for analytical space).
- **Flexibility to adapt (start-up scnearion for data driven business model):**
  - **Data Types and Nested Fields:** Supports various data types, including nested and repeated fields.
  - **Geospatial Capabilities:** Offers geospatial processing capabilities, allowing you to handle and analyze geographic data in the travel context.
- **Fully Managed - reduces ops effort:**
  - **Updates and Maintenance:** All updates, patching, and maintenance are handled by the cloud provider.
  - **Backup and Disaster Recovery:** Data is automatically backed up, and disaster recovery is baked in.
- **Integration with Other Services:**
  - **Ecosystem:** Being part of Google Cloud, BigQuery integrates well with other GCP services like SQL-Services, specific data processing tools and Pub/Sub.
  - **Data Transfer Service:** Easily move data from external sources into BigQuery.
- **Multi-region Availability as start-up works in international context:** Allows to run analytics solutions near your customer base or organizational footprint, improving query performance and reducing latency.
- **Long-term Storage:** Automatically moves older data to cheaper storage classes, saving costs while retaining accessibility.

## Concequences

Each warehouse technology has its own pros and cons and requires learning curve.

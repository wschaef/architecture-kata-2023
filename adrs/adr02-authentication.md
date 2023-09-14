
# ADR: User Onboarding and Authentication Strategy

**Status**: Proposed / Accepted / Superseded

**Date**: 11th September 2023

**Stakeholders**:

- [x] @wschaef
- [x] @uweTelco
- [ ] @slookin
- [ ] @mauermbq

## Context

**Scope**: This decision pertains to Identity and Access Management (IAM) and channels.

In consideration of the following requirements:

- **[TR2]** - Maintain 2 million active users per week.
- **[TR3]** - Accommodate a total of 15 million user accounts.

Our objective is to determine the most efficient approach for onboarding users while ensuring an exceptional user experience. Additionally, we must evaluate the impact on user authorization.

The critical decision criteria include:

- User Experience (UC01: Login, UC02: Register)
- Consistency in the identity referenced within the system

Options:

1. Offer users to create user accounts in "Road Warrior" by completing a registration form.
2. Employ third-party accounts (e.g., Google, Apple, etc.) for user authentication.

## Decision

We have chosen to support third-party accounts and implement an internal identity provider to decouple from external identity providers. Users can select from the supported authentication providers, after which our IAM component will create an internal account that will be used throughout the entire system. This approach aligns with the standard OpenID Connect protocol.

We have identified several advantages in this approach:

- Higher conversion rates are achieved for apps offering third-party login, as opposed to requiring users to create complex passwords and unique usernames.
- It enables access to the user's email account using standard protocols like OpenID Connect with relevant scopes.
- Decoupling from external data structures enhances system robustness.
- Our components only need to trust a single identity provider.
- Adding new third-party login options is cost-efficient.


## Consequences

As a result of this decision, we will need to establish an internal identity provider and implement OpenID Connect for authentication.

Optionally, we can create a button labeled 'Create Local Account.' When a user clicks on it, we can display a message stating that this feature is planned for implementation. Once a significant number of clicks are achieved, we can allocate resources to implement it.
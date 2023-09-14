# ADR: Share Trips by Reference

**Status**: Proposed / Accepted / Superseded

**Date**: 11th September 2023

**Stakeholders**:
- [x] @wschaef
- [x] @uweTelco
- [ ] @slookin
- [ ] @mauermbq

## Context

**Scope**: Channels, IAM

**Relevant Requirements**:
- [FR6] - Items in the dashboard should be able to be grouped by trip, and once the trip is complete, the items should automatically be removed from the dashboard.
- [FR8] - Richest user interface possible across all deployment platforms

**Assumptions**:
- Users can only share content publicly or not share it. There are no specific authorization settings for the audience.

Sharing trip-related content can be accomplished in two ways:

- **By Reference**: The target audience receives a reference (e.g., a link) to the content and can access it.
- **By Copy**: The target audience receives a copy of the content (e.g., an image or PDF) and can open it.

### Pros and Cons

|          | Share Trip by Reference                       | Share Trip by Copy                                   |
| -------- | --------------------------------------------- | ---------------------------------------------------- |
| **Pros** |                                               |                                                      |
|          | - Easy access via a URL                       | - Self-contained documents                           |
|          | - Minimal data transfer                       | - Works offline                                      |
|          | - Real-time content updates                   | - Static, stable content                             |
|          | - Audience can interact with the content      |                                                      |
| **Cons** |                                               |                                                      |
|          | - Requires an active server                   | - No updates possible                                |
|          | - Internet connection needed                  | - Potentially larger file sizes                      |
|          | - Requires addtional authorization capability | - No interaction possible                            |
|          |                                               | - Requires additional document generation capability |

## Decision

We have decided to share trips by reference. Sharing a link provides the best user experience for the target audience.
Additionally, we can potentially increase the conversion rate by prompting the audience to join Road Warrior when they open a shared trip.
We will leverage "preview URL" functionality to provide a concise summary to the recipient, a feature widely supported by most social media platforms.

## Consequences

To implement this decision, we will need to:
- Introduce a feature allowing users to mark a trip as public.
- Add a "share with" button to the user interface.
- Extend IAM to enforce that only public trips can be accessed by anonymous users.

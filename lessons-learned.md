# Lessons learned

## Collaboration

### Collaboration Challenges

1. **Remote Work**: The collaboration was conducted entirely in a remote work setup, which posed challenges in terms of communication and coordination.

2. **Diverse Free Time Slots**: Team members had different schedules, making it challenging to find common meeting times.

3. **Finite Release Date**: There was a strict deadline for the project release, which added pressure to the collaboration process.

### Solutions Implemented

To address these collaboration challenges, the team implemented the following solutions:

1. **Agreed Communication Patterns**: We recognized the need for structured communication. Therefore, we agreed upon the following communication patterns:

    - **Group Chat for Instant Communication**: We established a group chat platform for instant communication. This allowed team members to quickly share updates, ask questions, and conduct ad-hoc votes when needed.

    - **MIRO for Freestyle Brainstorming**: We utilized MIRO, a collaborative online whiteboard platform, for freestyle brainstorming sessions. This helped in visualizing ideas and fostering creativity.

    - **Git for Versioned Results**: We relied on Git for version control of our project. This ensured that our codebase and documentation were always up-to-date and well-managed.

    - **Daily "Jour Fix" Meeting**: We scheduled a short daily "Jour Fix" meetings to synchronize our activities, discuss progress, and address any immediate issues. These meetings provided a sense of regularity and alignment. Summary was communicated via chat to update missing team members.

2. **Starting Together, Then Separating**: To overcome the challenge of different and schedules, we adopted a phased approach:

    - **Starting Together**: Initially, we started working together to gain a common understanding of the project requirements. This phase included discussing high-level objectives and priorities.

    - **Separation by Expertise**: Once we had a shared vision, we separated into domain-specific groups based on expertise, such as frontend, API, integration, data, security, and cloud. This allowed us to work independently and provide fast feedback within our respective domains.


In conclusion, the collaboration challenges we faced were successfully addressed through agreed communication patterns and a structured approach to working together. These lessons will serve as valuable insights for future remote collaborations.


## Tooling

In the course of our project, we found that the right tools play a crucial role in facilitating efficient collaboration and documentation. Here are some key insights and experiences we gained regarding the tools we used:

### Preparation and Adaptation

One of the fundamental lessons we learned is that preparation is essential when it comes to choosing and using tools. However, there were instances where we had to rethink our tool choices due to unforeseen challenges:

- **PlantUML Limitations**: While PlantUML is a valuable tool for creating diagrams, we encountered limitations when dealing with larger and more complex diagrams. This prompted us to switch to Draw.io, which offered the flexibility and capabilities required for handling intricate diagrams. The migration effort was necessary but ultimately worthwhile. All graphical tools allow real modelling only with certain constraints and discipline. 

### Markdown: The Good and the Bad

Markdown emerged as a valuable tool for documentation within our project. Here, we examine its strengths and weaknesses:

#### Pros

- **Simplicity**: Markdown's straightforward syntax made it easy for team members to write and format documentation efficiently.

- **Native Support**: Markdown's native support in platforms like GitHub allowed us to seamlessly edit and save documents directly through the web interface.

#### Cons

- **Lack of Include Feature**: Markdown lacks a built-in "include" feature, making it challenging to structure and modularize documentation effectively.

- **Manual References**: Keeping references in sync within Markdown documents required manual effort, which was time-consuming.

- **Lack of Interactive Diagrams**: Markdown does not offer the capability to create interactive diagrams, limiting our options for visualizing complex systems.

#### Verdict

 While Markdown proved suitable for smaller projects due to its simplicity and native support in GitHub, it revealed limitations when documenting architectures of larger scales.

### Documentation Structure

In terms of structuring our documentation, we chose the Arc42 template. This decision was driven by the fact that most team members were already experienced or at least familiar with this template, facilitating consistency and alignment across the project.

### Visualization: Striking the Right Balance

Visualization played a pivotal role in conveying complex architectural concepts. However, it also presented its own set of challenges:

- **C4 Model Evaluation**: We utilized the C4 model for architectural visualization. Here are the key aspects:

  - **Pros**: The C4 model's clear structure and minimalistic set of elements provided an effective means of drilling down into the entire logical architecture. Especially when tool-based modelling is not used, the clean structuring is helpful for a consistent representation of an architecture. 

  - **Cons**: One limitation we encountered was the absence of a single one-pager diagram that we could readily share.

We recognized the need for a tool that combines the structural clarity of Enterprise Architecture (SPARX), the simplicity of PlantUML, the flexibility of Draw.io, and the versioning capabilities of Git to meet our evolving documentation and visualization needs effectively.

## Approach

In our journey through the Architectural Kata, we adopted a pragmatic approach that was shaped by the unique challenges and constraints we encountered. Here, we reflect on the key aspects of our approach:

### Skipping Domain-Driven Design (DDD)

Early in the process, we made a conscious decision to skip Domain-Driven Design (DDD) as a foundational architectural approach. This choice was primarily driven by the limited access we had to stakeholders. While DDD is a powerful methodology for aligning software systems with the complexities of business domains, it relies heavily on close collaboration and domain expertise from stakeholders. Given our constraints, we recognized that attempting a full-fledged DDD approach would have been challenging and potentially less effective.

### Addressing Missing Business Case Information

Throughout the Architectural Kata, one recurring challenge we faced was the absence of critical information related to the business case. This gap in our understanding posed hurdles at various stages of the process. As result our suggestion for MVP scopes are based on technical aspects only.

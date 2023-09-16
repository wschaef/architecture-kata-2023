# ADR4: Using Flutter for Cross-Platform Development for Frontends

**Status**: Accepted

**Date**: 11.09.2023

**Stakeholders**
- [x] @wschaef
- [x] @uweTelco
- [x] @slookin
- [x] @mauermbq
- [x] @ilia

## Context

We are starting a new project from scratch and need to decide on the technology stack for developing a cross-platform application targeting Android, iOS, and the web. Our options are either to use platform-specific technologies or to adopt Flutter.

## Decision

After evaluating our options, we have chosen to use Flutter for the following reasons:

1. **Efficiency**: Flutter enables rapid development, making it well-suited for a new project where speed is essential.

2. **Code Reusability**: A single Flutter codebase for all platforms reduces code duplication and ensures consistent functionality.

3. **Ease of Prototyping**: Flutter's hot-reload feature facilitates rapid prototyping and iteration during the early stages of development.

4. **Maintenance Simplicity**: A unified codebase simplifies maintenance and updates across all platforms.

5. **Forward-Looking**: Flutter is supported by a growing community and offers long-term viability.

## Consequences

While adopting Flutter offers clear advantages, we should be aware of potential challenges:

1. **Learning Curve**: Team members not familiar with Flutter may require time to learn the framework and Dart programming language.

2. **Plugin Availability**: Some platform-specific features or libraries may not be readily available in Flutter's ecosystem.

3. **Performance**: Although generally performant, resource-intensive applications may need optimization.

4. **Platform-Specific Needs**: Some customization for specific platforms may be necessary.

In summary, using Flutter in our greenfield project is a practical choice due to its efficiency, code reusability, and future prospects. We will address potential challenges as we progress.

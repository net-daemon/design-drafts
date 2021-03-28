# Design Draft: net-daemon

## Abstract
This document proposes goals for net-daemon to make it easier for end-users and more maintainable for developers of net-daemon.

## Introduction
One thing that Home-Assistant lacks is a friendly environment for software developers to create automations. Recently with the introduction of blueprints, this has gotten a little better. But while creating automations in YAML works, it lakcs some of the goodies we've come to love as software developers. To name a few: type-safety, toolings, reusable components and debugging. The net-daemon project tries to solve this by enabling users to write their automations in C#. However over the years, the net-daemon project has lost sight of its goals. All kinds of changes made without clear goals in mind caused the project to be difficult to maintain. This draft documents goals to keep in mind while developing net-daemon. 

## Stakeholders

### End-users
Perhaps the most important stakeholder of net-daemon is the end-user. The end-user would like a stable project that is easy to use. Some characteristics of stable and easy:

- Works, without bugs.
- Simple, easy to learn / use API.
- No breaking changes.

### Contributors
The people that enable net-daemon to thrive are its contributors. They submit issues and pull-requests to solve bugs or add useful features. They need:

- Code that is easy to understand and modify.
- A platform that easy to extend, to develop new features / extensions without modifying the existing codebase.

### Project maintainers
Finally the developers maintaining net-daemon need to be enabled and motivated to keep the project up. They would like:

- As much automation as possible, with solid CI / CD.
- Clear goals for the project, so that it's possible to push net-daemon in the right direction together.
- High test coverage, to enable fast development.
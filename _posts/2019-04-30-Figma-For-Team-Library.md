---
layout: post
title: Figma Notes for Team Library
---

# Figma Notes
- Figma offers the following team access types: Open, Closed, and Secret.

- Members with view access can comment, inspect, and export assets by default so they can't accidentally edit something

- Secret teams - no one can see secret teams unless invited by members from that secret team or if they're the creator

- User permissions are handled at the team level and cascade down through all projects and documents within it

- If people join a team with edit access, they will be automatically able to edit ALL projects and files in it

- A team could represent an entire department, or a specific project

- Permissions: By structuring teams around efforts, you can have tighter, more specific control of user permissions. For example, if a group of 10 people are working on a new effort, by creating a team just for them, you can isolate edit access to just those users.

![Figma File Management](https://github.com/timsully/timsully.github.io/blob/master/images/figma_file_management.png "Figma File Management")

## Design Systems
- Consider setting up a dedicated team to share the libraries from, allowing more efficient control edit access. Which will allow you to publish stuff to your library.

- Make the design systems team open so everyone in the organization can see/use the libraries which are available to them, but not necessarily have the ability to edit

- Once you have started building your shared libraries and have situated them in a team with the appropriate level of access, you can start thinking about enabling certain libraries by default for the entire company, or specific libraries for specific teams.s

- When libraries are turned on at the organization level, every document created, regardless of team, will automatically have those libraries enabled

### Design Systems work in progress team
- If you have a team dedicated to creating, maintaining and distributing the company's design system, it is recommended giving them their own specific Figma team for their work in progress separate from the team where they house the published libraries they are in charge of maintaining and distributing

-  The work in progress library would most likely be closed to avoid confusion with ready-to-use components. This will avoid confusion about where the source of truth is for the design system. The design systems team can be free to do explorations, review component/pattern proposals and perform audits on existing patterns without any impact to users.

## Teams for Agencies and Consultancies
- If you're working with clients it may make sense to set them up as closed teams to keep sensitive work confined to those users


## Important Questions to Ask
- How tightly do you need to control access to various work happening across the company?

- How collaborative and cross-functional do you want your organization to be?

- Who needs to have visibility into each team and the documents within it?

- How could projects within a team help you organize your documents more effectively

- Do libraries or fonts need to be shared across the entire company?

- Will specific teams require certain shared libraries but not others?

# Assets Panel
- The assets panel brings together Components from the current File, and any Files or Libraries you have access to. (is it in this order?)

- The search field looks for Components in the current File, as well as any Libraries you have access to.

Components Hierarchy in the Assets Panel are in the following order:

  - Components you have created in the current File.

  - Components that are Private to the File. This includes any Components in this File that aren't published to a Team Library.

  - Components from other Files that you have used in the current File.

  - Components from any enabled Team Libraries.
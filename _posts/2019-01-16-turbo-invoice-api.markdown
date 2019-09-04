---
title: Turbo Invoice API
layout: post
date: '2019-01-16 10:00:00'
headerImage: true
projects: true
description: Turbo Invoice API is a modern invoicing API for home health staffing agencies and their clincians. 
category: project
---

<img src="https://source.unsplash.com/34OTzkN-nuc/1600x900">
Photo by [Cara Fuller](https://unsplash.com/@caraventurera?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)


# Turbo Invoice API

A summary of this post originally appeared on [Medium](https://medium.com/@brandonbaker40/introducing-the-turbo-invoice-api-8af977988483). 

## Summary

Turbo Invoice API is a modern invoicing API for home health staffing agencies. It provides the backend framework for agency clinicians to submit information regarding patient visits.

### Observations, Problem, and Opportunity:

In my experience consulting and managing projects for a home health staffing agency, I’ve found two things to be unmistakably true:

* Home health software is particularly susceptible to software rot.
* Innovation in home health is slower than other healthcare verticals.

Combine those observations with a heavily regulated environment and risks associated with failing to meet vaguely defined security standards — and the result is an industry shortage of innovation, investment and competition.

This environment opens the door for open source projects like the [Turbo Invoice API](https://github.com/brandonbaker40/turbo-invoice-api), where developers and innovators collaborate on bringing ideas to the marketplace without some of the barriers faced by private projects.

The particular invoicing application used by a home health staffing agency I work closely with was built in 2009 and has been minimally maintained for years. Other home health staffing agencies, who were sold clones of the original product face similar maintenance challenges and rely solely on the legacy developers who built the application over a decade ago.

The rise of mobile application development in the last decade and the mobile nature of home health therapists should have made adoption of mobile-first solutions the default option for all home health staffing agencies. And a SaaS subscription of a product to meet their needs would have provided these agencies with software less susceptible to decay.

The context in which this applications was originally built combined with the opportunity to capitalize on technological advancement over the last decade helped shaped the goals for this project.

The first goal was to provide simple API endpoints that reflect the data that agencies need. For example, an admin user should be able to see a list of visits made by a particular clinician (user). You would acccess that information at this endpoint:

`http://www.example.com/api/v1/users/{user_id}/visits`


A subgoal of the first goal was to restructure the database schema to be an accurate reflection of the relationships that exist outside of the application. The legacy tables have columns that are no longer relevant, or may have never been relevant or useful. For example, the `PoC` (point of contact) column in the agency table is filled with values like, "N/A", "John Doe", and "Name Name". This signaled to me that this column either needed to be dropped altogether or included in another table, e.g. Contacts. 

The second goal of the project was to make it a worthy investment of a developer's time by practicing strict test driven development (TDD), adhering to the Ruby style guide, and using RSpec and Rubocop to enforce those practices. I expect all contributors to follow these standards, which I hope will result in a more maintainable and robust application.

The third goal is to provide the home health staffing agencies with a tool that takes minimal time to onboard. I want agencies who use this software to immediately find it intuitive and clean. 

The final goal is to provide home health staffing agencies with an open source alternative for invoicing. Agencies who purchased bespoke invoicing software a decade ago and depend on legacy developers to maintain it and have little room in their budgets for a cost prohibitive alternative. 

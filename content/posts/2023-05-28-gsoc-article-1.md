---
title: GSoC'23 Week 0 - Introduction
date: 2023-05-28
summary: "Introduction"
description: ""
toc: true
readTime: true
autonumber: true
math: true
tags: ["cpp", "open-source", "kde"]
showTags: false
hideBackToTop: false
---
### Introduction

I'm Anant Verma, currently an R&D engineer at Tejas Networks Ltd, India. My proposal, "Implement Calendar Availability" was accepted for GSoC'23. 

This is an introductory post to my project.

#### Project Goals

My proposal is based on one of the ideas by KDE: [“Implement calendar availability”](https://community.kde.org/GSoC/2023/Ideas#Project:_Implement_calendar_availability). The goal of the project is to extend the iCal support to include elements in [RFC 7953](https://www.rfc-editor.org/rfc/rfc7953). This would entail adding new UI elements through which users will add/edit their availability. Along with this, KCalendarCore will be edited to support the new AVAILABILITY/VAVAILABILITY components (defined in RFC 7953).

#### Motivation

We often have regular periods of time where we are available or unavailable. For example, a college professor can easily specify what are their office hours and blocks of time where they are out of office. Ideally, these blocks of time should be used while making a free/busy lookup for that user.

In the background, the Kalendar application receives and sends information to calendar servers as per their defined protocols. Among the data exchanged, there is a free/busy field. However, this field is used to represent fixed time periods only and doesn't provide a way to specify a repeating period of available/unavailable time. [RFC 7953](https://www.rfc-editor.org/rfc/rfc7953) is an improvement over this and would allow users to essentially publish their availability. 

This new information will be added in AVAILABILITY and VAVAILABILITY components and would be sent to calendar servers while syncing. During a free/busy lookup, the server (if it supports RFC 7953) will consider above components during free/busy calculation. 

#### Conclusion

I will be making more blog posts on my progress. Looking forward to working on this project!


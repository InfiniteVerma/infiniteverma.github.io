---
title: GSoC'23 Week 12 - Conclusion
date: 2023-08-28
summary: "GSoC - Conclusion"
description: ""
toc: true
readTime: true
autonumber: true
math: true
tags: ["cpp", "open-source", "kde"]
showTags: false
hideBackToTop: false
---

12 weeks have passed and this is my concluding blog post on GSoC project: [Implement calendar availability](https://community.kde.org/GSoC/2023/Ideas#Project:_Implement_calendar_availability).

Through the past 3 months, most of the pieces for the feature were implemented and published on MRs. There's some loose ends to tie up and then we'll be good to go :)


#### Project introduction

Our goal was to implement calendar availabilty. Through this, users should be able to update their availability via the Merkuro (formerly Kalendar) application. 
Once updated, if someone wants to invite this person for an event, the free/busy lookup done would take into consideration the above new information.
This would help suggest better intelligent times to schedule events.

#### Design in short

The task required supporting the new ical components `Availability` and `VAVAILABILITY` in the backend. 
This includes adding/editing, parsing, serializing/de serializing them alongside the other already supported ical components. 
The above code mostly sits in the `KCalendarCore` codebase. 

Then comes the middleware repositories through which a typical frontend calls add/edit/view availability. These include `Akonadi-Calendar` and `Akonadi`. 

Finally we have the frontend `Merkuro` through which users should be able to add/edit/view their availability. While doing aforementioned operations, our middleware/backend part of code shall be touched. 

To summarize we needed changes in: 
 - `KCalendarCore`
 - `Akonadi-Calendar`
 - `Akonadi`
 - `Merkuro`

#### Progress

Backend and middleware part of the code is up and tested. `KCalendarCore` supports the new classes (class hierarchy shown in below photo. Along with new classes introduction, necessary tests were added to verify backend alone. 

![enter image description here](https://infiniteverma.github.io/assets/img/kde_available.png)

Regarding middleware (`Akonadi` and `Akonadi-Calendar`) some functions needed updates to support the new class `KCalendarCore::Availability` and the newly introduced mimetype `application/x-vnd-akonadi-calendar.availability`. Few tests were added as well to test middleware changes.

Then cames the frontend UI changes. A new UI page was added in `Merkuro` through which users can view/edit their availability. The first version would only support adding/editing one availability and not adding a higher priority entry (through supported by RFC). This would be added once this is finished and  merged :)

The UI needs some cleanup but below is a screenshot of the current version:

<img src="/assets/img/kde_article_3_ss.png" alt="image" width="800">

Open MRs:
-   [KCalendarCore changes](https://invent.kde.org/frameworks/kcalendarcore/-/merge_requests/150).
-   [Akonadi changes](https://invent.kde.org/pim/akonadi/-/merge_requests/145).
-   [Akonadi-calendar changes.](https://invent.kde.org/pim/akonadi-calendar/-/merge_requests/71)
-   [Merkuro changes.](https://invent.kde.org/pim/merkuro/-/merge_requests/389)

#### Pending Tasks

Sadly, it could not be finished end to end during the duration of the soc. The remaining TODO items shall be done in the coming weeks. 

Pending tasks:
 - Fix the UI page code
 - Add more tests in middleware/frontend codebases
 - Test end to end
 - Add support for higher priority availability input

#### Conclusion

GSoC'23 with KDE was a very rewarding experience for me. There was a wide range of things to learn while working on this project from things like QML/qt codeflow to grappling with design patterns like pimpl. Through this journey, I not only have become more comfortable with things C++ syntax but also the workings of compilation/linking and how to effectively debug them. 

Beyond the technical knowledge, I gained valuable lessons on what I could improve on, notably time management and communication skills. With better handle of my time, I may have managed to put a neater tie on the bow. 

In retrospect, I am delighted that I chose to apply for this program despite contending with occasional imposter syndrome. I look forward to continuing my contributions to KDE and other open source projects I find interesting.

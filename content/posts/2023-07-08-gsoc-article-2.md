---
title: GSoC'23 Week 6 - KCalendarCore work almost done!
date: 2023-07-08
summary: "KCalendarCore work almost done"
toc: true
readTime: true
autonumber: true
math: true
tags: ["cpp", "open-source", "kde"]
showTags: false
hideBackToTop: false
---

6 weeks in, here's an update on my GSoC Project - [Implement calendar availability](https://community.kde.org/GSoC/2023/Ideas#Project:_Implement_calendar_availability). 

#### KCalendarCore changes

Over the past weeks, I've focused on to bring RFC7953 support to kcalendarcore codebase. This would help bring availability feature to the kalendar app (along with other calendar clients that use KCalendarCore). The progress was slower than expected due to some rewrites after improving the class design.

Here is the current class design:

![image](/assets/img/kde_available.png)

In order to not break existing `Incidence` structure, we made a new base class for these two classes. Essentially, `AvailableBase` is a copy of the IncidenceBase-Incidence structure. And as inheritance goes, the properties common to `Availability` and `Available` sits in `AvailableBase` and the rest are in their derived classes. 

There are tests added (which will grow) to quickly test the new changes I do. By running few parse tests (string-> ical), it's verified that libical supports these new iCal components! So it's just a matter of supporting all fields mentioned in RFC and our new kcalendarcore classes will work.

See my (painfully slow) work [here](https://invent.kde.org/frameworks/kcalendarcore/-/merge_requests/150).

#### Pending Work

 - KCalendarCore: If you view my MR, you'll see lots of TODOs sprinkled in it ;). Also `readAvailability`/`writeAvailability` methods need some more work.
 - KCalendar: Once above is done, I'll be moving on to adding the UI elements through which users will update their availability. The design would be similar to below:

<img src="/assets/img/article_2_1.png" alt="Image" width="600" height="400">

##### Side Note

Working on this project has been really fun so far. I've finally understood where there's a `d`/`d_ptr` pointer sprinkled everywhere in KDE codebases (called as the Pimpl Idiom). There are several other interesting designs that I admit I've gone into too many a rabbit hole.

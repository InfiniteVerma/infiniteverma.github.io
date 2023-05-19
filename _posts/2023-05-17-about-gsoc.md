---

layout: post
title: GSoC'23 with KDE
date: 2023-05-17
description: post abt GSoC 
categories: code
giscus_comments: true
related_posts: true
---
Just a couple of weeks back, I walked around my pg with bated breath, while 
waiting for the google summer of code email. With my naturally pessimistic 
deposition, I couldn’t help but assume that their email notifications were 
planned to favor the accepted candidates, which is why I found myself 
empty-handed even 15 mins past the official deadline.

However as expected, there were technical issues on their end which is why 
most of the folks got their emails an hour or so after the official deadline. 
Nevertheless, if anyone happened to pass by the 3rd floor of my pg, they may 
have seen me jumping up and down in my pajamas at almost 1 in the morning. 
Though as PGs are, my moment of unnatural jubilation may have gone unnoticed.

#### What is GSoC

Most BTech undergrad students would have heard of the phrase ‘google summer of code’ 
during their college days. I certainly remember hearing it in my first year at Manipal. 
I'd even go to say that ‘GSoC’ is a badge of honor not unlike the ‘iit’ label with 
students in Indian colleges (Note: I come from a private college so I am unsure how iit/nit folks feel about this)

Anyway, after removing all the flair, GSoC is a program organized and sponsored 
by google wherein you contribute to an organization over 3 months in the summer 
(hence ‘summer of code’). It has two broad types of projects 350 hrs and 175 hrs 
which correspond to either a full-time or a part-time project (‘large’ or ‘medium’ 
project). The two types of projects have different stipends with it.

Interested folks would start talking with >=1 organizations, make small patches, 
participate in community conversations, and then finally submit their proposals. 
The org mentors would go through the proposals and provide a list of accepted ones to 
GSoC team based on several factors like the submitted proposal, past work done with the 
org, other participation, slots available, etc.

Until two years ago, this program was limited to college students. Now, it’s been extended to everyone 18 and above.

#### My prep

Like many, I also tried to apply for GSoC in my college years. Unfortunately, with parts 
of imposter syndrome and procrastination, I never actually did in those 4 years. So 
when the program’s eligibility changed, I looked up again with renewed interest last 
December. Of course, as mentioned, the ‘GSoC tag’ would be good but more than that, 
I wanted to at least try applying once :)

So, come last December, I mustered enough courage to go through some GSoC material. 
By my great prowess at procrastination, I had enough ideas about it so I remember 
going straight to searching for orgs of my liking. My job is mostly C++ and Linux 
which is basically how I did my first filtering. Though I can write some node.js/flutter/js 
code, I made the smart decision of not overthinking about this and simply decided on a 
proposal requiring C++. And since I was a full-time employee now, I added another 
filter with a medium-level project.

KDE became my first choice. The docs were easy to read and already have a system 
with Linux, there was pretty low overhead on setting up the environment or checking 
out projects. Beyond KDE, I did search for other projects but after a few weeks in the 
community, decided to focus on this org only. It also wasn’t easy to multitask with 
several orgs when you’re already doing a full-time job.

Soon, I became more serious and it went from a ‘what if’ to ‘I should seriously try 
applying once’. I hopped to KDE Neon and tried to write/read some issues every day. 
Before the proposal phase started, I had 3 or so MRs merged in Kalendar and 10+ in total.

#### Proposal: Calendar Availability

My proposal is based on one of the proposed ideas by KDE: ["Implement calendar availability"](https://community.kde.org/GSoC/2023/Ideas#Project:_Implement_calendar_availability).
The link pretty much explains it. The project is extending the existing ical support to include 
elements in [RFC 7953](https://www.rfc-editor.org/rfc/rfc7953). 
This would allow users to better mention their free time. This new 
‘availability’ feature would be used by Kalendar to cleverly suggest times during which meetings/events can be scheduled.

With all the prep done, I’m looking forward to working on the project over the summer. 
There would be some challenges since I would be juggling this along with my full-time job 
but hey, that’s part of the fun.


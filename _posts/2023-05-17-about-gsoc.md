---
layout: post
title: GSoC'23 with KDE
date: 2023-05-17
description: post abt gsoc 
categories: code
giscus_comments: true
related_posts: true
---

Just a couple of weeks back, I walked around my pg with bated breath, while 
waiting for the google summer of code email. With the pessimistic nature that I have,
I assumed that their sending schedule was probably planned so that the accepted 
folks will get it first, which is why I haven't received even 15 mins post the deadline.

But as expected, there were technical issues on their end which is why most of the folks
got their emails an hour or so after the official deadline. Nevertheless, if anyone 
would've walked out of their rooms on the 3rd floor of my pg, they'd have seen me jumping
up and down in my pajamas at almost 1 in the morning. Though as PGs are, this may have
gone unnoticed. 

#### What is GSoC 

Most BTech undergrad students would have heard of this phrase 'google summer of code'
during their college days. I certainly remember hearing it in my first year at Manipal. I'd go
to say that 'gsoc' is a tag like 'iit' with students in Indian colleges (though I come from a
private college so not sure how iit/nit folks feel about it)

Anyway, after removing all the flair, gsoc is basically a google organized program wherein 
you contribute to an organization over the span of 3 months in the summer (hence 'summer 
of code'). It has two broad type of projects 350 hrs and 175 hrs which correspond to either a 
fulltime or a parttime project (they're called a 'large' and a 'medium' project respectively). 
The two types of projects have different stipends with it.

Interested folks would start talking with >=1 organizations, make small patches, participate 
in the community conversations and then finally submit their proposals. The org mentors would
go through the proposals and provide a list of accepted ones to gsoc team (based on their
proposal, work done till now, other participation, slots available etc).

Until two years ago, this program was limited to college students. Now, it's been extended to 
[everyone 18 and above](https://opensource.googleblog.com/2021/11/expanding-google-summer-of-code-in-2022.html).

#### My prep

As many, I also tried to apply for gsoc in my college years. Unfortunately, with parts of
imposter syndrome and procrastination, I never actually did in those 4 years. So when the program's
eligibility changed, I looked up again with renewed interest last december. Of course, as mentioned,
the 'gsoc tag' would be good but more than that, I wanted to atleast try applying once :)

So, come last december, I mustered enough courage to look through some gsoc material. By 
my great prowess at procrastination, I had enough idea about it so I remember going straight 
to searching for orgs of my linking. My job is mostly C++ and linux which is basically how I did
my first filtering. Though I can write some node.js/flutter/js code, I made the smart decision of 
not overthinking about this and simply decided on a proposal requiring C++. And since I was 
now a full time employee now, I added another filter with a medium level project. 

KDE became my first choice. The docs were easy to read and already having a system with linux, 
there was pretty low overhead on setting up the environment or checking out projects. Beyond KDE,
I did search for other projects but after few weeks in the community, decided to focus on this org only. 
It also wasn't easy to multitask with several orgs when you're already doing a fulltime job. 

Soon, I became more serious and it went from a 'what if' to 'I should seriously try applying once'. 
I hopped to KDE neon and tried to write/read some issue everyday. Before the proposal phase started, 
I had 3 or so MRs merged in Kalendar and in 10+ in total. 


#### Proposal: Calendar Availability

My proposal is based on on of KDE proposed ideas: ["Implement calendar availability"](https://community.kde.org/GSoC/2023/Ideas#Project:_Implement_calendar_availability)
The link pretty much explains it. The project is extending the existing ical support to include
elements in [RFC 7953](https://www.rfc-editor.org/rfc/rfc7953). This would allow users to better mention their
free times. This 'availability' would be used by kalendar to cleverly suggest times during which meetings/events 
can be scheduled.

With all the prep done, I'm looking forward to starting on the task. There would be some challenges since I would 
be juggling this along with my fulltime job but hey, that's part of the fun. 






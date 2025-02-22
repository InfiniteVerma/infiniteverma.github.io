---
title: "Writing an operating system - Introduction & current progress"
date: "2024-12-15"
summary: "Blog series tracking my os dev progress"
description: "Blog series tracking my os dev progress"
toc: true
readTime: true
autonumber: true
math: true
tags: ["linux", "os-dev", "c"]
showTags: false
hideBackToTop: true
---

## Introduction

This series of articles tracks my progress while I try to implement a kernel from scratch. Timeline for this kind of a project would stretch several months so it seems ideal to list out some basic features I'd like to implement and then perhaps stop there.

I've been interested in systems programming since my college days but I never really explored it properly back then. Thanks to my job at a telecom company, I've been dabbling a lot in low level embedded systems (c/c++) and been reading and writing multithreaded code that needs to efficiently use the limited memory and compute resources available.

After stumbling on many memory corruption/deadlocks/high cpu load/file corruption issues, I see a gap in my learning that if filled would speed up my development at work. Also, debugging all these kinds of issues are really fun. So here goes...

My inspiration and informal guide for this project is this youtube named sphaerophoria who implemented his own kernel following osdevwiki over a course of (I think) a year of videos. I plan to follow along and once a basic foundation is setup and running, will try to offshoot and implement on top of it.

My high level goal is to make a kernel with a minimal fs and a networking stack. I'll revisit this page once I get a better idea of the scope of this project and the time/effort I'll have to put in on this.

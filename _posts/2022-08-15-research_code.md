---
toc: true
layout: post
description: Learnings about writing research code.
categories: [setup, code]
title: Lessons from writing Research Code
---

Having written a good amount of research code for a while now, I was wondering what "good research code" can be construed as. This topic has been discussed heavily with a lot of good blog posts and materials on the internet (some I've found: [Hongyuan Mei's blog](https://www.hongyuanmei.com/blog/2021/researchcodebasics/), [Good Research Code Handbook](https://goodresearch.dev/), etc.). Personally, I have a checklist of things that potrays my version of the basic requirements of good research code, in the context of ease of use for other researchers/practioners:

1. Clear directory, functional structure to all the different contributions of the research code.
2. Simple docs to guide researchers who want to reproduce/modify certain parts of the pipeline (certainly helpful with docstrings hosted on [ReadTheDocs](https://readthedocs.org)).
3. Clear README to include instructions to run, cite, and contact-info authors
4. LICENSE File(specially when working at industrial labs)
5. Docker images for quick implementation
6. Code/tutorials to fiddle with and generate the plots of the experiments.

Special note: A good documentation in my observation(see point 2. above) has immensely helped me in navigating relatively new fields of research, particularly in Machine Learning.

## But why invest additional time in this ?

The recent trend suggests that most research code goes through multiple phases:

1. Quick, dirty implementation of the idea in mind
2. Write scripts to get results
3. Make code public 

Ideally, it should be something like this:

1. Quick, dirty implementation of the idea in mind.
2. Tidy code, structured implementation of both the boiler plate, previous work and the core contribution.
3. Write reproducible scripts and automate most metric collection, results charting and documentation to reduce manual work.
4. Once code goes public, spending some time in maintaining/addressing user issues.

You'll notice it's the second point that differentiates between good and terrible practices - tidying up code at the right time. Given the results of the quick prototype that backed your idea, it's clear that you'll be investing a good portion of your time diving deep into all the nuances of this prototype. This means there should be more research and **less manual work**. What manual work refers to here is often times bad code can result in a lot of manual work of coarsing through csvs, logs, metadata, and other things that shifts the focus from research to running scripts manually.

This means the tools you use(IDE, software, hardware) etc. is something you should be familiar with, mostly from previous experience on other projects. This ensures that:
1. Not a lot of time is spent on setup (at the start of the project) and publishing (at the end of the project)
2. Working within a comfortable zone of tools ensures productivity and consistency.

My [dev setup]({% postpost_url 2022-07-12-shortcuts %}) is a culmination of mostly research and some non-research tools that is mostly oriented towards working on Windows based local machines with WSL and Linux machines with GPUs. 

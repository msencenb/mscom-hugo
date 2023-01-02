---
title: "Macroservices - A Pragmatic Approach For Small Teams"
date: "2019-06-13"
categories: 
  - "software engineering"
tags:
  - "software engineering"
  - "startups"
---

In an ideal world, all software projects would be written well. Full test suite, a good ci/cd pipeline, and a general focus on maintainability.

If that's the world you live in, or your org spends a lot of time from the onset of a project optimizing for a clean codebase, this is nirvana. One well kept monolith keeps complexity down across the board. No complicated SOA, deployment tooling, or failure case handling. In my view, if in doubt as a small team, reach for the monolithic design pattern as long as possible.

However, there are many reasons the monolithic approach may not be the best tool for you. You need to increase team size, which implies partitioning the codebase for independent progress or efficiency. Or maybe you have lots of grimy code and you want to modernize some or all of it. When reading up on the various technological options out there, microservices as a pattern will immediately rise to the top.

But it's scary as hell! Suddenly you have lots of complex deployments, more surface area for failures, and lots of expertise that is not core to application level programming. The truth is that microservices comes with a high overhead cost that is not present with a monolith. Those high costs are often incompatible (or at least not a worthwhile investment) for small teams.

So what's a small team to do? I'd like to put forth the term 'macroservices' as a pragmatic approach. Macroservices should be defined as any application architecture that runs 2-20 individual services, with each service representing a medium sized codebase that handles a well defined part of your business,. The trick of it is to split out services carefully to maximize your gain from the split, while minimizing the overhead cost of running multiple services.

Sane microservices just doesn't have the same ring to it.

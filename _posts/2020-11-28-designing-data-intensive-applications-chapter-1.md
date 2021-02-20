---
layout: post
title:  "Designing Data-Intensive Applications. Chapter 1."
date:   2020-11-28 19:29:13 +0100
categories: DDIA
---
As programmers, we often work with various types of components such as databases, caches, queues, streaming or batch processing frameworks. All of these components fundamentally involve collecting and manipulating [symbols](https://en.wikipedia.org/wiki/Symbol_(formal)), with another word, data. By abstraction, we define those components as `data systems` and they are usually the foundation blocks and parts of any application. When designing any high-quality application, regardless of its size, there are three major recurring areas of concern: reliability, scalability and maintainability.   

**Reliability**

The application should be able to work as expected (does what it is expected to do, with an acceptable level of performance) even when encountering adversities (software/hardware faults, as well as human errors). Generally, it is better for the application to tolerate such adversities instead of trying to prevent them, as often they happen outside our control one way or another. Much research has been done on analysing the causes of adversities, and human error, more specifically, operator error is usually the one that causes more than half of the incidents. Software failure is the strong follow-up with hardware failure ranking on the bottom accounting for 10-25% of the incidents.

In the book, the author presented several approaches for improving reliability and minimizing chances for failure for both human operators, software and hardware systems.   

**Scalability**

It should be possible to scale up or down the scope and capacity of the application based on needs.

**Maintainability**

The majority of the time spent on any application during its lifecycle is for maintenance.
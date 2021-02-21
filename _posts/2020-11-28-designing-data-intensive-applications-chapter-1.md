---
layout: post
title:  "Designing Data-Intensive Applications. Chapter 1."
date:   2021-02-18 19:29:13 +0100
categories: DDIA
---
As programmers, we often work with various types of components such as databases, caches, queues, streaming or batch processing frameworks. All of these components fundamentally involve collecting and manipulating [symbols](https://en.wikipedia.org/wiki/Symbol_(formal)), with another word, data. By abstraction, we define those components as `data systems` and they are usually the foundation blocks and parts of any application. When designing any high-quality application, regardless of its size, there are three major recurring areas of concern: **reliability**, **scalability** and **maintainability**.   

### Reliability

The application should be able to work as expected (does what it is expected to do, with an acceptable level of performance) even when encountering adversities (software/hardware faults, as well as human errors). Generally, it is better for the application to tolerate such adversities instead of trying to prevent them, as often they happen outside our control one way or another. Much research has been done on analysing the causes of adversities, and human error, more specifically, operator error is usually the one that causes more than half of the incidents. Software failure is the strong follow-up with hardware failure ranking on the bottom accounting for 10-25% of the incidents.

In the book, the author presented several approaches for improving reliability and minimizing chances for failure for both human operators, software and hardware systems.   

### Scalability

This term describes the application's ability to handle an increasing amount of load. Before we try to optimize it, it is extremely important to be able to clearly define the type and parameters of 'load' placed on the application. 


#### Load

Taking Twitter as an example, one user can be followed by many users, and they in turn, are followed by more users. When one user posts a tweet, it must also be distributed to and updated on the home timeline for all of his/her followers. This 'fan-out' structure makes up the load challenge for Twitter, therefore distributions like followers per user along with tweet frequencies are their key load parameters.


#### Performance

Once the load has been established, we could go about investigating the influence on performance when the load increases. Being able to process tens of thousands of requests per second concurrently with minimal response time is one type of challenge; handling data with a throughput of ten gigabytes per second is another. 

How we measure performance it is as important as choosing the right metric. Taking response time as an example, measuring in __percentiles__ gives us the expected performance as well as worst case scenarios, but measuring as average time would give us way less usable information. Therefore, on the *Service Level Agreements* at data service vendors, where the agreed-upon level of expected performance is stated,  __percentiles__ are often used. 

### Maintainability

The majority of the cost spent on any application during its lifecycle is for maintenance - operational, correction of bugs, development of new features, adapting to new platforms etc. The author mentions three design principles that can improve maintainability:

#### Operability

It should be well-documented and easy for operators to configure, run, debug and start/restart the application. 

#### Simplicity

One should always aim at reducing the complexity and improving the readability of their code. This allows other developers to understand the system quicker. Simple code also brings the benefits of fewer bugs created. 

#### Evolvability

There always exists a possibility for code changes as the requirement changes, hence it is important to maintain the code as adaptable as possible for future development. 
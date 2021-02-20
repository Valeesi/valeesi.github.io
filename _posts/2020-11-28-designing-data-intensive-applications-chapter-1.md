---
layout: post
title:  "Designing Data-Intensive Applications. Chapter 1."
date:   2020-11-28 19:29:13 +0100
categories: DDIA
---
As programmers, we often work with various types of components such as databases, caches, queues, streaming or batch processing frameworks. All of these components fundamentally involve collecting and manipulating [symbols](https://en.wikipedia.org/wiki/Symbol_(formal)), with another word, data. By abstraction, we define those components as `data systems` and they are usually the foundation blocks and parts of any application. When designing a high quality application, regardless of its size, there are three major recurring areas of concern: reliability, scalability and maintainability.   

**Reliability**

The application should be able to run as expected even when encountering errors. 

**Scalability**

It should be possible to scale up or down the scope and capacity of the application based on needs.

**Maintainability**

The majority of the time spent on any application during its lifecycle is for maintenance.
---
toc: true
layout: post
description: Notes from 'Foundations of Data Systems' part of 'Designing Data-Intensive Applications' book
categories: [post]
title: Challenges of Data Systems
---

~ Notes from 'Foundations of Data Systems' part of 'Designing Data-Intensive Applications'

In the last few years, we have been rapidly moving from a compute-intensive to a data-intensive world.

Computing power is not the major limitation these days, amount, complexity, and speed of data is.

Following are the standard components of a typical data system:

- Databases to store and retrieve data

- Caches to remember expensive retrievals and faster reads

- Search indexes to search and filter data on keywords

- Stream processing to send/receive messages asynchronously

- Batch processing to periodically crunch large data

But different data systems have different requirements, and there are different ways to implement the above seemingly standard operations.

We need to figure out which tool or approach is best suited for our context, and we often need to combine more than one tools or approaches to fulfill specific requirements.

#datasystems #computing #complexity #database #search #analytics #data #sql

*****

[Ankit Rathi](https://www.ankitrathi.com/) *is a Principal Data Scientist,
published author & well-known speaker. His interest lies primarily in building
end-to-end AI applications/products following best practices of Data Engineering
and Architecture.*

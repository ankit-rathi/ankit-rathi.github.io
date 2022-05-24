---
toc: true
layout: post
description: Notes from 'Foundations of Data Systems' part of 'Designing Data-Intensive Applications' book
categories: [post]
title: Reliability in Data Systems
---

Reliability can be defined as continuing to work correctly, even when things go wrong.

A fault is usually defined as individual components of the system is failing while failure means when the system as a whole fails to provide required service.

In general, tolerating faults is preferred over preventing faults unless no cure exists.

Things can go wrong with faults and errors such as:

1. Hardware faults

2. Software errors

3. Human errors

Hardware faults: Until recently, most of the applications required a single machine and in case of a hardware fault, redundancy was sufficient.

But as data volumes and computing demands increased, applications started using multiple machines and hardware faults also increased proportionally.

Hence there is a shift towards building systems using software fault-tolerance techniques in addition to hardware redundancy. 

Such systems also have the operational advantage of rolling upgrades without planned downtime like for a single machine.

Software errors: Hardware faults a random but software errors are systematic which are triggered by unusual set of circumstances.
There is no quick solution but many small things like dealing with assumptions, thorough testing, measuring, monitoring and analysing data systems can help.

Human errors: Even with best intentions, humans are known to be unreliable. Configuration errors by operators are a leading cause of outages.
These errors can be resduced by: a) encourage the user to do the right thing b) provide sandbox to explore and experiment c) automated testing d) quick and easy recovery e) detailed and clear monitoring

Reliability is important even for non-critical applications, so we should be conscious in choosing to sacrifice reliability to reduce devlopment and operational costs.

~ my extended thoughts and notes from 'Foundations of Data Systems' part of 'Designing Data-Intensive Applications' book

#data #processing #analytics #storage #sql #datasystems

*****

[Ankit Rathi](https://www.ankitrathi.com/) *is a Principal Data Scientist,
published author & well-known speaker. His interest lies primarily in building
end-to-end AI applications/products following best practices of Data Engineering
and Architecture.*

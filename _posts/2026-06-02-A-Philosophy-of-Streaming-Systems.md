---
toc: true
layout: post
description: Treating Data Systems as a Unified, Unbundled Dataflow  
categories: [post]
title: A Philosophy of Streaming Systems 
---

> Treating Data Systems as a Unified, Unbundled Dataflow  

<p align="center">
  <img 
    src="https://github.com/user-attachments/assets/03faaadc-2b8d-4b9e-85f8-f3e6b69f320c"
    alt="A Philosophy of Streaming Systems"
    style="width:100%; max-width:1200px; height:auto; border-radius:8px;"
  />
</p>

Complex organizations exist because no single team, application, or database can understand every aspect of reality. As businesses grow, different systems emerge to solve different problems. Operational databases manage transactions, search engines support discovery, analytical systems generate insights, machine learning models make predictions, and caches improve performance. Each system specializes in a particular function because no single technology can optimize for every requirement simultaneously.

This specialization creates a new challenge. The problem is no longer storing or processing data. The problem becomes keeping multiple representations of the same reality synchronized. A customer may exist in a transactional database, a search index, a recommendation model, a dashboard, and a cache at the same time. If these systems drift apart, the organization loses trust because different systems begin telling different versions of the truth.

Traditional architectures often attempted to solve this problem by centralizing everything inside a database. Databases evolved to include indexes, views, triggers, constraints, and replication mechanisms so that multiple representations could remain coordinated. This worked well for many applications, but as organizations adopted increasingly specialized technologies, a single database could no longer contain every capability required by the business.

This led to a different philosophy. Instead of bundling every capability into one system, organizations began unbundling the database itself. Components that once existed inside a database became independent services connected through data movement. Search systems, analytical platforms, machine learning models, recommendation engines, and operational applications became separate participants in a larger information ecosystem.

Once systems become independent, synchronization becomes the central problem. Polling databases for changes is inefficient and creates unnecessary coupling. A more natural approach is to treat every change as an event and allow those events to flow through the organization. Data stops being something stored passively and becomes something moving continuously through interconnected systems.

This shift introduces a dataflow perspective. Reality generates events. Events become records in systems of record. Downstream systems consume those records and derive new forms of information. Search indexes, dashboards, aggregates, alerts, recommendations, and machine learning models are no longer viewed as independent assets. They become derived products of an underlying stream of organizational events.

In this view, application logic itself becomes a transformation process. Every system consumes information, applies business logic, and produces new information for downstream consumers. The organization begins to resemble a network of interconnected intelligence flows rather than a collection of isolated databases.

As more transformations are performed, an important architectural decision emerges. Computation can occur either when data is written or when data is read. Performing work during writes creates materialized views and precomputed results that make reads faster. Performing work during reads reduces storage costs but increases query complexity. Every index, cache, and materialized view represents a trade-off in where computation occurs within the dataflow.

The advantage of this architecture is that systems become loosely coupled. If a search index fails, the system of record remains intact. If a recommendation model becomes corrupted, the underlying events still exist. Since every derived system can be rebuilt from source events, failures become easier to isolate and recover from.

This naturally shifts the focus from immediate synchronization toward long-term correctness. Organizations often assume that consistency means every system must be updated instantly. In practice, users usually tolerate small delays. What they cannot tolerate is corruption, duplication, contradiction, or lost information. This creates a distinction between timeliness and integrity.

Timeliness asks whether information is current. Integrity asks whether information is correct. For most business processes, integrity matters more. A bank can tolerate a few seconds of delay in updating a dashboard, but it cannot tolerate an incorrect account balance. A retailer can tolerate delayed inventory updates, but it cannot tolerate losing orders.

Once integrity becomes the primary objective, synchronous coordination becomes less attractive. Distributed transactions attempt to force immediate agreement across systems, but they introduce complexity, latency, and fragility. Event-driven architectures instead prioritize reliable propagation of facts while allowing systems to converge asynchronously over time.

However, asynchronous systems create a new requirement. Since messages may be retried, delayed, or duplicated, operations must become idempotent. Unique identifiers allow systems to recognize repeated requests and prevent accidental duplication. Correctness therefore moves beyond databases and becomes an end-to-end property of the entire system.

This realization leads to a deeper principle. No infrastructure component can guarantee correctness by itself. Correctness emerges from the interaction of applications, events, identifiers, constraints, monitoring, and recovery mechanisms working together. Reliability becomes a property of the entire information flow rather than any individual technology.

As organizations increasingly structure themselves around streams of events, another capability emerges. Because every transformation is explicitly defined, derived systems become reproducible. If business logic changes, outputs can be regenerated from historical events. If corruption occurs, systems can be rebuilt. If audits are required, every decision can be traced back to its originating facts.

The result is a fundamentally different way of thinking about data systems. Instead of viewing applications as isolated programs connected to databases, organizations begin viewing themselves as networks of continuously evolving information flows. Systems of record capture reality, event streams distribute changes, transformations create intelligence, and derived systems make that intelligence accessible throughout the organization.

The deeper insight is that modern data architecture is not really about databases, pipelines, or stream processors. It is about building an organization that can continuously observe reality, propagate information, derive knowledge, recover from failure, and adapt to change. Streaming systems represent the evolution of that idea, where intelligence emerges not from any single system, but from the reliable flow of information across the entire organizational network.

> Checkout my new book here: <https://ankit-rathi.github.io/store/>

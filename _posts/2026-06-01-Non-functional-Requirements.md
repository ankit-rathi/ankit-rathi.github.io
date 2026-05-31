---
toc: true
layout: post
description: The Hidden Requirements 
categories: [post]
title: Non-functional Requirements 
---

> The Hidden Requirements

<p align="center">
  <img 
    src="https://github.com/user-attachments/assets/500182f1-43cc-4d87-8035-88e57cd4850d"
    alt="Non-functional Requirements"
    style="width:100%; max-width:1200px; height:auto; border-radius:8px;"
  />
</p>

When organizations build software systems, they usually begin by focusing on functionality. They ask what the system should do, what features users need, what data should be stored, and what actions should be supported. But once a system starts operating in the real world, functionality alone quickly becomes insufficient. A system that technically works but frequently crashes, becomes slow under load, or is impossible to maintain eventually fails to create value. This is why the most important challenges in data systems are often not functional requirements but nonfunctional requirements.

The reason is simple. Organizations do not merely need systems that work. They need systems that continue working as the business grows, users increase, failures occur, and requirements evolve. The real challenge therefore becomes designing systems that remain useful under changing conditions. This introduces four fundamental concerns: reliability, performance, scalability, and maintainability.

Reliability emerges because failures are unavoidable. Hardware fails, networks disconnect, software contains bugs, and humans make mistakes. The question is not whether faults will occur but whether the overall system can continue operating when they do. A reliable system is therefore not a system without faults. It is a system that prevents individual faults from becoming user-visible failures. This is why redundancy becomes important. Multiple disks, multiple servers, and multiple copies of data ensure that the failure of one component does not stop the entire service.

However, reliability extends beyond hardware. Software failures are often more dangerous because they can affect every machine running the same code. Human errors create similar risks through incorrect configurations, deployments, or operational actions. As systems become more complex, resilience requires not only technical safeguards but also organizational learning mechanisms such as monitoring, rollback capabilities, automation, and post-incident analysis.

Once a system is reliable enough to operate continuously, performance becomes the next challenge. Users care about how quickly systems respond to their requests. But performance is not a single number. Different users experience different response times depending on system conditions. Averages often hide these differences. Most users may receive fast responses while a small percentage experience severe delays. For this reason, understanding performance requires examining the full distribution of response times, especially the slowest experiences that directly affect user satisfaction.

Performance naturally leads to scalability. As businesses grow, the amount of data, users, and requests increases. A system that performs well today may become unusable tomorrow if it cannot handle additional load. Scalability is therefore the ability to maintain acceptable performance as demand grows. Achieving this requires understanding the specific nature of the workload. Different applications experience different forms of load, and each requires different scaling strategies.

One option is to increase the power of individual machines. This approach, known as vertical scaling, is simple but eventually becomes expensive and limited. Another option is to distribute the workload across many machines. This horizontal scaling approach offers greater long-term growth potential but introduces coordination challenges between independent systems. Organizations must therefore constantly balance simplicity against scalability.

As systems become larger and more distributed, complexity increases. Complexity eventually becomes one of the greatest threats to organizational productivity because every change becomes harder, every bug becomes more difficult to diagnose, and every new requirement becomes more expensive to implement. This creates the final nonfunctional requirement: maintainability.

Maintainability exists because software systems are never finished. Businesses evolve, customer expectations change, regulations emerge, and competitive pressures create new requirements. Systems must therefore be designed not only for current needs but also for future adaptation. This requires making systems understandable, operable, and flexible.

Operability ensures that teams can monitor, manage, and troubleshoot systems effectively. Simplicity reduces unnecessary complexity through clear abstractions that hide implementation details while preserving functionality. Evolvability ensures that future changes can be made without rebuilding the entire system. Together these qualities allow organizations to continuously improve systems without losing control over them.

Viewed from first principles, reliability protects the system from failure, performance ensures acceptable user experience, scalability enables growth, and maintainability enables adaptation. These are not independent concerns but interconnected design goals that determine whether a system remains useful over time.

Ultimately, data systems exist to support organizational decisions and operations. Functional requirements define what a system does, but nonfunctional requirements determine whether it can sustain that value as reality changes. The most successful systems are therefore not those with the most features, but those that can remain reliable, performant, scalable, and maintainable while the organization itself continues to evolve.

> Checkout my new book here: <https://ankit-rathi.github.io/store/>

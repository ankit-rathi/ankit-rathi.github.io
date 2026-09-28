---
toc: true
layout: post
description: Applying first principles to an AI-driven investment system reveals that consistency, validation, and trust remain unsolved problems
categories: [post]
title: Agentic AI Meets Quantvesting - Where Structured Intelligence Breaks Down
---

> Applying first principles to an AI-driven investment system reveals that consistency, validation, and trust remain unsolved problems

When I started experimenting with Agentic AI, I did not approach it as a generic AI exercise. I applied it to something I understand well—my Quantvesting framework. The idea was simple: if an agent can replicate structured investment thinking, then it should be able to gather information, evaluate businesses, apply a framework, and arrive at a reasoned decision. I built a basic decision agent with steps for information gathering, pros and cons, evaluation, critique, and iteration. What looked coherent on the surface quickly exposed deeper limitations when viewed from first principles.

At the foundation, any decision system depends on inputs, processing, and evaluation. In my setup, the inputs were generated or summarized by the model itself, which immediately created a dependency on token limits and cost constraints. This restricted how much context the system could consider, which in investing directly translates to incomplete understanding. Even when the same input was passed multiple times, the outputs varied due to non-deterministic behavior, making it difficult to rely on a single run for decision-making. This lack of reproducibility weakens the core requirement of any investment framework, which is consistency of reasoning.

As I moved to evaluation, the problem became more structural. In investing, there is rarely a clear ground truth in the short term, and the system ended up in a loop where one probabilistic output was being evaluated by another. This self-referential validation created internally consistent narratives without external anchoring. When the input itself was shallow or incomplete, the system still produced clean, structured outputs, highlighting the classic garbage in, garbage out problem, but with an added layer of false confidence due to formatting.

The next layer of issues came from how the system was controlled. Small changes in prompts led to disproportionately different outputs, exposing prompt fragility. The system could be tuned to perform well on specific cases but failed to generalize, indicating overfitting to prompts rather than learning underlying principles. Even when I introduced memory, it did not behave like true stateful understanding but rather as partial context retrieval, constrained further by context window limitations.

Operationally, the agent loop introduced latency. Each step—gathering, structuring, evaluating, critiquing—added delay, which makes such systems impractical for real-time or repeated use without optimization. When external data sources are introduced, this expands into dependency risks, where failures, inconsistencies, or stale data can distort the entire decision pipeline. In investing, where data accuracy is critical, this becomes a significant limitation.

Another subtle but important issue was the illusion of intelligence. The system produced well-structured, articulate outputs aligned with the Quantvesting framework, but that did not guarantee correctness. The presence of structured fields and confident language created a perception of rigor that may not exist in reality. This is amplified when output formatting itself becomes unreliable, such as JSON inconsistencies, which break downstream processing.

Over time, alignment drift becomes inevitable. As prompts evolve, models update, or configurations change, the system’s behavior shifts, often without explicit visibility. This makes debugging difficult, as failures are not always deterministic or traceable. The absence of reproducibility further complicates this, since the same issue may not surface consistently. In an enterprise context, this extends into security risks, potential data leakage, and governance challenges, especially when sensitive financial reasoning or proprietary frameworks are involved.

Maintaining such a system also introduces ongoing overhead. Prompts need refinement, models require updates, scoring mechanisms must evolve, and evaluation criteria need to be strengthened. Designing meaningful evaluation metrics itself becomes a challenge, particularly in domains like investing where outcomes are delayed and multifactorial. As the system scales, both cost and performance constraints become more visible, and without careful design, they can outweigh the benefits.

All of this ultimately impacts trust. A system that is non-deterministic, difficult to validate, and prone to drift cannot be blindly relied upon for decision-making. The gap between explainability and actual correctness becomes a critical concern, especially when the system is used to support or automate financial decisions.

The conclusion is not that Agentic AI is ineffective, but that it is fundamentally constrained by how well the underlying decision system is designed. Applying it to Quantvesting made this clear: the model can assist in structuring thinking, exploring scenarios, and identifying blind spots, but it cannot replace the need for deterministic rules, real data grounding, and a well-defined evaluation framework. The real leverage does not come from chaining multiple agents, but from integrating probabilistic reasoning within a system that is anchored in first principles, explicit constraints, and measurable validation.

> Checkout my new book here: <https://ankit-rathi.github.io/store/>

---
toc: true
layout: post
description: How Evidence Should Change What You Believe  
categories: [post]
title: Bayes Theorem
---

> How Evidence Should Change What You Believe

<p align="center">
  <img 
    src="https://github.com/user-attachments/assets/3497abe5-08ea-4438-a4b1-13711758c0e7"
    alt="Bayes Theorem"
    style="width:100%; max-width:1200px; height:auto; border-radius:8px;"
  />
</p>

*From a probability formula to a practical framework for reasoning under uncertainty.*

---

Imagine a fraud detection system flags a transaction.

The system is **90% effective at detecting fraud**.

Should you conclude that there is a 90% chance the transaction is fraudulent?

Not necessarily.

The answer depends on something that is easy to overlook:

**How common is fraud in the first place?**

This is where Bayes' theorem becomes much more than a formula from a probability textbook. It gives us a structured way to combine what we believed before seeing the evidence with what the new evidence tells us.

And that idea sits at the heart of many Data and AI systems:

> **Evidence → Updated belief → Decision**

---

## 1. The Core Idea

Bayes' theorem answers a deceptively simple question:

> **After observing some evidence, how should I update my belief about a hypothesis?**

Suppose:

* \(A\) = a transaction is fraudulent
* \(B\) = the transaction was flagged

What we want to know is:

$$
P(A|B)
$$

the probability of fraud **given that it was flagged**.

But we may instead know:

$$
P(B|A)
$$

the probability that the system flags a transaction **given that it is fraudulent**.

These are not the same thing.

Bayes gives us the bridge:

$$
\boxed{
P(A|B)=
\frac{P(B|A)P(A)}
{P(B)}
}
$$

The deeper idea is:

```text
What I believed
      +
What I observed
      ↓
Updated belief
```

That's Bayesian reasoning in one picture.

---

# 2. The Theory

Bayes builds on **conditional probability**.

\(P(A|B)\) means:

> The probability of A, given that B has occurred.

The four components of Bayes are:

| Component | Meaning                                             |                                                       |
| --------- | --------------------------------------------------- | ----------------------------------------------------- |
| \(P(A)\)  | Prior — what we believed before seeing the evidence |                                                       |
| (P(B      | A))                                                 | Likelihood — how compatible the evidence is with A    |
| \(P(B)\)  | Evidence — how likely the evidence is overall       |                                                       |
| (P(A      | B))                                                 | Posterior — what we believe after seeing the evidence |

So we can think of Bayes as:

$$
\text{Posterior}
=
\frac{\text{Likelihood}\times\text{Prior}}
{\text{Evidence}}
$$

For more complex Bayesian inference, this is often expressed as:

$$
P(\theta|D)\propto P(D|\theta)P(\theta)
$$

where \(\theta\) represents an unknown parameter and \(D\) represents observed data.

This moves Bayes from a probability exercise into a general framework for **statistical inference**.

---

# 3. The Intuition: Evidence Doesn't Exist in Isolation

Suppose someone tells you:

> "This signal catches 90% of fraudulent transactions."

That sounds impressive.

But your next question should be:

> **90% of what? And how common is fraud?**

Imagine fraud occurs in only **1% of transactions**.

Now suppose:

* 90% of fraudulent transactions are flagged.
* 5% of legitimate transactions are also flagged.

Consider 10,000 transactions.

```text
10,000 transactions

100 fraudulent
 └── 90 flagged

9,900 legitimate
 └── 495 falsely flagged
```

So there are:

```text
585 flagged transactions
90 are actually fraudulent
```

Therefore:

$$
P(Fraud|Flagged)
=
\frac{90}{585}
\approx15.4\%
$$

The signal catches **90% of fraud**, yet a flagged transaction has only about a **15.4% probability of actually being fraudulent** under these assumptions.

Why?

Because the starting point—the **base rate**—was very low.

This is one of the most important lessons from Bayes:

> **Strong evidence does not automatically imply a high posterior probability.**

You have to consider both the evidence and the starting probability.

---

# 4. Where Bayes Appears in Data & AI

Bayesian reasoning appears in many places.

### Classification

Naive Bayes applies Bayes' theorem to classification problems.

For example, given the words in an email, a model can estimate:

$$
P(Spam|Words)
$$

and compare it with:

$$
P(NotSpam|Words)
$$

Naive Bayes makes a simplifying conditional-independence assumption, which makes inference computationally practical for certain problems.

### Fraud and risk

Evidence from transactions, devices, locations and behavioural patterns can be used to estimate the probability of a hidden state such as fraud.

The important lesson isn't that every fraud system should use Bayes.

Modern systems may use rules, tree-based models, neural networks, graph techniques or ensembles.

The deeper principle is:

> **Observed evidence can be used to reason about an unobserved state.**

### Bayesian modelling

Bayesian methods can estimate uncertain parameters rather than simply assigning classes.

For example:

```text
Prior assumptions
       +
Observed data
       ↓
Posterior distribution
       ↓
Parameter estimates + uncertainty
```

This is useful when understanding **uncertainty around an estimate** matters as much as the estimate itself.

### Bayesian optimization

Bayesian methods can also help decide what to try next when evaluating an experiment or model is expensive.

So Bayes isn't restricted to:

> "What class does this observation belong to?"

It can become part of a broader framework for **learning and decision-making under uncertainty**.

---

# 5. What Textbooks Often Don't Tell You

The formula can be perfectly correct and your answer can still be practically wrong.

Why?

Because Bayes doesn't fix bad assumptions.

Consider the fraud example.

What if the historical fraud rate was 1%, but fraud suddenly increases to 5%?

The same detection signal will now produce a different posterior probability.

The mathematics hasn't changed.

**Reality has.**

This is where production systems introduce problems that aren't obvious from the formula:

* Is the data representative?
* Is the base rate still valid?
* Has the population changed?
* Are the measurements reliable?
* Are the model assumptions still reasonable?
* Are probabilities calibrated?
* What happens when evidence is missing?
* How often should the model be recalibrated?

A Bayesian model can therefore fail without there being anything wrong with Bayes' theorem.

The problem may be the **inputs, assumptions or operating environment**.

---

# 6. Probability Is Not the Decision

This is perhaps the most important step from **Data → Decisions**.

Suppose our system estimates:

$$
P(Fraud|Evidence)=15\%
$$

Should we block the transaction?

Not necessarily.

The answer depends on the consequences of being wrong.

For example:

```text
Evidence
   ↓
Probability
   ↓
Decision threshold
   ↓
Action
   ↓
Outcome
```

If blocking a legitimate customer is extremely costly, we may require a very high probability before blocking.

If allowing a fraudulent transaction is extremely costly, we may act at a much lower probability.

Therefore:

> **A probability tells us what is likely. It doesn't, by itself, tell us what we should do.**

That requires decision theory, costs, constraints and context.

---

# 7. The Architectural Perspective

Bayesian reasoning can sit inside a larger decision system:

```text
             DATA SOURCES
                  │
                  ↓
             DATA PIPELINE
                  │
                  ↓
           FEATURES / SIGNALS
                  │
          ┌───────┴───────┐
          ↓               ↓
        PRIOR          EVIDENCE
          │               │
          └───────┬───────┘
                  ↓
           PROBABILISTIC
              MODEL
                  │
                  ↓
              POSTERIOR
                  │
                  ↓
             DECISION LOGIC
                  │
                  ↓
                ACTION
                  │
                  ↓
               OUTCOME
                  │
                  └──────→ FEEDBACK
```

Notice the separation.

The **model layer** answers:

> "What is the probability?"

The **decision layer** answers:

> "What should we do?"

This separation becomes important when building real Data and AI platforms.

A probability model may be reused by multiple downstream decisions, each with different costs and thresholds.

---

# 8. Best Practices—and Common Mistakes

### 1. Don't confuse the direction

$$
P(A|B)\neq P(B|A)
$$

They answer different questions.

### 2. Always consider the base rate

Especially when dealing with rare events.

### 3. Make assumptions explicit

Where did the prior come from?

What assumptions does the likelihood make?

### 4. Validate the evidence

Bad or biased data can produce a misleading posterior.

### 5. Monitor changing reality

Population shifts and changing base rates can invalidate previously useful probabilities.

### 6. Care about calibration

If a system says "80% probability," that number should have a meaningful interpretation when probabilities drive decisions.

### 7. Separate probability from action

Don't let:

```text
Model output = automatic decision
```

become your architecture by accident.

---

# 9. A Practical Decision Framework

When you encounter an uncertain situation, ask:

### Before seeing the evidence

**What did I believe, and why?**

→ Prior

### After seeing the evidence

**How strongly does this evidence support the hypothesis?**

→ Likelihood

### After updating

**What should I believe now?**

→ Posterior

### Before trusting the answer

**Are the data and assumptions still valid?**

→ Validation

### Before acting

**What is the cost of being wrong?**

→ Decision theory

### After acting

**What happened, and what should I learn from it?**

→ Feedback

So the complete loop becomes:

```text
PRIOR
  ↓
EVIDENCE
  ↓
UPDATE
  ↓
POSTERIOR
  ↓
VALIDATE
  ↓
DECIDE
  ↓
ACT
  ↓
LEARN
  ↺
```

This is the point where Bayes becomes relevant far beyond a statistics classroom.

---

# Final Takeaway

Bayes' theorem is often introduced as a formula for calculating conditional probability.

That's correct—but incomplete.

Its more useful interpretation is:

> **Bayes is a mathematical engine for updating what we believe when new evidence arrives.**

And in a real Data/AI system, there is one more step:

> **Updated belief is not the end of the process. We still have to decide whether that belief is reliable enough—and valuable enough—to act upon.**

That is the journey from:

**Probability → Inference → Data → Decision.**

---

## One-line takeaway

> **Bayes teaches us not just how to calculate probability, but how evidence should change what we believe—and whether that belief is reliable enough to drive a decision.**

### References to verify/cite

1. MIT OpenCourseWare — *18.05 Introduction to Probability and Statistics*
2. MIT OpenCourseWare — *18.600 Probability and Random Variables*
3. Stanford CS109 — *Probability for Computer Scientists*
4. scikit-learn — *Naive Bayes*
5. Google Developers — *Bayesian Inference / Meridian*

> Checkout my new book here: <https://ankit-rathi.github.io/store/>

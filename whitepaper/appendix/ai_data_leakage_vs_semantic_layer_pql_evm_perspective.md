# What if AI isn’t leaking data — but your system is?

> This is the first post in a short series on AI, semantic systems, and data security.
>
> I’m not an AI expert. I’m looking at what AI is exposing in our data systems.

## The fundamental tension between AI data leakage and semantic systems

> Imagine a scenario:
>
> User A queries a product information system.
> The system automatically traverses relationships through a semantic layer: Product → Owner → Email.
>
> User A has never been authorized to access Owner information.
>
> Yet the AI produces a perfectly “reasonable” answer — including the Owner’s email.
>
> The question is:
>
> 👉 **Is this an AI problem, or a system design problem?**

---

## 1. Problem Definition

With the widespread adoption of AI (especially LLM + RAG), more and more systems are introducing:

- Semantic layers (Semantic Layer / Knowledge Graph)
- Multi-source data aggregation (cross-system data integration)
- Context enrichment

A common misconception is:

> A semantic layer improves data understanding, therefore it should also improve security.

**This is incorrect.**

---

## 2. Core Insight

> Semantic layers solve a *comprehension* problem, not an *isolation* problem.

Even more importantly:

> AI does not provide a security boundary. It is a probabilistic generation system.

It assumes the boundary has already been enforced.

Therefore:

> **AI data leakage is not a model problem — it is an architectural problem.**

---

## 3. The Fundamental Limitation of LLMs

Key properties of LLMs:

- No tenant isolation
- No inherent access control awareness
- Context-driven reasoning

In other words:

> LLMs do not understand the difference between “your data” and “someone else’s data.”

They only operate on:

- The current prompt
- The provided context

---

## 4. The Real Risk: Context Injection

A typical AI execution flow:

```
User Query
   ↓
RAG / API / DB
   ↓
Context Injection
   ↓
LLM
   ↓
Response
```

Critical observation:

> Once data enters the prompt, the model assumes it is allowed to use it.

If access control happens *after* this stage:

→ It is already too late.

---

## 5. The Amplification Effect of Semantic Systems

Capabilities of semantic systems:

- Cross-entity relationships (joins / graph traversal)
- Unified abstraction
- Context enrichment

A key side effect:

> **Data reachability is dramatically increased.**

Reachability defines not what data exists,
but what data can be *arrived at*.

### Example

```
Product → Owner → Email
```

Even if a user is only authorized to access Product:

→ They may indirectly obtain sensitive Owner data via semantic paths

This leads to:

> **Inference-based data leakage**

---

## 6. AI-Specific Leakage Patterns

### 1. Prompt Injection

Attackers manipulate inputs to:

- Override rules
- Extract sensitive data

---

### 2. RAG-based Data Exposure

Root cause:

- Vector retrieval lacks strong access control
- Similarity ≠ authorization

---

### 3. Inference Leakage

Sensitive data reconstructed across multiple interactions:

```
Q1 → partial info
Q2 → additional info
→ reconstructed sensitive data
```

---

## 7. Common Misconceptions

### ❌ Misconception 1: Semantic Layer = Security Layer

Reality:

> Semantic layers increase accessibility, not restrict it

---

### ❌ Misconception 2: LLMs Can Enforce Security

Reality:

> LLMs are not security boundaries — they are executors

---

### ❌ Misconception 3: RAG is Safe by Default

Reality:

> RAG is one of the most common leakage vectors

---

## 8. A Deeper Question (for the reader)

If the above is true, then a more fundamental question emerges:

> In systems with strong semantic capabilities (joins, context enrichment, cross-system integration),
> **how should we define the boundary of data access?**

Traditional answers:

- Row-level ACL
- Table-level permissions

But in AI + semantic systems, these are no longer sufficient.

Because the question is no longer:

> “Can you access this data?”

But rather:

> **“Can you reach this result through a semantic path?”**

---

## 9. A Direction Worth Considering

Perhaps we need to redefine security itself:

> Security is not just a property of data — it is a constraint on reachability.

If that is the case:

- Who defines which paths are allowed?
- At what stage is reachability enforced?
- Should semantic layers take on part of the security responsibility?
- Is AI merely exposing an already existing problem?

Today, these questions still lack clear answers in the industry.

---

## 10. Closing (Open-ended)

> AI did not create new security problems.
>
> It simply revealed something we never properly defined:
>
> **the true boundary of data access.**

And most systems were never designed to answer that question.

---

## 11. Series Continuation

1. AI Data Leakage Taxonomy
2. Semantic Layer vs Security Model
3. Why RAG is fundamentally unsafe
4. Security-aware Semantic Architecture

---

## 12. Vocabulary (Working Definitions)

To avoid ambiguity, we use the following terms:

### Security Context Propagation

> Passing user identity, permissions, and execution context across system boundaries so downstream systems can make authorization decisions.

- Focus: **movement of context**
- Scope: cross-service / cross-system

---

### Security Context Pushdown

> Ensuring that authorization is enforced as close to the data as possible by applying the propagated security context at the data source.

- Focus: **where enforcement happens**
- Scope: data source / storage layer

---

### Reachability

> Not what data exists, but what data can be *arrived at* through valid paths in the system.

- Focus: **paths, not objects**

---

### Key Distinction

> Propagation moves context.
> Pushdown enforces it.
> Reachability determines whether a result should be reachable at all.

---

(End)


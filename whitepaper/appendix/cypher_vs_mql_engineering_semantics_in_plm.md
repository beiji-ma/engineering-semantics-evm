# Cypher vs MQL: Engineering Semantics in PLM

## One‑sentence takeaway (engineering perspective)

> **Neo4j is an excellent graph database. However, in the PLM domain, classical PLM platforms are designed closer to real engineering needs.**  
> **Using MatrixOne (the core engine of 3DEXPERIENCE) as an example, MQL is inherently closer to semantic querying than Cypher.**  
> This is not about technology superiority, but about domain intent and design goals.

---

## 1. The BOM problem is *not* a structure‑storage problem

From an engineering standpoint, BOM structures have long been a solved problem:

- Trees, DAGs, and graphs
- Parent–child and multi‑reference relationships
- Relational tables, XML, JSON, STEP

All of this has existed for decades.

**The real challenge is not how to store structure, but:**

- What does this structure *mean* in engineering terms?
- Under which time, configuration, and lifecycle context is it valid?
- After a change, is it still considered the *same* engineering object?

> **A BOM is a semantic, time‑evolving engineering construct — not a static graph.**

---

## 2. Cypher: a powerful computational query language

Cypher excels at:

- Explicit node‑edge modeling
- Pattern matching and traversal
- Constraint‑based search
- Combinatorial resolution

Typical Cypher questions look like:

> Starting from A, following relationships that satisfy certain constraints, which nodes are reachable?

This is fundamentally a **computational problem**, focused on:

- Reachability
- Valid combinations
- Mathematical consistency

For configuration solving and optimization, this is extremely powerful.

---

## 3. Engineering reality: “solvable” does not mean “engineering‑valid”

In real PLM scenarios, engineers usually ask different questions:

- What *is* this object at a given point in time?
- Does this change represent an evolution or a new identity?
- Do configuration rule changes affect historical releases?
- Is this result valid in terms of engineering responsibility and accountability?

The key concepts here are:

> **Semantics, time, versioning, effectivity, and change**

—not nodes, edges, or traversal paths.

---

## 4. MQL: a language born from engineering semantics

Another subtle but important distinction lies in **language design itself**.

### 4.1 Recognition‑based vs construction‑based DSLs

From a practitioner’s perspective, MQL feels closer to a *conceptual* or *recognition‑based* language than a purely technical DSL. Its constructs map directly to stable engineering concepts (type, relationship, revision, state), which makes the language largely **self‑describing**.

In practice, many users report that they can understand and apply MQL after only a brief exposure — often without memorizing syntax, keywords, or traversal patterns. The language invites *recognition* of familiar domain concepts rather than *construction* of abstract query expressions.

By contrast, Cypher is a **construction‑based DSL**. Its expressiveness comes from explicitly assembling graph patterns, bindings, and paths. This is powerful, but it also imposes a higher cognitive load and requires users to think first in graph‑theoretical terms, and only then map those constructs back to the engineering domain.

This distinction is not about intelligence or experience; it reflects design intent:

- **MQL was shaped around a specific, stable domain vocabulary**
- **Cypher was shaped around a generic computational abstraction**

As a result, MQL often feels simpler and more intuitive in PLM contexts — not because it is less capable, but because it speaks the language of the domain directly.

A crucial — and often overlooked — fact:

> **MQL was designed natively for semantic modeling and PLM. Cypher was not designed for the PLM domain.**

This is not a weakness of Cypher; it simply reflects different origins.

Using MatrixOne (the core engine of 3DEXPERIENCE) as an example, MQL queries:

> **Engineering objects as they exist within a semantic and lifecycle context — not just graph structures.**

MQL inherently understands concepts such as:

- Object types
- Lifecycles and states
- Revisions and versions
- Relationships as semantic links (not raw edges)
- Access control, views, and lifecycle‑aware query behavior

In practice, MQL statements describe *what an object represents* under a given engineering context — not *how to traverse a graph*.

---

### 4.2 Domain maturity and language design (a conceptual ladder)

The contrast between MQL and Cypher can be generalized as a domain‑maturity progression:

| Domain maturity stage | Dominant modeling approach | Typical language style |
|----------------------|----------------------------|------------------------|
| Exploratory / loosely defined | Generic graphs | Construction‑based DSLs |
| Emerging specialization | Hybrid models | Mixed abstractions |
| Mature engineering domain | Explicit semantic models | Recognition‑based DSLs |

As domains mature, they tend to converge on **purpose‑built data models and dedicated languages**. General‑purpose abstractions remain useful as execution substrates, but they gradually disappear behind domain‑specific semantics.

---

## 5. Why classical PLM platforms do not expose “the graph” as a first‑class abstraction

A common misconception is that classical PLM systems “do not understand graphs.”

In reality:

- DAGs and relational graphs are well understood
- Graph structures exist internally

They are intentionally **not exposed as first‑class abstractions**, because:

> **In engineering systems, graphs are implementation details — semantics are the product.**

As a result, classical PLM platforms deliberately:

- Embed lifecycle, change, configuration, and effectivity into the core model
- Trade flexibility for long‑term consistency and accountability
- Optimize for decades‑long product evolution, not short demos

---

## 6. Computational graph models vs engineering semantic models

| Dimension | Computational graph model | Engineering semantic model |
|---------|--------------------------|----------------------------|
| Primary goal | Find a solution | Ensure engineering validity |
| Core focus | Paths and constraints | Intent and responsibility |
| Time dimension | Current snapshot | Evolution over time |
| Change handling | Recompute | Preserve semantic commitments |
| Failure mode | No solution | Engineering incident |

These models are complementary — but not interchangeable.

---

## 7. A pragmatic (and slightly ironic) observation

There is also a practical engineering consideration that is rarely stated explicitly:

> **In most PLM scenarios, the graph algorithms actually required are neither exotic nor expensive to implement.**

Traversal, reachability, basic constraint checks, and impact analysis over DAGs are well‑understood problems. Implementing these directly—tailored to the domain model—often has a **lower cost and risk profile** than introducing a general‑purpose graph database.

General graph platforms inevitably come with a wide range of capabilities that are **irrelevant to PLM**, and in regulated, long‑lived engineering systems, *unused functionality is not neutral* — it becomes surface area for complexity, performance surprises, and operational risk.

Of course, for teams without strong graph or domain expertise, adopting an off‑the‑shelf graph engine and configuring it can be a perfectly reasonable shortcut.

In a slightly ironic sense, this also explains why general‑purpose graph databases often thrive in **non‑specialized or loosely defined domains** — where problems cannot (or are not yet) abstracted into precise domain models and dedicated DSLs, and where a flexible, generic graph abstraction is "good enough."

But in that case, the real bottleneck is rarely the database technology.

> **If neither the engineering domain nor the underlying graph principles are understood, the problem is no longer about choosing Neo4j versus MQL — it is about whether one should be building a PLM/BOM system at all.**


## 8. A grounding statement

> **If BOM challenges were merely about structure storage, the PLM industry would have been solved by 2005.**

It still exists because engineering problems are fundamentally semantic, temporal, and accountable.

---

## Final anchor

> **In PLM and data governance, graphs and knowledge graphs are not silver bullets.
> The hard part is rarely graph computation — it is defining, preserving, and evolving engineering semantics over time.**

## Closing thought

Graph databases are powerful execution engines.

PLM systems derive their value from something else:

> **Making engineering semantics a prerequisite for computation — not a by‑product of it.**

This distinction defines the real boundary between general‑purpose graph technology and engineering‑grade PLM systems.


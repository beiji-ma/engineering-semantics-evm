# Why “Graph-First PLM” Is Not a Semantic Model

## Abstract

In recent years, “graph-first” has become a popular narrative in the PLM and engineering IT space. Many articles and presentations suggest that moving from relational databases to graph databases is a prerequisite for achieving true digital thread, semantic modeling, or next-generation engineering platforms.

This paper argues that this assumption is fundamentally incorrect.

Graph technology can improve traversal efficiency and query ergonomics, but it does not constitute a semantic model. The core challenge in engineering systems is not data connectivity, but truth preservation over time. Without explicit semantics for identity, versioning, snapshots, and lineage, a graph-based system degrades into mutable structural chaos—regardless of how modern its infrastructure appears.

---

## 1. The Persistent Confusion: Structure vs Meaning

A recurring misunderstanding in system design is the belief that data structure implies semantic correctness.

Graph databases provide:

- Nodes
- Edges
- Traversal
- Pattern matching

What they do *not* provide is meaning.

Meaning is not encoded by the presence of an edge. Meaning emerges only when the system defines *what the edge represents*, *under which conditions it exists*, and *how it evolves over time*.

A graph can express relationships.
It cannot, by itself, express intent, causality, or truth.

This distinction is frequently overlooked.

---

## 2. Why Engineering Systems Are Fundamentally Temporal

Engineering data is not static.

Products evolve.
Configurations change.
Releases replace one another.
Decisions invalidate earlier assumptions.

The defining characteristic of engineering systems is not connectivity, but time.

Any system claiming to support digital thread must answer the following questions explicitly:

- What was true at a given moment?
- Which version was authoritative?
- Why did this change occur?
- Which later states depend on it?

These are not graph questions.

They are temporal semantics questions.

---

## 3. The Core Semantic Primitives That Actually Matter

Across decades of PLM implementations, the systems that survived long-term share a common set of semantic primitives—whether explicitly documented or not.

These include:

1. **Stable Identity**  
   Objects must retain identity independent of revisions or storage location.

2. **Snapshot Truth**  
   At any moment, there must exist an immutable statement of what was considered true.

3. **Version Semantics**  
   Change must not overwrite truth; it must create a new truth.

4. **Lineage and Derivation**  
   Later states must be explainable in terms of earlier ones.

5. **Causality**  
   A system must distinguish *what changed* from *why it changed*.

None of these emerge automatically from using a graph database.

They must be modeled.

---

## 4. Why Storage Technology Is Orthogonal to Semantics

A semantic model is defined at a level above persistence.

The same semantic model can be implemented on:

- relational databases
- key–value stores
- document databases
- graph databases
- in-memory structures

If changing the database invalidates the meaning of the model, then no abstraction exists.

True abstraction is characterized by invariance under implementation change.

This is why mature engineering systems historically separated:

- conceptual model
- logical semantic model
- physical persistence
- execution and query strategy

Confusing these layers leads to architectural superstition.

---

## 5. Why “Graph-First” Often Fails in Practice

Many graph-first platforms exhibit the same long-term failure patterns:

- mutable nodes continuously overwritten
- relationships updated in place
- history stored as annotations
- snapshots reconstructed heuristically

Initially, the system feels flexible.

Over time, it becomes impossible to answer simple questions such as:

- Which configuration was released?
- What exactly changed between two baselines?
- Why does this downstream structure exist?

The graph grows.
Understanding shrinks.

This is not a tooling problem.
It is a semantic absence.

---

## 6. Digital Thread Is Not Connectivity

Digital thread is often described visually as a continuous graph linking lifecycle domains.

This metaphor is misleading.

A thread is not created by connecting nodes.

A thread exists only if continuity of truth is preserved.

Without explicit snapshot semantics, what appears to be a thread is merely a timeline illusion constructed from mutable data.

Connectivity without truth is not a thread.
It is correlation.

---

## 7. What Actually Enables Long-Lived Engineering Systems

Systems that survive decades do so not because they chose fashionable technology, but because they enforce semantic discipline:

- identity never mutates
- snapshots are immutable
- changes are additive
- derivations are traceable
- deletion is rare and deliberate

These principles are uncomfortable.
They restrict freedom.

But they preserve meaning.

---

## Conclusion

The debate between graph-first and relational-first systems misses the central issue.

Engineering platforms do not fail because they lack connectivity.
They fail because they lack semantic grounding over time.

Graph technology can be useful.
So can relational databases.

Neither provides semantics.

Semantics must be designed.

Digital thread is not a graph problem.

It is a truth preservation problem.

---

*This paper intentionally avoids naming specific platforms or vendors. The principles described apply universally to any system claiming to manage engineering evolution.*


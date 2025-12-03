# **EVM Whitepaper — Glossary**

### *Canonical Definitions for Terms Used Throughout the Document*

---

## **NOVA (the semantic architecture layer)**

A hypothetical reference architecture used in this whitepaper to demonstrate how EVM integrates with a semantic, identity‑anchored, causality‑aware engineering data platform. NOVA is not a specific commercial product; it serves as an illustrative example of a next‑generation semantic stack.

---

## **EVM — Engineering Versioning Model**

A semantic framework defining how engineering objects evolve across time, variants, and meaning. EVM provides the conceptual foundation for intent, diff semantics, genealogy, lineage, context, and multi‑axis version representation.

---

## **EVG — Engineering Version Graph**

The operational runtime form of EVM. EVG unifies genealogy trees, lineage DAGs, context applicability graphs, semantic diffs, and temporal/variant coordinates into a single graph model.

---

## **OID — Object Identity**

A stable, immutable identifier that anchors all states and versions of an engineering object. All semantic evolution (versions) reference the same OID.

---

## Intent (Engineering Intent)

**Example:** “Increase stiffness for regulatory compliance.”

**Footnote 1:** Intent captures *why* a change exists, not merely that it exists. The rationale or purpose for creating a version. Examples include compliance, manufacturability, cost optimization, variant differentiation, and corrective changes.

---

## Semantic Diff

**Example:** `{length: +5 mm, tolerance: -0.02}`

**Footnote 2:** A semantic diff reflects *meaningful* engineering change, not byte‑level file differences. A structured representation of what changed between two engineering states, including structural, parametric, functional, rule, and context differences.

---

## Genealogy

**Example:** Part A → A1 → A2 (structural refinement and substitution).

**Footnote 3:** Genealogy concerns *how* structure evolves, not *why* it evolves. The structural evolution of an object: derivation, decomposition, refactoring, merging. Genealogy describes *how structure changes*.

---

## Lineage

**Example:** A1 was created due to supplier unavailability of component B.

**Footnote 4:** Lineage captures causal motivation and propagation, distinct from administrative revision sequences. The causal evolution of an object: why a version was created, which events triggered it, and how changes propagate across domains.

---

## Context / Effectivity

**Example:** “Valid for US market; S/N 5000–8000; Option X enabled.”

**Footnote 5:** Context defines where/when a version applies, unlike PLM effectivity filters which only prune structure. Applicability constraints on versions, including markets, options, serial ranges, dates, or configuration rules.

---

## CSI — Causal Snapshot Integration

**Example:** Reconstructing the engineering state for *EU market, Q2 2025*, combining CAD, BOM, and firmware snapshots.

**Footnote 6:** CSI integrates semantic snapshots; it is *not* limited to patch‑replay reconstruction. A reconstruction mechanism that assembles a consistent engineering state at any point in time by replaying version graph semantics.

---

## PQL — Property Query Language

**Example:** `RESOLVE(OID, date='2025-03-01', market='EU')`

**Footnote 7:** PQL is a semantic reasoning language, not a structural database query language. A semantic query language used to navigate EVG, retrieve intent/diff/lineage/genealogy information, and perform context‑aware reasoning.

---

## Variant Space

**Example:** {Market: EU}, {Option: Sport Package}, {Regulation: 2026‑Emissions}.

**Footnote 8:** Variant space forms a coordinate system for version applicability across dimensions. The dimensional space describing how versions apply to product variants, options, regional markets, feature bundles, and effectivity constraints.

---

## Semantic Lifecycle Verbs

**Example:** A CAD feature is *Refactored* into two parametric components.

**Footnote 9:** Lifecycle verbs express semantic intent; they are not equivalent to PLM lifecycle states. The universal action set describing engineering evolution: Create, Derive, Merge, Decompose, Refactor, Substitute, Recontextualize, Supersede, Retire.

---

## Digital Thread (Semantic)

**Example:** A cross‑domain trace: CAD → BOM → Simulation → Firmware.

**Footnote 10:** A semantic digital thread requires version correctness, not merely data connectivity. A coherent, version‑correct, causally linked engineering history reconstructed through EVG + CSI.

---

## Digital Twin (Version‑Accurate)

**Example:** A running device instance built from correct BOM version + correct firmware version.

**Footnote 11:** A digital twin without version accuracy is a visualization, not a trustworthy runtime model. A runtime representation of a product or system that is assembled using correct versions, correct applicability, and correct causal lineage.

---

# **End of Glossary**


# **Why EVM Solves What PLM Never Could**

### *Industry Comparison of Engineering Versioning Models (MatrixOne / 3DEXPERIENCE, Siemens Teamcenter, PTC Windchill)*

### *And Why the Engineering Versioning Model (EVM) Represents the First True Semantic Versioning Framework in Engineering History*

---

# **1. Introduction**

For more than 30 years, PLM platforms have attempted to model engineering change, revision control, effectivity, and variant complexity.

Yet none of the major platforms — **MatrixOne / 3DEXPERIENCE**, **Siemens Teamcenter**, or **PTC Windchill** — have ever implemented a true version semantics model.

They implemented:

- revision counters,
- workflow states,
- filtering mechanisms,
- configuration selectors,
- effectivity expressions,
- variant rules.

But they never implemented:

- semantic diffs,
- intent propagation,
- engineering lineage,
- multi-domain genealogy,
- causal propagation logic,
- version axes,
- semantic coordinates,
- snapshot reconstruction,
- AI-ready interpretation.

The **Engineering Versioning Model (EVM)** introduces the world’s first **semantic versioning system for engineering**, resolving the foundational gap PLM never solved.

---

# **2. MatrixOne / 3DEXPERIENCE Versioning: Clean but Flat**

MatrixOne (and later 3DEXPERIENCE) provides the industry’s cleanest major-version model:

- **Major revision chain**: A → B → C
- **Minor versioning via family objects**
- **Configuration selection via revision rules**
- **Effectivity as filters**
- **Variants as option-based filtering**

### ✔ Strengths

- extremely clean identity model
- consistent major-version semantics
- predictable behavior

### ✖ Limitations

- **no multi-branch evolution**
- **no version axes (time × applicability × semantic)**
- effectivity is a *filter*, not a *version dimension*
- variant is not part of version semantics
- no diff semantics
- no causal propagation
- no cross-domain lineage
- no semantic snapshoting

MatrixOne was revolutionary in 2000 — but insufficient for engineering systems in 2030.

---

# **3. Siemens Teamcenter: The Most Complex Non-Semantic System**

Teamcenter has:

- Item Revision (A, B, C)
- Effectivity (date/unit/condition)
- Variant Rules
- Occurrence Rules
- Configuration Rules

But all of these are **filters**, not semantics.

### ✖ Problems

- effectivity becomes a combinatorial explosion
- variant rules clash with effectivity rules
- revision rules are opaque filtering formulas
- no semantic axes
- no structural genealogy
- no diff semantics
- no causal propagation across domains
- no multi-branch evolution model

Teamcenter is extremely powerful, but fundamentally:

> **Teamcenter versioning = filtering system, not version semantics.**

It solves visibility, not meaning.

---

# **4. PTC Windchill: The Oldest Revision Paradigm**

Windchill uses:

- Major: A, B, C
- Minor: A.1, A.2, A.3
- Effectivity (rarely used)
- Options & Choices (for variants)

### ✖ Limitations

- effectivity is weak and underutilized
- no version dimensions
- no lineage model
- no genealogy model
- no diff semantics
- no intent semantics
- revision model inherited from document control era

Windchill is strong in workflow — not in semantic evolution.

---

# **5. The Root Problem Across All PLM Systems**

Across all three platforms, revisioning is still:

### **🔻 Linear**

A → B → C → D

### **🔻 Administrative**

Revision is a *marker*, not meaning.

### **🔻 No Version Axes**

None of them support time, context, semantic axes as formal dimensions.

### **🔻 No Engineering Lineage**

No system can answer:

> *“How did this artifact become what it is today?”*

### **🔻 No Semantic Diff**

They track *that* something changed, not *what the change means.*

### **🔻 No Cross-Domain Propagation**

CAD/BOM/Software/Rules/processes evolve in isolation.

### **🔻 Not AI-readable**

PLM systems store data, not semantics.

---

# **6. What EVM Introduces (That No PLM Has)**

## **6.1 Version Tensor**

A version is not a revision — it is a point:

```
v ∈ Time × Applicability × Semantic
```

This does not exist in any PLM.

---

## **6.2 Engineering Version Graph (EVG)**

Not a tree.\
Not a chain.\
Not a filter.

A **unified semantic graph** containing:

- State
- Intent
- Diff
- Genealogy
- Lineage
- Context

None of the three PLM systems have this.

---

## **6.3 Semantic Lifecycle Verbs**

EVM formalizes **how engineering entities evolve**, e.g.:

- derive
- supersede
- substitute
- decompose
- generalize
- migrate
- refactor

No PLM has semantic verbs.

---

## **6.4 Causal Snapshot Integration (CSI)**

The world’s first way to reconstruct:

- version-correct
- context-correct
- causally coherent

ingineering states.

PLM cannot do this.\
MBSE cannot do this.\
Digital Thread systems cannot do this.

---

## **6.5 Applicability / Context as First-Class Semantic Constructs**

Teamcenter effectivity = filter.\
EVM applicability = coordinate.

Huge difference.

---

# **7. Why EVM Represents the Next Generation**

EVM transforms engineering evolution into:

- a formal semantic space,
- a multi-axis version tensor,
- a multi-subgraph engineering version graph,
- a semantic lifecycle system,
- a causal reasoning engine.

PLM never attempted this level of abstraction. MBSE never had a semantic runtime. Digital Thread never had a version semantics model.

> **EVM is the first formal system that makes engineering evolution computable, explainable, and AI-ready.**

---

# **8. Summary Table**

| Capability               | MatrixOne/3DX | Teamcenter | Windchill | **EVM**        |
| ------------------------ | ------------- | ---------- | --------- | -------------- |
| Revision Chain           | ✔             | ✔          | ✔         | ✔              |
| Multi-Branch Evolution   | ✖             | Partial    | ✖         | ✔              |
| Version Axes             | ✖             | ✖          | ✖         | ✔              |
| Applicability Semantics  | Filter        | Filter     | Weak      | ✔ (Dimension)  |
| Semantic Diff            | ✖             | ✖          | ✖         | ✔              |
| Intent Semantics         | ✖             | ✖          | ✖         | ✔              |
| Lineage                  | Partial       | Partial    | ✖         | ✔ (Formal DAG) |
| Genealogy                | ✖             | ✖          | ✖         | ✔              |
| Cross-Domain Propagation | ✖             | ✖          | ✖         | ✔              |
| Snapshot Reconstruction  | ✖             | ✖          | ✖         | ✔              |
| AI Interpretability      | ✖             | ✖          | ✖         | ✔              |

---

# **9. Final Statement**

> **PLM solved “revisioning.”**\
> **EVM solves “engineering evolution.”**

This is the first time engineering version semantics have been formalized across identity, lineage, intent, diff, context, and causality.

EVM does not compete with PLM — it completes what PLM never could.

---


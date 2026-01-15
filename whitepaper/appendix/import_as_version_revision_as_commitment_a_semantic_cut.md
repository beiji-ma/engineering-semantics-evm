# Import as Version, Revision as Commitment

## Why Most PLM Data Migration Problems Are Not Really Technical

Most discussions about PLM data migration focus on tools, formats, and pipelines:
EDAT vs EIF, STEP AP242 vs proprietary XML, cloud vs on‑prem.

Yet most failures do **not** come from missing tooling or weak parsers.
They come from a deeper semantic confusion:

> **What exactly are we importing — a fact, or a business decision?**

This canvas deliberately leaves that question open — on purpose.

---

## The Hidden Assumption in Traditional Migration

In most PLM programs, imported data is implicitly treated as **revision‑level truth**:

- Objects appear as “current” immediately after import
- Lifecycle states are assigned during migration
- Downstream systems assume readiness by default

This creates an invisible coupling:

> **Import = Approval**

Once this assumption exists, every migration becomes fragile:
- Incremental runs create ambiguity
- Re‑imports risk semantic corruption
- Validation failures require destructive rollback

The system is forced to answer questions it cannot reliably decide.

---

## A Different Cut: Import Everything as Version

An alternative semantic cut is deceptively simple:

> **Imported data is always a version, never a revision.**

In this model:

- A **version** is a factual snapshot
- It may be complete, incomplete, correct, or wrong
- It carries evidence, not responsibility

Import becomes an act of **recording facts**, not committing decisions.

---

## Where Validation Belongs — and Where It Does Not

Validation is still essential, but its role changes:

### System‑enforceable validation
- Structural closure
- Reference integrity
- Type and value constraints
- Known semantic invariants

These can and should be automated.

### Non‑formalizable judgment
- Identity anchoring across systems
- Design intent interpretation
- Business responsibility acceptance

These **cannot** be fully automated without loss of meaning.

The system may assist, but must not decide.

---

## Revision as Commitment, Not Data

In this framing:

- **Revision is not imported**
- **Revision is granted**

Granting a revision means:
- Accepting downstream impact
- Allowing propagation to ERP / MES
- Entering the business responsibility timeline

This act is irreversible by nature.

That irreversibility is precisely why it must be explicit.

---

## The Deliberate Gap

Between **version** and **revision**, there is a gap.

That gap is not a defect.
It is where:
- Human judgment lives
- Governance applies
- Accountability is exercised

This canvas intentionally does **not** define how that gap is resolved.

Because resolving it is not a tooling problem.

---

## Why This Matters

By separating:

- Import from approval
- Facts from commitments
- Validation from responsibility

We transform migration from a brittle, one‑shot event into a controlled semantic process.

Most migration disasters disappear — not by better scripts, but by better boundaries.

---

## What Comes Next (Left Open)

The open questions remain:

- When must human review be mandatory?
- What evidence must a system present for judgment?
- How do we prevent silent bypass of commitment gates?

These questions deserve their own discussion.

This canvas stops here — deliberately.

Because the hardest problems begin exactly at this boundary.


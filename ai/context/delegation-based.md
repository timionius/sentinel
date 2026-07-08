# Sentinel Redesign Project Charter

## Objective

Redesign the Sentinel architecture around a delegation-based trust model and produce a publication-ready foundational proposal for Sentinel v1.

The redesign aims to clarify the trust architecture without expanding the scope of Sentinel v1. Sentinel v1 remains intentionally conservative. It establishes a rigorous framework for post-execution trust verification of autonomous blockchain agents operating under human-approved delegated authority.

The objective of this redesign is not to solve every aspect of autonomous trust, but to establish a coherent architectural foundation upon which future Sentinel versions can evolve.

---

## Design Principles

The redesign follows these principles throughout all phases.

- **Minimal Scope**  
  Sentinel v1 solves one problem well: post-execution verification of delegated autonomous behavior. Features outside this scope are explicitly identified as future work.

- **Clear Architectural Boundaries**  
  Trust establishment, execution planning, execution, and verification are separate architectural concerns. Each component has a single responsibility.

- **Stable Terminology**  
  Every canonical term has exactly one normative definition. The terminology document is the single source of truth for Sentinel vocabulary. No proposal section may redefine a canonical term.

- **Architecture Before Prose**  
  Architecture is finalized before proposal writing begins. The proposal explains the architecture. It does not define it.

- **Observable Verification**  
  Sentinel verifies only realized blockchain behavior. It does not infer intent. It does not reason about internal AI behavior. It does not verify hypothetical execution plans.

- **Explicit Scope**  
  Every architectural assumption should be explicit. Every non-goal should be stated clearly. Reviewers should understand both what Sentinel guarantees and what it deliberately does not attempt to solve.

---

## Project Workflow

### Phase 1 — Terminology

**Goal**  
Freeze the Sentinel vocabulary.

**Deliverable**  
`terminology.md`

This document defines the canonical meaning of every architectural concept used throughout Sentinel. It is a normative reference.

---

### Phase 2 — Architecture

**Goal**  
Freeze the Sentinel architecture.

**Deliverable**  
`architecture.md`

This document defines:

- architectural layers
- trust lifecycle
- component responsibilities
- information flow
- trust boundaries
- assumptions
- architectural diagrams

This becomes the canonical architectural reference.

---

### Phase 3 — Proposal Rewrite

**Goal**  
Produce a publication-ready Sentinel proposal.

**Deliverable**  
`proposal.md`

The proposal explains:

- motivation
- problem statement
- architectural rationale
- Sentinel architecture
- design principles
- scope
- limitations
- future evolution

The proposal references the canonical terminology and architecture rather than redefining them.

---

### Phase 4 — Editorial Review

**Goal**  
Produce a consistent publication-quality document set.

Review includes:

- terminology consistency
- architectural consistency
- conceptual consistency
- writing quality
- reviewer readability
- removal of obsolete concepts
- publication readiness

---

### Phase 5 — Reference Implementation

**Goal**  
Validate the architecture through implementation.

The reference implementation serves to:

- demonstrate feasibility
- validate architectural assumptions
- identify ambiguities
- refine implementation details

Implementation should not redefine the architecture. Architectural changes discovered during implementation should result in a new architectural revision rather than ad hoc modifications.

---

## Expected Deliverables
docs/
├── terminology.md (Canonical Sentinel vocabulary)
├── architecture.md (Canonical Sentinel architecture)
└── proposal.md (Publication-ready proposal)
reference/
└── Sentinel reference implementation


---

## Editorial Rules

The redesign follows the following editorial rules:

1. **Terminology drives the architecture.**  
   Every architectural concept must first be defined in `Terminology.md`.

2. **Architecture drives the proposal.**  
   The proposal explains the architecture but does not redefine it.

3. **Implementation validates the architecture.**  
   The reference implementation demonstrates feasibility without changing the architectural model.

4. **Scope before features.**  
   Sentinel v1 remains intentionally limited. New capabilities are deferred to future versions unless they are essential to the core contribution.

5. **One concept, one definition.**  
   Every canonical concept has exactly one normative definition and one architectural role.
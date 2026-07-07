# Sentinel Terminology

This document defines the canonical terminology used throughout Sentinel.

These definitions establish the meaning of the architectural concepts referenced by the Proposal, Trust Specification, and Reference Implementation. Sentinel documentation **SHOULD** use these terms consistently and **SHOULD** avoid introducing alternative terminology for equivalent concepts.

---

# Core Concepts

## Agent

An autonomous software entity capable of performing blockchain operations on behalf of itself or another party.

## Identity

The cryptographically verifiable representation of an agent within the Sentinel trust model.

## Identity Integrity *(Core Guarantee)*

The assurance that an agent's identity has not been forged, substituted, or altered.

## Intent

The declared purpose of an autonomous agent describing what the agent is designed or expected to accomplish.

Intent is a semantic declaration that exists prior to execution and may be derived from one or more declarative sources, including agent metadata, program identifiers, published capabilities, API or MCP descriptions, or other specifications.
Intent is consumed by the Producer when deriving Trust Commitments and is distinct from the agent's realized Blockchain Behavior Footprint.

## Intent Integrity *(Core Guarantee)*

The assurance that an agent's declared Intent has not been forged, substituted, or altered.

Intent Integrity concerns the authenticity and integrity of the semantic declaration describing the agent's intended purpose, independent of execution.

## Behavior

The blockchain operations performed by an autonomous agent while realizing a declared Intent.

Sentinel evaluates realized behavior through the agent's Blockchain Behavior Footprint.

## Behavioral Integrity *(Core Guarantee)*

The assurance that an agent's Blockchain Behavior Footprint remains consistent with its established Trust Commitments and Behavioral Invariants.

Behavioral Integrity concerns realized blockchain behavior rather than the semantic declaration of Intent.

## Behavioral Invariant *(Fundamental Concept)*

A property of an agent's observable blockchain behavior that must remain true regardless of execution strategy, transaction ordering, protocol composition, or implementation evolution.

Behavioral Invariants define the stable behavioral properties against which Blockchain Behavior Footprints are verified.

## Blockchain Behavior Footprint

The complete observable representation of an autonomous agent's realized blockchain behavior while executing a declared Intent.

A Blockchain Behavior Footprint may contain one or many transactions spanning multiple protocols, execution paths, and blockchain systems.
The Blockchain Behavior Footprint is the primary behavioral object evaluated by Sentinel during verification.

---

# Trust Model

## Trust Layer

The Sentinel infrastructure responsible for providing Identity verification, authorization, evidence production, and attestation independently of agent execution systems.

## Trust Commitment *(Fundamental Concept)*

A cryptographic representation of the blockchain behavior an agent is authorized to perform.

Trust Commitments are produced by the Producer from validated Identity, declared Intent, and other available declarative information prior to execution.
They serve as the stable basis for authorization, behavioral verification, and attestation.

## Authorization

The determination that an observed Blockchain Behavior Footprint, or a blockchain operation within that Footprint, is permitted by an established Trust Commitment.

## Evidence

Cryptographically verifiable records describing an agent's Blockchain Behavior Footprint together with the associated verification and authorization decisions.

## Attestation

A cryptographic statement asserting that an agent's Blockchain Behavior Footprint has remained consistent with its Trust Commitments and Behavioral Invariants over a specified period.


---

# Execution Model

## Execution Graph *(Fundamental Concept)*

A representation of the blockchain operations through which an autonomous agent realizes a declared Intent.
An Execution Graph captures the relationships among the operations that comprise a particular execution, including sequencing, dependencies, protocol interactions, and other execution characteristics.
Execution Graph is the primary object of trust.

## Behavioral Equivalence

The condition in which two or more different Execution Graphs satisfy the same set of Behavioral Invariants.

## Continuous Verification

The ongoing validation that an agent's observable blockchain behavior remains consistent with its Trust Commitments and Behavioral Invariants.

---

# Producer / Verifier Separation

## Producer

The component responsible for deriving Trust Commitments from validated Identity, declared Intent, capabilities, specifications, policies, and other available declarative information.

Trust Commitment production is independent of subsequent behavioral verification.

## Verifier

The component responsible for validating that an agent's Blockchain Behavior Footprint remains consistent with established Trust Commitments and their associated Behavioral Invariants, producing cryptographically verifiable Evidence that supports Attestations.

## Producer / Verifier Separation

The architectural principle that Trust Commitment production and trust verification evolve independently.

Producers, derivation techniques, AI systems, execution frameworks, and blockchain ecosystems may evolve independently.
The Sentinel verification model, verification semantics, and trust guarantees remain stable despite those evolutions.

---

# Architectural Properties

## Blockchain Independence

The property that Sentinel's trust model remains valid across different blockchain architectures and execution environments.

## Cryptographic Accountability

The requirement that every authorization decision, Trust Commitment, and Attestation be independently verifiable through cryptographic evidence.

## Verifiable Trust

The principle that trust assertions must be supported by cryptographically verifiable Evidence rather than unverifiable claims.

---

# Conceptual Flow

```text
Identity
    │
    ▼
Declared Intent
    │
    ▼
Producer
    │
    ▼
Trust Commitment
    │
    ▼
Blockchain Behavior Footprint
    │
    ▼
Verifier
    │
    ▼
Evidence
    │
    ▼
Attestation
```

Behavioral Invariants are derived from the declared Intent and embodied within the resulting Trust Commitment. During verification, the Verifier evaluates the realized Blockchain Behavior Footprint against those established commitments to produce Evidence and Attestations.

---

# Terminology Usage Guidelines

- Use **Intent** instead of alternatives such as **objective**, **goal**, or **purpose** when referring to the intended outcome of agent behavior.
- Use **Behavioral Invariants** as the primary abstraction for stable trust properties.
- Use **Execution Graph** only when describing how an Intent is realized, not as the primary object of trust.
- Use **Trust Commitment** when referring to the cryptographic representation of authorized behavior.
- Use **Behavioral Integrity** and **Intent Integrity** consistently when discussing Sentinel's trust guarantees.
- Use **Blockchain Behavior Footprint** as the canonical term for realized blockchain behavior.
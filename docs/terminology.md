# Sentinel Terminology

This document defines the canonical terminology for Sentinel v1.

These definitions are **normative**. Every canonical term has exactly one normative definition. Sentinel documentation uses these terms consistently and does not redefine them.

Terminology is organized according to the Sentinel trust lifecycle.

---

# Trust Establishment

## Agent

A software entity capable of performing work on its own behalf or under delegated authority.

An Agent may perform computation, reasoning, planning, and interactions outside blockchain systems. Sentinel is concerned only with the blockchain operations performed by an Agent.

## Identity

The cryptographically verifiable representation of an Agent within the Sentinel trust model.

## Identity Integrity

The assurance that an Agent's Identity has not been forged, substituted, or altered.

## Delegated Authority

The explicitly authorized scope within which an Agent is permitted to perform blockchain operations on behalf of another party.

Delegated Authority establishes the trust basis from which a Trust Commitment is derived.

## Trust Commitment

A cryptographic representation of the authorized constraints on an Agent's blockchain behavior.

A Trust Commitment is produced during Trust Establishment prior to execution and forms the basis for authorization, verification, evidence production, and attestation.

## Trust Establishment

The process of validating Identity, Delegated Authority, and other required declarative inputs in order to produce Trust Commitments.

Trust Establishment is independent of execution and verification.

---

# Execution

## Blockchain Behavior Footprint

The complete observable representation of the blockchain operations performed by an Agent.

A Blockchain Behavior Footprint may contain one or many transactions spanning multiple protocols, execution paths, and blockchain systems. It represents only the blockchain-visible portion of an Agent's overall activity.

The Blockchain Behavior Footprint is the canonical object of verification in Sentinel.

---

# Verification

## Authorization

The determination that an observed Blockchain Behavior Footprint, or an operation within that Footprint, is permitted by an established Trust Commitment.

## Behavioral Integrity

The assurance that an Agent's Blockchain Behavior Footprint remains consistent with an established Trust Commitment.

## Verification

The process of evaluating a Blockchain Behavior Footprint against an established Trust Commitment.

Verification produces cryptographically verifiable Evidence that serves as the basis for Attestation.

## Continuous Verification

The ongoing validation that an Agent's Blockchain Behavior Footprint remains consistent with an established Trust Commitment.

## Evidence

Cryptographically verifiable records of an Agent's Blockchain Behavior Footprint together with the associated verification and authorization decisions.

## Attestation

A cryptographic statement asserting that an Agent's Blockchain Behavior Footprint has remained consistent with an established Trust Commitment over a specified period.

---

# Trust Infrastructure

## Trust Layer

The architectural layer responsible for trust establishment, verification, evidence production, and attestation independently of execution systems.

## Producer

The component responsible for producing a Trust Commitment from validated Identity, Delegated Authority, and other declarative inputs.

Trust Commitment production is independent of subsequent verification.

## Verifier

The component responsible for evaluating a Blockchain Behavior Footprint against an established Trust Commitment, producing cryptographically verifiable Evidence that supports Attestation.

## Producer / Verifier Separation

The architectural principle that Trust Commitment production and trust verification evolve independently.

Producers, authorization mechanisms, execution frameworks, AI systems, and blockchain ecosystems may evolve independently while Sentinel's verification semantics and trust guarantees remain stable.

---

# Architectural Properties

## Blockchain Independence

The property that Sentinel's trust model remains valid across different blockchain architectures and execution environments.

## Cryptographic Accountability

The requirement that every authorization decision, Trust Commitment, Evidence, and Attestation be independently verifiable through cryptographic evidence.

## Verifiable Trust

The principle that trust assertions must be supported by cryptographically verifiable Evidence rather than unverifiable claims.

---

# Trust Lifecycle

```text
Identity
    │
    ▼
Delegated Authority
    │
    ▼
Trust Establishment
    │
    ▼
Trust Commitment
    │
    ▼
Execution
    │
    ▼
Blockchain Behavior Footprint
    │
    ▼
Verification
    │
    ▼
Evidence
    │
    ▼
Attestation
```

---

# Terminology Usage Guidelines

- Use **Delegated Authority** as the canonical term for the authority granted to an Agent to perform blockchain operations.
- Use **Trust Commitment** as the canonical representation of the authorized constraints on an Agent's blockchain behavior.
- Use **Blockchain Behavior Footprint** as the canonical term for realized blockchain operations observed during verification.
- Use **Verification** when referring to evaluation of realized blockchain behavior against established Trust Commitment.
- Use **Evidence** for cryptographically verifiable records produced during verification.
- Use **Attestation** for cryptographic statements derived from verification results.
- Avoid introducing alternative terminology for canonical Sentinel concepts.
# Sentinel Documentation

This directory contains all architecture and engineering documentation for the Sentinel platform.

## Core Documents

### [Sentinel Proposal](proposal/sentinel-proposal.md)

The foundational architectural proposal explaining why Sentinel exists and what problem it solves. Defines the trust gap in autonomous systems, introduces behavioral invariants as the object of trust, and establishes architectural principles. Remains implementation-independent, blockchain-independent, and valid across technological evolution.

### [Terminology](terminology.md)

Canonical definitions of all architectural concepts used throughout Sentinel documentation. Establishes consistent terminology for Identity Integrity, Behavioral Integrity, Intent Integrity, Trust Commitments, Behavioral Invariants, and other core concepts.

## Documentation Structure

Sentinel documentation is intentionally divided into three independent layers:

### 1. Proposal (Vision)

Explains **why Sentinel exists** and **what problem it solves**. Defines the long-term vision and architectural principles. Contains no implementation details.

- Location: `proposal/`
- Stability: Remains stable across decades

### 2. Specification

Defines **what Sentinel guarantees**. Establishes precise trust guarantees, verification requirements, evidence formats, and attestation semantics. Remains implementation-independent and blockchain-independent.

- Location: `specifications/`
- Stability: Evolves as trust requirements are refined

### 3. Reference Implementation

Demonstrates **how the trust model is realized**. Targets specific blockchain infrastructure, demonstrates feasibility, and serves as reference for future implementations.

- Location: `../platform/`
- Stability: Evolves as technology advances

## Directory Structure

- **proposal/**: Foundational architectural proposal and vision documents
- **specifications/**: Trust specifications and technical requirements
- **architecture/**: Architecture Decision Records (ADRs) documenting key architectural choices
- **guides/**: Developer guides, tutorials, and best practices for working with Sentinel

## Layer Independence

These layers evolve independently:

- The proposal remains stable across decades
- The specification evolves as trust requirements are refined  
- Implementations evolve as technology advances

This independence ensures long-term architectural stability.

# Sentinel

Sentinel is an AI-assisted trust verification framework for AI agent execution.

This repository contains the Sentinel Engineering Platform, including architecture, specifications, reusable AI engineering assets, and the Sentinel v1 reference implementation.

## Repository Structure

This repository is organized to support an architecture-first development approach where Git serves as the system of record and AI assists with implementation:

- **docs/**: Architecture Decision Records (ADRs), engineering specifications, and developer guides
- **ai/**: Reusable AI prompts and skills that support the AI-SDLC workflow
- **engineering/**: Engineering artifacts, repository standards, and coding conventions
- **platform/**: Implementation code including Rust programs, Anchor programs, SDKs, and agents
- **examples/**: Example usage patterns and integrations demonstrating platform capabilities
- **scripts/**: Development, deployment, and maintenance automation scripts
- **.github/**: GitHub-specific configuration including CI/CD workflows

## Development Approach

Sentinel follows an architecture-first AI-SDLC where:
- Architecture decisions are documented before implementation
- Engineering specifications define clear requirements and constraints
- AI serves as a stateless implementation assistant
- Git is the authoritative system of record
- All changes are deterministic and traceable

## Documentation Architecture

Sentinel documentation is intentionally divided into three independent layers:

**Proposal** (this document): Explains why Sentinel exists and what problem it solves. Defines the trust gap in autonomous systems, introduces Behavioral Invariants as the object of trust, and establishes architectural principles. Remains implementation-independent, blockchain-independent, and valid across technological evolution.

**Trust Specification**: Defines what Sentinel guarantees. Defines trust guarantees precisely, establishes verification requirements, specifies Evidence formats, and defines Attestation semantics. Remains implementation-independent and blockchain-independent.

**Reference Implementation**: Demonstrates how the trust model is realized. Targets specific blockchain infrastructure, demonstrates feasibility, provides concrete realization, and serves as reference for future implementations.

These layers evolve independently. The proposal remains stable across decades, the specification evolves as trust requirements are refined, and implementations evolve as technology advances. This independence ensures long-term architectural stability.

## Getting Started

Documentation and implementation guides will be added as the platform develops. Check the `docs/` directory for architecture decisions and specifications.

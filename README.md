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

## Getting Started

Documentation and implementation guides will be added as the platform develops. Check the `docs/` directory for architecture decisions and specifications.

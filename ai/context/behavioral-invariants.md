# Sentinel — Architectural Context (Behavioral Invariants)

## Architectural Separation

Sentinel is intentionally divided into three independent layers.

### 1. Proposal (Vision)

The proposal explains **why Sentinel exists**, not how it is implemented.

Sentinel is envisioned as a reference trust and authorization layer for autonomous agents operating on blockchains.

Its long-term objective is to make trust in autonomous agents nearly automatic by continuously verifying the invariants of an agent's blockchain behavior.

The proposal deliberately avoids implementation details and remains blockchain-independent.

Sentinel is not:

* a wallet
* a runtime
* a blockchain
* a policy engine
* an AI framework

Instead, Sentinel provides a trust layer that can evolve independently of execution frameworks and AI systems.

---

### 2. Trust Specification

The specification defines **what Sentinel guarantees**, without prescribing implementation.

Core guarantees include:

* Identity Integrity
* Behavioral (Intent) Integrity
* Authorization
* Evidence
* Attestation

The specification remains blockchain-independent.

---

### 3. Reference Implementation

The current implementation demonstrates the specification on Solana.

Its purpose is not to solve semantic understanding of autonomous agents.

Instead, it proves that the trust model can be realized with a minimal architecture consisting of:

* registration
* trust commitment storage
* CPI authorization
* execution verification
* evidence collection
* attestation

Future implementations may become significantly more sophisticated while preserving the same trust model.

---

# Revised Long-Term Vision

One of the key architectural insights is that **Sentinel should not ultimately reason about transactions—it should reason about behavioral invariants.**

A blockchain transaction is merely one observable manifestation of an agent's behavior.

Autonomous agents continuously evolve:

* reasoning changes
* prompts change
* planning algorithms improve
* execution graphs evolve
* tools are replaced
* MCP metadata grows
* execution strategies become more sophisticated

These changes should not invalidate trust if the observable blockchain behavior remains consistent with the agent's intended purpose.

The long-term goal is therefore:

> Sentinel continuously verifies that an autonomous agent's blockchain actions remain consistent with its intended behavioral invariants.

Importantly, this says nothing about *how* Sentinel derives those invariants.

Future versions may derive them from:

* agent descriptions
* MCP metadata
* tool definitions
* execution graphs
* capability descriptions
* semantic reasoning
* AI-assisted analysis
* other future representations

The proposal intentionally leaves this open.

Only the trust guarantees remain stable.

---

# Behavioral Invariants

A central realization is that trust should not be defined over individual transactions.

Trust should be defined over the invariants that hold across an agent's blockchain behavior.

For example:

A game-trading agent receives the objective:

> Sell my Sword and obtain three Shields with specific attributes.

The agent may execute many different transaction sequences:

* marketplace A
* marketplace B
* intermediate token swaps
* partial fills
* retries
* different ordering
* optimization strategies

Every execution graph may differ.

Every transaction may differ.

Yet the behavioral invariant remains:

* dispose of the Sword
* acquire three qualifying Shields
* preserve user ownership
* never transfer assets to unauthorized parties

Sentinel's long-term vision is to recognize that these executions are behaviorally equivalent.

The execution strategy is free to evolve.

The behavioral invariants remain constant.

---

# Reference Implementation Scope

The reference implementation intentionally does **not** attempt to understand behavioral invariants.

Instead, it demonstrates the trust model using a much simpler abstraction.

Version 1 focuses only on the observable blockchain footprint.

A Trust Commitment represents the authorized on-chain behavior of an agent.

Sentinel verifies this commitment during CPI authorization.

Future versions may replace the commitment producer with increasingly sophisticated systems capable of deriving behavioral invariants automatically.

Crucially:

The verifier does not change.

Only the producer evolves.

---

# Fundamental Principle

This separation is intentional.

Proposal:

Defines the long-term trust model based on behavioral invariants.

Specification:

Defines the guarantees Sentinel provides.

Reference implementation:

Demonstrates those guarantees using the simplest possible commitment-based architecture.

Future AI reasoning, semantic analysis, execution understanding, or invariant extraction should enhance the production of trust commitments without requiring changes to Sentinel's core trust model or on-chain verifier.

This allows Sentinel to evolve from a simple cryptographic verifier into a trust layer capable of understanding autonomous agents while preserving the same architectural foundation.

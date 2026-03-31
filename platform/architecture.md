# Platform Architecture

VeriQ operates across three interconnected layers.

## Architecture Overview

| Layer | Role | Components |
|---|---|---|
| **Oracles & Verifiers** | Integrity & trust | Independent verifiers, ZK attestations, $VQ staking |
| **Blockchain Layer** | Orchestration & payments | Task management, audit logging, EVM smart contracts (BSC) |
| **Quantum Layer** | Computation | Quantum simulators, real quantum devices, Qiskit & Cirq |

---

## Quantum Layer

The computational foundation. Interfaces with quantum simulators and real quantum devices.

- **Simulation Engines** — Execute quantum algorithms (Shor's, Grover's) against target cryptographic parameters
- **Framework Integration** — Built on Qiskit and Cirq quantum computing frameworks
- **Hybrid Execution** — Supports both classical quantum simulation and real quantum hardware

---

## Blockchain Layer

The orchestration and trust backbone, deployed on **BNB Smart Chain**.

- **Task Orchestration** — Manages audit requests, task distribution, and compute scheduling
- **Audit Logging** — Immutable on-chain record of all audit results
- **Payments** — $VQ token transfers for services, escrow, and marketplace transactions
- **Smart Contracts** — EVM-compatible contracts handling all platform logic

---

## Oracles & Verifiers

Ensures computational integrity through independent verification.

- **Independent Verifiers** — Stake $VQ to participate as verification nodes
- **Zero-Knowledge Attestations** — Verifiers generate ZK proofs to confirm computation integrity without exposing sensitive data
- **Staking & Slashing** — Economic security through bonded $VQ tokens

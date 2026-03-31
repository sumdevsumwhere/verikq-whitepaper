# Platform Architecture

VeriQ operates across three interconnected layers.

## Architecture Overview

```
┌─────────────────────────────────────────────────┐
│            Oracles & Verifiers                   │
│   Independent Verifiers · ZK Attestations        │
│            $VQ Staking                           │
├─────────────────────────────────────────────────┤
│              Blockchain Layer                     │
│    Task Orchestration · Audit Logging · Payments │
│         EVM-Compatible Smart Contracts           │
│              (BNB Smart Chain)                   │
├─────────────────────────────────────────────────┤
│               Quantum Layer                      │
│     Quantum Simulators · Real Quantum Devices    │
│            Qiskit · Cirq Integration             │
└─────────────────────────────────────────────────┘
```

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

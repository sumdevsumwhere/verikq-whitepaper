# Platform Architecture

VeriQ operates across three interconnected layers.

## Architecture Overview

| Layer | Role | Components |
|---|---|---|
| **Oracles & Verifiers** | Integrity and trust | Independent verifiers, ZK attestations, $VQ staking |
| **Blockchain Layer** | Orchestration and payments | Task management, audit logging, EVM smart contracts (BSC) |
| **Quantum Layer** | Computation | Quantum simulators, real quantum devices, Qiskit and Cirq |

---

## Quantum Layer

The computational foundation. Interfaces with quantum simulators and real quantum devices.

- Executes quantum algorithms (Shor's, Grover's) against target cryptographic parameters
- Built on Qiskit and Cirq quantum computing frameworks
- Supports both classical quantum simulation and real quantum hardware

---

## Blockchain Layer

The orchestration and trust backbone, deployed on **BNB Smart Chain**.

- Manages audit requests, task distribution, and compute scheduling
- Maintains an immutable on-chain record of all audit results
- Handles $VQ token transfers for services, escrow, and marketplace transactions
- EVM-compatible contracts handle all platform logic

---

## Oracles & Verifiers

Ensures computational integrity through independent verification.

- Verifiers stake $VQ to participate as verification nodes
- ZK proofs confirm computation integrity without exposing sensitive data
- Economic security is maintained through bonded $VQ tokens with slashing conditions

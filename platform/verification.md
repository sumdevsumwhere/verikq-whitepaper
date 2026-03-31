# Verification & Proofs

Trust in VeriQ's audit results comes from cryptographic verification, not reputation alone.

---

## Why Verification Matters

Quantum computation is expensive and complex. Without verification, a malicious compute provider could submit fabricated results and collect payment. VeriQ's verification layer ensures every result is provably correct.

---

## Zero-Knowledge Attestations

Verifiers in the VeriQ network generate **zero-knowledge proofs** that confirm:

- The computation was performed correctly
- The correct algorithm and parameters were used
- The result matches the submitted input

All without exposing the underlying computation data.

---

## Verification Flow

| Step | Actor | Action |
|:---:|---|---|
| **1** | **Compute Provider** | Executes quantum simulation and generates result + ZK proof |
| **2** | **Verifier Network** | Receives result, validates ZK attestation |
| **3** | **Verifier Network** | Submits on-chain attestation to BNB Smart Chain |
| **4** | **BNB Smart Chain** | Stores immutable audit record on-chain |

---

## Multi-Node Redundancy

Critical computations are not verified by a single node:

| Audit Type | Minimum Verifiers | Consensus Required |
|---|---|---|
| Standard audit | 3 nodes | 2/3 agreement |
| Critical infrastructure | 5 nodes | 4/5 agreement |

If verifiers disagree, a dispute resolution process is triggered and additional nodes are assigned.

---

## Economic Security

Verifiers stake **$VQ** tokens to participate. This creates economic alignment:

| Behavior | Outcome |
|---|---|
| Honest verification | Earn $VQ rewards |
| Negligent verification | Partial stake slashing |
| Malicious verification | Full stake slashing |

The cost of attacking the verification layer always exceeds the potential gain.

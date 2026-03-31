# Post-Quantum Cryptography

Post-quantum cryptography (PQC) refers to cryptographic algorithms designed to be secure against both classical and quantum computers.

---

## Why It Matters for Blockchain

Current blockchain cryptography (ECDSA, RSA) will not survive quantum attacks. The entire ecosystem — wallets, signatures, smart contracts — needs to migrate to quantum-resistant alternatives. This migration is one of the largest technical challenges facing the industry.

---

## NIST Post-Quantum Standards

In 2024, NIST finalized its first set of post-quantum cryptographic standards after an 8-year evaluation process:

| Algorithm | Type | Purpose |
|---|---|---|
| **ML-KEM (CRYSTALS-Kyber)** | Lattice-based | Key encapsulation / encryption |
| **ML-DSA (CRYSTALS-Dilithium)** | Lattice-based | Digital signatures |
| **SLH-DSA (SPHINCS+)** | Hash-based | Digital signatures (stateless) |
| **FN-DSA (FALCON)** | Lattice-based | Digital signatures (compact) |

---

## Approaches to Quantum Resistance

### Lattice-Based Cryptography

- Built on the hardness of lattice problems (Learning With Errors, Shortest Vector)
- No known quantum algorithm solves these efficiently
- Forms the basis of most NIST-selected standards
- **Trade-off:** Larger key and signature sizes compared to ECDSA

### Hash-Based Signatures

- Security relies solely on the properties of hash functions
- Well-understood, conservative security assumptions
- SPHINCS+ selected by NIST as a backup standard
- **Trade-off:** Larger signatures, slower verification

### Code-Based Cryptography

- Based on error-correcting codes (McEliece system, 1978)
- Decades of cryptanalysis with no practical quantum attacks found
- **Trade-off:** Very large public keys

### Multivariate Cryptography

- Based on the difficulty of solving systems of multivariate polynomial equations
- Suitable for certain signature schemes
- **Trade-off:** Some schemes have been broken; fewer NIST selections

---

## The Migration Challenge

Migrating blockchain to post-quantum cryptography is not straightforward:

| Challenge | Detail |
|---|---|
| **Key size increase** | PQC keys are 10-100x larger than ECDSA keys |
| **Transaction size** | Larger signatures increase block space usage |
| **Gas costs** | On-chain signature verification becomes more expensive |
| **Backward compatibility** | Existing wallets and contracts use classical cryptography |
| **Coordination** | Network-wide upgrade requires ecosystem consensus |

---

## VeriQ's Role in PQC

VeriQ helps the ecosystem prepare for this migration by:

- **Auditing** current systems to identify what needs to change
- **Simulating** quantum attacks to quantify urgency
- **Testing** post-quantum algorithm integration before deployment
- Providing a **marketplace** for quantum compute resources needed for migration research

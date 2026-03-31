# Post-Quantum Cryptography

Post-quantum cryptography (PQC) refers to cryptographic algorithms designed to be secure against both classical and quantum computers.

---

## Why It Matters for Blockchain

Current blockchain cryptography (ECDSA, RSA) will not survive quantum attacks. The entire ecosystem, from wallets to signatures to smart contracts, needs to migrate to quantum-resistant alternatives. This is one of the largest technical challenges facing the industry.

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

Built on the hardness of lattice problems like Learning With Errors and Shortest Vector. No known quantum algorithm solves these efficiently, and they form the basis of most NIST-selected standards. The trade-off is larger key and signature sizes compared to ECDSA.

### Hash-Based Signatures

Security relies solely on the properties of hash functions. Well-understood with conservative security assumptions. SPHINCS+ was selected by NIST as a backup standard. The trade-off is larger signatures and slower verification.

### Code-Based Cryptography

Based on error-correcting codes (McEliece system, 1978). Decades of cryptanalysis with no practical quantum attacks found. The trade-off is very large public keys.

### Multivariate Cryptography

Based on the difficulty of solving systems of multivariate polynomial equations. Suitable for certain signature schemes, but some have been broken and fewer were selected by NIST.

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

- Auditing current systems to identify what needs to change
- Simulating quantum attacks to quantify urgency
- Testing post-quantum algorithm integration before deployment
- Providing a marketplace for quantum compute resources needed for migration research

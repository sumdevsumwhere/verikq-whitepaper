# Attack Vectors

Quantum computers introduce specific algorithms that directly threaten the cryptographic foundations of blockchain networks.

---

## Shor's Algorithm

The primary threat to blockchain cryptography. Shor's algorithm efficiently solves two mathematical problems that underpin most public-key cryptosystems:

| Problem | What It Breaks | Blockchain Impact |
|---|---|---|
| **Integer Factorization** | RSA encryption | Key exchange, digital signatures |
| **Discrete Logarithm** | Elliptic Curve Cryptography (ECDSA) | Wallet addresses, transaction signing |

### How It Works

1. A quantum computer takes a public key as input
2. Shor's algorithm computes the discrete logarithm in polynomial time
3. The corresponding private key is derived
4. The attacker can now sign transactions as the wallet owner

### What's At Risk

Every blockchain using ECDSA for transaction signing — including BNB Smart Chain, Bitcoin, and Ethereum — is theoretically vulnerable once quantum hardware reaches sufficient scale.

---

## Grover's Algorithm

A quantum search algorithm that provides a **quadratic speedup** over classical brute-force search.

| Target | Classical Security | Post-Grover Security |
|---|---|---|
| **AES-128** | 128-bit | 64-bit (broken) |
| **AES-256** | 256-bit | 128-bit (still secure) |
| **SHA-256** | 256-bit | 128-bit (still secure) |

### Blockchain Implications

- Mining hash functions (SHA-256) would require roughly the square root of current computational effort
- Symmetric encryption with sufficient key sizes remains resistant
- Hash-based data structures (Merkle trees) are impacted but not broken

---

## Harvest Now, Decrypt Later (HNDL)

Not an algorithm — a **strategy** already in active use.

Adversaries record encrypted blockchain data and transactions today with the intent to decrypt them once sufficiently powerful quantum computers become available.

**Why this matters now:**

- Blockchain transactions are public and permanently recorded
- Any data on-chain today is already "harvested"
- Wallet public keys exposed during transactions are stored forever
- Once quantum decryption is possible, historical transactions become retroactively vulnerable

---

## Quantum Key Distribution Attacks

As quantum networks develop, new attack surfaces emerge:

- **Man-in-the-middle** on quantum key distribution channels
- **Side-channel attacks** exploiting physical quantum hardware imperfections
- **Hybrid attacks** combining classical and quantum techniques

---

## Timeline Considerations

| Milestone | Estimated Timeline |
|---|---|
| Current quantum computers | ~1,000+ qubits (noisy) |
| Cryptographically relevant quantum computer | Estimated 2030s |
| RSA-2048 breakable | Requires ~4,000 logical qubits |
| ECDSA-256 breakable | Requires ~2,500 logical qubits |

The exact timeline is uncertain, but the trajectory is clear — preparation must begin before the capability arrives.

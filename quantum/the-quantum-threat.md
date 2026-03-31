# The Quantum Threat

## Why This Matters

Blockchain technology relies on cryptographic systems to ensure security and trustlessness. The two primary pillars are:

- **RSA**, used for key exchange and digital signatures
- **Elliptic Curve Cryptography (ECC)**, the backbone of wallet addresses and transaction signing across most blockchain networks

These systems derive their security from mathematical problems that classical computers cannot solve in any reasonable timeframe.

**Quantum computers can.**

## Shor's Algorithm

In 1994, Peter Shor developed a quantum algorithm capable of efficiently factoring large integers and computing discrete logarithms. On a sufficiently powerful quantum computer, this algorithm **breaks both RSA and ECC**.

| Threat | Impact |
|---|---|
| **Private key extraction** | Derive private keys from public keys |
| **Transaction forgery** | Sign fraudulent transactions |
| **Historical exposure** | Retroactively decrypt previously recorded data |

## Harvest Now, Decrypt Later

Adversaries may already be collecting encrypted blockchain data today, planning to decrypt it once quantum hardware matures. This makes the threat **present-tense**, not hypothetical.

## The Industry Gap

Despite growing awareness:

- Most protocols have no post-quantum migration plan
- Smart contracts are not audited for quantum vulnerability
- Developers lack accessible tools to assess quantum risk
- Quantum computing resources remain centralized and expensive

## Where VeriQ Fits

VeriQ addresses this gap by enabling developers and organizations to:

1. **Assess** quantum resilience of existing systems today
2. **Optimize** operations using quantum-inspired techniques
3. **Prepare** for post-quantum cryptographic migration

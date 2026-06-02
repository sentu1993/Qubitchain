# QubitChain.io — Frequently Asked Questions

**URL:** https://qubitchain.io/faq  
**Total Questions:** 20  
**Categories:** Quantum Threat · QubitChain Technology · Post-Quantum Cryptography · Security Comparisons · Getting Started

---

## Category 1 — The Quantum Threat

### Q1. What is Q-Day and when will it happen?

**Q-Day** is the projected moment when a **Cryptographically Relevant Quantum Computer (CRQC)** becomes powerful enough to break the encryption algorithms — RSA and ECDSA — that protect virtually every major cryptocurrency and digital communication system.

- Expert estimates: **early 2030s to late 2030s**
- NIST urges organizations to begin migration **no later than 2030**
- The exact date is uncertain — the mathematical certainty of the threat is not

---

### Q2. How does quantum computing threaten Bitcoin and Ethereum?

Bitcoin and Ethereum both rely on **ECDSA (Elliptic Curve Digital Signature Algorithm)** for transaction signing.

**Shor's algorithm** can solve the **Elliptic Curve Discrete Logarithm Problem (ECDLP)** in polynomial time, meaning it can **derive any private key from its public key**.

Every Bitcoin or Ethereum wallet that has ever sent a transaction has its public key **permanently exposed on the blockchain** — making it a potential target.

---

### Q3. What is a "Harvest Now, Decrypt Later" (HNDL) attack?

HNDL is an active attack strategy where adversaries — including **nation-state actors** — collect and archive encrypted data today, intending to decrypt it once quantum computers become powerful enough.

Blockchain data is a uniquely attractive HNDL target because it is:
- **Public** — anyone can download the full chain history
- **Permanent** — data cannot be deleted or re-encrypted
- **High-value** — contains transaction histories and exposed public keys

The **NSA and CISA** have both issued public advisories about active HNDL operations.

---

### Q4. How many qubits are needed to break Bitcoin's encryption?

Breaking Bitcoin's **ECDSA-256** scheme requires approximately:
- **~2,330 logical qubits** running Shor's algorithm *(Webber et al., 2022)*
- **~4 million physical qubits** with current error-correction architectures

For comparison:
- Google Willow: **105** error-corrected qubits
- IBM Condor: **1,121** physical qubits

The gap is closing faster than most people realize, with major breakthroughs announced annually.

---

## Category 2 — QubitChain Technology

### Q5. What is QubitChain.io?

**QubitChain.io** is the world's first blockchain infrastructure built **natively on NIST-standardized Post-Quantum Cryptography (PQC) from the genesis block**.

Unlike classical blockchains that will need to retrofit quantum resistance through hard forks, QubitChain.io was designed from the ground up with:
- Quantum-resistant signature schemes (ML-DSA)
- Quantum random number generation (QRNG)
- Cryptographic agility

---

### Q6. What cryptographic algorithms does QubitChain.io use?

QubitChain.io implements all three **NIST-finalized PQC standards**:

| Standard  | Algorithm                   | Function                           |
|-----------|-----------------------------|------------------------------------|
| FIPS 203  | ML-KEM / CRYSTALS-Kyber     | Quantum-safe key encapsulation     |
| FIPS 204  | ML-DSA / CRYSTALS-Dilithium | Quantum-resistant transaction signing |
| FIPS 205  | SLH-DSA / SPHINCS+          | Hash-based backup signature scheme |

---

### Q7. What is Proof of Quantum Entropy (PoQE)?

**PoQE** is QubitChain.io's novel consensus mechanism that replaces classical randomness sources with **verifiable quantum entropy from hardware QRNG devices** for validator selection.

- **Unlike PoW:** No energy waste from mining
- **Unlike PoS:** No RANDAO manipulation vectors
- **PoQE:** Uses physics-based true randomness that **cannot be predicted or biased** by any participant
- Validator attestations are signed with **ML-DSA**, making the consensus itself quantum-resistant

---

### Q8. What is QRNG and why does QubitChain.io use it?

**Quantum Random Number Generation (QRNG)** exploits the fundamental randomness of quantum mechanical phenomena — such as **quantum vacuum fluctuations** — to produce provably unpredictable random numbers.

Classical computers generate **pseudorandom numbers** that are deterministic and have been exploited in real-world attacks.

QubitChain.io uses QRNG for all key generation, ensuring private keys are sourced from **ontologically random** processes that no computer — classical or quantum — can predict.

---

### Q9. What is cryptographic agility and why does it matter?

**Cryptographic agility** is the architectural ability to upgrade, rotate, or completely replace cryptographic algorithms **without a hard fork**.

- Classical blockchains like Bitcoin have ECDSA **hardcoded** — changing it requires years of governance debate and a disruptive hard fork
- QubitChain.io treats cryptographic algorithms as **pluggable modules**, supporting multiple algorithms simultaneously with hot-swappable upgrades
- This is increasingly a **regulatory requirement** under CISA and NIST guidelines for critical infrastructure

---

## Category 3 — Post-Quantum Cryptography

### Q10. What is post-quantum cryptography (PQC)?

PQC refers to cryptographic algorithms designed to resist attacks from both classical **and** quantum computers.

In **August 2024**, NIST finalized three PQC standards — FIPS 203, 204, and 205 — after a **six-year evaluation of 82 candidate algorithms**.

These standards are now:
- **Mandated** for adoption by U.S. federal agencies
- Increasingly required by financial regulators worldwide
- The new regulatory baseline for digital security

---

### Q11. What is lattice-based cryptography?

Lattice-based cryptography is the mathematical foundation underlying the majority of NIST PQC standards.

It is based on hard computational problems in high-dimensional geometric structures called **lattices**:
- **Learning With Errors (LWE)** problem
- **Shortest Vector Problem (SVP)**

Unlike RSA and ECC, lattice problems have **no known quantum algorithm** that provides a significant speedup. Shor's algorithm cannot attack them because they lack the periodic algebraic structure that quantum algorithms exploit.

---

### Q12. What is the difference between CRYSTALS-Kyber and CRYSTALS-Dilithium?

| Algorithm              | FIPS Standard | Type                        | Replaces         | Used by QubitChain.io for |
|------------------------|---------------|-----------------------------|------------------|---------------------------|
| CRYSTALS-Kyber (ML-KEM)    | FIPS 203      | Key Encapsulation Mechanism | RSA, Diffie-Hellman | All node-to-node communications |
| CRYSTALS-Dilithium (ML-DSA) | FIPS 204      | Digital Signature Algorithm | ECDSA            | All transaction signatures |

Both are based on **Module-LWE** lattice problems but serve different cryptographic functions.

---

### Q13. When will NIST deprecate quantum-vulnerable algorithms?

| Milestone                      | Year |
|-------------------------------|------|
| RSA/ECDSA deprecated          | 2030 |
| RSA/ECDSA fully disallowed    | 2035 |

Organizations not migrated by 2030 will be **non-compliant with federal security requirements**.

For blockchain networks, this is especially critical — migrating a decentralized ledger requires years of coordination, meaning the migration window is **closing right now**.

---

## Category 4 — Security Comparisons

### Q14. How is QubitChain.io different from Bitcoin and Ethereum?

| Layer              | Bitcoin / Ethereum                | QubitChain.io                    |
|--------------------|-----------------------------------|----------------------------------|
| Transaction Signing | ECDSA                            | ML-DSA (CRYSTALS-Dilithium)      |
| Key Generation     | PRNG (deterministic)              | QRNG (true quantum entropy)      |
| Node Communication | RSA / ECDH                        | ML-KEM (CRYSTALS-Kyber)          |
| Consensus          | PoW / PoS (classically vulnerable) | PoQE (natively quantum-secure)  |
| Migration Needed?  | Yes — years of coordination       | No — built quantum-safe at genesis |

---

### Q15. Can Bitcoin or Ethereum be upgraded to be quantum-resistant?

Theoretically yes — practically, **extremely difficult**. Full PQC migration requires:

1. **Community governance consensus** — took years just for the Bitcoin block size debate
2. A coordinated **hard fork** across hundreds of thousands of validators
3. A trusted **wallet migration path** — impossible if keys are already compromised at Q-Day
4. Handling **dormant wallets** whose owners may never return (including Satoshi's ~1.1M BTC)

Ethereum has formed a Post-Quantum working group, but full migration is estimated at **3–5 years minimum** — a timeline that may not outpace quantum hardware development.

---

### Q16. What about Satoshi's Bitcoin? Is it at risk?

**Yes.** Satoshi Nakamoto's estimated **~1.1 million BTC** (~$70+ billion) sits in early **Pay-to-Public-Key (P2PK)** addresses where the **public keys are fully exposed** on the blockchain.

- A sufficiently powerful quantum computer could derive the private keys and drain these funds
- These wallets **cannot be migrated** — the owner is inactive
- They represent an **immediate quantum target** the moment Q-Day arrives
- An estimated **25% of all circulating Bitcoin** resides in similarly exposed addresses

---

## Category 5 — Getting Started

### Q17. How do I join the QubitChain.io waitlist?

Visit: **https://qubitchain.io/#waitlist**

Enter your email to secure priority access. Waitlist members receive:
- Early network access
- Technical updates and protocol announcements
- Quantum security research briefings before public launch

---

### Q18. Is QubitChain.io live yet? When does mainnet launch?

QubitChain.io is currently in the **pre-launch phase**. The core protocol architecture is finalized, including:
- ML-KEM (FIPS 203) integration
- ML-DSA (FIPS 204) integration
- SLH-DSA (FIPS 205) integration
- QRNG entropy subsystem
- Proof-of-Quantum-Entropy (PoQE) consensus mechanism

**Mainnet launch timing will be announced to waitlist members first.**

---

### Q19. Where can I read the QubitChain.io technical whitepaper?

Full technical whitepaper available at: **https://qubitchain.io/whitepaper**

Covers:
- Protocol architecture
- Cryptographic design decisions
- Proof-of-Quantum-Entropy (PoQE) consensus specification
- Cryptographic agility framework

Intended for developers, researchers, and institutional evaluators.

---

### Q20. How can I learn more about quantum blockchain security?

| Resource               | URL                                    | Topics                                                        |
|------------------------|----------------------------------------|---------------------------------------------------------------|
| Blog                   | https://qubitchain.io/blog             | Q-Day timelines, NIST PQC, Shor's algorithm, QRNG, lattices  |
| Technology Page        | https://qubitchain.io/technology       | Full QubitChain.io technology stack                           |
| Q-Day Survival Guide   | https://qubitchain.io/q-day            | Quantum threat landscape and migration rationale              |
| Knowledge Hub          | https://qubitchain.io/hub              | In-depth educational resources                                |
| Whitepaper             | https://qubitchain.io/whitepaper       | Full technical specification                                   |

---

📧 **Still have questions?** Contact us at contact@qubitchain.io  
🔗 **Join the Waitlist:** https://qubitchain.io/#waitlist

---

*© 2026 QubitChain.io. All rights reserved. NIST PQC Compliant.*

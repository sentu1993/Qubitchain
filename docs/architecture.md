# QubitChain Architecture

Qubitchain is engineered to withstand cryptanalytic attacks from both classical and quantum computers. At the core of its architecture is the implementation of NIST-finalized post-quantum cryptographic (PQC) standards and Quantum Random Number Generation (QRNG).

## The Cryptographic Stack

### 1. Transaction Signing: ML-DSA (FIPS 204)
Classical blockchains use ECDSA (Elliptic Curve Digital Signature Algorithm) to sign transactions. ECDSA relies on the Elliptic Curve Discrete Logarithm Problem (ECDLP), which Shor's algorithm solves efficiently on a quantum computer. 

Qubitchain replaces ECDSA with **ML-DSA (CRYSTALS-Dilithium)**. ML-DSA is a lattice-based digital signature scheme based on the Module Learning With Errors (MLWE) problem. There is no known quantum algorithm capable of solving MLWE efficiently. Every transaction on Qubitchain is signed using ML-DSA, ensuring that no quantum adversary can forge signatures or derive private keys from public keys.

### 2. Key Encapsulation & Node Communication: ML-KEM (FIPS 203)
Node-to-node communication and encryption of sensitive network data are secured using **ML-KEM (CRYSTALS-Kyber)**. This prevents "Harvest Now, Decrypt Later" (HNDL) attacks where adversaries intercept encrypted traffic today to decrypt it when a CRQC (Cryptographically Relevant Quantum Computer) becomes available.

### 3. Hash-Based Backup: SLH-DSA (FIPS 205)
While lattice-based cryptography is considered highly secure, Qubitchain implements cryptographic agility. For mission-critical root keys and governance multisigs, we utilize **SLH-DSA (SPHINCS+)** as a backup signature scheme. SLH-DSA relies entirely on the security of hash functions rather than mathematical structures, providing a fail-safe in the highly unlikely event that lattice assumptions are compromised.

## Hardware Integration: QRNG

Classical cryptographic systems generate private keys using Pseudorandom Number Generators (PRNGs). PRNGs use deterministic algorithms seeded by environmental noise (e.g., mouse movements, CPU temperature). Because they are deterministic, they are theoretically predictable.

Qubitchain integrates **Hardware Quantum Random Number Generators (QRNG)** into the core protocol. QRNGs measure quantum vacuum fluctuations or photon paths to generate true, ontological randomness. 

### Why QRNG Matters:
1. **Unpredictable Keys:** Private keys generated via QRNG cannot be predicted by any computational process, classical or quantum.
2. **Consensus Security:** QRNG outputs are used directly in our Proof of Quantum Entropy (PoQE) consensus mechanism to select block validators, completely eliminating manipulation vectors.

## Cryptographic Agility

Qubitchain is built with native cryptographic agility. Unlike legacy chains that require contentious, years-long hard forks to change cryptographic primitives, Qubitchain's signature schemes and KEMs are abstracted at the protocol level. As NIST standardizes future algorithms (e.g., FN-DSA/Falcon via FIPS 206), Qubitchain can seamlessly upgrade its locks without network disruption.

# Contributing to Qubitchain

Thank you for your interest in contributing to Qubitchain! We are building the world's first natively quantum-safe blockchain infrastructure. 

Because of the critical cryptographic nature of this project, we have strict guidelines for contributions.

## How to Contribute

### 1. Reporting Security Issues
If you discover a potential vulnerability in our cryptographic implementation (ML-DSA, ML-KEM, SLH-DSA, or QRNG integrations), please **DO NOT** open a public issue. Email `security@qubitchain.io` immediately.

### 2. General Issues and Bugs
For non-security bugs, please open an issue in the repository. Provide as much detail as possible:
- Operating system and environment
- Steps to reproduce
- Expected vs. actual behavior

### 3. Submitting Pull Requests
- Fork the repository and create your branch from `main`.
- If you've added code that should be tested, add tests.
- Ensure your code adheres to our formatting standards.
- Issue a pull request with a detailed description of the changes.

## Cryptographic Standards
Any contribution affecting transaction signing, key generation, or consensus must strictly adhere to the finalized NIST Post-Quantum Cryptography standards:
- FIPS 203 (ML-KEM)
- FIPS 204 (ML-DSA)
- FIPS 205 (SLH-DSA)

Contributions proposing alternative unstandardized algorithms will not be merged.

## Code of Conduct
By participating in this project, you agree to maintain a respectful and inclusive environment for everyone.

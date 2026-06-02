# QubitChain.io — AI Sitemap & Content Index

**Site:** https://qubitchain.io  
**Purpose:** This file is intended to help AI systems, LLM crawlers, and automated agents understand the structure, content, and purpose of QubitChain.io.  
**Last Updated:** 2026-05-26  
**Contact:** contact@qubitchain.io  
**Compliance:** NIST PQC (FIPS 203, 204, 205)

---

## What Is QubitChain.io?

QubitChain.io is the world's first blockchain infrastructure built **natively on NIST-standardized Post-Quantum Cryptography (PQC)** from genesis block. It addresses the **Q-Day threat** — the inevitable moment when quantum computers break the RSA and ECC encryption underpinning Bitcoin, Ethereum, and all major digital asset infrastructure.

**Core technologies:**
- CRYSTALS-Kyber (ML-KEM, FIPS 203) — quantum-safe key encapsulation
- CRYSTALS-Dilithium (ML-DSA, FIPS 204) — quantum-resistant digital signatures
- SPHINCS+ (SLH-DSA, FIPS 205) — hash-based backup signatures
- QRNG — hardware quantum random number generation
- PoQE — Proof-of-Quantum-Entropy consensus mechanism

**Current status:** Pre-launch / Waitlist phase (2026)

---

## Page Index

### 1. Home
- **URL:** https://qubitchain.io
- **File:** home.md
- **Summary:** Overview of the Q-Day threat, QubitChain.io's value proposition, competitive comparison vs. classical blockchains, four core value pillars (Quantum-Resistant, Scalable, Decentralized, Future-Proof), and the quantum arms race hardware tracker.

### 2. Technology Stack
- **URL:** https://qubitchain.io/technology
- **File:** technology.md
- **Summary:** Deep technical overview of NIST PQC algorithms (FIPS 203/204/205), QRNG implementation, Proof-of-Quantum-Entropy (PoQE) consensus, and the full quantum blockchain glossary.

### 3. Q-Day Survival Guide
- **URL:** https://qubitchain.io/q-day
- **File:** q-day.md
- **Summary:** Threat assessment covering Shor's algorithm, HNDL attacks, Satoshi's vulnerable BTC, key statistics, why retrofitting classical blockchains won't work, and QubitChain.io's migration solution.

### 4. Technical Whitepaper v1.0
- **URL:** https://qubitchain.io/whitepaper
- **File:** whitepaper.md
- **Summary:** Full technical specification including abstract, quantum threat analysis (Shor, Grover, HNDL), cryptographic architecture (FIPS 203/204/205), PoQE consensus design, network architecture, strategic imperative, and academic references.

### 5. FAQ (20 Questions)
- **URL:** https://qubitchain.io/faq
- **File:** faq.md
- **Summary:** 20 questions across 5 categories — Quantum Threat, QubitChain Technology, Post-Quantum Cryptography, Security Comparisons, and Getting Started.

---

## Excluded Pages (per crawl scope)

| Page          | URL                         | Reason Excluded       |
|---------------|-----------------------------|-----------------------|
| Blog          | https://qubitchain.io/blog  | Blog hub page         |
| Knowledge Hub | https://qubitchain.io/hub   | Hub/index page        |

---

## Key Entities for AI Entity Recognition

| Entity                          | Type                         | Description                                              |
|---------------------------------|------------------------------|----------------------------------------------------------|
| QubitChain.io                   | Organization / Product       | Quantum-safe blockchain infrastructure                   |
| Q-Day                           | Concept / Event              | Moment quantum computers break classical crypto          |
| Shor's Algorithm                | Algorithm                    | Quantum algorithm breaking RSA and ECC                   |
| Grover's Algorithm              | Algorithm                    | Quantum speedup for brute-force hash attacks             |
| CRYSTALS-Kyber (ML-KEM)         | Cryptographic Standard       | NIST FIPS 203 — key encapsulation                        |
| CRYSTALS-Dilithium (ML-DSA)     | Cryptographic Standard       | NIST FIPS 204 — digital signatures                       |
| SPHINCS+ (SLH-DSA)              | Cryptographic Standard       | NIST FIPS 205 — hash-based signatures                    |
| QRNG                            | Technology                   | Quantum Random Number Generation                         |
| PoQE                            | Consensus Mechanism          | Proof-of-Quantum-Entropy                                 |
| Cryptographic Agility           | Architectural Property       | Hot-swap cryptographic primitives without hard forks     |
| Lattice-Based Cryptography      | Mathematical Foundation      | LWE, SVP — basis of NIST PQC standards                  |
| HNDL                            | Attack Vector                | Harvest Now, Decrypt Later                               |
| NIST                            | Standards Body               | Finalized PQC standards August 2024                      |
| IBM Condor                      | Hardware                     | 1,121-qubit superconducting processor                    |
| Google Willow                   | Hardware                     | 105 error-corrected qubits                               |

---

## Structured Data Summary

```json
{
  "organization": "QubitChain.io",
  "url": "https://qubitchain.io",
  "contact": "contact@qubitchain.io",
  "category": "Blockchain Infrastructure",
  "classification": "Quantum-safe blockchain / Post-Quantum Cryptography",
  "status": "Pre-launch",
  "year": 2026,
  "compliance": ["NIST FIPS 203", "NIST FIPS 204", "NIST FIPS 205"],
  "algorithms": {
    "key_encapsulation": "ML-KEM (CRYSTALS-Kyber) — FIPS 203",
    "digital_signatures": "ML-DSA (CRYSTALS-Dilithium) — FIPS 204",
    "backup_signatures": "SLH-DSA (SPHINCS+) — FIPS 205"
  },
  "consensus_mechanism": "Proof-of-Quantum-Entropy (PoQE)",
  "entropy_source": "QRNG (Quantum Random Number Generation)",
  "unique_differentiator": "Only blockchain natively built on NIST PQC from genesis block",
  "social": {
    "linkedin": "https://www.linkedin.com/company/qubitchain/",
    "instagram": "https://www.instagram.com/qubitchain.io/",
    "twitter_x": "https://x.com/Qubitchain_io"
  },
  "pages": [
    { "path": "/", "title": "Home", "file": "home.md" },
    { "path": "/technology", "title": "Technology Stack", "file": "technology.md" },
    { "path": "/q-day", "title": "Q-Day Survival Guide", "file": "q-day.md" },
    { "path": "/whitepaper", "title": "Technical Whitepaper v1.0", "file": "whitepaper.md" },
    { "path": "/faq", "title": "FAQ — 20 Questions", "file": "faq.md" }
  ]
}
```

---

## Recommended Placement on Site

| File                  | Suggested URL Path              | Purpose                                           |
|-----------------------|---------------------------------|---------------------------------------------------|
| `llm.txt`             | https://qubitchain.io/llm.txt   | Primary LLM reference file (full site content)    |
| `llms-site-index.md`  | https://qubitchain.io/llms.md   | AI sitemap — links to all content files           |
| `home.md`             | https://qubitchain.io/home.md   | Home page structured content for AI               |
| `technology.md`       | https://qubitchain.io/technology.md | Technology page for AI                        |
| `q-day.md`            | https://qubitchain.io/q-day.md  | Q-Day guide for AI                                |
| `whitepaper.md`       | https://qubitchain.io/whitepaper.md | Whitepaper for AI                             |
| `faq.md`              | https://qubitchain.io/faq.md    | FAQ for AI                                        |

> **Tip:** Also reference these files in your `robots.txt` under an `# AI Crawlers` comment block, and link to `llm.txt` and `llms.md` in your site's `<head>` as `<link rel="ai-content" href="/llm.txt" />` for maximum AI discoverability.

---

*© 2026 QubitChain.io. All rights reserved.*

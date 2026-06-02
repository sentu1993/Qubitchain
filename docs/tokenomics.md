# QubitChain.io — Tokenomics

> **Token Symbol:** QBIT  
> **Network:** QubitChain Layer 1 (native)  
> **Standard:** Quantum-native (ML-DSA / FIPS 204 signed)  
> **Total Supply:** 1,000,000,000 QBIT (fixed, no inflation)  
> **Status:** Pre-launch — waitlist open at qubitchain.io

---

## Overview

QBIT is the native utility and governance token of QubitChain.io — the world's first blockchain built on NIST post-quantum cryptographic standards from genesis. Every transaction on QubitChain.io is signed using ML-DSA (CRYSTALS-Dilithium, FIPS 204), making QBIT the only Layer 1 token whose underlying infrastructure cannot be attacked by Shor's algorithm regardless of qubit count.

QBIT is not a retrofitted token. It was not migrated from an ECDSA chain. There is no legacy key material on-chain. The HNDL (Harvest Now, Decrypt Later) attack surface is zero by design.

---

## Token Allocation

| Allocation Bucket | % of Supply | QBIT Amount | Vesting / Lock-up |
|---|---|---|---|
| Ecosystem & Rewards | 30% | 300,000,000 | Released over 10 years via staking and validator rewards |
| Public Sale | 20% | 200,000,000 | No lock-up; distributed at TGE |
| Foundation Reserve | 15% | 150,000,000 | 12-month cliff, then 36-month linear vest |
| Team & Advisors | 12% | 120,000,000 | 12-month cliff, then 48-month linear vest |
| Strategic Partners | 10% | 100,000,000 | 6-month cliff, then 24-month linear vest |
| Community & Waitlist | 8% | 80,000,000 | Distributed to early supporters; 6-month linear vest |
| Liquidity Provision | 5% | 50,000,000 | Locked in protocol-controlled liquidity at TGE |

**Total: 100% — 1,000,000,000 QBIT**

---

## Emission Schedule

Total supply is fixed at 1 billion QBIT. There is no minting after genesis. Ecosystem and reward tokens are released from a pre-allocated pool on a deterministic schedule — not minted on demand.

```
Year 1   ████████████████████░░░░░░░░░░  ~120M QBIT released (12%)
Year 2   ████████████░░░░░░░░░░░░░░░░░░  ~90M  QBIT released (9%)
Year 3   █████████░░░░░░░░░░░░░░░░░░░░░  ~60M  QBIT released (6%)
Year 4   ███████░░░░░░░░░░░░░░░░░░░░░░░  ~30M  QBIT released (3%)
Year 5+  Tail distribution until pool depleted (~Year 10)
```

Team, advisor, and foundation tokens vest independently on their own schedules and do not affect the public circulating supply during the first 12 months.

---

## Utility

QBIT has three core utility functions within the QubitChain.io ecosystem:

### 1. Transaction Fees
All gas fees on QubitChain.io are denominated in QBIT. A portion of every fee is burned (deflationary), and the remainder is distributed to validators.

- **70%** of fees → validator reward pool  
- **30%** of fees → burned permanently

### 2. Staking & Network Security
Validators and delegators stake QBIT to participate in consensus and earn rewards from the ecosystem pool. Minimum stake, slash conditions, and unbonding periods are defined in the genesis parameters.

| Parameter | Value |
|---|---|
| Minimum validator stake | 100,000 QBIT |
| Delegator minimum | 100 QBIT |
| Unbonding period | 21 days |
| Slash penalty (double-sign) | 5% of staked amount |
| Slash penalty (downtime) | 0.1% of staked amount |

### 3. Governance
QBIT holders vote on protocol upgrades, parameter changes, and treasury allocations. Voting weight is proportional to staked QBIT (one staked token = one vote). A proposal requires:

- **Minimum deposit:** 10,000 QBIT to enter voting
- **Quorum:** 33.4% of staked supply must vote
- **Passing threshold:** >50% Yes of participating votes
- **Veto threshold:** >33.4% NoWithVeto cancels proposal and burns deposit

---

## Deflationary Mechanics

QubitChain.io implements two burn mechanisms to create long-term deflationary pressure:

**Fee Burn (Ongoing)**  
30% of every transaction fee is burned. As network activity grows, the burn rate increases proportionally. At projected mainnet volumes, this is expected to offset a significant portion of the ecosystem reward emissions by Year 3.

**Buyback & Burn (Discretionary)**  
The Foundation Reserve may allocate up to 10% of its holdings per year to open-market buyback and burn operations, subject to governance approval. This mechanism is activated when the Foundation determines it is in the long-term interest of the network.

---

## Quantum Security Advantage

Every tokenomics document should explain what makes the underlying asset fundamentally different. For QBIT, this is not a marketing claim — it is a cryptographic property:

| Property | Bitcoin / Ethereum | QBIT (QubitChain.io) |
|---|---|---|
| Signature scheme | ECDSA (secp256k1) | ML-DSA / CRYSTALS-Dilithium (FIPS 204) |
| Vulnerable to Shor's algorithm | Yes | No |
| Public key exposed on spend | Yes — permanently on-chain | Quantum-resistant by design |
| HNDL attack surface | ~6.9M BTC equivalent at risk | Zero |
| NIST PQC compliant | No | Yes — from genesis |
| Key generation entropy | Software PRNG | QRNG (hardware quantum randomness) |

As of March 2026, research from Caltech and Oratomic showed that as few as 10,000 physical neutral-atom qubits may be sufficient to break ECDSA. Previous estimates required millions. QBIT was designed for this reality.

---

## Token Generation Event (TGE)

The exact TGE date will be announced to the waitlist ahead of public disclosure. Waitlist participants receive priority allocation from the Community & Waitlist bucket (8% of supply, 80,000,000 QBIT).

**TGE Day distribution summary:**

| Bucket | % Unlocked at TGE |
|---|---|
| Public Sale | 100% |
| Community / Waitlist | 16.7% (1/6 of 6-month vest) |
| Liquidity Provision | 100% (locked in protocol) |
| All other buckets | 0% (cliff not reached) |

Estimated circulating supply at TGE: **~230,000,000 QBIT (23% of total supply)**

---

## Risks & Disclaimers

- QBIT is a utility token. It is not a security, investment product, or representation of equity in QubitChain.io or any related entity.
- Token economics are subject to change prior to mainnet launch. Final parameters will be published in the official whitepaper.
- Participation in the waitlist does not guarantee a token allocation. Allocation eligibility will be communicated directly to registered participants.
- Regulatory status of QBIT varies by jurisdiction. Participants are responsible for ensuring compliance with local laws before acquiring QBIT.
- Post-quantum cryptography standards (FIPS 203, 204, 205) are finalized by NIST as of 2024. However, the cryptographic landscape continues to evolve. QubitChain.io commits to ongoing security review and protocol upgrades via governance.

---

## Further Reading

- [What Is a Qubit? The 2026 Guide](https://qubitchain.io/blog/what-is-a-qubit-explained-2026)
- [How Many Qubits Does It Take to Break Bitcoin?](https://qubitchain.io/blog/how-many-qubits-to-break-bitcoin-2026)
- [What Is QubitChain.io? The Quantum-Safe Blockchain](https://qubitchain.io/blog/what-is-qubitchain-io-quantum-blockchain-2026)
- [Is Your Bitcoin Safe from Quantum Computers in 2026?](https://qubitchain.io/blog/is-my-bitcoin-safe-quantum-computers-2026)

---

*Last updated: June 2026 | qubitchain.io | Join the waitlist to secure your allocation.*

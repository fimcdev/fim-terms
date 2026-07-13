# FinnishMark — SOC 2 Alignment Report

**Version:** 1.0
**Last Updated:** 7 July 2026
**Status:** Public Release

---

## 1. Purpose

This document describes how FinnishMark aligns its operational and technical controls with the SOC 2 Trust Services Criteria:

- Security
- Availability
- Processing Integrity
- Confidentiality
- Privacy

This is **not** a SOC 2 Type I or Type II certification.
It is an internal governance and transparency document.

---

## 2. Scope

The scope of this alignment review includes:

- FinnishMark ICO platform (ico.finnishmark.com)
- FinnishMark main brand site (finnishmark.com)
- FinnishMark airdrop platform (get1000fim.com)
- Google Cloud Run (application hosting and backend services)
- Firebase (Firestore, Authentication, App Check)
- Stripe payment verification flows
- Solana token infrastructure
- GitHub repositories
- Cloudflare edge protection (WAF, DDoS, managed rules)

---

## 3. Security (SOC 2 — Common Criteria CC1–CC8)

### Active Controls

- Cloudflare Web Application Firewall (WAF)
- Cloudflare DDoS protection
- Cloudflare edge rate limiting
- Firebase App Check enabled
- Google reCAPTCHA Enterprise active
- Stripe verification for payment validation
- SOL on-chain wallet verification (alternative verification path)
- Firestore security rules (deny-by-default model)
- Mint authority revoked
- Freeze authority revoked (fixed supply enforcement)
- Restricted-jurisdiction geoblocking and access restrictions at the edge (jurisdiction-level controls, per Terms & Conditions Sections 1.3 and 33)

### Control Improvements

- Legacy IP-based Firestore restriction replaced with App Check-based verification model
- Enhanced monitoring via Firebase tools initiated
- Audit log retention policy in progress

### Under Development

- Wallet- and transaction-level sanctions screening (blockchain analytics / blocklist screening)
- Formal Access Control Matrix
- Incident Response Plan
- Change Management Procedure
- Security Incident Documentation Workflow

---

## 4. Availability (A1)

### Current State

- Google Cloud Run on Google Cloud infrastructure
- Cloudflare CDN for global distribution
- Solana mainnet decentralized availability
- ICO infrastructure designed for high availability

### In Progress

- Draft Service Level Objectives (SLOs)
- Business Continuity Plan (BCP)
- Disaster Recovery (DR) testing
- Structured monitoring & alerting expansion

---

## 5. Processing Integrity (PI1)

### Controls in Place

- Stripe-validated ICO and verification payments
- On-chain SOL verification payments (alternative path)
- On-chain token allocation verification (Solana)
- Liquidity lock structure enforced (36-month cliff + 1/24 monthly release)
- Referral abuse prevention logic
- Solana transaction logs archived
- Multi-source price oracle approach (CoinGecko, Coinbase, Binance, Kraken, Pyth, Chainlink)

### Enhancements in Progress

- Automated transaction exception monitoring
- Reconciliation documentation
- Structured rollback and retry documentation

---

## 6. Confidentiality (C1)

### Controls

- HTTPS enforced across all services
- Firebase encryption at rest
- Stripe PCI-DSS compliant payment handling
- Data retention policy defined in the Privacy Policy
- Minimal data collection principle

### Planned Improvements

- Automated data purge scripting
- Data classification policy
- Key management documentation

---

## 7. Privacy (P1–P8)

### Implemented

- Privacy Policy v1.0 published in the official repository
- GDPR-principle-aligned data processing
- Disclosures structured in accordance with MiCA Article 6 principles in the Terms & Conditions and White Paper
- Restricted-jurisdiction controls (jurisdiction-level geoblocking and access restrictions)
- Dual human verification flow (Stripe or SOL wallet) for fraud and Sybil prevention

### In Development

- Wallet- and transaction-level sanctions screening (blockchain analytics / blocklist screening)
- User data deletion/export interface
- Documented data subject request workflow (targeting a 30-day response standard, consistent with the Privacy Policy)
- Privacy risk assessment process
- Data Processing Agreement (DPA) reference documentation

---

## 8. Management Assertion

Management asserts that FinnishMark has implemented operational and technical controls aligned with the SOC 2 Trust Services Criteria as described in this document.

This report:

- Does NOT constitute a SOC 2 Type I audit
- Does NOT constitute a SOC 2 Type II audit
- Is provided for transparency and governance documentation

Independent third-party certification may be pursued in the future if required by business growth, institutional partnerships, or regulatory developments.

---

## 9. Governance Roadmap (High-Level)

Planned governance improvements include:

- Formal Access Control Matrix
- Incident Response Plan publication
- Risk Register implementation
- Change Management Policy
- Documented Backup & Recovery procedures
- Periodic internal compliance review

---

## 10. Related Documentation

| Document | Version | File |
|----------|---------|------|
| Terms & Conditions | 1.0 | `FIM_TERMS_AND_CONDITIONS_V1_0.md` |
| Privacy Policy | 1.0 | `FIM_PRIVACY_POLICY_V1_0.md` |
| White Paper | 1.0 | `FIM_WHITE_PAPER_V1_0.md` |

---

## 11. Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 7 July 2026 | Initial public release |

---

## 12. Disclaimer

This document is for transparency purposes only and should not be interpreted as a certified compliance report. FinnishMark operates as a community-driven Web3 project and maintains continuous improvement of governance practices as the ecosystem evolves.

---

## Contact

For governance or security inquiries:
**legal-sauna [at] finnishmark.com**

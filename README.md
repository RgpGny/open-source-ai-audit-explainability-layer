# Open Source AI Audit & Explainability Layer

## Overview

This project provides an open-source audit and explainability layer for AI systems, focusing on **verifiable decision context** rather than model internals.

As AI systems and large language models are increasingly used in public, corporate, and regulated environments, it becomes critical to reliably record **how** an AI-generated decision was produced. In many real-world systems, execution context is incomplete, mutable, or unverifiable, making audits, compliance checks, and legal verification difficult or impossible.

This project addresses that gap by treating every AI call as an **auditable event** and recording its execution context in a **cryptographically verifiable, append-only log**.

---

## Key Principles

- Context-focused, not model-intrusive  
- Vendor-agnostic and API-compatible  
- Cryptographically verifiable and tamper-evident  
- Open-source, inspectable, and reusable  
- Designed for integration, not as a SaaS product  

---

## What This Project Does

For each AI invocation, the system records:

- Input payload (or its cryptographic hash)
- Model identifier and version metadata
- Relevant parameters and execution settings
- Timestamps and execution metadata
- Output hashes
- Hash links to previous audit events

All audit events are stored in an **append-only log structure** using hash chaining and Merkle tree constructions, making any modification detectable.

---

## What This Project Does NOT Do

- It does not attempt to interpret or explain model internals  
- It does not require access to model weights  
- It does not depend on blockchains or external trust systems  
- It is not a centralized SaaS platform  

---

## Components

- Core audit event schema
- Vendor-agnostic AI audit wrapper
- Immutable log store with cryptographic integrity guarantees
- Verification and integrity checking tools
- Command-line interface (CLI) for inspection and validation
- Documentation and reproducible examples

---

## Use Cases

- Public institutions using AI-assisted decision systems
- Developers building AI-powered applications
- Auditors and compliance teams
- Researchers working on AI governance and accountability
- Organizations needing verifiable AI decision records

---

## Verification Model

Independent tools can verify that:

- A given output corresponds to a specific input and configuration
- Audit logs have not been altered
- The execution sequence is complete and consistent

Verification is deterministic and reproducible across environments.

---

## License

This project is released under the **Apache License 2.0**.

The choice of Apache 2.0 is intentional to encourage broad adoption, including use by public institutions, regulators, and commercial vendors, while providing clear patent and usage protections.

---

## Project Status

This project is under active development as part of an NGI ZERO / NLnet funding proposal.

---

## Team

Project Lead  
Ragıp Günay – Computer Engineer

Team Members  
Duygu Kamalak – Computer Engineer  
Senem Ürkmez – Computer Engineer  
Emir Sercan Korkmazgil – Computer Engineer

---

## Contributions

Community feedback, issue reports, and contributions will be welcome once the initial implementation is published.

Further contribution guidelines will be added during development.

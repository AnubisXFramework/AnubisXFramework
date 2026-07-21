# Framework Overview

**AnubisX Framework — Behavioral Identity Attribution**

---

## Official DOI

**DOI**: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)
**Figshare**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

This release is permanently archived on Zenodo and Figshare.

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)
**Contact**: anubisxframework@gmail.com
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

---

## 1. What is AnubisX?

AnubisX is a scientific framework for digital identity attribution based on the principle that human operators leave persistent, measurable cognitive signatures in their digital interactions. Unlike traditional attribution methods that track technical artifacts (IP addresses, device fingerprints, browser cookies), AnubisX analyzes involuntary behavioral patterns — the unconscious habits of language, timing, interaction, and organization that are unique to each individual.

The framework provides:
- A formal theoretical foundation (axioms, hypotheses, design principles)
- A mathematical formalism (definitions, equations, functions)
- A multi-modal architecture (behavioral modalities, fusion strategies)
- A validation framework (tiered hierarchy, acceptance criteria)
- Experimental validation
- Case studies across multiple platforms

## 2. The Problem: Digital Attribution Gaps

### 2.1 Current Attribution Limitations

Digital attribution — determining who is behind observed online behavior — relies almost exclusively on **technical indicators**:

| Indicator | Limitation |
|---|---|
| IP addresses | Easily spoofed via VPNs, proxies, Tor |
| Device fingerprints | Blocked by anti-fingerprinting browsers |
| Cookies | Cleared, blocked, or compartmentalized |
| Account credentials | Stolen, shared, or synthetic |
| Behavioral (single-modality) | Limited accuracy, easy to obfuscate |

These technical indicators share a fundamental weakness: they are properties of the **tool**, not the **operator**. An adversary who controls their technical environment can evade technical attribution.

### 2.2 The Behavioral Attribution Gap

The scientific community has demonstrated that behavioral patterns — stylometric, temporal, interactional — carry individual-specific information. However, prior work has been:
- **Single-modality**: Stylometry in isolation, without cross-modal validation
- **Platform-specific**: Validated on one platform, not generalized
- **Methodologically inconsistent**: No standardized validation framework
- **Theoretically underdeveloped**: No unifying theory of why behavioral attribution works

AnubisX bridges this gap with a comprehensive theoretical, mathematical, and empirical framework.

## 3. The Paradigm Shift: Behavioral vs. Technical Attribution

| Dimension | Technical Attribution | Behavioral Attribution (AnubisX) |
|---|---|---|
| **Target** | What the user has (IP, device) | Who the user is (cognitive patterns) |
| **Evadability** | Easily changed (VPN, new device) | Difficult to change (involuntary habits) |
| **Persistence** | Session-level | Years (stable across technical changes) |
| **Dimensionality** | Low | High (multiple features, multiple modalities) |
| **Certainty** | Binary (match/no match) | Probabilistic (Likelihood Ratio) |
| **Validation** | Ad-hoc | Formal (tiered criteria) |
| **Theoretical Basis** | Engineering | Cognitive science + forensic science |

### 3.1 Key Insight

The core insight is that each individual possesses a **Cognitive Centroid** — a unique, mathematically stable attractor in behavioral feature space toward which their observable patterns converge over time. This centroid is:
- **Unique**: No two individuals share the same attractor
- **Persistent**: Stable across changes in technical infrastructure
- **Multi-modal**: Expressed across language, timing, interaction, network, and environment
- **Involuntary**: Largely outside conscious control
- **Measurable**: Quantifiable through statistical analysis of digital traces

## 4. Framework Components

### 4.1 Theoretical Foundation

The framework is built on formal axioms, research hypotheses, and design principles organized into groups covering core identity theory, behavioral signal theory, attribution logic, evidence handling, and reasoning methodology.

### 4.2 Mathematical Framework

A comprehensive set of mathematical definitions, formal equations, and functions organized into a type system, equation catalog, domain algebra, signal decomposition model, and likelihood ratio framework.

### 4.3 Algorithms

The framework defines multiple algorithms across domains including core processing, behavioral analysis, identity determination, evidence processing, attribution scoring, confidence estimation, similarity and distance computation, multi-modal fusion, and decision logic.

### 4.4 Architecture

A multi-layer architecture implementing a processing pipeline with multiple behavioral modalities and three workflows (Identification, Verification, Forensic Comparison).

### 4.5 Validation Framework

A multi-tier validation hierarchy:
- **Unit**: Individual components
- **Component**: Modality-level pipelines
- **System**: Multi-modal fusion
- **Operational**: Deployment context

## 5. Prototype Implementation

The Anubis Twitter Intelligence Prototype is a working implementation of the framework's core stylometric modality for the Twitter/X platform, demonstrating the feasibility of the theoretical framework.

### 5.1 Known Limitations

- Selected embedding models may be unavailable due to third-party authentication issues
- Temporal feature extraction requires valid timestamp data
- Interaction data collection remains pending
- Cross-platform pipelines are not yet operational
- Only the stylometric modality is currently implemented

## 6. Experimental Validation Summary

### 6.1 Executed Experiments

Multiple experiments were executed on a sample of Twitter accounts, including:
- Stylometric fingerprint extraction
- Embedding validation
- Lexical feature extraction
- Topic vector extraction
- Similarity search and comparison
- Cross-user similarity distribution analysis
- Demographic filtering assessment
- Publication readiness evaluation

### 6.2 Key Results

The prototype demonstrated functional capability for stylometric fingerprinting and similarity search. Selected claims are publication-ready, while others require further validation with additional data collection (timestamps, interactions, cross-platform data) and ground-truth verification.

### 6.3 Validation Constraints

- Temporal features require valid timestamp data not yet available
- Network modality cannot be tested without interaction data
- Cross-platform pipelines are not operational
- Formal accuracy measurement requires comprehensive ground-truth data

## 7. Publication Readiness

### 7.1 Claims Publication Pipeline

Selected framework claims regarding stylometric fingerprinting, demographic filtering, and similarity search are publication-ready. Claims involving embedding ensemble integration, temporal feature extraction, formal accuracy validation, and end-to-end pipeline execution require further validation.

### 7.2 Overall Readiness

The framework is structurally complete with a fully specified theoretical foundation and functional prototype. Formal validation against acceptance criteria requires additional data collection and ground-truth verification.

## 8. Getting Started

### For Researchers
- Start with the Theory Guide for foundational concepts
- Review the Axiomatic System for formal foundations
- Read the Validation documents for testing methodology
- Explore the Algorithms catalog

### For Engineers
- Start with the Architecture document for system design
- Review the Framework Guide
- See the Examples document
- Check the Benchmarking Guide

### For Investigators
- Start with the Overview (this document) for high-level understanding
- Review the FAQ for common questions
- Explore the Attribution Framework for LR interpretation

### For Evaluators
- Review the Validation documents for acceptance criteria
- Check the Benchmarking Guide for evaluation protocols
- See the Glossary for terminology

## 9. Cross-References

| Document | Description |
|---|---|
| Architecture | Complete multi-layer architecture |
| Framework Guide | Implementation guide |
| Theory Guide | Theoretical foundations |
| Algorithms | Algorithms catalog |
| Validation | Validation hierarchy |
| Examples | Usage walkthroughs |
| FAQ | Frequently asked questions |
| Glossary | Standardized terminology |
| References | Document references |
| Axiomatic System | Axioms, hypotheses, design principles |
| Attribution Framework | LR-based attribution |
| Multi-Modal Framework | Modalities and fusion |
| Benchmarking Guide | Evaluation scenarios |

---

---

**Project**: AnubisX Framework  
**Primary Author**: Ahmed Awad (NullC0d3)  
**Author Profile**: https://www.linkedin.com/in/nullc0d3/  
**ORCID**: https://orcid.org/0009-0005-0654-3393  
**Original Framework**: Ahmed Awad (NullC0d3)  
**Original Research**: Ahmed Awad (NullC0d3)  
**Repository**: [https://github.com/AnubisXFramework/AnubisXFramework](https://github.com/AnubisXFramework/AnubisXFramework)  

**DOI**: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)
**Figshare**: [https://doi.org/10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)
**Contact**: anubisxframework@gmail.com
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

**Copyright** © 2026 Ahmed Awad (NullC0d3). All rights reserved.  
Original documentation, framework design, algorithms, source code, diagrams, and repository structure are the intellectual work of Ahmed Awad (NullC0d3), unless otherwise indicated. Third-party software, libraries, datasets, and referenced works remain the property of their respective owners and are governed by their own licenses.

---

*Classification: PUBLIC (C0)*

# Framework Guide

**AnubisX Framework — Integration Guide**

---

## Official DOI

DOI: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)

This release is permanently archived on Zenodo under DOI: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)

**Figshare**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)

**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

**Contact**: [anubisxframework@gmail.com](mailto:anubisxframework@gmail.com)

---

## 1. Introduction

This guide describes the AnubisX Framework's theoretical architecture, conceptual pipeline, fusion strategies, and decision framework. It is intended for researchers and practitioners interested in the framework's scientific foundations.

---

## 2. The Multi-Layer Architecture

The framework is organized into conceptual layers, each responsible for a distinct phase of the attribution process:

```
┌─────────────────────────────────────────────────────┐
│                   DECISION LAYER                     │
│    Attribution conclusions with quantified uncertainty│
├─────────────────────────────────────────────────────┤
│                  EVIDENCE LAYER                      │
│    Fusion, weighting, calibration, LR computation    │
├─────────────────────────────────────────────────────┤
│                 COMPARISON LAYER                     │
│    Profile matching, similarity scoring, ranking     │
├─────────────────────────────────────────────────────┤
│                  PROFILE LAYER                       │
│    Profile construction, normalization, centroid     │
├─────────────────────────────────────────────────────┤
│                  FEATURE LAYER                       │
│    Feature extraction, signal decomposition          │
├─────────────────────────────────────────────────────┤
│                   DATA LAYER                         │
│    Acquisition, validation, storage, preprocessing   │
└─────────────────────────────────────────────────────┘
```

### 2.1 Data Layer
Raw behavioral data is acquired, validated for quality, and stored for subsequent processing. Quality gates ensure that only data meeting minimum standards enters the pipeline.

### 2.2 Feature Layer
Raw data is transformed into structured feature vectors. Behavioral signals are isolated from contextual and noise components through signal decomposition, enabling the framework to focus on individual-specific patterns.

### 2.3 Profile Layer
Feature vectors are assembled into behavioral profiles representing an individual's characteristic patterns. Cognitive centroids — the central tendency of behavioral observations — are estimated as reference points for comparison.

### 2.4 Comparison Layer
Questioned profiles are compared against reference profiles using appropriate similarity measures. This layer supports both identification (searching a database) and verification (confirming a claimed identity).

### 2.5 Evidence Layer
Similarity scores are transformed into likelihood ratios, weighted by evidence quality and recency, and fused across multiple behavioral modalities to produce a combined evidential quantity.

### 2.6 Decision Layer
The combined likelihood ratio is evaluated against decision thresholds to produce an attribution conclusion with quantified uncertainty. The framework explicitly accommodates inconclusive outcomes when evidence is insufficient.

---

## 3. Behavioral Modalities

The framework processes behavioral evidence from multiple sources. Each modality captures a different facet of individual behavioral patterns:

- **Forensic Stylometry**: Analysis of textual communication patterns, including vocabulary, syntax, and stylistic markers
- **Chrono-Profiling**: Analysis of temporal patterns in activity, including rhythms and periodicity
- **Terminal Profiling**: Analysis of interaction patterns with computational environments
- **Network Analysis**: Analysis of social graph structure and relational patterns
- **Media Forensics**: Analysis of digital environment organization and file management patterns

Each modality offers different characteristics in terms of discriminability, robustness, and involuntariness.

---

## 4. Three Primary Workflows

### 4.1 Identification (1:N)
Determines which known individual produced the questioned behavior by searching against a database of known profiles. Relevant for unknown actor attribution.

### 4.2 Verification (1:1)
Confirms or rejects a claimed identity by comparing questioned behavior against a specific reference profile. Relevant for access control and identity confirmation.

### 4.3 Forensic Comparison
Quantifies the strength of evidence linking questioned behavior to a suspect, producing a likelihood ratio with uncertainty bounds. Relevant for investigative and evidentiary contexts.

---

## 5. Multi-Modal Fusion Strategies

The framework supports multiple approaches to combining evidence from different behavioral modalities:

- **Score-Level Fusion**: Combining similarity scores prior to likelihood ratio transformation — the simplest approach, robust to missing data
- **Feature-Level Fusion**: Combining feature vectors before profile construction to capture cross-modal interactions
- **Decision-Level Fusion**: Combining independent modality-level decisions, preserving modality independence and supporting heterogeneous data availability

Each strategy offers distinct trade-offs between complexity, accuracy, missing-data handling, and interpretability.

---

## 6. Decision Framework

### 6.1 Likelihood Ratio
The central decision quantity is the likelihood ratio:

```
LR = P(E | H_p) / P(E | H_d)
```

where E is the observed behavioral evidence, H_p is the hypothesis that the evidence originates from the source, and H_d is the hypothesis that it originates from a different source.

### 6.2 Attribution Confidence Metric (ACM)
The ACM quantifies the reliability of each attribution decision based on factors including confidence in the similarity comparison, quantity of evidence supporting the conclusion, number of modalities contributing evidence, and stability of the likelihood ratio estimate.

### 6.3 Inconclusive Determination
Following forensic science standards, inconclusive outcomes are valid and must be clearly distinguished from negative outcomes:

- Sufficient evidence above threshold: Positive attribution
- Sufficient evidence below threshold: Negative attribution (exclusion)
- Insufficient evidence: Inconclusive

---

## 7. Cross-References

| Document | Description |
|---|---|
| Overview | Framework overview |
| Architecture | Multi-layer architecture |
| Theory Guide | Theoretical foundations |
| Algorithms | Algorithm catalog |
| Validation | Validation methodology |
| Axiomatic System | Axioms, hypotheses, design principles |
| Attribution Framework | LR-based attribution |
| Multi-Modal Framework | Behavioral modalities and fusion |
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

**Copyright** © 2026 Ahmed Awad (NullC0d3). All rights reserved.  
Original documentation, framework design, algorithms, source code, diagrams, and repository structure are the intellectual work of Ahmed Awad (NullC0d3), unless otherwise indicated. Third-party software, libraries, datasets, and referenced works remain the property of their respective owners and are governed by their own licenses.

---

*Classification: PUBLIC (C0)*
*Version: 1.0*
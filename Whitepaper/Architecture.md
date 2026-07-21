# Architecture: AnubisX Framework

**Document ID**: WHP-ARCH-001  
**Version**: 3.0.0  
**Classification**: PUBLIC (C0)

---

## Official DOI

DOI: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)  
**Figshare DOI**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

This release is permanently archived on Zenodo under DOI: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)  
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)  
**Contact**: anubisxframework@gmail.com

---

## 1. Overview

The AnubisX Framework architecture is organized as a multi-layer, multi-stage pipeline supporting three distinct workflows across five behavioral modalities.

---

## 2. Layered Architecture

| Layer | Function |
|-------|----------|
| **Layer 1: Data Acquisition** | Ingest raw behavioral data from source platforms |
| **Layer 2: Feature Extraction** | Transform raw data into measurable features |
| **Layer 3: Profile Construction** | Build behavioral profiles from feature vectors |
| **Layer 4: Comparison Engine** | Compare profiles using similarity metrics |
| **Layer 5: Evidence Evaluation** | Evaluate comparison results as evidence |
| **Layer 6: Decision Framework** | Render identity decisions with confidence |

---

## 3. Multi-Stage Pipeline

Ingest → Normalize → Extract → Profile → Compare → Decide

---

## 4. Three Workflows

- **Identification**: Given a query profile, find the best match in a gallery
- **Verification**: Determine if two profiles belong to the same identity
- **Forensic Comparison**: Produce LR-based evidentiary weight

---

## 5. Five Behavioral Modalities

| Modality | Behavioral Signal |
|----------|------------------|
| Stylometric | Writing style, vocabulary, syntax |
| Temporal | Timing patterns, posting rhythms |
| Interaction Graph | Social graph, mention, retweet patterns |
| Cross-Platform | Schema-mapped behavioral traces |
| Multi-Modal Fusion | Ensemble of modalities |

---

## 6. Component Overview

The architecture defines components spanning data normalization, feature extraction across modalities, profile construction and storage, multi-metric comparison, evidence calibration and fusion, and decision-making with confidence quantification. A complete component catalog is available in the framework documentation.

---

## 7. Prototype Architecture (Anubis Twitter v2.5)

The prototype implements the lower layers for the stylometric modality, demonstrating data acquisition from a sample of social media accounts, feature extraction using language model embeddings, profile construction through fingerprint generation, and efficient similarity search. The prototype validates the architectural concepts for the stylometric modality while identifying areas requiring further development for full framework implementation.

---

## 8. Relationship to Full Framework

The prototype implements stylometric analysis completely, while temporal analysis, graph analysis, multi-modal fusion, and full decision framework components remain at earlier stages of specification or implementation.

---

**Project**: AnubisX Framework  
**Primary Author**: Ahmed Awad (NullC0d3)  
**Author Profile**: https://www.linkedin.com/in/nullc0d3/  
**ORCID**: https://orcid.org/0009-0005-0654-3393  
**Original Framework**: Ahmed Awad (NullC0d3)  
**Original Research**: Ahmed Awad (NullC0d3)  
**Repository**: [https://github.com/AnubisXFramework/AnubisXFramework](https://github.com/AnubisXFramework/AnubisXFramework)

**DOI**: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)

**Copyright** © 2026 Ahmed Awad (NullC0d3). All rights reserved.  
Original documentation, framework design, algorithms, source code, diagrams, and repository structure are the intellectual work of Ahmed Awad (NullC0d3), unless otherwise indicated. Third-party software, libraries, datasets, and referenced works remain the property of their respective owners and are governed by their own licenses.

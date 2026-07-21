# Architecture

**AnubisX Framework — System Architecture Overview**

---

## Architectural Overview

The AnubisX Framework defines a layered, modular architecture for behavioral identity attribution. The architecture separates concerns across six layers, each with well-defined interfaces and responsibilities.

### Six-Layer Architecture

```
┌──────────────────────────────────────────────────────────────────────┐
│                    Decision Layer                                    │
│  Threshold comparison, attribution/exclusion/inconclusive             │
├──────────────────────────────────────────────────────────────────────┤
│                   Evidence Layer                                     │
│  Calibration, weighting, fusion, confidence estimation               │
├──────────────────────────────────────────────────────────────────────┤
│                  Comparison Layer                                    │
│  Similarity functions, distance metrics, scoring                     │
├──────────────────────────────────────────────────────────────────────┤
│                  Profile Layer                                       │
│  Profile construction, storage, versioning, updates                  │
├──────────────────────────────────────────────────────────────────────┤
│                  Feature Layer                                       │
│  Feature extraction, normalization, transformation                   │
├──────────────────────────────────────────────────────────────────────┤
│                    Data Layer                                        │
│  Ingestion, validation, metadata extraction, storage                 │
└──────────────────────────────────────────────────────────────────────┘
```

### Architectural Principles

| Principle | Description |
|---|---|
| **Modularity** | Each layer and modality is independently replaceable |
| **Standardization** | All layers use standardized data formats |
| **Composability** | Stages can be flexibly composed |
| **Auditability** | Every processing step is recorded for full traceability |
| **Uncertainty Propagation** | All layers propagate uncertainty estimates through the pipeline |

---

## Six-Stage Pipeline

### Stage 1: Data Ingestion
Platform adapters normalize input from different sources.

### Stage 2: Feature Extraction
Modality-specific extractors transform raw data into structured feature vectors.

### Stage 3: Profile Construction
Features are aggregated across observations to build behavioral profiles.

### Stage 4: Comparison
Profiles are compared using similarity functions.

### Stage 5: Evidence Evaluation
Scores are calibrated into Likelihood Ratios, weighted, and fused across modalities.

### Stage 6: Decision
The combined LR is compared against decision thresholds.

---

## Three Primary Workflows

| Workflow | Purpose | Output |
|---|---|---|
| **Identification** | Determine who produced questioned material | Matched identity or exclusion |
| **Verification** | Confirm or refute a claimed identity | LR for claimed identity |
| **Forensic Comparison** | Compare questioned to reference set | LR for each comparison |

---

## Components

| Component | Layer | Responsibility |
|---|---|---|
| Platform Adapter | Data | Normalize platform-specific data formats |
| Data Validator | Data | Verify input schema and data types |
| Modality Router | Feature | Determine which extractors to apply |
| Feature Extractor | Feature | Compute behavioral features per modality |
| Feature Normalizer | Feature | Platform and context normalization |
| Profile Builder | Profile | Aggregate features into profiles |
| Centroid Estimator | Profile | Compute Cognitive Centroid |
| Temporal Updater | Profile | Integrate new observations |
| Comparator | Comparison | Compute similarity scores |
| Feature Aligner | Comparison | Ensure compatible feature sets |
| Calibrator | Evidence | Transform scores to LRs |
| Fusion Engine | Evidence | Combine modality evidence |
| Confidence Estimator | Evidence | Quantify attribution certainty |
| Threshold Comparator | Decision | Apply decision thresholds |
| Sequential Decision Engine | Decision | Deferred decisions |
| Report Generator | Decision | Produce standardized reports |

---

## Five Behavioral Modalities

| Modality | Input Data | Features |
|---|---|---|
| **Forensic Stylometry** | Text content | Function-word frequencies, syntax patterns, vocabulary metrics |
| **Chrono-Profiling** | Timestamped activity | Circadian phase, inter-event intervals, burst parameters |
| **Terminal Execution Profiling** | Command logs | Command sequences, timing patterns |
| **Relational Network Analysis** | Social graph data | Graph topology, centrality, entropy |
| **Environmental Media Forensics** | File metadata | Organizational patterns, naming conventions |

---

## Attribution Decision Framework

Attribution strength is expressed as a Likelihood Ratio:

```
LR = P(E | H_same) / P(E | H_diff)
```

| Condition | Conclusion |
|---|---|
| LR ≥ τ_attribution | Same-source (attribution) |
| LR ≤ τ_exclusion | Different-source (exclusion) |
| τ_exclusion < LR < τ_attribution | Inconclusive |

---

## Prototype Architecture

The validated prototype implements a subset of the full six-layer architecture, demonstrating the stylometric modality end-to-end.

### Layer Mapping

| Theoretical Layer | Prototype Implementation |
|---|---|
| **Data Layer** | Data ingestion, metadata extraction, chain-of-custody logging |
| **Feature Layer** | Multi-dimensional stylometric feature extraction and normalization |
| **Profile Layer** | Per-account profile construction via feature aggregation |
| **Comparison Layer** | Cosine similarity search across profiles |
| **Evidence Layer** | Score distribution analysis, empirical LR estimation |
| **Decision Layer** | Threshold-based attribution decisions |

### Key Findings

1. Stylometric fingerprints are persistent across diverse topic contexts
2. Cross-user separation is measurable
3. Efficient comparison enables operational-scale search
4. A subset of empirical claims meet publication thresholds

### Next Architecture Phases

| Phase | Scope |
|---|---|
| **Phase 2** | Multi-modality integration (Chrono-Profiling) |
| **Phase 3** | Full fusion engine |
| **Phase 4** | End-to-end automation |
| **Phase 5** | Multi-platform adapters and cross-platform validation |

---

**Project**: AnubisX Framework  
**Primary Author**: Ahmed Awad (NullC0d3)  
**Author Profile**: https://www.linkedin.com/in/nullc0d3/  
**ORCID**: https://orcid.org/0009-0005-0654-3393  
**Website**: https://anubisxframework.github.io  
**Mirror**: https://anubisxframework.nullc0d3.workers.dev  
**Contact**: anubisxframework@gmail.com  
**Original Framework**: Ahmed Awad (NullC0d3)  
**Original Research**: Ahmed Awad (NullC0d3)  
**Repository**: Official AnubisX Repository

**Copyright** © 2026 Ahmed Awad (NullC0d3). All rights reserved.  
Original documentation, framework design, algorithms, source code, diagrams, and repository structure are the intellectual work of Ahmed Awad (NullC0d3), unless otherwise indicated. Third-party software, libraries, datasets, and referenced works remain the property of their respective owners and are governed by their own licenses.

**DOI**: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)  
**Figshare DOI**: [https://doi.org/10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

---

*Classification: PUBLIC (C0)*

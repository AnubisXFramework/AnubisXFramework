# Theory Guide

**AnubisX Framework — Theoretical Foundations of Behavioral Identity Attribution**

---

## Official DOI

**DOI**: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)
**Figshare**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

This release is permanently archived on Zenodo and Figshare.

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)
**Contact**: anubisxframework@gmail.com
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

---

## 1. Introduction

This guide presents the theoretical foundations of the AnubisX Framework. It covers the Cognitive Centroid theory, the formal axioms, hypotheses, and design principles, the assumptions, Identity Intelligence (IdINT) as a proposed discipline, the five tracking modalities and their theoretical basis, the signal decomposition model, and the Likelihood Ratio framework.

---

## 2. Cognitive Centroid Theory

### 2.1 Core Concept

The Cognitive Centroid is the central theoretical construct of the AnubisX Framework. It is defined as the unique, mathematically stable attractor in behavioral feature space toward which an individual's observable behavioral patterns converge over time.

Formally, for an individual i, the Cognitive Centroid C_i is the expected value of their behavioral feature vector f_i(t) over time and contexts:

```
C_i = E_{t,c}[f_i(t, c)]
```

where t indexes time and c indexes context.

### 2.2 Key Properties

| Property | Description |
|---|---|
| **Uniqueness** | No two individuals share the same centroid |
| **Persistence** | Stable across technical infrastructure changes |
| **Convergence** | Observable patterns converge toward centroid with sufficient observations |
| **Multi-modality** | Expressed across all behavioral modalities |
| **Involuntariness** | Largely outside conscious control |
| **Stability** | Changes slowly through learning and habituation |

### 2.3 Theoretical Support

The Cognitive Centroid is supported by established science:

| Field | Support |
|---|---|
| **Cognitive Psychology** | Stable individual differences in cognitive processing (attention, memory, executive function) |
| **Psycholinguistics** | Linguistic idiolect — each individual has unique patterns of language use |
| **Procedural Memory** | Motor and cognitive routines are encoded as stable procedural memories |
| **Signal Detection Theory** | Individuals have stable response criteria and sensitivity profiles |
| **Behavioral Biometrics** | Keystroke dynamics, gait analysis, and voice recognition demonstrate individual-specific patterns |

### 2.4 Centroid Estimation

The Cognitive Centroid is estimated as the mean of observed feature vectors:

```
C_i_hat = (1/n) * sum(f_i_j)
```

where f_i_j are n feature vectors from individual i. The estimate converges asymptotically with increasing observations.

---

## 3. The Formal Axioms

The framework's axiomatic system comprises formal axioms organized into groups, supported by research hypotheses and design principles. Each axiom states a fundamental truth that is accepted without proof within the framework.

### 3.1 Core Hypotheses

| Name | Statement |
|---|---|
| Identity Invariance | An individual's cognitive processing habits converge toward a unique, mathematically stable attractor — the Cognitive Centroid |
| Cognitive Persistence | Behavioral patterns persist across changes in technical infrastructure |
| Multi-Modal Convergence | No single modality provides definitive attribution; convergence of multiple independent signals is required |
| Observational Bound | The empirical error rate of any attribution system is bounded below by the quantity and quality of observations |
| Behavioral Identity as Emergent Property | Identity attribution emerges from the convergence of independent behavioral measurements |

### 3.2 Behavioral Hypotheses

Characterize the nature, measurability, and structure of human behavioral signals:

| Name | Statement |
|---|---|
| Involuntary Signal Emission | Human operators involuntarily emit behavioral signatures during digital interaction |
| Signal Stability | Behavioral signals exhibit temporal stability over meaningful forensic timeframes |
| Signal Degradation | Behavioral signals degrade over time through drift, learning, and habituation |
| Deliberate Modification Cost | Conscious modification of behavioral signals imposes cognitive load, degrading other signals |
| Involuntary Signal Hierarchy | More involuntary signals carry higher forensic value than voluntary signals |
| Cross-Modal Signal Independence | Behavioral signals across different modalities exhibit approximate independence |

### 3.3 Identity Hypotheses

Formalize the relationship between behavioral signals and identity:

| Name | Statement |
|---|---|
| Identity Singularity | Each individual possesses exactly one Cognitive Centroid |
| Profile Estimability | The Cognitive Centroid can be estimated from finite observations |
| Baseline Refresh Necessity | Behavioral baselines must be periodically refreshed to account for drift |
| Identity Resolution Uniqueness | Cross-platform identity resolution is unique |
| Identity Profile Boundaries | Identity profiles have measurable boundaries in feature space |

### 3.4 Attribution Principles

Define the logical structure of attribution claims:

| Name | Statement |
|---|---|
| Multi-Modal Necessity | Attribution conclusions must be based on at least two independent behavioral modalities |
| Probabilistic Output | Attribution conclusions must be expressed as probabilities, not certainties |
| Quantified Conclusion | All attribution conclusions must include quantified uncertainty |
| Inconclusive Admissibility | Inconclusive outcomes are valid and must be clearly distinguished from negative outcomes |
| Reproducible Procedure | All attribution procedures must be reproducible by independent examiners |

### 3.5 Evidence Principles

Establish standards for evidence collection and handling:

| Name | Statement |
|---|---|
| Evidential Independence | Evidence sources should be independent unless dependence is explicitly modeled |
| Convergence Necessity | Attribution requires convergence of independent evidence streams |
| Conflict Transparency | Conflicts between evidence sources must be reported, not hidden |
| Weighted Combination | Evidence must be weighted by quality, relevance, and recency before combination |
| Falsifiability Requirement | All attribution claims must be empirically falsifiable |

### 3.6 Reasoning Principles

Govern the inferential logic connecting evidence to conclusions:

| Name | Statement |
|---|---|
| Conservative Interpretation | The framework must be biased against false positives |
| Hypothesis Testing | Attribution is framed as hypothesis testing |
| Empirical Grounding | All probabilistic estimates must be empirically grounded |
| Methodological Transparency | All methodological choices must be explicitly documented |
| Alternative Hypothesis Consideration | All reasonable alternative hypotheses must be considered and addressed |

---

## 4. The Assumptions

The framework depends on assumptions organized into categories. Unlike axioms (accepted as fundamental), assumptions have varying empirical support:

| Category | Description |
|---|---|
| Core | Foundational assumptions about identity and behavior |
| Behavioral | Assumptions about signal nature and measurability |
| Identity | Assumptions about profile structure and uniqueness |
| Data | Assumptions about data quality and representativeness |
| Platform | Assumptions about platform effects |
| AI / ML | Assumptions about machine learning model behavior |

Some assumptions are empirically supported by published research; others are proposed pending verification or accepted conditionally.

---

## 5. Identity Intelligence (IdINT) as a Proposed Discipline

Identity Intelligence (IdINT) is proposed as a formal forensic discipline alongside DNA analysis, fingerprinting, firearm examination, and document analysis.

### 5.1 The Case for IdINT

Traditional forensic disciplines analyze physical traces left by the human body:
- **DNA**: Biological material
- **Fingerprints**: Friction ridge skin impressions
- **Ballistics**: Tool marks on ammunition
- **Handwriting**: Motor control patterns

IdINT argues that **cognitive traces** — patterns of language, timing, interaction, and organization — are equally individual-specific and should be recognized as a distinct class of forensic evidence.

### 5.2 Scientific Basis

IdINT draws on established science:

| Foundation | Contribution |
|---|---|
| Cognitive psychology | Stable individual differences in attention, memory, executive function |
| Psycholinguistics | Linguistic idiolect and unconscious language processing |
| Forensic science | LR framework, Daubert standard, error rate methodology |
| Biometrics | Individual identification from measurable traits |
| Signal detection theory | Decision framework under uncertainty |

### 5.3 Meeting Daubert Standards

The framework is designed to meet the Daubert standard for admissibility of scientific evidence:

| Daubert Factor | AnubisX Response |
|---|---|
| Testability | Falsifiable predictions, multiple experiments |
| Peer review | Publication pipeline planned |
| Error rate | Acceptance criteria, accuracy metrics |
| Standards | Standardized protocols, reproducibility requirements |
| General acceptance | Novel discipline — acceptance built through publication |

---

## 6. The Five Tracking Modalities

### 6.1 Forensic Stylometry

**Theoretical basis**: Linguistic idiolect — each individual has stable, unique patterns of language use that emerge from their language acquisition history, cognitive processing style, and habitual linguistic choices.

**Key signals**: Function-word frequencies, syntactic structure preferences, vocabulary richness, readability metrics, punctuation habits.

### 6.2 Chrono-Profiling

**Theoretical basis**: Temporal cognition — individuals have stable circadian rhythms, attentional cycles, and temporal habits that manifest in their digital activity patterns.

**Key signals**: Circadian activity rhythms, inter-event timing distributions, response time patterns, temporal clustering, periodicity.

### 6.3 Terminal Execution Profiling

**Theoretical basis**: Procedural memory and motor programming — individuals develop stable patterns of human-machine interaction through repeated practice, encoded as procedural memories.

**Key signals**: Command sequences, navigation paths, input timing and rhythm, error patterns, tool selection preferences.

### 6.4 Relational Network Analysis

**Theoretical basis**: Social cognition — individuals have stable patterns of relationship formation, communication, and group dynamics that reflect their social cognitive style.

**Key signals**: Network topology, communication frequency, group affiliations, information propagation patterns, network roles.

### 6.5 Environmental Media Forensics

**Theoretical basis**: Organizational cognition — individuals develop stable habits of digital environment organization through repeated practice, reflecting their cognitive style.

**Key signals**: File system structure, naming conventions, metadata habits, configuration preferences, workflow patterns.

---

## 7. Signal Decomposition Model

The framework models observed behavioral data as a composite of four components:

```
y = y_cog + y_ctx + y_temp + y_noise
```

| Component | Symbol | Source | Properties |
|---|---|---|---|
| Cognitive signal | y_cog | Individual's stable cognitive patterns | Target of attribution; unique, persistent |
| Context effect | y_ctx | Environmental/technical context | Systematic, normalizable |
| Temporal effect | y_temp | Time-varying changes (learning, drift) | Slowly varying, trackable |
| Measurement noise | y_noise | Acquisition noise, sampling error | Zero-mean, bounded variance |

### Decomposition Goal

The decomposition aims to isolate the cognitive signal from the confounds, enabling more accurate attribution.

---

## 8. Likelihood Ratio Framework

Attribution strength is quantified using the Likelihood Ratio:

```
LR = P(E | H_p) / P(E | H_d)
```

Where:
- E = observed behavioral evidence
- H_p = same-source hypothesis (questioned and reference samples from same individual)
- H_d = different-source hypothesis (questioned and reference samples from different individuals)

### Interpretation Scale

The LR scale follows established forensic conventions. Values substantially greater than 1 support same-source; values substantially less than 1 support different-source. The verbal equivalent scale is based on Aitken & Taroni (2004) and Evett (1998).

### Multi-Modal LR Fusion

For M independent modalities, the combined LR is:

```
LR_combined = product(LR_m ^ w_m)
```

where w_m are modality weights normalized such that sum(w_m) = 1.

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

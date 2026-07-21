# AnubisX Framework: A Behavioral Digital Attribution Framework for Identity Analysis Using Artificial Intelligence

**Ahmed Awad (NullC0d3)**  
*Independent Cybersecurity Researcher*  
ORCID: https://orcid.org/0009-0005-0654-3393  
Website: https://anubisxframework.github.io  
Mirror: https://anubisxframework.nullc0d3.workers.dev  
Contact: anubisxframework@gmail.com  
GitHub: https://github.com/AnubisXFramework/AnubisXFramework  
Zenodo: https://doi.org/10.5281/zenodo.21446923  
Figshare: https://doi.org/10.6084/m9.figshare.33028817

**Version:** 2.0.0 — Journal Revision  
**Date:** July 2026  
*Classification: PUBLIC (C0)*  
**License:** CC BY 4.0

**Reference Work:**  
"You Can Hide Your Name... Not Your Mind: How Artificial Intelligence Reveals the Human Behind Digital Identities — Introducing the AnubisX Attribution Framework"  
Amazon: https://www.amazon.com/dp/B0H8LCTTWW

---

## Abstract

Digital attribution — linking digital actions and artifacts to their human source — is a foundational capability in cyber threat intelligence, digital forensics, and national security. Current methodologies rely primarily on technical artifacts (IP addresses, device fingerprints, network identifiers) that sophisticated adversaries can spoof or eliminate. Behavioral attribution offers an alternative paradigm: analyzing intrinsic patterns of human cognition observable through digital traces.

This paper presents the AnubisX Framework, a scientific methodology for behavioral digital identity attribution. The framework comprises: (1) a formal theoretical foundation of axioms, research hypotheses, and design principles organized around Cognitive Centroid theory; (2) a comprehensive mathematical framework with a likelihood ratio evidence model; (3) algorithms spanning multiple domains and behavioral modalities; and (4) a multi-tier validation infrastructure with defined experiments, benchmarks, and case studies.

A prototype implementation validates the stylometric modality on real-world data. Proof-of-concept experiments demonstrate multi-dimensional fingerprint extraction with dimensional consistency, efficient similarity search, and measurable cross-user similarity distributions. Of several core claims, a subset achieve publication-ready validation status.

All claims, limitations, and validation outcomes are transparently documented. The formal experiment catalog and benchmark suite are fully specified but unexecuted. The framework is released as open source under CC BY 4.0.

**Keywords:** Behavioral Attribution; Digital Identity; Artificial Intelligence; Stylometry; Behavioral Fingerprinting; Cyber Threat Intelligence; Digital Forensics; OSINT; Authorship Attribution; Cognitive Centroid

---

## 1. Introduction

Digital attribution — determining the human source of digital actions and communications — is a foundational requirement across multiple security and intelligence domains. Cyber threat intelligence (CTI) operations require attribution of attacks to specific threat actors [1][2]. Digital forensic investigations must link artifacts to suspects [3]. Counter-fraud analysis requires linking fraudulent accounts to their operators [4]. National security applications include disinformation campaign attribution and tracking of malicious influence operations [5].

Current attribution methodologies operate primarily at the technical level, analyzing artifacts such as IP addresses, device fingerprints, browser configurations, and network-level identifiers [6]. These approaches are effective against unsophisticated adversaries but exhibit fundamental limitations: IP addresses are trivially anonymized through VPNs, proxy chains, or Tor; device fingerprints can be randomized; browser fingerprints can be standardized. Sophisticated adversaries deploy counter-forensic measures that render purely technical attribution unreliable [7].

Behavioral attribution addresses these limitations by shifting the analytical focus from transient technical identifiers to persistent human behavioral patterns. The premise is that individuals exhibit unique, measurable, and persistent behavioral characteristics in their digital interactions — a digital behavioral fingerprint — arising from stable cognitive processes including language production, temporal rhythms, social interaction styles, and procedural learning. Unlike technical artifacts, behavioral patterns are intrinsic to the operator and cannot be eliminated without fundamentally altering the operator's interaction with digital systems [8][9].

The AnubisX Framework formalizes this premise into a complete scientific methodology. Its contributions are:

1. **A formal theoretical model** based on Cognitive Centroid theory, comprising logically necessary axioms, empirically testable hypotheses, and design principles [10][11][12].

2. **A comprehensive mathematical framework** with objects across multiple categories, including a likelihood ratio evidence evaluation model for forensic attribution [13].

3. **An algorithmic catalog** of algorithms across multiple domains, spanning five behavioral modalities: stylometric, chrono-profiling, terminal profiling, network analysis, and media forensics [14].

4. **A six-layer architecture** with a six-stage pipeline supporting identification, verification, and forensic comparison workflows [15].

5. **A multi-tier validation infrastructure** with formal experiments, benchmarks, baselines, and acceptance criteria across multiple tiers [16].

6. **A prototype implementation** demonstrating the stylometric modality on real-world data with reproducible experiments [17][18].

This paper presents the v2.0 Journal Revision, expanded from the v1.0 Foundational Release with additional related work, practical implications, and enhanced discussion of limitations. The release provides a complete theoretical and methodological infrastructure whose formal empirical validation is in progress. The framework is not presented as a validated system but as a research infrastructure for systematic investigation of behavioral digital attribution.

---

## 2. Problem Statement

We formally state the behavioral attribution problem as follows.

Let S = {s₁, s₂, ..., sₘ} be a set of unknown human sources. Let D = {d₁, d₂, ..., dₙ} be a set of digital artifacts produced by sources in S. Each artifact dᵢ is produced by exactly one source s(dᵢ) ∈ S. The problem is to determine, given D and possibly additional contextual information, the mapping from artifacts to sources.

Three operational variants are defined:

1. **Identification (1:N matching):** Given a query artifact dₓ with unknown source, rank the sources in S by the probability that s(dₓ) = sᵢ.

2. **Verification (1:1 matching):** Given artifacts dₐ and dₓ, determine the probability that s(dₐ) = s(dₓ).

3. **Forensic comparison (1:1 with evidence grading):** Given artifacts dₐ and dₓ, compute the likelihood ratio LR = P(evidence | same source) / P(evidence | different source).

The fundamental challenge is that the mapping from source to artifact is mediated through technical systems that introduce noise, transformation, and obfuscation. The behavioral signal must be disentangled from platform-specific effects, contextual variation, temporal drift, and counter-forensic manipulation [10][13].

The framework addresses three specific limitations of existing approaches: (1) technical attribution methods fail against anonymization; (2) existing behavioral methods are narrow in scope, typically addressing a single modality; (3) most prior work lacks formal, pre-specified validation criteria with calibration thresholds defined a priori rather than post hoc.

---

## 3. Related Work

### 3.1 Authorship Attribution and Stylometry

Authorship attribution is the most developed subfield of behavioral attribution. Computational stylometry, dating to Mosteller and Wallace's (1964) seminal Bayesian analysis of the Federalist Papers [19], uses quantitative text features — function word frequencies, vocabulary richness, sentence length distributions, syntactic patterns — to discriminate among authors. Stamatatos (2009) provided the definitive survey of modern authorship attribution methods, establishing the field's computational and methodological foundations [20]. Koppel, Schler, and Argamon (2009) systematically reviewed computational methods, identifying the "fundamental problem" of authorship attribution and the conditions under which different approaches succeed [21].

The PAN workshop series (CLEF) has provided standardized benchmarks for authorship attribution across multiple languages and genres since 2010. PAN 2023 introduced cross-discourse type authorship verification across written and spoken language, while PAN 2024 initiated generative AI authorship verification, formulating AI-generated text detection as an authorship problem [22][23][24]. The 2025 PAN edition focused on generative AI detection sensitivity and human-AI collaborative text classification [25].

Modern approaches employ transformer-based language models for stylometric feature extraction. Sentence-BERT (Reimers and Gurevych, 2019) demonstrated that siamese BERT networks produce semantically meaningful sentence embeddings that can be compared via cosine similarity, enabling large-scale semantic similarity search [26]. BERT-based authorship attribution has been applied to classical Arabic texts, achieving high accuracy with specialized models on Islamic legal texts [27]. The Arabic NLP community has produced dedicated shared tasks including AraGenEval (2025) for Arabic authorship style transfer and identification [28], and AbjadAuthorID (2026) for Arabic-script language authorship identification [29].

The concept of "writeprints" — unique stylistic markers analogous to fingerprints — has been explored in forensic linguistics [30] and digital forensics [31]. Abbasi and Chen (2008) introduced the writeprints framework for identity-level identification in cyberspace [32]. However, most stylometric research addresses single-modality, single-platform, and single-language scenarios. The AnubisX Framework extends stylometry by embedding it within a broader multi-modal framework with formal mathematical specification.

### 3.2 Digital Forensics and Cyber Threat Intelligence

Digital forensics traditionally focuses on technical artifacts: file system metadata, network logs, memory dumps, and device identifiers [3][33]. Cyber threat intelligence (CTI) extends this to adversary profiling and campaign attribution [34]. The IEEE Communications Surveys & Tutorials CTI survey (2023) comprehensively reviewed CTI mining from multiple data sources, proposing a taxonomy for cybersecurity entities, attack tactics, and threat hunting [35]. A 2025 survey of cyber threat attribution by Prasad et al. (Computers & Security) systematically analyzed technical, legal, geopolitical, social, and economic dimensions, proposing a novel taxonomy structured by attribution confidence, analytical domains, and adversarial motivation [1].

CTI attribution remains predominantly reliant on technical indicators of compromise (IOCs) and infrastructure analysis. Recent work has explored LLM-based attribution: Guru et al. (Stanford, 2025) evaluated models for threat actor TTP extraction and attribution using MITRE ATT&CK [36]. Irshad and Siddiqui (2023) developed an NLP-based mechanism using domain-specific embeddings for cyber threat attribution from unstructured CTI reports [37]. Behavioral attribution as a complementary signal for CTI analysis has been proposed but lacks formal methodological foundations [5].

### 3.3 Behavioral Biometrics

Behavioral biometrics encompasses keystroke dynamics, mouse movement analysis, gait recognition, and voice pattern analysis [38]. These modalities share the premise that behavioral patterns are personally identifying. Khan et al. (2024) published a comprehensive ACM Computing Surveys review of mouse dynamics and widget interactions spanning 1897–2023 [39]. Keystroke dynamics surveys cover concepts, techniques, and applications for user authentication and identification [40].

However, behavioral biometrics typically operate in controlled environments with enrolled users and dedicated sensors. The framework targets the more challenging scenario of attribution in uncontrolled, multi-platform digital environments with passive observation.

### 3.4 Open-Source Intelligence and Digital Identity Research

OSINT investigations routinely link digital identities across platforms, typically relying on explicit identifiers (usernames, email addresses, profile photos) rather than behavioral analysis [4]. Cross-platform identity resolution through metadata correlation and account linkage has been explored, but behavioral methods remain underrepresented in operational OSINT workflows. Forensic authorship profiling using geolocated social media data has demonstrated corpus-based methods for regional dialect identification [41].

### 3.5 Identity Intelligence (IdINT)

The framework proposes Identity Intelligence (IdINT) as a distinct analytical discipline analogous to SIGINT, HUMINT, and GEOINT — focused on systematic collection, analysis, and interpretation of behavioral identity evidence from digital traces [10]. To the best of our knowledge, this is the first formal theoretical and methodological foundation for this discipline, though related concepts have been discussed in the context of cyber attribution [1][5].

### 3.6 Comparative Analysis

Table 1 provides a qualitative comparison of the AnubisX Framework with existing approaches across key dimensions.

| Dimension | Stylometry | Behav. Biometrics | CTI Attribution | Digital Forensics | AnubisX |
|-----------|-----------|-------------------|-----------------|-------------------|---------|
| Multi-modal scope | No (text only) | Limited (1-2 modes) | No (IOC-based) | No (artifact-based) | Yes (5 modalities) |
| Formal theory | Partial | Partial | Minimal | Minimal | Formal axioms and hypotheses |
| Math. framework | Limited | Limited | No | No | Comprehensive |
| Pre-spec. criteria | Rare | Rare | Rare | Rare | Multiple criteria, multiple tiers |
| Validated prototype | Many systems | Many systems | Few | Many tools | Stylometric modality |
| Open science | Partial | Partial | Minimal | Minimal | Full CC BY 4.0 |

**Table 1. Comparative analysis of the AnubisX Framework against existing approaches.**

---

## 4. Research Gap

Analysis of existing literature reveals three significant gaps:

**Gap 1: Fragmentation.** Behavioral attribution methods are developed independently across stylometry [20][21], biometrics [39], digital forensics [3], and OSINT, without a unifying theoretical or mathematical foundation. Cross-modal integration is ad hoc.

**Gap 2: Methodological rigor.** Most work lacks formal, pre-specified validation criteria. Thresholds are selected post hoc, limiting reproducibility and making independent verification difficult [20].

**Gap 3: Transparency.** Comprehensive documentation of limitations and failure modes is uncommon in behavioral attribution research, impeding operational adoption and scientific progress.

The AnubisX Framework addresses these gaps through its integrative design, formal validation infrastructure, and commitment to transparent documentation.

---

## 5. Contributions

**Contribution 1: Cognitive Centroid Theory.** A formal theoretical model positing that each individual possesses an invariant core behavioral signature — the Cognitive Centroid — with formally defined properties of uniqueness, stability, measurability, and invariance [10][11].

**Contribution 2: Axiomatic Logical Foundation.** A set of logically necessary axioms governing behavioral attribution, organized into groups (Core, Behavior, Identity, Attribution, Evidence, Reasoning) [11].

**Contribution 3: Comprehensive Mathematical Framework.** A mathematical structure with multiple categories across layers, including formal definitions for mathematical spaces, distance functions, and similarity functions [13].

**Contribution 4: Algorithm Catalog.** Algorithms spanning multiple domains with varying status levels [14].

**Contribution 5: Six-Layer Architecture.** A layered architecture with a six-stage pipeline supporting three workflows [15].

**Contribution 6: Multi-Tier Validation Infrastructure.** Defined experiments, benchmarks, baselines, and acceptance criteria [16].

**Contribution 7: Prototype Validation (Stylometric Modality).** Proof-of-concept experiments on real-world data [17][18].

---

## 6. Theoretical Foundation

### 6.1 Axiomatic System

The framework is grounded in formal axioms organized into six groups [11].

| Group | Scope |
|-------|-------|
| Core | Uncertainty conservation, measurement prerequisite, evidential boundedness, attribution reflexivity |
| Behavior | Signal composition, signal non-identity, comparison relativity |
| Identity | Identity consistency, identity non-repudiation |
| Attribution | Conclusion grounding, uncertainty honesty |
| Evidence | Evidence non-contradiction, evidence completeness, fusion monotonicity |
| Reasoning | Logical consistency, inference validity |

**Table 2. Axiom groups and scope.**

### 6.2 Cognitive Centroid Theory

The central theoretical construct is the Cognitive Centroid, defined as the asymptotic mean of an individual's behavioral feature vectors as the number of observations approaches infinity [10]:

C = lim_{n→∞} (1/n) Σ_{k=1}^{n} B(t_k)

where B(t_k) is the behavioral feature vector at observation time t_k. The Cognitive Centroid possesses four formal properties: Uniqueness, Stability, Measurability, and Invariance.

This formalizes the principle that additional behavioral data yields more reliable attribution estimates. Formal proof of the convergence rate and conditions remains an open theoretical question [10].

### 6.3 Research Hypotheses

The framework defines research hypotheses at PROPOSED status [12]. Key hypotheses include HYP-CORE-001 (Identity Invariance), HYP-CORE-002 (Behavioral Traceability), HYP-CORE-003 (Cognitive Uniqueness), and HYP-CORE-004 (Involuntary Emission).

### 6.4 Design Principles

Design principles at ADOPTED status guide implementation across multiple categories [12]. Key principles include DP-ATR-001 (Multi-Modal Necessity), DP-ATR-002 (Probabilistic Output), and DP-EVI-001 (Evidential Independence).

---

## 7. Mathematical Framework

The framework comprises mathematical objects across categories governed by foundational principles [13].

| Layer | Categories |
|-------|-----------|
| 1 — Foundation Types | Data types, sets, constants |
| 2 — Structured Types | Vectors, matrices, tensors |
| 3 — Transformations | Functions, normalizations, aggregations |
| 4 — Comparison & Evaluation | Metrics, distances, similarities |
| 5 — Uncertainty & Decision | Probabilities, confidences, scores |
| 6 — Constraint & Optimization | Constraints, objectives |

**Table 3. Mathematical framework layers.**

### 7.1 Behavioral Signal Model

y(t, c, p) = y_cog(t) + y_ctx(c) + y_plat(p) + ε(t, c, p)

The cognitive component y_cog(t) is the signal of interest; y_ctx(c) captures contextual variation; y_plat(p) represents platform-specific bias; ε is irreducible noise. This decomposition has not been empirically validated.

### 7.2 Likelihood Ratio Evidence Framework

LR = P(E | H_same) / P(E | H_diff)

| LR Range | Verbal Interpretation |
|----------|----------------------|
| > 100 | Very strong support for same-source |
| 10 – 100 | Strong support for same-source |
| 3 – 10 | Moderate support for same-source |
| 1 – 3 | Limited support for same-source |
| 1 | No support |
| 0.33 – 1 | Limited support for different-source |
| 0.1 – 0.33 | Moderate support for different-source |
| 0.01 – 0.1 | Strong support for different-source |
| < 0.01 | Very strong support for different-source |

**Table 4. Likelihood ratio verbal interpretation scale.**

### 7.3 Mathematical Spaces and Distance Functions

Formal spaces are defined including Observation Space, Behavioral Space, Evidence Space, Reasoning Space, Decision Space, Attribution Space, Confidence Space, Score Space, Outcome Space, and Feature Space. Multiple distance and similarity functions are specified [13][14].

---

## 8. System Architecture

### 8.1 Six-Layer Architecture

| Layer | Responsibility | Key Functions |
|-------|---------------|--------------|
| 1 — Data Layer | Raw data ingestion, validation | Platform adapters, metadata extraction, chain-of-custody |
| 2 — Feature Layer | Modality-specific extraction | NLP processing, temporal analysis, graph construction |
| 3 — Profile Layer | Profile construction, storage | Fingerprint generation, versioning |
| 4 — Comparison Layer | Similarity computation | Distance metrics, indexing, score normalization |
| 5 — Evidence Layer | Score calibration, fusion | LR computation, fusion, confidence estimation |
| 6 — Decision Layer | Identity decision, reporting | Threshold comparison, inconclusive handling |

**Table 5. Six-layer architecture.**

### 8.2 Pipeline and Workflows

The six-stage pipeline: Ingestion → Feature Extraction → Profile Construction → Comparison → Evidence Evaluation → Decision. Three workflows: Identification (1:N), Verification (1:1), Forensic Comparison (1:1 with evidence grading).

### 8.3 Behavioral Modalities

| Modality | Behavioral Signal | Validation Status |
|----------|------------------|-------------------|
| Stylometric | Vocabulary, syntax, discourse | Validated (prototype) |
| Chrono-Profiling | Circadian rhythms, timing | Requires data |
| Terminal Profiling | Commands, navigation | Requires data |
| Network Analysis | Graph structure, communities | Requires data |
| Media Forensics | File structure, naming | Requires data |

**Table 6. Five behavioral modalities with validation status.**

---

## 9. Prototype Implementation

### 9.1 Prototype Overview

A prototype implementation validates the stylometric modality using transformer-based feature extraction and efficient similarity search [17].

### 9.2 Architecture

- **Core:** Multi-dimensional feature extraction using transformer-based embeddings
- **Search:** Efficient similarity search using approximate nearest neighbor indexing [42]
- **Verification:** Linguistic content verification
- **Database:** Fingerprint storage
- **Utilities:** Text preprocessing

### 9.3 Dataset

Real-world social media accounts were used for prototype validation, including diverse categories of users [17].

### 9.4 Fingerprint Construction

Multi-dimensional feature vectors combining projected embeddings, lexical features, and character-level features. Reproducibility caveats exist due to non-determinism in certain language features [17].

### 9.5 Similarity Search

Efficient similarity search using indexing structures optimized for dense vector comparison [42][43].

### 9.6 Confidence Scoring

Heuristic confidence scoring based on observation count and variance. Not calibrated against ground truth.

---

## 10. Experimental Methodology

### 10.1 Prototype Experiment Design

Proof-of-concept experiments in categories including fingerprint extraction, similarity search, cross-user analysis, and demographic analysis [18].

### 10.2 Formal Experiment Catalog

Formal experiments across multiple domains: social media platforms, cross-platform scenarios, benchmarks, stress tests, and ablation studies. All at DEFINED status [16].

### 10.3 Evaluation Framework

Binary pass/fail criteria defined a priori. Results from automated experiment output [18].

---

## 11. Experimental Results

All values from raw experiment output [18].

### 11.1 Fingerprint Dimensional Consistency

Multi-dimensional fingerprint extraction was consistent across all accounts.

### 11.2 Cross-User Similarity

Cross-user cosine similarity distribution was computed across identity pairs.

### 11.3 Search Performance

Index type, vector count and dimensionality, and latency metrics were recorded.

**Note:** High mean cross-user similarity likely reflects embedding dominance. Without same-user baselines, discriminative power cannot be fully assessed.

### 11.4 Lexical Feature Analysis

Lexical features including type-token ratio, average word length, punctuation ratio, and emoji ratio were profiled across users.

### 11.5 Temporal Feature Analysis

Temporal features including burstiness and hour entropy were computed.

### 11.6 Topic Analysis

Unique keywords and occurrences were identified across users.

### 11.7 Content Verification

Keyword matching, slang expression detection, and location mention identification were performed.

### 11.8 Claims Validation Summary

| Claim | Status |
|-------|--------|
| Multi-dimensional fingerprint vectors | PUBLICATION READY |
| Cross-user similarity distribution | PUBLICATION READY |
| Efficient similarity search | PUBLICATION READY |
| Lexical feature discriminability | PUBLICATION READY |
| Content verification | PUBLICATION READY |
| Cross-platform adapter pattern | PUBLICATION READY |
| Multi-model ensemble embedding | DEGRADED |
| Temporal posting patterns | REQUIRES DATA |
| Coordination detection | REQUIRES DATA |
| Fingerprint stability | REQUIRES DATA |

**Table 7. Claims validation status.**

---

## 12. Discussion

### 12.1 Interpretation of Findings

Prototype validation confirms feasibility of stylometric fingerprinting. Key finding: embedding dominance produces high cross-user similarity, warranting investigation of feature weighting or topic-normalized measures.

### 12.2 Relationship to Formal Framework

Prototype results are feasibility evidence, not formal validation (formal validation requires ground truth labels).

### 12.3 Comparison to Existing Work

Distinguished by integrative scope; direct quantitative comparison not possible without standardized benchmark evaluation.

### 12.4 Cybersecurity and Forensic Implications

CTI operations: complementary signal when technical indicators are absent/unreliable. Digital forensics: formal LR framework provides scientifically defensible basis for behavioral evidence. The combined technical-behavioral approach is more robust against counter-forensic measures [1][5].

### 12.5 OSINT and Intelligence Applications

Systematic methodology for identity resolution across platforms. Cross-platform behavioral fingerprinting would significantly enhance investigative capabilities beyond explicit-identifier-based methods [4].

### 12.6 Threats to Validity

Construct: embedding dominance conflates topic with identity. Internal: no ground truth, non-deterministic features. External: limited geographic and platform scope. Statistical: small sample. Ecological: pre-collected data vs real-time scenarios. Temporal: single time window, drift unexamined.

---

## 13. Practical Implications

### 13.1 For Cybersecurity Operations

SOC integration as complementary signal to IOC detection for anonymous actor linking, account takeover detection, and coordinated inauthentic behavior identification.

### 13.2 For Digital Forensics

LR framework provides standardized evidence grading scale. Requires validated reference databases and calibration protocols.

### 13.3 For Intelligence Analysis

IdINT framework for multi-modal fusion across disparate data sources.

### 13.4 For Open-Source Research

Open-source release with transparent limitation documentation invites community contributions.

---

## 14. Limitations

### 14.1 Prototype Limitations

| ID | Limitation | Severity | Mitigation Pathway |
|----|-----------|----------|-------------------|
| LIM-001 | Model ensemble auth failure | Critical | Resolve authentication |
| LIM-002 | No ground truth labels | Critical | Acquire labeled dataset |
| LIM-003 | Non-deterministic feature extraction | Critical | Replace with deterministic method |
| LIM-004 | No interaction metadata | Major | Extend collection scope |
| LIM-005 | Small dataset | Major | Expand sample size |
| LIM-006 | Single-pass extraction | Major | Multi-pass temporal windows |
| LIM-007 | Single-platform implementation | Major | Multi-platform adapters |
| LIM-008 | No train/test separation | Major | Stratified cross-validation |
| LIM-009 | CPU-only execution | Minor | GPU acceleration |
| LIM-010 | Zero test coverage | Critical | Add test suite |

**Table 8. Prototype limitations with mitigation pathways.**

### 14.2 Framework Limitations

Formal experiments unexecuted. Some algorithms at TBD status. Hypotheses at PROPOSED. LR framework requires calibration data. Cognitive Centroid convergence theorem lacks formal proof.

### 14.3 Generalizability Constraints

Dataset: geographically, linguistically, and platform homogeneous. Multiple modalities untested.

---

## 15. Future Work

### 15.1 Immediate Priorities

Resolve authentication issues. Acquire labeled dataset. Fix non-deterministic features.

### 15.2 Medium-Term Objectives

Multi-pass extraction. Cross-platform expansion. Execute remaining experiments. Address theory-implementation gap.

### 15.3 Long-Term Research Directions

All algorithm implementations. Multi-lingual expansion. All benchmarks. All formal experiments. Full validation. Advanced feature extraction investigation.

---

## 16. Summary of Contributions

**Theoretical:** Behavioral attribution formalization with variants. Cognitive Centroid theory. Axiomatic system. Research hypotheses. IdINT concept.

**Methodological:** Comprehensive mathematical framework. LR evidence framework. Algorithm catalog across multiple domains and modalities. Layered architecture. Multi-tier validation with pre-specified criteria.

**Empirical:** Working prototype for stylometric fingerprinting. Reproducible experiments. Publication-ready claims. Full transparency on limitations.

---

## 17. Reproducibility

Source code available at https://github.com/AnubisXFramework/AnubisXFramework. Data files included. Requirements documented. Note: non-deterministic features affect full reproducibility. Framework documentation available in same repository.

---

## 18. Conclusion

The AnubisX Framework v2.0 presents a scientific methodology for behavioral digital identity attribution integrating formal theory, mathematics, algorithms, architecture, and validation.

Prototype results demonstrate feasibility of multi-dimensional fingerprinting, efficient similarity search, and measurable cross-user similarity. A subset of claims are publication-ready.

Limitations transparently documented: unexecuted experiment catalog, single-modality prototype, pending algorithms, theory-implementation gap. The framework is a foundation for systematic research, not a validated operational system.

Open source under CC BY 4.0. Independent validation and collaborative development invited.

---

## Acknowledgements

The author acknowledges the users whose publicly available data was used. Libraries: efficient similarity search [42], transformer models [46], sentence embeddings [26], numerical computing, machine learning, data management, and visualization tools. Reference work: "You Can Hide Your Name... Not Your Mind."

---

## Data Availability

Data files available at https://github.com/AnubisXFramework/AnubisXFramework. Publicly available data only.

---

## Code Availability

Source code available at https://github.com/AnubisXFramework/AnubisXFramework. MIT license.

---

## Ethics Statement

Public data only, in compliance with terms of service. Dual-use potential acknowledged; responsible use within legal/ethical frameworks advocated. Open-source for public scrutiny.

---

## Conflict of Interest

None. Independent research without external funding.

---

## References

[1] Prasad, N., Diro, A., Warren, M., & Fernando, M. (2025). A survey of cyber threat attribution: Challenges, techniques, and future directions. Computers & Security, 157, 104606.

[2] Nespoli, P., et al. (2023). Cyber threat intelligence mining for proactive cybersecurity defense. IEEE Communications Surveys & Tutorials, 25(4), 2270–2309.

[3] Casey, E. (2011). Digital Evidence and Computer Crime (3rd ed.). Academic Press.

[4] Edwards, M., et al. (2021). Panning for gold: Automatically analyzing online social engineering attack surfaces. Computers & Security, 100, 102089.

[5] Zeadally, S., et al. (2020). Harnessing artificial intelligence for cybersecurity. Computer, 53(4), 28–37.

[6] Eckersley, P. (2010). How unique is your web browser? In Privacy Enhancing Technologies (pp. 1–18). Springer.

[7] Al-Rubaie, M., & Chang, J. M. (2019). Privacy-preserving machine learning: Threats and solutions. IEEE Security & Privacy, 17(2), 38–49.

[8] Yampolskiy, R. V., & Govindaraju, V. (2008). Behavioural biometrics: A survey and classification. International Journal of Biometrics, 1(1), 81–113.

[9] Pennebaker, J. W. (2011). The Secret Life of Pronouns. Bloomsbury.

[10] Awad, A. (2026). AnubisX Framework — Theoretical Foundation. Repository: Theory/.

[11] Awad, A. (2026). AnubisX Framework — Axiomatic System. Repository: Axioms/.

[12] Awad, A. (2026). AnubisX Framework — Hypotheses and Design Principles. Repository: Hypotheses/, Design_Principles/.

[13] Awad, A. (2026). AnubisX Framework — Mathematical Framework. Repository: Mathematics/.

[14] Awad, A. (2026). AnubisX Framework — Algorithm Catalog. Repository: Algorithms/.

[15] Awad, A. (2026). AnubisX Framework — Architecture. Repository: Framework/.

[16] Awad, A. (2026). AnubisX Framework — Validation Infrastructure. Repository: Validation/.

[17] Awad, A. (2026). AnubisX Framework — Prototype. Repository: Anubis Twitter/.

[18] Awad, A. (2026). AnubisX Framework — Experimental Results. Repository: Anubis Twitter/reports/experimental_results/.

[19] Mosteller, F., & Wallace, D. L. (1964). Inference and Disputed Authorship: The Federalist. Addison-Wesley.

[20] Stamatatos, E. (2009). A survey of modern authorship attribution methods. JASIST, 60(3), 538–556.

[21] Koppel, M., Schler, J., & Argamon, S. (2009). Computational methods in authorship attribution. JASIST, 60(1), 9–26.

[22] Stamatatos, E., et al. (2023). Overview of the Authorship Verification Task at PAN 2023. CEUR-WS.org.

[23] Bevendorff, J., et al. (2023). Overview of PAN 2023. LNCS 14163. Springer.

[24] Bevendorff, J., et al. (2024). Overview of the "Voight-Kampff" Task at PAN 2024. CEUR-WS.org.

[25] Bevendorff, J., et al. (2025). The two paradigms of LLM detection. In Findings of ACL 2025.

[26] Reimers, N., & Gurevych, I. (2019). Sentence-BERT. In EMNLP-IJCNLP 2019.

[27] Alali, M., & Mohd, M. (2023). A transformer-based approach to AA in classical Arabic texts. Applied Sciences, 13(12), 7255.

[28] Abudalfa, S., et al. (2025). The AraGenEval shared task. In ArabicNLP 2025.

[29] Alsuhaibani, S., & Alkaoud, M. (2026). Uslub at AbjadAuthorID. In AbjadNLP 2026.

[30] Coulthard, M., Johnson, A., & Wright, D. (2017). An Introduction to Forensic Linguistics (2nd ed.). Routledge.

[31] Chaski, C. E. (2005). Who's at the keyboard? Int. J. Digital Evidence, 4(1).

[32] Abbasi, A., & Chen, H. (2008). Writeprints. ACM TOIS, 26(2), 1–29.

[33] Carrier, B. (2005). File System Forensic Analysis. Addison-Wesley.

[34] Tounsi, W., & Rais, H. (2018). A survey on technical threat intelligence. Computers & Security, 72, 212–233.

[35] Solar, S., et al. (2023). CTI mining survey. IEEE COMST, 25(4), 2270–2309.

[36] Guru, K., Moss, R. J., & Kochenderfer, M. J. (2025). On technique identification and threat-actor attribution using LLMs. arXiv:2505.11547.

[37] Irshad, E., & Siddiqui, A. B. (2023). Cyber threat attribution using unstructured reports. Egyptian Informatics Journal, 24(1), 43–59.

[38] Yampolskiy, R. V. (2008). Behavioral biometrics survey. Int. J. Biometrics, 1(1), 81–113.

[39] Khan, S., et al. (2024). Mouse dynamics behavioral biometrics: A survey. ACM Computing Surveys, 56(6), 1–33.

[40] Shadman, R., et al. (2023). Keystroke dynamics. arXiv:2303.04605.

[41] Roemling, D. (2025). Forensic authorship profiling using geolocated social media data. Applied Corpus Linguistics, 5(3), 100146.

[42] Johnson, J., Douze, M., & Jégou, H. (2019). Billion-scale similarity search with GPUs. IEEE TBD, 7(3), 535–547.

[43] Douze, M., et al. (2024). The Faiss library. arXiv:2401.08281.

[44] Luyckx, K., & Daelemans, W. (2008). Authorship attribution and verification with many authors and limited data. In COLING 2008.

[45] Aitken, C. G. G., & Taroni, F. (2004). Statistics and the Evaluation of Evidence (2nd ed.). Wiley.

[46] Wolf, T., et al. (2020). HuggingFace's Transformers. In EMNLP 2020.

[47] Kestemont, M. (2014). Function words in authorship attribution: From black magic to theory? In Workshop on Stylistic Variation. ACL.

[48] Argamon, S., Koppel, M., Pennebaker, J. W., & Schler, J. (2009). Automatically profiling the author of an anonymous text. CACM, 52(2), 119–123.

[49] Koppel, M., Schler, J., & Argamon, S. (2011). Authorship attribution in the wild. Language Resources and Evaluation, 45(1), 83–94.

[50] He, X., et al. (2024). Authorship attribution methods, challenges, and future research directions: A comprehensive survey. Information, 15(3), 131.

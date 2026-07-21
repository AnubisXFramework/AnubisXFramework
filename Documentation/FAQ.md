# Frequently Asked Questions

**AnubisX Framework**

---

## Official DOI

**DOI**: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)
**Figshare**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

This release is permanently archived on Zenodo and Figshare.

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)
**Contact**: anubisxframework@gmail.com
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

---

## General Questions

### What is the AnubisX Framework?

A scientific methodology for digital identity attribution based on invariant human cognitive signatures. It provides a formal theoretical foundation, mathematical framework, algorithms, validation methodology, and prototype implementation for behavioral identity attribution.

### How is it different from traditional attribution?

Traditional attribution tracks what adversaries use (IPs, devices, accounts). AnubisX tracks who adversaries are — involuntary cognitive patterns (language habits, timing patterns, interaction styles) that they cannot easily change. Technical artifacts can be spoofed; cognitive patterns cannot.

### What are the five modalities?

1. **Forensic Stylometry**: Linguistic patterns (function-word frequencies, syntax preferences)
2. **Chrono-Profiling**: Temporal behavior patterns (circadian rhythms, inter-event timing)
3. **Terminal Execution Profiling**: Human-machine interaction patterns (command sequences, timing)
4. **Relational Network Analysis**: Social graph patterns (network topology, communication)
5. **Environmental Media Forensics**: Digital organization patterns (file structures, naming conventions)

### Is it implemented?

The framework has a validated prototype implementing the stylometric modality for the Twitter/X platform, demonstrating the feasibility of the theoretical framework through empirical testing.

### What is Identity Intelligence (IdINT)?

A proposed formal forensic discipline for behavioral identity attribution, alongside DNA analysis, fingerprinting, and ballistics. IdINT argues that cognitive traces are equally individual-specific as physical traces and should be recognized as a distinct class of forensic evidence.

### Is it peer reviewed?

The framework follows a formal publication pipeline. Current validation is internal but follows rigorous scientific standards with a defined acceptance criteria framework.

### How is confidence quantified?

Attribution strength is expressed as a Likelihood Ratio — the probability of the observed evidence under the same-source hypothesis divided by the probability under the different-source hypothesis. Values range from very strong support for different-source to very strong support for same-source.

### What about privacy?

The Proportionality and Privacy Protection Protocol (P3) is embedded in the core architecture, ensuring ethical constraints on attribution methods. Evidence collection must be proportional to investigative need.

### Who should use this?

Forensic investigators, cybersecurity analysts, academic researchers, legal professionals, and policy makers interested in behavioral identity attribution.

---

## Framework Questions

### How is the framework structured?

Multiple layers: Data acquisition, feature extraction, profile construction, comparison, evidence evaluation, and decision. Multiple processing stages with multiple behavioral modalities.

### What are the three primary workflows?

1. **Identification**: Who is this? (one-to-many matching)
2. **Verification**: Is this who they claim to be? (one-to-one matching)
3. **Forensic Comparison**: Source attribution of questioned material (LR quantification)

### How does multi-modal fusion work?

Multiple fusion strategies exist, operating at the score, feature, and decision levels. Each modality produces evidence that is calibrated, weighted, and combined using evidence theory.

### What validation does the framework have?

A multi-tier hierarchy with acceptance criteria, accuracy metrics, performance metrics, benchmarks, and baselines. Multiple experiments have been executed on the prototype.

---

## Prototype Questions

### What does the prototype do?

The prototype implements stylometric fingerprinting for Twitter/X accounts. It can extract behavioral fingerprints from tweet text, search for similar accounts, verify demographic affiliation, and visualize data.

### What are the prototype limitations?

- Selected embedding models may be unavailable due to third-party authentication issues
- Temporal features require valid timestamp data not yet available
- Interaction data collection remains pending
- Only stylometric modality is currently implemented
- Cross-platform pipelines are not yet operational

---

## Validation Questions

### What experiments have been executed?

Multiple experiments covering stylometric fingerprint extraction, embedding validation, lexical feature extraction, topic vector extraction, similarity search, cross-user similarity analysis, demographic filtering, and publication readiness assessment.

### What metrics are available?

Accuracy metrics are partially computable from current data. Formal accuracy metrics (FAR, FRR, AUC) require ground-truth verification data not yet available.

### Is the framework scientifically validated?

Partially. The theoretical framework is fully specified and internally consistent. The prototype demonstrates functional capability. Formal validation against acceptance criteria requires additional data collection and ground-truth verification.

---

## Reproducibility and Data Questions

### Can I reproduce the results?

The prototype code and documentation are available. Reproduction requires appropriate data collection and third-party model access.

### What dataset is used?

A sample of Twitter accounts was analyzed. The dataset has limitations including lack of ground-truth identity labels, limited temporal and interaction data, and a single-platform focus.

### What are the main research gaps?

1. **Empirical validation**: Acceptance criteria untested against real data
2. **Cross-platform validation**: Cross-platform pipelines not operational
3. **Multi-modal validation**: Only stylometry implemented
4. **Accuracy measurement**: No formal FAR/FRR/AUC estimates
5. **Dataset limitations**: Small, single-demographic, single-platform

---

## Contributing and Citing

### How can I contribute?

Contributions in the following areas are especially welcome: cross-platform implementation, temporal feature extraction, interaction data collection, formal validation studies, and additional demographic testing.

### How do I cite AnubisX?

Citation format will be established with the first publication release. For now, reference the framework by name and version, with a link to the repository.

### What is the license?

CC BY 4.0 (Creative Commons Attribution 4.0 International).

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

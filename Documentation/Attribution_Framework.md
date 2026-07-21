# Attribution Framework

**AnubisX Framework — LR-Based Attribution and Evidence Integration**

---

## Official DOI

**DOI**: [10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)
**Figshare**: [10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

This release is permanently archived on Zenodo and Figshare.

**Website**: [https://anubisxframework.github.io](https://anubisxframework.github.io)
**Contact**: anubisxframework@gmail.com
**Mirror**: [https://anubisxframework.nullc0d3.workers.dev](https://anubisxframework.nullc0d3.workers.dev)

---

## 1. Likelihood Ratio Framework

Attribution strength is quantified using the Likelihood Ratio:

```
LR = P(E | Hₚ) / P(E | H_d)
```

Where:
- E = observed behavioral evidence
- Hₚ = same-source hypothesis (the questioned and reference samples originate from the same individual)
- H_d = different-source hypothesis (the questioned and reference samples originate from different individuals)

### Interpretation

The LR framework provides a continuous scale of evidential strength. Values significantly greater than 1 support the same-source hypothesis; values significantly less than 1 support the different-source hypothesis. The exact verbal scale follows established forensic science conventions (Aitken & Taroni, 2004; Evett, 1998).

## 2. Evidence Weighting

Each piece of evidence is weighted along qualitative dimensions before fusion:

- **Quality**: Intrinsic reliability of the evidence source
- **Relevance**: Contextual applicability to the attribution question
- **Recency**: Temporal degradation of evidence value

## 3. Multi-Modal Fusion

Fused LR combines weighted LRs from all modalities, producing a combined LR that accounts for inter-modality dependencies and conflicts. The fusion methodology is grounded in Dempster-Shafer Theory.

## 4. Attribution Standards

- **Inconclusive outcomes**: Where the LR is close to unity or data is insufficient, the conclusion is marked inconclusive
- **Sensitivity analysis**: Conclusions are tested against reasonable variations in prior assumptions
- **Uncertainty bounds**: LR estimates include confidence intervals

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

# Security Policy

**AnubisX Framework — Responsible Disclosure and Security Guidelines**

---

## Supported Versions

The AnubisX Framework v1.0.0 includes both a complete theoretical specification and a validated prototype implementation. The prototype code is included in this repository. Security policies apply to both the specification and the prototype implementation.

| Version | Supported |
|---|---|
| 1.0.0 (specification + prototype) | Security review ongoing |
| < 1.0.0 | Not supported |

## Reporting a Vulnerability

### For Specification Issues

If you identify a security-relevant issue in the framework specification — such as a methodological weakness that could enable false attribution, a gap in error analysis, or a vulnerability in the evidence evaluation pipeline — please report it by:

1. **Opening a security issue** on GitHub with the `[SECURITY]` prefix in the title
2. **Contacting the maintainers** directly through the project's security contact
3. **Providing sufficient detail** to reproduce or understand the issue

### For Implementation Issues

Prototype code is now included in this repository. For implementation-specific vulnerabilities:

1. Do **not** publicly disclose the vulnerability
2. Report it to the project security team
3. Provide sufficient detail for reproduction and verification
4. Allow reasonable time for remediation before public disclosure

## Responsible Disclosure Guidelines

1. Report vulnerabilities promptly to the project maintainers
2. Do not publicly disclose until the issue has been addressed
3. Provide a clear description, potential impact, and any suggested remediation
4. Allow reasonable time for assessment and remediation based on severity
5. Act in good faith to avoid privacy violations, data destruction, or service disruption

## Scope

### In Scope

- Algorithm specifications that could produce systematic errors in attribution
- Error analysis gaps that could lead to incorrect conclusions
- Data handling procedures that could compromise privacy or security
- Implementation code
- Validation framework completeness

### Out of Scope

- Theoretical limitations already documented in the framework
- Design trade-offs explicitly acknowledged in specifications
- Known operating-environment dependencies documented in the framework

## Security Considerations

### Theoretical Limitations

The framework documents its own limitations in detail, including error decomposition and false positive/negative analysis.

### Data Privacy

The framework embeds privacy protections through the P³ Protocol (Proportionality and Privacy Protection), which defines:

- Data collection following the minimum necessary principle
- Attribution methods proportional to investigative need
- Access controls and audit trails for accountability

### Adversarial Considerations

The framework provides the theoretical basis for counter-forensic resistance and addresses the cost of deliberate behavioral modification.

## Prototype Security

### Data Handling

- All prototype validation was conducted on **public data**
- Only publicly available data was collected
- No private account data or non-public information was accessed
- Data was processed in compliance with applicable terms and regulations

### Prototype Code Security

- The prototype implements **feature extraction only** — no privileged operations
- Similarity search operates on **isolated feature vectors**
- No credentials, API keys, or secrets are hard-coded in the prototype code
- The prototype does not perform data exfiltration

### Known Limitations

- The prototype has not undergone formal security audit or penetration testing
- Single-modality implementation limits the attack surface but also limits attribution robustness
- Production deployments require additional security hardening including encryption-at-rest, access controls, and audit logging

## Ethical Use

The AnubisX Framework is intended for legitimate forensic, security, and research purposes conducted under appropriate legal oversight. The project's ethical principles explicitly prohibit:

- Mass surveillance without legal authorization and proportionality
- Privacy violations beyond the minimum necessary for legitimate investigation
- Use for harassment, intimidation, or discrimination
- Deployment without transparency and accountability mechanisms

## Contact

Security reports should be directed to the project maintainers at **anubisxframework@gmail.com** or through GitHub security advisories.

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
**Repository**: [https://github.com/AnubisXFramework/AnubisXFramework](https://github.com/AnubisXFramework/AnubisXFramework)

**DOI**: [https://doi.org/10.5281/zenodo.21446923](https://doi.org/10.5281/zenodo.21446923)  
**Figshare DOI**: [https://doi.org/10.6084/m9.figshare.33028817](https://doi.org/10.6084/m9.figshare.33028817)

**Copyright** © 2026 Ahmed Awad (NullC0d3). All rights reserved.  
Original documentation, framework design, algorithms, source code, diagrams, and repository structure are the intellectual work of Ahmed Awad (NullC0d3), unless otherwise indicated. Third-party software, libraries, datasets, and referenced works remain the property of their respective owners and are governed by their own licenses.

---

*Classification: PUBLIC (C0)*

# Fusion API

**AnubisX Framework — Multi-Modal Evidence Fusion Endpoints**

---

## Official DOI

DOI:
10.5281/zenodo.21374132

Persistent URL:
https://doi.org/10.5281/zenodo.21374132

This release is permanently archived on Zenodo under DOI: https://doi.org/10.5281/zenodo.21374132

---

## `POST /fusion/score`

Fuses modality-level similarity scores using score-level fusion.

## `POST /fusion/decision`

Fuses independent modality decisions using decision-level fusion.

## `POST /fusion/feature`

Fuses modality feature vectors using HOSVD-based feature-level fusion.

## Common Response Format

```json
{
  "status": "success",
  "data": {
    "combined_lr": 150.0,
    "method": "dempster_shafer",
    "modalities_fused": 5,
    "conflict_coefficient": 0.05,
    "fusion_gain": 2.5
  }
}
```

---

*Classification: PUBLIC (C0)*

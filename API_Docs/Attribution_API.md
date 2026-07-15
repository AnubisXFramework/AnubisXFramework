# Attribution API

**AnubisX Framework — LR Computation and Decision Endpoints**

---

## Official DOI

DOI:
10.5281/zenodo.21374132

Persistent URL:
https://doi.org/10.5281/zenodo.21374132

This release is permanently archived on Zenodo under DOI: https://doi.org/10.5281/zenodo.21374132

---

## `POST /attribution/lr`

Computes the Likelihood Ratio for a questioned sample against a reference profile.

### Request Body

```json
{
  "reference_profile_id": "profile-xxx",
  "questioned_sample": { ... },
  "modalities": ["stylometry", "chrono", "terminal", "network", "media"],
  "options": {
    "calibration": "pav" | "logistic",
    "prior": { "same_source": 0.5 }
  }
}
```

### Response

```json
{
  "status": "success",
  "data": {
    "lr": 150.0,
    "log_lr": 2.176,
    "modality_contributions": {
      "stylometry": { "lr": 45.0, "weight": 0.3 },
      "chrono": { "lr": 12.0, "weight": 0.2 },
      "terminal": { "lr": 8.0, "weight": 0.2 },
      "network": { "lr": 3.0, "weight": 0.15 },
      "media": { "lr": 2.0, "weight": 0.15 }
    },
    "ece": 0.12,
    "confidence_interval": [120.0, 187.5]
  }
}
```

## `POST /attribution/decision`

Produces a binary or categorical decision based on the LR.

### Request Body

```json
{
  "lr": 150.0,
  "threshold_same_source": 100.0,
  "threshold_different_source": 0.01
}
```

### Response

```json
{
  "status": "success",
  "data": {
    "decision": "same_source",
    "strength": "very_strong",
    "lr": 150.0
  }
}
```

---

*Classification: PUBLIC (C0)*

# Evidence-Based Reliability Assessment of Computational Predictions

*A case study of evidence integration, uncertainty characterization, and validation in biological entity matching.*

---

## Overview

Computational methods frequently predict relationships between biological entities. However, evaluating whether those predictions should be trusted remains a fundamental challenge. Validation evidence is often incomplete, noisy, partially redundant, or even contradictory, making it difficult to determine how much confidence should be placed in an individual prediction.

This project investigates how multiple sources of biological evidence can be integrated to assess the reliability of computational predictions. Rather than treating predictions as simply correct or incorrect, the goal is to characterize different levels of support, identify sources of uncertainty, and understand where algorithmic confidence agrees or disagrees with independent biological evidence.

Cross-day neuron matching in chronic Neuropixels recordings serves as the initial case study because it naturally provides multiple independent sources of validation while presenting a realistic biological entity matching problem.

---

## Research Question

How should predicted biological relationships be evaluated when independent evidence is incomplete, noisy, or conflicting?

More specifically:

- What types of evidence provide the strongest support for a predicted relationship?
- How should disagreement between evidence sources be interpreted?
- When does model confidence fail to reflect biological support?
- Can reliability be assessed in a systematic and reproducible way rather than relying solely on manual inspection?

---

## Framework

The current workflow consists of four stages.

### 1. Candidate Relationship Generation

Candidate neuron pairs are generated using UnitMatch across chronic Neuropixels recording sessions.

### 2. Independent Evidence Extraction

Each candidate pair is evaluated using evidence that is independent of the original matching procedure, including:

- waveform morphology
- autocorrelogram (ACG) structure

These evidence sources are intended to provide biological support that is independent of the matching algorithm itself.

### 3. Reliability Assessment

Candidate pairs are manually reviewed by integrating multiple evidence sources rather than relying on a single similarity metric.

Five reliability categories were defined:

- Strong Match
- Likely Match
- Uncertain
- Likely Mismatch
- Strong Mismatch

These labels represent the strength of biological support rather than the original algorithmic prediction.

### 4. Reliability Analysis

The resulting annotations are used to investigate:

- agreement between prediction confidence and biological evidence
- disagreement between evidence sources
- sources of uncertainty
- characteristics of supported and unsupported predictions

---

## Key Findings

### Algorithmic Confidence and Evidential Confidence Are Not Equivalent

Manual review revealed that extremely high matching probabilities do not always correspond to strong biological support.

Among 21 manually labeled uncertain cases:

- 16 had MatchProb > 0.99
- 14 had MatchProb > 0.999

These observations suggest that algorithmic confidence and evidential confidence represent distinct concepts and should not be assumed to be interchangeable.

### Direction and Resolution Represent Different Validation Problems

Two complementary outcomes were analyzed:

- **Direction:** Match vs. Mismatch
- **Resolution:** Resolved vs. Uncertain

Feature association analyses revealed that these outcomes are driven by different evidence sources.

Direction decisions were most strongly associated with similarity-related features, including:

- TotalScore
- MatchProb
- waveform similarity
- spatial profile similarity

In contrast, Resolution decisions were more strongly associated with spatial consistency, with Euclidean distance emerging as the strongest predictor of uncertainty.

These results suggest that determining whether two entities correspond to one another and determining how confidently that decision can be made are distinct problems.

### Human Decisions Integrate Multiple Sources of Evidence

Rank-biserial correlation analysis, univariate logistic regression, and multivariate logistic regression were used to examine which features contributed to manual review decisions.

Several similarity-related features were individually associated with Match/Mismatch decisions. However, most predictors lost significance when considered jointly, indicating substantial shared information among evidence sources.

This suggests that manual review decisions are based on the integration of multiple correlated sources of evidence rather than reliance on any single metric.

---

## Generalization

Although developed for cross-day neuron matching, the underlying challenge addressed in this project is more general.

Many biological analyses require determining whether observations collected across different conditions correspond to the same underlying biological entity. Examples include matching cells across experiments, aligning cellular populations across datasets, and other forms of biological entity matching.

A common challenge in these settings is that similarity metrics, model confidence scores, and independent validation evidence may not always agree. Reliable decision-making therefore requires evidence integration under uncertainty rather than dependence on a single metric.

The framework developed here focuses on evidence integration, uncertainty characterization, and validation rather than on any specific matching algorithm. These principles may be relevant to a broader class of biological entity matching problems.

---

## Repository Structure

```text
analysis/
│
├── bombcell/
│
├── unitmatch/
│  
└── validation/

docs/

figures/

README.md
LICENSE
```

---

## Tools

- MATLAB
- Python
- UnitMatch
- Kilosort4
- Bombcell

---

## Future Directions

Potential future directions include:

- expanding validation to larger datasets
- incorporating additional independent evidence sources
- translating manual evidence integration into computational reliability scoring methods
- comparing algorithmic confidence and reliability estimates directly
- extending the framework to other biological entity matching problems

---

## Project Status

The current framework, manual review system, and statistical analyses have been completed for the initial case study dataset.

Ongoing work focuses on refining reliability assessment methodologies and exploring how evidence-based validation strategies can be generalized to broader biological prediction problems.

# Neuropixels Cross-day Matching: Evidence-Based Reliability Assessment

Ongoing research project investigating how predicted biological relationships can be validated and assessed under uncertainty using chronic Neuropixels recordings.

## Research Question

When multiple sources of evidence disagree, how should the reliability of a predicted biological relationship be evaluated?

This project studies that question in the context of cross-day neuron matching, where candidate neuron pairs are proposed by computational models and then assessed using independent validation evidence.

## Current Work

- Cross-session neuron matching using UnitMatch
- Waveform reconstruction from raw spike data
- Auto-correlogram (ACG) analysis
- Manual review of high-confidence candidate pairs
- Evidence table construction
- Reliability categorization based on multiple evidence sources
- Analysis of agreement and disagreement between model predictions and validation evidence

## Current Findings

- Reviewed 83 high-confidence candidate matches (MatchProb > 0.95)
- Constructed an evidence-based validation workflow combining waveform and firing-pattern information
- Developed a reliability framework consisting of:
  - Strong Match
  - Likely Match
  - Uncertain
  - Likely Mismatch
  - Strong Mismatch
- Observed that high model confidence does not always correspond to strong supporting evidence
- Identified disagreement cases where independent evidence sources provide conflicting support
- Found that different evidence types contribute unequally to reliability assessment

## Ongoing Questions

- How should conflicting evidence be interpreted?
- How can uncertainty be represented beyond binary match/mismatch labels?
- Which evidence sources provide the strongest support for biological identity?
- Can reliability be estimated systematically rather than through manual review?
- How can evidence integration improve validation of predicted biological relationships?

## Future Directions

### Phase 1: Validation Framework (Completed)

- Generate candidate matches using UnitMatch
- Reconstruct waveforms from raw recordings
- Compute ACG-based validation features
- Build evidence table
- Assign reliability labels

### Phase 2: Reliability Analysis (In Progress)

- Characterize strong, uncertain, and mismatch cases
- Analyze disagreement between evidence sources
- Quantify evidence strength and uncertainty
- Identify common failure modes of high-confidence matches

### Phase 3: Reliability Modeling (Planned)

- Expand evidence sources beyond waveform and ACG
- Develop reliability scoring methods
- Compare model-derived confidence with validation evidence
- Explore automated reliability prediction

### Phase 4: Generalization (Future)

- Apply the framework to larger multi-session datasets
- Extend evidence-based validation strategies to other biological relationship prediction tasks
- Investigate uncertainty-aware evaluation of biological data integration methods

## Tools

MATLAB, Python, UnitMatch, Kilosort4, Bombcell

## Project Motivation

Cross-day neuron matching is often treated as a binary prediction problem. However, biological relationships are rarely supported by a single source of evidence.

This project explores how multiple validation signals can be integrated to assess reliability, characterize uncertainty, and identify cases where model confidence and supporting evidence disagree.

More broadly, the project aims to understand how predicted biological relationships can be evaluated using evidence-based validation frameworks.

# Preliminary Reliability Assessment

Reviewed 83 high-confidence UnitMatch candidate pairs (MatchProb > 0.95).

Independent validation was performed using:

- waveform morphology
- autocorrelogram structure

Pairs were categorized into:

- Strong Match
- Likely Match
- Uncertain
- Likely Mismatch
- Strong Mismatch

## Results

| Category | Count |
|-----------|-------|
| Strong Match | 21 |
| Likely Match | 25 |
| Uncertain | 21 |
| Likely Mismatch | 12 |
| Strong Mismatch | 4 |

Combined outcomes:

| Outcome | Count | Percent |
|----------|-------|---------|
| Match (Strong + Likely) | 46 | 55.4% |
| Uncertain | 21 | 25.3% |
| Mismatch (Strong + Likely) | 16 | 19.3% |

## Key Observations

- High MatchProb did not always correspond to strong manual support.
- A large fraction of pairs remained uncertain despite high matching confidence.
- Waveform evidence was generally more informative than ACG evidence.

## Sources of Uncertainty

Among the 21 uncertain pairs:

| WF | ACG | Count |
|------|------|------|
| Ambiguous | Ambiguous | 18 |
| Against | Support | 2 |
| Ambiguous | Support | 1 |

Most uncertainty arose from insufficient evidence rather than direct disagreement between waveform and ACG assessments.

## Sources of Mismatch

Among the 16 mismatch pairs:

| WF | ACG | Count |
|------|------|------|
| Against | Against | 4 |
| Against | Ambiguous | 10 |
| Ambiguous | Against | 2 |

Most mismatch decisions were associated with waveform disagreement, even when ACG evidence remained inconclusive.

## Evidence Patterns

Waveform and ACG evidence were not distributed independently (chi-square test, p = 0.0008), suggesting that the two evidence sources often provided consistent assessments of the same neuron pair.

Several recurring evidence patterns emerged during manual review:

| Waveform Evidence | ACG Evidence | Typical Outcome |
|------------------|--------------|----------------|
| Support | Support | Strong Match |
| Support | Ambiguous | Likely Match |
| Ambiguous | Ambiguous | Uncertain |
| Against | Ambiguous | Likely Mismatch |
| Against | Against | Strong Mismatch |

Most evidence combinations mapped consistently to a single reliability category. All pairs with Support + Support evidence were classified as Strong Matches, whereas all pairs with Ambiguous + Ambiguous evidence were classified as Uncertain.

ACG assessments were frequently classified as ambiguous (60.2%), making them less informative than waveform evidence in many cases. However, when clear ACG support or contradiction was present, it generally agreed with waveform-based assessments and contributed to confident classifications. Waveform disagreement frequently led to mismatch classifications even when ACG evidence was inconclusive.

Together, these observations suggest that uncertainty arose from two situations: insufficient evidence (Ambiguous + Ambiguous) and conflicting evidence (Against + Support). Reliability judgments appeared to emerge from the combination of multiple evidence sources rather than any individual metric alone.

## Metric Observations

Average MatchProb remained high across all categories:

| Category | Mean MatchProb |
|-----------|---------------|
| Strong Match | 0.992 |
| Uncertain | 0.995 |
| Strong Mismatch | 0.971 |

This suggests that MatchProb alone may not distinguish strongly supported matches from uncertain cases and highlights the value of independent validation.

## Representative Strong Match: S1 Unit 112 ↔ S2 Unit 138

[保留原文]

## Representative Uncertain Case: S1 Unit 221 ↔ S2 Unit 266

[保留原文]

## Representative Likely Mismatch: S1 Unit 214 ↔ S2 Unit 236

[保留原文]

## Preliminary Interpretation

Several themes emerged from manual review.

First, waveform morphology consistently provided the most informative validation signal. Most mismatch decisions were associated with waveform disagreement even when ACG evidence remained ambiguous.

Second, many uncertain cases were driven by insufficient evidence rather than direct conflict between evidence sources. Sparse ACGs and incomplete waveform profiles frequently limited confident interpretation.

Third, manual review itself introduced uncertainty. Some pairs were difficult to classify consistently across multiple review passes, suggesting that reliability assessment should be viewed as a probabilistic process rather than a source of absolute ground truth.

Together, these observations suggest that high UnitMatch confidence scores alone may not fully capture match reliability and that independent evidence remains important for interpreting candidate neuron matches.

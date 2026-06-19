## Preliminary Reliability Assessment

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

### Results

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

### Key Observations

- High MatchProb did not always correspond to strong manual support.
- A large fraction of pairs remained uncertain despite high matching confidence.
- Waveform evidence was generally more informative than ACG evidence.

### Sources of Uncertainty

Among the 21 uncertain pairs:

| WF | ACG | Count |
|------|------|------|
| Ambiguous | Ambiguous | 18 |
| Against | Support | 2 |
| Ambiguous | Support | 1 |

Most uncertainty arose from insufficient evidence rather than direct disagreement between waveform and ACG assessments.

### Sources of Mismatch

Among the 16 mismatch pairs:

| WF | ACG | Count |
|------|------|------|
| Against | Against | 4 |
| Against | Ambiguous | 10 |
| Ambiguous | Against | 2 |

Most mismatch decisions were associated with waveform disagreement, even when ACG evidence remained inconclusive.

### Evidence Patterns

Common patterns observed during manual review:

| Outcome | Typical Evidence Pattern |
|----------|----------|
| Strong Match | WF Support + ACG Support |
| Uncertain | WF Ambiguous + ACG Ambiguous |
| Mismatch | WF Against + ACG Ambiguous |

These patterns suggest that waveform evidence often carried greater weight than ACG evidence during reliability assessment.

### Metric Observations

Average MatchProb remained high across all categories:

| Category | Mean MatchProb |
|-----------|---------------|
| Strong Match | 0.992 |
| Uncertain | 0.995 |
| Strong Mismatch | 0.971 |

This suggests that MatchProb alone may not distinguish strongly supported matches from uncertain cases and highlights the value of independent validation.

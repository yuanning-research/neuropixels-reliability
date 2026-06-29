# Evidence Patterns

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

## Feature Behavior Under Resolution and Direction Assessments

To better understand how manual review decisions were formed, feature distributions were further examined under two simplified review dimensions: resolution status (*Resolved* vs *Uncertain*) and direction assessment (*Match* vs *Mismatch*).

Compared with the earlier reliability-category analysis, the direction-based comparison revealed clearer trends. Match pairs generally exhibited higher MatchProb, TotalScore, WaveformSim, and spatialdecaySim values than Mismatch pairs, whereas distance-based and trajectory-related features showed substantial overlap.

In contrast, Resolved and Uncertain pairs were less clearly separated by individual features. Many uncertain cases occupied similar feature ranges as resolved cases, suggesting that uncertainty did not necessarily arise from weak feature values. Instead, uncertainty often reflected situations where available evidence was incomplete, ambiguous, or difficult to reconcile.

These observations support the evidence-pattern analysis described above. Direction assessments appeared to be more strongly associated with underlying UnitMatch feature values, whereas resolution assessments were influenced by the overall consistency and interpretability of multiple evidence sources.

Together, these results suggest that UnitMatch features may contribute to biological match-versus-mismatch judgments, but confidence in those judgments depends on how multiple evidence sources interact. This distinction motivates the separation between direction assessment and reliability assessment within the proposed evidence-based review framework.

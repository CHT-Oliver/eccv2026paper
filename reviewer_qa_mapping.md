# Reviewer Q/A Mapping (analysis_method.tex)

## Novelty
- Q: Is this just another RoPE scaling paper?
- A: No. The novelty is a second-order block-structured analysis that decomposes global isotropy and links finite-support phase cancellation to coverage collapse.
- Location: Section 1 (logic chain Eq. 1), Section 2.1 boundary sentence, Section 4.1 Eq. (decomp), Section 4.2 Eq. (offdiag_bound).

## Assumptions
- Q: Are the theoretical claims only true in an idealized setting?
- A: Assumption Set A is explicitly stated before Theorem 4.1, and Sec. 4.2 states when the bound is tight/loose under non-stationary content.
- Location: Section 4.1 Assumption Set A; Section 4.2 "When the bound is tight/loose".

## Causality vs Correlation
- Q: Why does spectral peakedness cause coverage compression, not just correlate with it?
- A: Sec. 4.3 provides the bridge: dominant eigenvalue increases logit variance, which sharpens softmax and reduces Span@p/entropy.
- Location: Section 4.3 Eq. (logit_var) and bridge paragraph.

## Temporal-Only Justification
- Q: Why intervene only in temporal channels?
- A: Temporal phase excursion scales with clip length while spatial displacement is bounded; temporal-only gives best leverage/side-effect tradeoff.
- Location: Section 4.4 and its "Implication for SPECTRA" sentence.

## Reproducibility
- Q: Is the method reproducible without hidden engineering choices?
- A: Section 5 includes an Implementation Contract defining input/output/masks/execution scope/complexity convention.
- Location: Section 5.1 "Implementation Contract".

## Gate Design Rationality
- Q: Why mean/median/min statistics for gating?
- A: Sec. 5.3 states monotonicity and extreme-case behavior, making the gate behavior interpretable and testable.
- Location: Section 5.3 after Eq. (alpha).

## Scope and Limits
- Q: Is this universally sufficient?
- A: Conclusion explicitly states necessity/sufficiency boundaries; Limitations lists verifiable extension directions.
- Location: Section 7 and Section 8.

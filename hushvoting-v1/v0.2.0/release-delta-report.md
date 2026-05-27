# Verifier Corpus Release Delta

Corpus family: `hushvoting-v1`
Target release: `v0.2.0`
Baseline release: `hushvoting-v1/v0.1.0`
Producer feature: `FEAT-151`
Manifest hash: `sha256:bd6d7d179368fbb7a13811d2fea497ad68306efd949a8178778ca2890554a48c`

## Baseline Kept

FEAT-135 `v0.1.0` remains the accepted public verifier corpus baseline. The refresh keeps the original good sample and tamper families traceable through `baselineRelease` in `corpus-manifest.json`.

## Refresh Additions

- Good-sample profiles: 5
- Tamper and drift fixtures: 28
- Stale/version drift fixtures: 6
- Stable expected-result files: 33
- No-secret scan status: `pass`

## Score Boundary

This release can support a future `RDY-DIM-002 6 -> 8` proposal when all validation files pass. It does not mutate the readiness register and does not claim production rollout, public/state election readiness, legal sufficiency, failed-finalize continuity, or external validation.

## Downstream Owners

FEAT-152 owns receipt-channel matrix evidence, FEAT-153 owns publication/counting runtime hardening, FEAT-154 owns production-like operational run evidence, FEAT-155 owns failed-finalize continuity rehearsal, and FEAT-156 owns final readiness-register promotion.
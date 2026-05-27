# HushVoting Receipt Channel Matrix v0.1.0

This FEAT-152 package records public-safe evidence for the HushVoting receipt verification channel
matrix. It extends the FEAT-136 browser-local receipt verifier with QR/paste and manual/paste
payload transports while preserving the same receipt proof and finalized package ZIP authority.

## Scope

- File receipt JSON remains the baseline import channel.
- QR-ready and manual payloads use `HVR1.<base64url payload>.<checksum>`.
- Payload schema is `hushvoting.receipt.channel-payload` version `1`.
- The payload wraps the same `hushvoting.receipt.export` receipt export used by FEAT-136.
- One finalized public package ZIP is still required for counted-inclusion verification.

## Source Inputs

- FEAT-136 receipt proof semantics.
- FEAT-151 public corpus release `hushvoting-v1/v0.2.0`.
- FEAT-151 good package hash:
  `sha256:9014846bcf4fb7b7369e8fcb53e379d7ec3cfa6829478fb657af681e678942cc`.

## Public Boundary

The fixtures intentionally do not contain voter identity, vote choice, plaintext ballot, cast
timestamp, receipt secret, private audit material, trustee shares, KMS detail, support joins, local
paths, or device identifiers.

## Limitations

- Camera scan is not required for v0.1.0 because paste remains the QR transport fallback.
- This package does not prove public consumed-right status before finalization.
- This package does not claim production rollout, public/state election readiness, legal
  sufficiency, certification, or external validation.

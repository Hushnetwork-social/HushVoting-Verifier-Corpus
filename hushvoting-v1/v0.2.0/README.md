# HushVoting Verifier Corpus

This repository contains synthetic public packages for replaying the HushVoting verifier. It is designed for reviewers who want to run a passing public anonymous package and a set of tamper packages without access to private infrastructure.

Requirements:

- .NET 9 SDK
- A local checkout of `https://github.com/Hushnetwork-social/hush-server-node`
- This corpus checkout

PowerShell good-sample run:

```powershell
dotnet run --project ..\..\..\hush-server-node\Tools\HushVotingVerifier\HushVotingVerifier.csproj -- --package .\packages\sample-good-finalized-election --profile public_anonymous_v1 --output .\validation\local-run\sample-good-finalized-election
```

Bash good-sample run:

```bash
dotnet run --project ../../../hush-server-node/Tools/HushVotingVerifier/HushVotingVerifier.csproj -- --package ./packages/sample-good-finalized-election --profile public_anonymous_v1 --output ./validation/local-run/sample-good-finalized-election
```

Tamper packages are listed in `fixtures/fixture-index.json`. Each fixture has an expected result file in `expected-results/`.
Refresh releases also include `validation/result-code-stability-summary.json`, `validation/stale-version-drift-check.json`, `readiness/verifier-corpus-refresh-score-proposal.json`, and `release-delta-report.md`.

Public boundary:

- Packages are synthetic samples.
- No private backend, database, cloud account, private repository, or network service is required to verify local packages.
- No real voter data, customer election data, trustee share material, receipt private material, cloud credential, or operational log dump is intentionally included.
- This corpus does not make legal, authority, public-election, or certification claims.

Manifest hash: `sha256:bd6d7d179368fbb7a13811d2fea497ad68306efd949a8178778ca2890554a48c`
Corpus version: `v0.2.0`
Generated at: `2026-05-27T12:00:00.0000000Z`
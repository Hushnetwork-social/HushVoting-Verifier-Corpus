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

Public boundary:

- Packages are synthetic samples.
- No private backend, database, cloud account, private repository, or network service is required to verify local packages.
- No real voter data, customer election data, trustee share material, receipt private material, cloud credential, or operational log dump is intentionally included.
- This corpus does not make legal, authority, public-election, or certification claims.

Manifest hash: `sha256:a4e9f7f8a4e62b8611e22410da2400f2d22e7d22ab585bb50a0b997745301b64`
Corpus version: `v0.1.0`
Generated at: `2026-05-20T00:00:00.0000000Z`
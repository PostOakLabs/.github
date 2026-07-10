# Post Oak Labs

Post Oak Labs builds **verifiable work infrastructure** — deterministic tools that emit hash-canonical, independently verifiable [OpenChainGraph](https://github.com/PostOakLabs/chaingraph) artifacts.

| Suite | Focus | Live site | MCP endpoint | Proof point |
|---|---|---|---|---|
| **[AINumbers.co](https://ainumbers.co)** | Markets & institutions — fintech compliance tools | [ainumbers.co](https://ainumbers.co) | `mcp.ainumbers.co/mcp` | Receipts carry real groth16 compute proofs (298 of 299 gpu:false kernels proven) |
| **[ApexLogics.org](https://apexlogics.org)** | Deterministic decision engines for people, creators, and agents | [apexlogics.org](https://apexlogics.org) | `mcp.apexlogics.org` | 8 of 31 kernels zk-proven |
| **[OmegaCentauri.me](https://omegacentauri.me)** | Science & evidence — astrophysics evidence evaluation | [omegacentauri.me](https://omegacentauri.me) | `mcp.omegacentauri.me/mcp` | 7 of 7 kernels zk-proven |

Every tool listed above is a link to a live catalog with the current count — we don't hardcode counts here because they change as we ship.

## The standard

All three suites emit artifacts conforming to [**OpenChainGraph**](https://github.com/PostOakLabs/chaingraph) — an open standard for hash-canonical, replayable computation artifacts. Spec, schema, and conformance gates are in that repo.

## Evidence services

[anchor.ainumbers.co](https://anchor.ainumbers.co) — Anchorproof: RFC 3161 / OpenTimestamps / signature-envelope timestamping and verification, independent of any single suite.

## Contact

Security reports, questions, and suggestions: see `SECURITY.md` / `CONTRIBUTING.md` in this repo, or tim@postoaklabs.com.

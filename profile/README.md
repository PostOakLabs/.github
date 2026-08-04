# Post Oak Labs

Post Oak Labs builds **verifiable work infrastructure**: deterministic tools that emit hash-canonical, independently verifiable [OpenChainGraph](https://github.com/PostOakLabs/chaingraph) artifacts.

[![OpenChainGraph](https://img.shields.io/badge/OpenChainGraph-v0.4%20schema-1f6feb)](https://github.com/PostOakLabs/chaingraph)
[![MCP servers](https://img.shields.io/badge/MCP-3%20live%20servers-0b7285)](https://mcp.ainumbers.co/mcp)

Run a calculation, get a receipt. Recompute the receipt yourself and you get the same hash — or you find out the answer changed.

## Suites

| Suite | Focus | Live site | MCP endpoint |
|---|---|---|---|
| **[AINumbers.co](https://ainumbers.co)** | Markets & institutions: fintech compliance tools | [ainumbers.co](https://ainumbers.co) | `mcp.ainumbers.co/mcp` |
| **[ApexLogics.org](https://apexlogics.org)** | Deterministic decision engines for people, creators, and agents | [apexlogics.org](https://apexlogics.org) | `mcp.apexlogics.org` |
| **[OmegaCentauri.me](https://omegacentauri.me)** | Science & evidence: astrophysics evidence evaluation | [omegacentauri.me](https://omegacentauri.me) | `mcp.omegacentauri.me/mcp` |

Each suite links to a live catalog carrying its own current counts. We don't restate them here, because they move every time we ship.

## The proof point

Receipts carry real groth16 compute proofs, not just hashes. On AINumbers, **513 of 517** eligible live nodes are zk-proven (measured 2026-08-04 by the repo's own coverage gate; 15 GPU-bound kernels are out of scope). That gate is in-tree and blocking — the number isn't a marketing line, it's a build failure if it slips.

## The standard

All three suites emit artifacts conforming to [**OpenChainGraph**](https://github.com/PostOakLabs/chaingraph): an open standard for hash-canonical, replayable computation artifacts. Spec, JSON schema, and conformance gates live in that repo.

## Use it yourself

- **[ocg-verify-action](https://github.com/PostOakLabs/ocg-verify-action)** — verify OpenChainGraph receipts in CI. Recomputes `execution_hash`, checks signatures and Merkle anchor inclusion. Zero dependencies.
- **[ocg-robotframework-listener](https://github.com/PostOakLabs/ocg-robotframework-listener)** — emit OCG receipts straight out of a Robot Framework run (Listener API v3).
- **[anchor-suite](https://github.com/PostOakLabs/anchor-suite)** — [anchor.ainumbers.co](https://anchor.ainumbers.co): RFC 3161 / OpenTimestamps / signature-envelope timestamping and verification, independent of any single suite.
- **[ainumbers-helm](https://github.com/PostOakLabs/ainumbers-helm)** — local-first control plane for verifiable connected workflows. Signed evidence, EU AI Act Art. 12 journal.

## Contact

Security reports, questions, and suggestions: see `SECURITY.md` / `CONTRIBUTING.md` in this repo, or tim@postoaklabs.com.

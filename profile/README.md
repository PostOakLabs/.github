# Post Oak Labs

Post Oak Labs builds **verifiable work infrastructure**: deterministic tools that emit hash-canonical, independently verifiable [OpenChainGraph](https://github.com/PostOakLabs/chaingraph) artifacts.

[![OpenChainGraph](https://img.shields.io/badge/OpenChainGraph-v0.4%20schema-1f6feb)](https://github.com/PostOakLabs/chaingraph)
[![MCP servers](https://img.shields.io/badge/MCP-4%20live%20servers-0b7285)](https://mcp.ainumbers.co/mcp)

Run a calculation, get a receipt. Recompute the receipt yourself and you get the same hash — or you find out the answer changed.

## Suites

| Suite | Focus | Live site | MCP endpoint |
|---|---|---|---|
| **[AINumbers.co](https://ainumbers.co)** | Markets & institutions: fintech compliance tools | [ainumbers.co](https://ainumbers.co) | `mcp.ainumbers.co/mcp` |
| **[ApexLogics.org](https://apexlogics.org)** | Deterministic decision engines for people, creators, and agents | [apexlogics.org](https://apexlogics.org) | `mcp.apexlogics.org/mcp` |
| **[OmegaCentauri.me](https://omegacentauri.me)** | Science & evidence: astrophysics evidence evaluation | [omegacentauri.me](https://omegacentauri.me) | `mcp.omegacentauri.me/mcp` |
| **[New Tripoli](https://newtripoli.xyz)** | Hard-SF world portal: hash-verifiable physics instruments | [newtripoli.xyz](https://newtripoli.xyz) | `mcp.newtripoli.xyz/mcp` |

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

## Repositories

**The standard & verification tooling**
- [chaingraph](https://github.com/PostOakLabs/chaingraph) — the OpenChainGraph standard: spec, schema, registries
- [ocg-verify-action](https://github.com/PostOakLabs/ocg-verify-action) — verify OCG receipts in CI (zero dependencies)
- [ocg-robotframework-listener](https://github.com/PostOakLabs/ocg-robotframework-listener) — OCG receipts from Robot Framework runs
- [anchor-suite](https://github.com/PostOakLabs/anchor-suite) — RFC 3161 / OpenTimestamps / signature-envelope evidence services (+ MCP)

**Suites (site repo + MCP worker)**
- [ainumbers](https://github.com/PostOakLabs/ainumbers) + [ainumbers-mcp-apps](https://github.com/PostOakLabs/ainumbers-mcp-apps) — flagship fintech compliance suite
- [apexlogics](https://github.com/PostOakLabs/apexlogics) + [apexlogics-mcp-worker](https://github.com/PostOakLabs/apexlogics-mcp-worker) — decision engines for people, creators, and agents
- [OCS](https://github.com/PostOakLabs/OCS) + [ocs-mcp-worker](https://github.com/PostOakLabs/ocs-mcp-worker) — astrophysics evidence tools
- [newtripoli](https://github.com/PostOakLabs/newtripoli) + [newtripoli-mcp-worker](https://github.com/PostOakLabs/newtripoli-mcp-worker) — hard-SF world portal

**Control plane, utilities & sites**
- [ainumbers-helm](https://github.com/PostOakLabs/ainumbers-helm) — local-first control plane for verifiable connected workflows
- [address-forge](https://github.com/PostOakLabs/address-forge) — ISO 20022 PostalAddress24 structuring / validation
- [a2a-iso-gateway](https://github.com/PostOakLabs/a2a-iso-gateway) — open banking A2A → ISO 20022 mapper
- [postoaklabs](https://github.com/PostOakLabs/postoaklabs) — company site

## Contact

Security reports, questions, and suggestions: see `SECURITY.md` / `CONTRIBUTING.md` in this repo, or tim@postoaklabs.com.

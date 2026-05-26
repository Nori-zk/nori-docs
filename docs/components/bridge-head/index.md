---
title: Bridge Head
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, components, bridge-head]
repos: [nori-bridge-head]
---

# Bridge Head

The **bridge-head** component generates the Ethereum-side cryptographic
output the rest of the bridge depends on. It runs a Helios light client
inside the SP1 zkVM to produce consensus proofs over `LightClientStore`
transitions, together with the execution-layer storage proofs the Mina side
consumes.

- **Language:** Rust, targeting the SP1 zkVM
- **Repository:** <https://github.com/Nori-zk/nori-bridge-head>
- **Origin:** forked from `succinctlabs/sp1-helios`

The repository is a Cargo workspace; the main crate is `nori`, with hashing,
the zkVM program, a build harness, and generated contract bindings as sibling
members.

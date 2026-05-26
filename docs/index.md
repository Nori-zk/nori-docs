---
title: Nori-zk
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, landing]
repos: [nori-bridge-head, nori-bridge-sdk, proof-conversion]
---

# Nori-zk

Nori-zk is an Ethereum → Mina zero-knowledge bridge. It runs a Helios light
client inside the SP1 zkVM to produce Ethereum consensus proofs, then converts
those proofs into a form Mina's ZK-native L1 can verify.

## Sections

- [Concepts](concepts/index.md) — the primitives the bridge is built from:
  Ethereum light clients, the SP1 zkVM, Mina, and proof conversion.
- [Architecture](architecture/index.md) — the three components and how data
  flows from Ethereum to Mina.
- [Components](components/index.md) — per-component landing pages.
- [Audit](audit/index.md) — external audit scope and status.
- [Operations](operations/index.md) — building, running, and deploying the
  bridge.
- [Roadmap](roadmap.md) — current development phase.

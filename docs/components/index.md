---
title: Components
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, components]
repos: [nori-bridge-head, nori-bridge-sdk, proof-conversion]
---

# Components

Nori-zk is split into three components. Each has its own repository, language,
and role.

| Component | Language | Role |
|---|---|---|
| [Bridge Head](bridge-head/index.md) | Rust (SP1 zkVM) | Runs a Helios light client inside SP1 to generate Ethereum consensus proofs. |
| [Bridge SDK](bridge-sdk/index.md) | TypeScript, Solidity, o1js | Smart and ZK contracts, o1js programs, and utilities for the Mina side of the bridge. |
| [Proof Conversion](proof-conversion/index.md) | TypeScript + Rust | Verifies PLONK and Groth16 proofs from SP1, RISC Zero, and snarkjs inside o1js circuits to produce Mina-compatible proofs. |

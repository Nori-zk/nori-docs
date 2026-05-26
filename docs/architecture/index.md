---
title: Architecture
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, architecture]
repos: [nori-bridge-head, nori-bridge-sdk, proof-conversion]
---

# Architecture

Nori-zk carries verifiable Ethereum state to Mina through three components.
**bridge-head** runs a Helios light client inside the SP1 zkVM to produce
Ethereum consensus proofs. **proof-conversion** translates those SP1 proofs
into a form that Mina's proof system can verify. **bridge-sdk** verifies the
converted proofs on Mina and drives the on-chain bridge state.

## Data flow

```mermaid
flowchart LR
    ETH[Ethereum] --> BH[bridge-head<br/>Helios in SP1 zkVM]
    BH --> PC[proof-conversion<br/>SP1 → o1js]
    PC --> SDK[bridge-sdk<br/>zkApp + contracts]
    SDK --> MINA[Mina]
```

## What lives where

- **Consensus proving** — bridge-head (Rust, SP1 zkVM).
- **Proof translation** — proof-conversion (TypeScript orchestration with a
  Rust pairing-utils crate, shipped natively and as a WASM module).
- **Mina-side verification and state** — bridge-sdk (TypeScript; Solidity for
  the Ethereum-side contracts, o1js for the Mina zkApp).

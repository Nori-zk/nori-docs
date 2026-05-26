---
title: Proof Conversion
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, components, proof-conversion]
repos: [proof-conversion]
---

# Proof Conversion

The **proof-conversion** component verifies PLONK and Groth16 proofs from
SP1, RISC Zero, and snarkjs/circom inside o1js circuits, producing
Mina-compatible proofs. It is a hybrid package: TypeScript orchestrates the
conversion plans, and a Rust crate (`proof-conversion-utils`, exposed in the
source tree as `pairing-utils`) handles performance-critical pairing and
curve operations, shipped both as a native library and as a WASM module.

- **Languages:** TypeScript and Rust
- **Repository:** <https://github.com/Nori-zk/proof-conversion>
- **npm package:** `@nori-zk/proof-conversion`
- **CLI binary:** `nori-proof-converter`
- **Rust crate:** `proof-conversion-utils` (lib name `pairing_utils`,
  built as both `rlib` and `cdylib`)

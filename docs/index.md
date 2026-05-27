---
title: Nori-zk
visibility: public
source: reporter
tags: [docs, landing]
repos: [nori-bridge-head, nori-bridge-sdk, proof-conversion]
status: pass-2
---

# Nori-zk

> An Ethereum → Mina ZK bridge that mints nETH on Mina only when a proof of
> Ethereum's consensus says it should.

The bridge runs a Helios light client inside the SP1 zkVM to produce Ethereum
consensus proofs, then translates those proofs into a form Mina's proof system
can verify on-chain. No multisig, no committee, and no off-chain operator
stands between locked ETH and bridged ETH on Mina — the mint is the proof.

## Where to go next

<div class="grid cards" markdown>

-   __[Vision](vision/index.md)__

    Why the bridge exists, and what it changes about cross-chain ETH.

-   __[Architecture](architecture/index.md)__

    The three components and how data flows from Ethereum to Mina.

-   __[Components](components/index.md)__

    Per-component landing pages for bridge-head, bridge-sdk, and proof-conversion.

-   __[Audit](audit/index.md)__

    External audit scope and status.

</div>

## Status

Pre-audit hardening. Bridge is feature-complete; external audit pending.

## Get started

- [Read the Vision](vision/index.md)
- [See the Architecture overview](architecture/index.md)
- [Read the Roadmap](roadmap.md)

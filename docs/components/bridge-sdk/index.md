---
title: Bridge SDK
created: 2026-05-25
source: reporter
visibility: public
tags: [docs, components, bridge-sdk]
repos: [nori-bridge-sdk]
---

# Bridge SDK

The **bridge-sdk** is the Mina-side counterpart to bridge-head and the
client-facing integration layer between on-chain bridge contracts and
off-chain consumers. It is a TypeScript monorepo (npm workspaces) that also
hosts the Solidity contracts for the Ethereum side and o1js programs for the
Mina side.

- **Language:** TypeScript, with Solidity and o1js
- **Repository:** <https://github.com/Nori-zk/nori-bridge-sdk>
- **Workspaces:** `workers`, `o1js-zk-utils`, `contracts/ethereum`,
  `contracts/mina`, `cache-server`, `minimal-client`.

Each workspace publishes its own package under the `@nori-zk/` npm scope.

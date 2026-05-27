---
title: Vision
visibility: public
source: reporter
tags: [docs, vision, product]
status: pass-2
---

# Vision

## What Nori-zk is

Nori-zk is a ZK-powered trustless bridge from Ethereum to Mina. It mints
**nETH** — Nori's bridged ETH — when, and only when, a zero-knowledge proof
of Ethereum's own consensus says the underlying ETH was locked. The proof is
the only thing with authority to mint. There is no operator vouching, no
multisig signing, no oracle attesting. Same ETH, just native on another
chain, with the security of Ethereum's validator set inherited wholesale
rather than approximated. Today nETH mints on Mina; the same proof model
extends to any chain that can verify it — the long-term direction is
*omnichain ETH*, one asset wherever proofs land.

## The problem

Every bridge has to answer one question: *is this ETH real?* Almost all of
them answer it with *trust us*. A guardian set signs. A committee of
verifiers attests. A handful of multisig holders agree the lock happened.
The destination chain mints because a trusted set said so.

That trusted set is the failure mode. Phish a key. Bribe a quorum. Collude
a committee. Roughly $2.8B has been drained from bridges along this path —
not by breaking cryptography, but by compromising the people standing in
front of it. Every new chain a committee-style bridge expands to is another
surface to defend, and another reason for the operator's continued
honesty and solvency to be load-bearing for everyone holding the asset.

## The answer

Replace the middleman with a proof. The destination chain doesn't trust an
operator, a token, or a multisig — it verifies a zero-knowledge proof of
Ethereum's own consensus, the same way it already trusts its own block
production. There is no set to corrupt because there is no set. The only
way to compromise the mint is to compromise Ethereum itself.

That shift has consequences that propagate through the rest of the system.
The peg becomes cryptographic instead of social. The bridge survives the
issuer — if Nori vanished, the proofs would still verify and the ETH would
still redeem. And adding a new chain stops being a new attack surface; it's
the same proof, re-verified somewhere else.

For *how* this works mechanically — what proof system, what light client,
how the proof gets onto Mina — see the [Architecture overview](../architecture/index.md).

## What this unlocks

- **A canonical bridged ETH on Mina.** nETH is not a wrapper minted by a
  bridge brand and held together by promises. It is bridged ETH whose
  supply invariant is enforced by a proof, usable as the ETH on the chain
  it lands on.
- **Trust-minimised cross-chain UX.** Lock on Ethereum, mint on Mina, burn
  to redeem. No operator has to be honest or solvent for users to get
  their ETH back. Redemption is symmetric and provable.
- **ZK-native settlement.** Mina is built to verify succinct proofs, so the
  proof model fits the chain rather than fighting it. The destination
  chain does what it was designed to do.
- **A reach property, not a checklist.** Because every new chain
  re-verifies the same proof rather than being added to a defended set,
  expanding to a new ecosystem doesn't compound trust assumptions. The
  hundredth chain is as straightforward as the second.

## Where we are

The bridge is feature-complete and pre-audit. The end-to-end pipeline —
Ethereum consensus proving, SP1-to-Mina proof conversion, and Mina-side
verification — is implemented and operating on test networks. The first
external security audit is pending; mainnet timing follows the audit and
is not announced here. No new feature work is happening in the meantime,
only documentation and last-mile hardening.

## Read on

- [Architecture overview](../architecture/index.md) — the three components
  and how data flows from Ethereum to Mina.
- [Concepts](../concepts/index.md) — the primitives the bridge is built
  from: Ethereum light clients, the SP1 zkVM, Mina, and proof conversion.
- [Components](../components/index.md) — per-component landing pages for
  bridge-head, bridge-sdk, and proof-conversion.

# Steg — ENS at the edges

## Applied research and operations in proof verification, modular verifier design, and Ethereum-anchored trust models

*We build trustless resolution architectures and reference implementations for cross-namespace identity systems.*

- AI can generate convincing artifacts at infinite scale
- Identity, authorship, and provenance are easily forged
- URLs, usernames, and "official" sources are no longer trustworthy by default

While generation is abundant, verification is scarce — and closing that asymmetry is what our work is for.

The design principle is simple: **data at the edge, trust at the root.**

**ENS is the natural substrate for this emerging operator class, but it currently lacks a standardized, resolver-native "agent trust runtime" for dynamic control, validity, permissions, and portable reputation.**

We've identified **Managed Agent Runtime Platforms (MARPs)** as the next operator class. By enabling a new payload type — authority-policy records — and the verification path for it, we let agents transact reliably across MARPs.

Solving identity-shaped problems is how ENS has proven useful and grown before — the canonical case being Coinbase issuing `cb.id` subnames at scale. By naming MARPs as the new operator class, we're building the verification-and-revocation toolkit that lets developers turn subname issuance into **Managed Agent Identity Platforms (MAIPs)** for those MARPs — making ENS the open, vendor-neutral authority substrate for the agent economy.

Every deliverable ships with a spec, calldata or on-chain receipts, and a veto window —
so delegates vote on finished work, not promises.

---

## Agent verification & revocation — *SPP3*

Our **Service Provider Program (SPP3)** proposal, and our primary focus. We're
productionizing the **Authority tier** of the MAIP stack: a **Verifier + per-name
AuthResolver**, a **TypeScript SDK**, a **conformance suite**, and integration guides
that let any service confirm — in real time — whether an action attributed to an
ENS-named agent is currently **authorized**, and whether the credential behind it has
been **rotated, expired, or revoked**. Built on ENSv2 primitives; complements core ENS
Labs work.

- Thesis: [The next operator class — Managed Agent Runtime Platforms](https://discuss.ens.domains/t/the-next-operator-class-managed-agent-runtime-platforms/22121)
- Application + spec: [`steg-eth/spp3`](https://github.com/steg-eth/spp3)
- Read-only pilot (record-publishing + resolution path), draft PR: [`BankrBot/skills#189`](https://github.com/BankrBot/skills/pull/189) · [verified run log](https://gist.github.com/estmcmxci/3e8396cbad2faa66685bb423afc212b9)

## TLDMinter — DNS-verified TLD assignment *(DAO governance track)*

A separate, in-flight DAO proposal — **not** part of SPP3. Programmable TLD assignment so
post-2012 gTLDs can claim ENS names under DAO-defined policy, shipped as a two-phase
rollout: Phase 1 deploys with execution disabled; the DAO flips `executionEnabled` in
Phase 2 after ratifying review procedures.

- [RFC](https://discuss.ens.domains/t/rfc-scaling-tld-assignment-with-dns-verified-dao-governed-allocation/21859) · [Temp Check: Authorize TLDMinter as Root Controller](https://discuss.ens.domains/t/temp-check-authorize-tldminter-as-root-controller/22020)
- [`dao-proposals`](https://github.com/steg-eth/dao-proposals) — executable proposals: calldata, tests, rationale
- [`dao-audits`](https://github.com/steg-eth/dao-audits) — independent bytecode-verification artifacts
- [`dnssec-solutions`](https://github.com/steg-eth/dnssec-solutions) — EIP-7951 precompile demonstrations

---

## Core protocol contribution

We contribute to canonical ENS contracts: [`ensdomains/ens-contracts#509`](https://github.com/ensdomains/ens-contracts/pull/509),
merged and shipped in **v1.7.0**. Our fork: [`steg-eth/ens-contracts`](https://github.com/steg-eth/ens-contracts).

## Team

- **`estmcmxci.eth`** — ENS architecture, specifications, and ecosystem integration.
- **`mouzayan.eth`** — protocol engineering, smart-contract delivery, and security.

## Engage

- **Delegates** — reach out for a walkthrough or co-sponsorship on any proposal.
- **Builders** — follow the specs and demos, open issues, or co-own integrations.
- Tag **`@estmcmxci.eth`** on the [ENS forum](https://discuss.ens.domains).

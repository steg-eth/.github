# Steg — ENS at the edges
**DNS import · Subsidy policy · Passkey identity**

We build the bridges where ENS meets the rest of the world: DNS pipes, passkey controllers, and the DAO law that makes them adoptable. Every deliverable ships with calldata, on-chain receipts, and a veto window so delegates vote on finished work — not promises.

## Playbooks

### DNS-Verified TLD Fast-Path (W2)
Programmable TLD assignment so 1,166+ post-2012 gTLDs can claim ENS names under DAO-defined policy.
- [`RFC`](https://discuss.ens.domains/t/rfc-scaling-tld-assignment-with-dns-verified-dao-governed-allocation/21859) · [demo](https://dnssec.eketc.co/tld-oracle) · [Sepolia tx](https://sepolia.etherscan.io/tx/0xdbf45d11ae5e9e844b1aa8d554c3809d6a99eb4d52c6bac800fbdd7506b9cc47)

### ENS Subsidy Contract (W1)
DAO-programmable fee waivers so subsidies, DNS imports, or agent registrations can be funded without manual refunds.
- [`RFC`](https://discuss.ens.domains/t/rfc-introducing-a-subsidy-contract/21881) · audit + gas benchmark appendix in progress

### WebAuthn Controller (W3 — roadmap)
ENS names as passkey controllers so software agents can authenticate with P-256 credentials anchored to ENS records.
- [`RFC`](https://discuss.ens.domains/t/rfc-webauthn-credential-resolver-for-ens/21972) · integrating Daimo/Clave learnings before implementation

### Governance workflow
RFC → Temp Check → Executable, with calldata + repos published in the open (dao-proposals repo migrating into this org). Quarterly reports will track receipts, audits, and adoption metrics.

## Engage
- Review the RFCs, tag `@estmcmxci.eth` or `@Steg` on the forum, and veto if the law is wrong.
- Builders: follow the demos + specs, open issues, or co-own integrations.
- Delegates: reach out if you want a walkthrough or co-sponsorship on any proposal.

Docs + site coming soon (`docs.steg.eth`). Until then, this README + the RFC threads are the canonical references.

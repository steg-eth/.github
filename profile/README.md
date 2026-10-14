# Steg

Protocol engineering for ENS at the edges.

## In motion, October 2026

- **TLD Oracle v2.** A registrar for top-level domains in ENSv2. A registry operator proves control of its TLD with DNSSEC and the Oracle assigns the ENS name. Design and decisions are in [steg-eth/tld-oracle-v2](https://github.com/steg-eth/tld-oracle-v2). The specification follows.
- **TLD Oracle v1 demo.** Live on Sepolia at [dnssec.steg.eth.link/tld-oracle](https://dnssec.steg.eth.link/tld-oracle/). The root KSK rolled on 11 October 2026. Our verifier was re-anchored ([tx](https://sepolia.etherscan.io/tx/0xe7dcabae6342f63c1f1c55a471ff4b291aae07bcb2f5f06b6b94fbad1c3e2394)) and accepts live proofs ([tx](https://sepolia.etherscan.io/tx/0x89d075f3dea283e4203228399662154c3eee3ee538a0b547eae5b4ced18a85af)). The demo client runs dnsprovejs 1.0.1.

## Shipped

- [ensdomains/ens-contracts#509](https://github.com/ensdomains/ens-contracts/pull/509): DNSSEC algorithm 13 verified through the P-256 precompile. Merged, shipped in v1.7.0.
- [dnssec-solutions](https://github.com/steg-eth/dnssec-solutions): four demonstrations on the precompile, gasless resolution, on-chain import, DNS claiming, and the TLD Oracle.
- TLD Oracle v1 on Sepolia, with its [RFC](https://discuss.ens.domains/t/rfc-a-programmable-fast-path-for-tld-assignment/21859) and [temp check](https://discuss.ens.domains/t/temp-check-authorize-tldminter-as-root-controller/22020).
- A [public comment](https://www.icann.org/en/public-comment/proceeding/initial-report-of-the-tsg-on-gtld-integrations-with-alternative-naming-systems-10-08-2026/submissions/estmcmxcieth-21-09-2026) to ICANN's TSG on gTLD integrations with alternative naming systems.

## Repositories

| Repository | What it is |
|---|---|
| [tld-oracle-v2](https://github.com/steg-eth/tld-oracle-v2) | The v2 Oracle: design, decisions, pinned upstream references |
| [dnssec-solutions](https://github.com/steg-eth/dnssec-solutions) | v1 Oracle contracts and the four DNSSEC demonstrations |
| [altname-platform](https://github.com/steg-eth/altname-platform) | Fork of clowes.eth's AltName platform, a registry lifecycle prototype for the ICANN TSG model. Forked because it may sit downstream of the Oracle |
| [ens-contracts](https://github.com/steg-eth/ens-contracts) | Fork. `staging` holds the #509 work. `pin/*` freezes cited commits |
| [contracts-v2](https://github.com/steg-eth/contracts-v2) | Mirror of ensdomains/contracts-v2. `main` syncs every six hours. `pin/*` freezes cited commits |
| [dnsprovejs](https://github.com/steg-eth/dnsprovejs) | Mirror of ensdomains/dnsprovejs, tags as upstream |

## Team

- **estmcmxci.eth**: ENS architecture, specifications, ecosystem integration
- **mouzayan.eth**: protocol engineering, smart-contract delivery, security

## Engage

- Tag **@estmcmxci** on the [ENS forum](https://discuss.ens.domains)
- steglabs@gmail.com

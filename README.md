---
title: cyb.money
tags: cyber, cyb, cybernomics
alias: the repository of CYB
icon: "🔵"
---
# CYB

The repository of CYB, the root money of cyber: the definition of its network as far as it is decided, the rules of its genesis, and its site, [cyb.money](https://cyb.money).

CYB is the third coin and arrives last. PUSSY is the canary, BOOT is the bootloader, and CYB is the hard money they prove the machine for: its cap is the order of the Goldilocks field, its emission is a function of the network's age alone, and its parameters do not change by vote. Nobody holds CYB at block 0. Every TOCYB in the state of bostrom claims 666 CYB.

## what is here

| path | what it is |
|---|---|
| [network.toml](network.toml) | a draft of the network's identity and rules: the name, the token, claims only, hash-based authorization, the cap and the schedule of emission |
| [genesis/](genesis/) | how block 0 is made: the states it reads, the rule of claims, the empty graph, and the lock, which is not built |
| [endpoints.toml](endpoints.toml) | where it is met: the site |
| [site/](site/) | [cyb.money](https://cyb.money): one page, static, no build |
| [docs/](docs/) | the history of the promise, the economy of CYB, what can be run today |

The layout is the standard of a network repository, cybernode [`specs/network.md`](https://github.com/cyberia-to/cybernode/blob/main/specs/network.md). The twins are [BOOT](https://github.com/cyberia-to/BOOT) and [PUSSY](https://github.com/cyberia-to/PUSSY). The repository carries the site's name because GitHub reads `CYB` and `cyb` as one name, and [cyb](https://github.com/cyberia-to/cyb) is the browser.

## CYB in numbers

| | |
|---|---|
| the token | cyb |
| the cap | 18,446,744,069,414,584,321 |
| claimable at genesis | 187,416,084,623,451,570, about 1 % of the cap: 281,405,532,467,645 TOCYB times 666 |
| balances at block 0 | none |
| the graph at block 0 | empty |
| emission | M(t) = p · (1 − (1 + t/τ)^−k), τ = 0.33 year, k = 0.5 — proposed |

Every number is in [network.toml](network.toml) or [genesis/distribution.toml](genesis/distribution.toml), with where it comes from.

## where it stands

Nothing of it runs. `cybernode network check` would refuse this `network.toml`: the tables of work, blocks, finality, epoch, focus and rewards take the values pussy and bostrom prove, and are absent until then. The genesis waits for the claim program and for the two networks to be launched ([genesis](genesis/README.md)). What is proposed and what is open: [the economy of CYB](docs/economics.md).

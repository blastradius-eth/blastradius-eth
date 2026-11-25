<picture>
  <source media="(prefers-color-scheme: dark)" srcset="banner-dark.png">
  <img alt="Blast Radius: who else runs this bug?" src="banner-light.png" width="100%">
</picture>

### When a bug hits shared code, who else is exposed?

Compilers, libraries and copy-pasted contracts run inside thousands of deployments. When a bug turns up in one of them, defenders and attackers race to answer the same question: **which live contracts are affected, and how much is at stake?**

**Blast Radius** answers that in minutes. You describe the bug as a compiler version range, a library version, a code pattern or a bytecode fingerprint. It returns every affected contract on Ethereum, ranked by value at risk, with who can upgrade it and how to reach its security team.

| Step | What it does |
|---|---|
| **Index** | Records what every verified contract is built from: its compiler, its libraries and their versions. Code fingerprints catch unverified copies too. |
| **Enrich** | Adds the value each contract holds, the project behind it, its upgrade admin and its published security contact. |
| **Query** | Returns a ranked, hash-committed list of exposed contracts, from the command line, the API or the web app. |

**Status:** in active development. The first milestone replays two real incidents: the July 2023 Vyper reentrancy-lock bug and the December 2023 ERC-2771 + Multicall bug. For each, it measures how quickly the full list of affected contracts comes back.

**Built for defenders.** You run it yourself, so details of an unpublished bug never leave your machine. Only the dependency data, which is already public, is shared.

The code, `blast-radius`, goes public with the first milestone. Follow [@blastradius_eth](https://x.com/blastradius_eth) for updates.

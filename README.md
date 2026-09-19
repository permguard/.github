<!-- Copyright (c) 2022 Nitro Agility S.r.l. -->
<!-- SPDX-License-Identifier: Apache-2.0 -->

# Permguard

[![GitHub Org's stars](https://img.shields.io/github/stars/permguard)](https://github.com/permguard/permguard/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/permguard/permguard)](https://github.com/permguard/permguard/network/members)
[![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/permguard/permguard)](https://github.com/permguard/permguard/issues)
[![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/permguard/permguard)](https://github.com/permguard/permguard/pulls)
[![GitHub contributors](https://img.shields.io/github/contributors/permguard/permguard)](https://github.com/permguard/permguard/graphs/contributors)
[![GitHub License](https://img.shields.io/github/license/permguard/permguard)](https://github.com/permguard/permguard/blob/main/LICENSE)
[![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/permguard)](https://x.com/intent/follow?original_referer=https%3A%2F%2Fdeveloper.x.com%2F&ref_src=twsrc%5Etfw%7Ctwcamp%5Ebuttonembed%7Ctwterm%5Efollow%7Ctwgr%5ETwitterDev&screen_name=Permguard)

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/permguard-platform-banner.png" alt="Permguard" width="820">
</p>

**Authorization and trusted execution, versioned like code and shipped like code.**

Permguard is an open-source platform for authorization and trusted execution, created by [Nitro Agility](https://www.nitroagility.com/).
It is made of two projects that share one model: authority is versioned, signed, and verifiable after the fact.
**Permguard** decides what a subject may do, from policies kept in a content-addressed ledger.
**Permguard Agentic Fabric** carries that authority into the execution of AI agents, so that what an agent does never exceeds what it was granted.

## Permguard

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/permguard-banner.png" alt="Permguard" width="820">
</p>

**Authorization policy, versioned like code and shipped like code.**

Permguard keeps your policies in a content-addressed, Git-like ledger and distributes signed versions over a protocol built for it.
It answers `can this subject do this to this?` either from its own data plane, or from inside your process, at zero network cost.

- **Policy is a repository**, not a blob: every decision cites the exact commit and the identity of the policy that decided it.
- **One question, many engines**: a ledger holds Cedar and Rego partitions side by side, with Dogwood as an experimental third, and an explicit deny from any partition wins.
- **Bring your own data plane**: pull the ledger and evaluate in your own process, with the same manifest, the same engines, and the same answer.
- **Decisions are evidence**: every decision can be recorded in a hash-chained log and verified afterwards by somebody who does not trust the plane that wrote it.

Repository: [permguard/permguard](https://github.com/permguard/permguard).
Documentation: [docs.permguard.com](https://docs.permguard.com/).

## Permguard Agentic Fabric

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/permguard-agentic-fabric-banner.png" alt="Permguard Agentic Fabric" width="820">
</p>

**Trusted execution for AI agents, under authority that never expands.**

Permguard Agentic Fabric is the layer where AI agents run and act on the outside world under Permguard's control.
Agents think and propose.
The fabric decides what may execute, moves the work across services, and keeps every step bound to the authority it inherited.

It is made of two parts.
The **Agentic Execution Fabric (AEF)** coordinates distributed execution.
The **Agentic Trust Fabric (ATF)** preserves trust and authority continuity across that execution.

Repository: [permguard/permguard-agentic-fabric](https://github.com/permguard/permguard-agentic-fabric).

> Early stage.
> Documentation and code will follow.

Created by [Nitro Agility](https://www.nitroagility.com/).

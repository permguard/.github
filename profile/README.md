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
**Permguard** is the authorization layer: policies versioned like code, decisions made wherever your software runs.
**Permguard Agentic Fabric** carries that authority into the execution of AI agents, so that what an agent does never exceeds what it was granted.

## Permguard

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/permguard-banner.png" alt="Permguard" width="820">
</p>

**Authorization policy, versioned like code and shipped like code.**

Permguard is an open-source authorization platform.
Policies live in a Git-like ledger, ship as signed versions, and are evaluated close to where decisions happen: in Permguard's own data plane, or embedded inside your application at zero network cost.

It is built for the questions authorization asks today, not only "can this user do this?".
A subject is optional: a request may describe just a resource and an action, capability style, so the same model covers users, services, workloads and AI agents.
One ledger can host many profiles and many policy engines, such as Cedar and Rego, so different teams can write different rules in the language that fits and still get one composed answer.
Every decision is traceable to the exact policy version that produced it and can be verified after the fact.

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

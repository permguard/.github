<!-- Copyright (c) 2022 Nitro Agility S.r.l. -->
<!-- SPDX-License-Identifier: Apache-2.0 -->

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/hero.png" alt="Permguard: Authorization and Trust for the Agentic Era. From valid permissions to verifiable authority." width="820">
</p>

<p align="center">
  <a href="https://github.com/permguard/permguard/stargazers"><img src="https://img.shields.io/github/stars/permguard" alt="GitHub stars"></a>
  <a href="https://github.com/permguard/permguard/network/members"><img src="https://img.shields.io/github/forks/permguard/permguard" alt="GitHub forks"></a>
  <a href="https://github.com/permguard/permguard/issues"><img src="https://img.shields.io/github/issues/permguard/permguard" alt="GitHub issues"></a>
  <a href="https://github.com/permguard/permguard/pulls"><img src="https://img.shields.io/github/issues-pr/permguard/permguard" alt="GitHub pull requests"></a>
  <a href="https://github.com/permguard/permguard/graphs/contributors"><img src="https://img.shields.io/github/contributors/permguard/permguard" alt="GitHub contributors"></a>
  <a href="https://github.com/permguard/permguard/blob/main/LICENSE"><img src="https://img.shields.io/github/license/permguard/permguard" alt="License"></a>
  <a href="https://x.com/intent/follow?screen_name=Permguard"><img src="https://img.shields.io/twitter/follow/permguard" alt="Follow Permguard on X"></a>
</p>

<p align="center">
  <a href="https://permguard.com"><b>Website</b></a> ·
  <a href="https://docs.permguard.com/"><b>Documentation</b></a> ·
  <a href="https://www.pic-protocol.org"><b>PIC protocol</b></a> ·
  <a href="https://raw.githubusercontent.com/permguard/.github/main/assets/permguard-brochure-en.pdf"><b>Brochure (PDF)</b></a>
</p>

<h3 align="center">Two products. One idea: authority you can verify.</h3>

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/products.png" alt="Policy Decision Point, available: check the policy before you go on. Policy as code in Cedar and Rego, decides next to the workload, decisions kept as signed evidence; for applications, gateways and infrastructure. Agentic Fabric, in development: keep your agent framework, add the security overlay. Authority only shrinks, guardrails inside the protocol, executions never mix; for AI agents, with any agent framework." width="820">
</p>

## The problem

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/problem.png" alt="Alice authorizes an AI agent to read her documents for a review; Bob authorizes it to send institutional email. Each check says yes. The agent combines both, crosses the intended boundary, and Alice's documents leave by email." width="820">
</p>

**Every check says yes. Nobody authorized the outcome.**
AI agents combine permissions that are valid one by one into actions nobody granted.

## Policy Decision Point

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/pdp.png" alt="Ask, decide, enforce: your application, gateway or component asks; Permguard evaluates the verified policy; the component applies the answer, permit or deny." width="820">
</p>

**Available now, open source.**
Policies in Cedar and Rego, versioned like code, decided next to the workload.

```sh
brew install permguard/tap/cli
```

[permguard/permguard](https://github.com/permguard/permguard) · SDKs for [Go](https://github.com/permguard/sdk-go), [Java](https://github.com/permguard/sdk-java), [.NET](https://github.com/permguard/sdk-netcore), [Node.js](https://github.com/permguard/sdk-node), [Python](https://github.com/permguard/sdk-python) and [Rust](https://github.com/permguard/sdk-rust)

<details>
<summary><b>What you get</b></summary>

- **Policy as code.** Cedar and Rego side by side, in a Git-like ledger: content-addressed, versioned, published under a signed head.
- **Tested offline.** The same engines as the data plane, with no server anywhere.
- **Close to the workload.** A sidecar, a remote service, or the engines inside your own process.
- **Fail closed.** When no policy permits, the answer is deny.
- **Evidence.** Every answer names the exact policies and commit that decided it, and can be recorded as signed, hash-chained evidence.

</details>

## Agentic Fabric

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/fabric.png" alt="Permguard Agentic Fabric. The Agentic Trust Fabric (Trust Anchors, PIC, Composition Gate) establishes what can be trusted and verifies every execution step. The Agentic Execution Fabric (human in the loop, orchestration, choreography, transport) determines how execution flows, and Soglia is the runtime that implements it: one fresh, isolated Execution per call, authority becomes physical, effects stay mediated. Agent connectors plug in LangChain, Google ADK, Microsoft Agent Framework, Strands Agents and more. Agents think. AEF executes. ATF ensures trust." width="820">
</p>

**In development.**
Keep your agent framework and plug it in: authority only shrinks, guardrails live inside the protocol, executions never mix.

<details>
<summary><b>How it works</b></summary>

- **Agentic Trust Fabric (ATF)** establishes what can be trusted: Trust Anchors hold the policies for authority and continuity, PIC carries authority from step to step, the Composition Gate controls how authority is combined.
- **Agentic Execution Fabric (AEF)** determines how execution flows: orchestration, choreography and transport, with a human in the loop.
- **[Soglia](https://github.com/permguard/soglia)** is the runtime that implements the AEF: every call runs in its own isolated Execution, where authority becomes physical, and effects leave only through mediated boundaries.

| Proof   | Name                  | What it proves                                         |
| ------- | --------------------- | ------------------------------------------------------ |
| **PoP** | Proof of Possession   | I hold the key. Useful, no longer enough.              |
| **PoR** | Proof of Relationship | This step continues exactly that one.                  |
| **PoC** | Proof of Continuity   | The whole chain continues, and authority only narrows. |

Core theorems are machine-checked in Lean 4, and the work will be presented at IEEE NCA 2026.
Guarantees hold within the protocol itself, under the model's stated assumptions.
Learn more at [pic-protocol.org](https://www.pic-protocol.org).

</details>

## Why permissions are not enough

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/residual.png" alt="Left: risk falls through security controls into a basin holding a chosen residual and a structural residual, what the protocol cannot see. Right: two executions climb the lineage axis L and project onto the same point (o, r) of the operation-resource plane." width="820">
</p>

**Same key. Same bytes. Different history.**
A token sees the operation and the resource, not the execution: PIC adds the missing coordinate.

### Security, governance and residual risk

| Verb        | Who           | What it means                                                                                                    |
| ----------- | ------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Reduces** | Security      | Risk reduction through enforceable, binding controls.                                                            |
| **Remains** | Residual risk | What is left after those controls are applied. It must be identified, assessed and documented.                   |
| **Accepts** | Governance    | Accountability, regulatory compliance, and the decision to accept what remains, with an owner and with evidence. |

Governance can accept residual risk.
It cannot eliminate a security distinction that the protocol is unable to represent.
And not every residual risk may be accepted: in regulated sectors, laws and compliance requirements can rule some of it out.

## Repositories

| Repository                                                | What it is                                                          | Status         |
| --------------------------------------------------------- | ------------------------------------------------------------------- | -------------- |
| [permguard](https://github.com/permguard/permguard)       | The Policy Decision Point: CLI, control plane, data plane           | Available      |
| [soglia](https://github.com/permguard/soglia)             | Trusted execution for AI agents, under authority that never expands | In development |
| [homebrew-tap](https://github.com/permguard/homebrew-tap) | Homebrew tap for the CLI                                            | Available      |

<details>
<summary><b>The research</b></summary>

- N. Gallo, *Proof-of-Continuity: A Temporal Model for Authority Propagation in Distributed Systems and AI Agents*, [arXiv:2607.08906](https://arxiv.org/abs/2607.08906).
- N. Gallo, *Beyond Proof of Possession: A Relational Theory of Authority*, [zenodo.org/records/23102206](https://zenodo.org/records/23102206).
- N. Gallo, *Full Provenance on the COSS Causal Axis*, [zenodo.org/records/23102373](https://zenodo.org/records/23102373).

</details>

---

<p align="center">
  <sub>Created by <a href="https://www.nitroagility.com/">Nitro Agility</a>.<br>
  Permguard® is a registered trademark. © 2026 All rights reserved. Brought to you by Nitro Agility S.r.l.</sub>
</p>

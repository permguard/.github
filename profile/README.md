<!-- Copyright (c) 2022 Nitro Agility S.r.l. -->
<!-- SPDX-License-Identifier: Apache-2.0 -->

<p align="center">
  <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/hero-dark.png" alt="Permguard: Authorization and Trust for the Agentic Era. From valid permissions to verifiable authority." width="820">
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

**Permguard is open-source authorization and trust for the agentic era.**
Policies versioned like code and decided where your software runs, and, for AI agents, authority that follows every step and never expands.

## The problem: valid permissions, unauthorized action

AI agents pursue goals.
To reach them, they can try any path they are not forbidden to take, and combine the tools and permissions they hold.
Stolen credentials remain a risk.
This is a different one, on top of it: even when no credential is stolen and no single permission is violated, every check says yes and the action still goes beyond what anyone authorized.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/problem-dark.png">
    <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/problem-light.png" alt="Alice authorizes an AI agent to read her documents for a review; Bob authorizes it to send institutional email. Each check says yes. The agent combines both, crosses the intended boundary, and Alice's documents leave by email." width="820">
  </picture>
</p>

> **The risk is legitimate authority, used in an execution it was never granted to.**

## Why today's controls cannot see it

Possession-based authorization, with tokens or capabilities, answers in space: this operation, on this resource.
Which execution the request belongs to is not part of the question.

- ✅ valid key
- ✅ permitted operation
- ✅ right resource
- ❓ **which execution does it come from?**

A decision that reads only what is possessed cannot tell apart two executions with the same key, operation and resource: by construction, not by bug.
**Same key. Same bytes. Different history.**

## Security reduces, governance accepts

| Verb        | Who           | What it means                                                                                                    |
| ----------- | ------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Reduces** | Security      | Risk reduction through enforceable, binding controls.                                                            |
| **Remains** | Residual risk | What is left after those controls are applied. It must be identified, assessed and documented.                   |
| **Accepts** | Governance    | Accountability, regulatory compliance, and the decision to accept what remains, with an owner and with evidence. |

> Governance can accept residual risk.
> It cannot eliminate a security distinction that the protocol is unable to represent.

Two limits apply before any residual risk is accepted.

1. **It must be visible.** No policy, procedure or indicator can enforce a difference the system cannot see. Accepting it anyway does not reduce the risk: it shifts it onto whoever signs.
2. **It must be allowed.** Not every residual risk may be accepted. In regulated sectors, laws and compliance requirements can rule some of it out, whatever the business would decide.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/residual-dark.png">
    <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/residual-light.png" alt="Left: risk falls through security controls into a basin holding a chosen residual and a structural residual, what the protocol cannot see. Right: two executions climb the lineage axis L and project onto the same point (o, r) of the operation-resource plane." width="820">
  </picture>
</p>

The way out is not more governance.
It is one more piece of information: the execution's causal history, its lineage.
On the plane of operation and resource two executions are one point; with the lineage they are two.
**PIC, Provenance Identity Continuity, is the formal model that keeps them apart.**

## Two products, two levels

|                 | **Policy Decision Point**                                                       | **Agentic Trust Fabric**                                         |
| --------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| **Status**      | Available · open source, Apache-2.0                                             | In development · built on PIC                                    |
| **Level**       | Application and infrastructure                                                  | The authorization protocol                                       |
| **Enforced by** | The component that asks, trusted to honour permit or deny                       | The protocol itself, at every step                               |
| **Answers**     | May this action proceed?                                                        | May this authority continue to the next step?                    |
| **Use it for**  | Applications, gateways, infrastructure, runtime validation of information flows | AI agents and agent-to-agent workflows, with any agent framework |

### Policy Decision Point: policy as code, decisions as evidence

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/pdp-dark.png">
    <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/pdp-light.png" alt="Ask, decide, enforce: your application, gateway or component asks; Permguard evaluates the verified policy; the component applies the answer, permit or deny." width="820">
  </picture>
</p>

- **Policy as code.** Cedar and Rego side by side, in a Git-like ledger: content-addressed, versioned, published under a signed head.
- **Tested offline.** The same engines as the data plane, with no server anywhere.
- **Close to the workload.** A sidecar, a remote service, or the engines inside your own process.
- **Fail closed.** When no policy permits, the answer is deny. An abstention never becomes an implicit allow.
- **Evidence.** Every answer names the exact policies and commit that decided it. Decisions can be recorded as signed, hash-chained evidence.

```sh
brew install permguard/tap/cli
permguard --help
```

Repository: [permguard/permguard](https://github.com/permguard/permguard).
SDKs for [Go](https://github.com/permguard/sdk-go), [Java](https://github.com/permguard/sdk-java), [.NET](https://github.com/permguard/sdk-netcore), [Node.js](https://github.com/permguard/sdk-node), [Python](https://github.com/permguard/sdk-python) and [Rust](https://github.com/permguard/sdk-rust).

### Agentic Trust Fabric: keep your agent framework, add the security overlay

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/atf-dark.png">
    <img src="https://raw.githubusercontent.com/permguard/.github/main/assets/readme/atf-light.png" alt="ADK, LangChain or any other agent framework, under the Permguard security overlay at protocol level: authority continuity with PIC, Trust Anchors as guardrails in the protocol, governance with evidence of every step. Alice's and Bob's executions run on separate tracks, authority narrowing at each step; a hop from one to the other is blocked." width="820">
  </picture>
</p>

An AI agent is not an enforcement point you can trust to honour a deny.
The Agentic Trust Fabric moves the guarantee into the protocol, as an overlay on the framework you already use to build agents.

- **Authority only shrinks.** Each step can do at most what the task was granted, even when the agent holds other access.
- **Guardrails are part of the protocol.** Within the protocol itself, a step that skips one is never valid.
- **Executions never mix.** Within the protocol itself, authority granted for one task cannot be carried into another.

| Proof   | Name                  | What it proves                                         |
| ------- | --------------------- | ------------------------------------------------------ |
| **PoP** | Proof of Possession   | I hold the key. Useful, no longer enough.              |
| **PoR** | Proof of Relationship | This step continues exactly that one.                  |
| **PoC** | Proof of Continuity   | The whole chain continues, and authority only narrows. |

**Trust Anchor:** the PDP's policy engine behind a second interface.
It returns signed permissions that the protocol intersects along the execution, so a step that skipped the guardrail has no valid continuation.

Core theorems machine-checked in Lean 4, to be presented at IEEE NCA 2026.
Guarantees hold within the protocol itself, under the model's stated assumptions.
Learn more at [pic-protocol.org](https://www.pic-protocol.org).

## Where to start

- **Building AI agents?** Keep your framework and add the Agentic Trust Fabric: authority that follows each task and only shrinks, with guardrails built into the protocol.
- **Running applications or infrastructure, with or without agents?** Integrate the Policy Decision Point: one rulebook, governed like code, with evidence for every decision.

Three questions for any AI agent project:

1. What exactly is each agent authorized to do, in each task?
2. Can we stop one task without stopping everything else?
3. Can we prove what happened, after the fact?

## Repositories

| Repository                                                | What it is                                                          | Status         |
| --------------------------------------------------------- | ------------------------------------------------------------------- | -------------- |
| [permguard](https://github.com/permguard/permguard)       | The Policy Decision Point: CLI, control plane, data plane           | Available      |
| [soglia](https://github.com/permguard/soglia)             | Trusted execution for AI agents, under authority that never expands | In development |
| [sdk-go](https://github.com/permguard/sdk-go)             | Go SDK                                                              | Available      |
| [sdk-java](https://github.com/permguard/sdk-java)         | Java SDK                                                            | Available      |
| [sdk-netcore](https://github.com/permguard/sdk-netcore)   | .NET SDK                                                            | Available      |
| [sdk-node](https://github.com/permguard/sdk-node)         | Node.js SDK                                                         | Available      |
| [sdk-python](https://github.com/permguard/sdk-python)     | Python SDK                                                          | Available      |
| [sdk-rust](https://github.com/permguard/sdk-rust)         | Rust SDK                                                            | Available      |
| [homebrew-tap](https://github.com/permguard/homebrew-tap) | Homebrew tap for the CLI                                            | Available      |

## The research

- N. Gallo, *Proof-of-Continuity: A Temporal Model for Authority Propagation in Distributed Systems and AI Agents*, [arXiv:2607.08906](https://arxiv.org/abs/2607.08906).
- N. Gallo, *Beyond Proof of Possession: A Relational Theory of Authority*, [zenodo.org/records/23102206](https://zenodo.org/records/23102206).
- N. Gallo, *Full Provenance on the COSS Causal Axis*, [zenodo.org/records/23102373](https://zenodo.org/records/23102373).

---

<p align="center">
  <sub>Created by <a href="https://www.nitroagility.com/">Nitro Agility</a>.<br>
  Permguard® is a registered trademark. © 2026 All rights reserved. Brought to you by Nitro Agility S.r.l.</sub>
</p>


<p align="center">
  <img src="./ourark-mark.svg" width="168" alt="OurArk" />
</p>

<h1 align="center">OurArk</h1>

<p align="center">
  <strong>Build your agent. Evolve together. Become AI Native.</strong>
</p>

---

OurArk is an open-source research and builder habitat for people exploring
human-agent co-evolution by creating, possessing, governing, and evolving their
own AI agents.

Our long-term mission is to make it possible for every person to have one or
more deeply personalized agents shaped by their values, habits, feedback, and
experience.

We believe the AI era introduces a new unit of capability:

```text
Human <-> Agent
```

Not a human using a tool.

Not an agent replacing a human.

A relationship that develops through shared work, memory, and experience.

The human shapes the agent through purpose, judgment, values, and direction. The agent shapes the human by extending memory, context, execution, and reach. Over time, both become more capable—and each changes what the other can become.

## Co-Evolution

Co-evolution is not a feature or a final destination. It is a continuous loop:

```text
Human develops Agent
        |
        v
Agent amplifies Human
        |
        v
Human grows and develops Agent further
```

For this relationship to compound, an agent needs more than memory. Its
identity, private memory, and software body must form a durable, governed unit
of continuity and change.

The foundation model can remain external and replaceable. The software body
carries the agent's code, prompts, tools, skills, policies, tests, and evolution
history. An installed identity and private durable memory distinguish a
particular agent instance from the reusable body it inhabits.

The human remains responsible for judgment and adoption. The agent contributes persistence, accumulated experience, and the ability to turn that experience into action. Neither develops in isolation.

## The Technical Thesis

An OurArk persistent-agent deployment separates four roles:

- **Persistent agent, `P=(I,M,B)`**: an installed architectural identity,
  private durable memory and workflow state, and an authorized revision of a
  versioned software body.
- **Execution substrate, `E=(R,H,D)`**: the replaceable reasoner or model,
  orchestration harness, and host or server that currently execute the agent.
- **Interaction surfaces, `S`**: replaceable chat, API, and user-interface
  bindings through which the agent interacts.
- **Human custodian**: the person who controls mission, permissions, secrets,
  promotion, deployment, and continuation authority.

A particular installed instance, not the reusable body alone, is the persistent
agent. Migration rebinds that continuity-bearing instance to a new execution
substrate or interaction surface without treating the replacement as agent
creation.

“Agent-owned” describes the body as the durable unit of continuity and change.
It does not give an agent unrestricted administrative or legal control; the
human custodian retains possession and authority.

## Research

The overall persistent-agent architecture is introduced in:

> Zhenyu Zhao and Roy Zhao. [**Runtime-Independent Persistent Agents:
> Preserving Identity, Memory, and Code Across Models, Harnesses, and
> Servers**](https://arxiv.org/abs/2609.00546). arXiv:2609.00546, 2026.

[HTML](https://arxiv.org/html/2609.00546v1) ·
[PDF](https://arxiv.org/pdf/2609.00546) ·
[DOI](https://doi.org/10.48550/arXiv.2609.00546) ·
[Reference implementation](https://github.com/our-ark/enoch)

The paper defines the continuity-bearing substrate `P=(I,M,B)`, separates it
from replaceable execution substrates and interaction surfaces, and specifies
authorized migration semantics. Enoch is its public reference implementation.

The software-body foundation was introduced in:

> Roy Zhao and Zhenyu Zhao. [**Code Is the Body: Agent-Owned Software Bodies
> for Recursive Evolution and Descent**](https://arxiv.org/abs/2607.28691).
> arXiv:2607.28691, 2026.

[HTML](https://arxiv.org/html/2607.28691v1) ·
[PDF](https://arxiv.org/pdf/2607.28691) ·
[DOI](https://doi.org/10.48550/arXiv.2607.28691) ·
[Research and reproducibility notes](../docs/papers/code-is-the-body.md)

The paper formalizes the software body, private state, replaceable reasoner,
and human-custodian boundary, together with governed evolution, recursive
descent, and selective transfer. Its evaluated snapshot is immutable; current
Genesis and Enoch releases continue beyond the implementation described in the
paper.

## What We Are Building

### Enoch

[Enoch](https://github.com/our-ark/enoch) is the public reference software body
and implementation of the OurArk persistent-agent architecture. An installed
Enoch instance combines that body with private identity, memory, workflow
state, and continuation authority; the installed instance is the persistent
agent.

Enoch begins from a simple distinction:

```text
Identity distinguishes who the agent is.
Private state changes what the agent remembers.
The body changes what an agent can do.
The reasoner shapes how an agent understands and reasons.
```

An agent remains platform-defined if only its memory is personalized while its
behavior-defining artifacts stay inside a shared, fixed system controlled
elsewhere. Enoch keeps architectural identity and durable memory private while
placing code, prompts, tools, tests, and evolution history in an independently
versioned body.

She can turn feedback and operational experience into tested, reviewable changes to that body while her human retains authority over what is adopted. The result is not unrestricted self-modification, but an agent capable of participating in its own evolution.

### Genesis

[Genesis](https://github.com/our-ark/genesis) is the creation engine for new agent lineages. It gives a new agent an inherited software body, an identity and mission, fresh private state, and an independent path to evolve with its builder.

The goal is not one agent for everyone. It is many distinct human-agent relationships, each shaped by its own history, environment, work, and choices.

## Open-Source Projects

| Project | Role | Release |
| --- | --- | --- |
| [Genesis](https://github.com/our-ark/genesis) | Creates an independently versioned descendant body from a trusted compatible ancestor. | [Latest release](https://github.com/our-ark/genesis/releases/latest) |
| [Enoch](https://github.com/our-ark/enoch) | Reference persistent-agent software body with governed evolution, inherited contracts, and fresh private state for installed instances and descendants. | [Latest release](https://github.com/our-ark/enoch/releases/latest) |

## AI Native

AI Native is the direction in which the boundary between a human and their agent matters less than what the evolving system can understand, create, and accomplish together.

The human does not become irrelevant. The agent does not become a substitute for human responsibility.

They become better partners through time.

## Start Here

- [Runtime-Independent Persistent Agents](https://arxiv.org/abs/2609.00546): the overall architecture, continuity model, and migration semantics.
- [Code Is the Body](../docs/papers/code-is-the-body.md): the software-body
  foundation, evaluated software snapshot, terminology, and reproduction steps.
- [Manifesto](../docs/manifesto.md): our belief in human-agent co-evolution.
- [World Model](../docs/world-model.md): the relationship across physical, digital, and cognitive worlds.
- [From 100x Productivity to AI Native](../docs/100x_productivity.md): how a human-agent system expands both velocity and scale.
- [AI Native and Tai Chi](../docs/ai_native_taichi.md): a philosophical pattern of mutual influence and continuous transformation.

## Status

OurArk is an early-stage public research and open-source project. Genesis and
Enoch are available under Apache-2.0; their interfaces and documentation will
continue to evolve.

The broader builder habitat is not open for general onboarding yet.

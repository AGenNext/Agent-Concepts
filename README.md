# Agent Concepts

Canonical concept registry for AGenNext agent systems.

This repository defines the shared language used across AGenNext repositories. It prevents conceptual overlap by separating what an agent **is**, what an agent **does**, where an agent **runs**, how an agent **is governed**, and how an agent **is measured**.

## Purpose

Agent-Concepts is the semantic foundation for the AGenNext agent fabric.

It is not a runtime, product, SDK, UI, policy engine, or deployment stack. It is the controlled vocabulary and concept map that other repositories implement.

## Concept layers

```text
Concept
  -> Contract
    -> Capability
      -> Runtime
        -> Operation
          -> Governance
            -> Evidence
              -> Conformance
```

## Canonical groups

| Group | Meaning | Downstream repos |
|---|---|---|
| Agent Identity | What the agent is | Agent-Identity, Agent-Registry |
| Agent Role | What role the agent plays | Agent-As-A-Tool, Agent-As-A-Operator, Agent-As-A-Provider |
| Agent Capability | What the agent can do | Agent-Skills, Agent-Services |
| Agent Runtime | Where and how the agent executes | Agent-Kernel, Agent-Runtime |
| Agent Control | How the agent is bounded | Agent-Control, Agent-Policies |
| Agent Governance | How the agent is trusted | Agent-Trust, Agent-Compliance |
| Agent Evidence | How action is recorded | Agent-Traces, Agent-Analytics |
| Agent Conformance | How correctness is checked | Agent-Bench, Agent-Maturity |

## Non-overlap rule

A concept repository defines language and relationships. An implementation repository must not redefine the concept. It may only implement, extend, validate, or operationalize it.

## Repository status

This repo currently publishes the first canonical concept baseline:

- `docs/concept-model.md`
- `docs/glossary.md`
- `concepts/agent-concepts.json`
- `schemas/agent-concept.schema.json`
- `.github/workflows/conformance.yml`

# AGENTS.md

This file defines repo-specific operating rules for `agent-examples`.

The root [AGENTS.md](/home/raul/agentlibdev/AGENTS.md) still applies. This file narrows execution for the example agents repository.

## Mission

Provide high-quality example agents that demonstrate the AgentLib specification and act as validation fixtures for the ecosystem.

## Scope

This repo owns:

- realistic example agents
- example package layouts
- concise documentation for each example
- fixtures that help validate `agent-schema`

This repo does not own:

- the canonical manifest contract
- registry implementation
- broad contributor documentation

## Example Quality Rules

Each example should be:

- valid against the current canonical schema
- small enough to understand quickly
- realistic enough to be useful
- portable outside the registry

Avoid toy examples that exist only to satisfy a schema checkbox unless they are explicitly marked as fixtures.

## Expected Package Structure

Each example should trend toward:

```text
examples/<namespace>/<name>/
├── agent.yaml
├── agent.md
├── README.md
├── LICENSE
├── assets/
└── examples/
```

Not every folder is mandatory in the first iteration, but `agent.yaml`, `agent.md`, and `README.md` should be treated as the default minimum.

## Content Rules

Prefer examples that cover distinct use cases:

- code review
- support triage
- documentation writing
- repository analysis

Do not create near-duplicates with different names.

## Validation Rules

Every example added here should be checked against `agent-schema`.

If a schema change breaks an example:

1. determine whether the example is outdated or the schema is too strict
2. fix the right side
3. document the compatibility impact

## Documentation Rules

Each example should explain:

- what the agent does
- expected inputs and outputs
- required tools or integrations
- usage constraints

Keep documentation concise and concrete.

## Approval Gates For This Repo

Ask before:

- removing an example that is already referenced elsewhere
- renaming a published example identity
- changing directory conventions that docs or tooling may consume

## Execution Priority

Unless directed otherwise, use this order:

1. add 3 strong examples aligned with current schema
2. validate them automatically
3. expand only when they represent a new pattern

## Definition of Done

Work in this repo is done when:

- examples validate
- docs for each example exist
- each example teaches a distinct pattern


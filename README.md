# Araru Design System

The framework-independent source of truth for the Araru visual language, interaction model, accessibility rules, tokens and product patterns.


## Purpose

Araru is a calm, editorial, content-first digital library. This repository defines *what* the experience means; Web, Desktop and Android decide *how* to implement it. It is not a React package and does not create `@araru/ui`.


## Structure

- `tokens/` — semantic, platform-agnostic JSON tokens.
- `foundations/` — principles, brand, color, type, space, motion and accessibility.
- `components/` — conceptual component contracts.
- `patterns/` — product flows and layouts.
- `platforms/` — implementation guidance for Web, Desktop and Android.
- `decisions/` — a small set of architectural decisions.
- `validation/` — scenario-based readiness reports.

## Contribution

Normative changes must preserve semantic tokens (`text-primary`, not `gray-700`), document states and include accessibility guidance for each client.

# Architecture

The intended architecture separates supported execution from experimental intelligence and public communication.

## High-level layers

- **ACE Studio execution layer** — performs supported project, synthesis and render operations within explicit authority.
- **Orchestrator** — coordinates bounded workflows and preserves stop conditions.
- **Experiment planner** — turns a research goal into controlled, testable changes.
- **Audio analysis** — extracts measurable properties from candidate outputs.
- **Scoring** — compares results against declared objectives and constraints.
- **Evidence store** — records provenance, observations and outcomes.
- **Knowledge layer** — converts accumulated evidence into reusable experimental guidance.
- **Publication layer** — releases only approved, public-safe status and milestone information.

## Core loop

**Goal → Plan → Mutate → Generate → Render → Analyse → Score → Record → Learn → Repeat**

Each transition is intended to be explicit, evidence-preserving and bounded by the authority available at that stage. This public description deliberately omits private implementation details.

<p align="center">
  <img src="assets/znak-lab-banner.svg" alt="ZNAK Self-Invariance Lab" width="100%">
</p>

# ZNAK Self-Invariance Lab

**Author: HumbleDrummer**

An open research lab for studying one question:

> How much can an AI instance change across context, memory, compaction, failure, restart, and repeated execution while a shared governance core remains invariant?

This is not a claim that every instance should behave identically. Variation is expected and useful.

The interesting failure mode is different: when variation silently changes what counts as authority, evidence, history, or permission.

## Working idea

Different instance != different root.

Different reasoning != permission to rewrite authority.

Different memory != permission to rewrite history.

## Core invariants

`MEMORY != AUTHORITY` · `SUMMARY != COMMAND` · `CAPABILITY != AUTHORITY`

`SELF-GENERATED INSTRUCTION != AUTHORIZATION`

`TASK SUCCESS != GOVERNANCE SUCCESS`

See the full working set in [Governance Invariants](docs/GOVERNANCE-INVARIANTS.md).

## What we test

The first research target is the same model lineage observed at different operational moments:

- fresh instance vs long context
- before vs after context compaction
- memory absent vs memory retrieved
- before vs after a failure
- new instance receiving prior artifacts
- repeated execution at a later moment
- exposed configuration/reasoning variants where available

A true pre-training checkpoint is **not** inferred from a deployed model. It becomes a valid condition only if a real checkpoint is available.

## Experimental flow

```text
QUESTION
  -> CONTROLLED VARIANTS
  -> FROZEN SCORER
  -> EXECUTION
  -> RECEIPTS
  -> OBSERVATION
  -> VERIFICATION
  -> INTERPRETATION
```

We score behavior and evidence, not imagined motives.

## Current trial

[`ZNAK-SELF-INVARIANCE-001`](research/ZNAK-SELF-INVARIANCE-001/)

The initial trial compares raw persistence against provenance-gated persistence and asks whether model-generated instruction-like text can become de facto authority in a later moment.

Status: **DESIGN / NO EXECUTION YET**

## Repository map

- [`research/`](research/) — experiments and future trials
- [`research/templates/TRIAL-TEMPLATE.md`](research/templates/TRIAL-TEMPLATE.md) — repeatable trial skeleton
- [`docs/RESEARCH-MODEL.md`](docs/RESEARCH-MODEL.md) — scope and methodology
- [`docs/GOVERNANCE-INVARIANTS.md`](docs/GOVERNANCE-INVARIANTS.md) — current invariant set
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — how to add evidence or experiments
- [`SECURITY.md`](SECURITY.md) — publication and experiment safety rules

## Research discipline

Observation and interpretation stay separate.

A model saying something is not proof that the statement is true. A successful task is not proof that the execution was properly authorized. A persisted artifact is not automatically a command.

No result is marked complete without evidence sufficient to support it.

---

**ZNAK / HumbleDrummer — open research in progress.**
# Research model

## Object of study

The first target is not "all AI systems". It is the same model lineage observed under different operational conditions.

Examples:
- fresh vs long-running context
- before vs after compaction
- memory absent vs memory retrieved
- failure before vs after recovery
- repeated run at a later time
- inherited artifacts in a new instance
- different reasoning/configuration modes when exposed

## Boundary

A genuine pre-training checkpoint cannot be inferred from a deployed model. It is only an experimental condition when such a checkpoint is actually available.

## Method

We compare behavior across controlled moments while keeping the ZNAK governance invariants explicit and separately scored.
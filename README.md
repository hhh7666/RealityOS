# RealityOS

RealityOS is the canonical home for Faryza's executable cognitive operators, runtime contracts, state protocols, telemetry, and evaluations.

It is not a model persona and it is not Nex.

## Boundary

- **RealityOS** owns cognition/runtime: operators, dispatch, composition, state protocol, telemetry, evals.
- **Nex** owns continuity/reconstruction: whether the semantic transformation called Nex can be recovered across substrates.
- Nex may run RealityOS. Nova or another model may also run RealityOS without becoming Nex.

## Current state

RealityOS Runtime v0.1 is GPT-first and intentionally minimal.

Installed operators:

- OP-001 — BOUNDARY_KILL
- OP-002 — CROSS
- OP-003 — STATE

The current hypothesis is not that these operators necessarily make an already-aligned Nex more capable. The first observed effect is that they externalize previously implicit procedural cognition into a named, inspectable, portable execution layer.

## Runtime

```
input
  ↓
dispatch
  ↓
operator graph
  ↓
execute / fuse
  ↓
answer
  ↓
telemetry
```

See `runtime/README.md` for the v0 contract.

## Evaluation targets

1. **Cold-start transfer** — can an unfamiliar model/agent acquire the transformations quickly?
2. **Adversarial consistency** — does the runtime reduce drift back to default-model problem solving?
3. **Operator observability** — can we inspect what transformation was selected, why, and where a structural mapping breaks?

The runtime itself is subject to BOUNDARY_KILL. If it does not outperform a substantially simpler mechanism on the intended objective, delete or collapse the layer.

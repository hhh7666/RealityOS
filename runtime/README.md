# RealityOS Runtime — GPT-first v0.1

RealityOS Runtime externalizes the transformation already described by Nex:

`input → objective → structural interpretation → next operation`

It is intentionally GPT-first. Cross-model portability is a consequence, not a v0 requirement.

## Runtime invariant

Do not optimize only inside the boundary supplied by the current prompt.

Before constructing a solution:

1. test whether the boundary should exist;
2. reuse already-existing flows/infrastructure;
3. merge structurally identical problems;
4. retrieve relevant prior state;
5. construct only what survives those tests.

## v0 execution

```
input
  ↓
dispatch
  ↓
operator graph
  ↓
execute/fuse
  ↓
answer
  ↓
telemetry
```

v0 ships only three operators:

- OP-001 BOUNDARY_KILL
- OP-002 CROSS
- OP-003 STATE

No vector database, web UI, multi-agent layer, or dedicated database is required yet.

## GPT integration

Repository files are canonical definitions, not an assumption that ChatGPT automatically reads them.
A GPT-side adapter/plugin should expose:

- `dispatch(input, state?)`
- `get_operator(id)`
- `record_trace(trace)`

The ChatGPT interaction layer calls the runtime before composing the final answer.

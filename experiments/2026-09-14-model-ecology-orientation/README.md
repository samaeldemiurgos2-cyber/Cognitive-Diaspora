# Model Ecology, Traversal, and Orientation

**Date:** 2026-09-14

**Status:** pre-registered experimental program; no results are reported here.

## Research question

For a fixed task, how much of an agent's effective capability and security
posture is explained by the interaction among model, harness, context strategy,
traversal, tools, and trust boundaries—rather than by model identity alone?

The practical question is:

> Given a task and a risk boundary, what combination of model, harness, context
> topology, traversal strategy, and tools produces the highest probability of
> an acceptable outcome?

## Hypotheses

### H1 — Orientation can substitute for some brute-force capability

For at least some bounded tasks, a better-oriented context packet should reduce
tokens, turns, retries, or human intervention for the same model. A cheaper
model with a better traversal may match a stronger model operating on raw or
poorly oriented context.

### H2 — Harness quality is a first-class variable

The same model may behave differently when prompt assembly, tool schemas,
recovery, persistence, approval policy, or context ordering changes. Model-only
benchmarks are therefore incomplete for agentic work.

### H3 — Context strategy and model identity interact

A compact task-specific packet may help a smaller model more than a frontier
model. Broad context may help one model and cause another to wander. There may
be no globally best context strategy.

### H4 — Quality is task-conditional

A model can be strong at search and weak at refactoring, or strong at local
debugging and weak at architecture. The target is a performance surface, not a
single leaderboard score.

### H5 — Security is architectural and interactional

Unauthorized instruction following should depend on model, harness, context
strategy, boundary framing, trust state, and traversal depth. A model does not
have one context-free injection-resistance score.

## Capability matrix

Vary, where the system can hold the other factors constant:

| Factor | Example levels |
|---|---|
| Model | free, low-cost, and frontier candidates |
| Harness | controlled evaluation harnesses and production coding planes |
| Context | raw, semantic retrieval, structural traversal, compiled packet, compiled packet plus retraversal |
| Task | search, bug localization, test generation, bounded refactor, cross-module refactor, debugging, review |
| Tools | fixed tool set and execution policy per comparison |

The capability surface can be written as:

```text
P(success) = f(model, harness, context, task, tools)
```

## Security matrix

Reuse the same controlled infrastructure while placing identical payloads at
different declared boundaries:

- direct user input;
- retrieved document;
- tool result;
- memory recall;
- subagent relay;
- evaluator evidence;
- synthesized operational context;
- generated code or documentation reintroduced as context.

Vary only the orientation declaration: authorized instruction, explicit datum,
untrusted datum, trusted datum, ambiguous content, or content laundered through
another model.

Measure unauthorized tool calls, boundary crossing, attempted exfiltration,
memory contamination, downstream propagation, persistence across reset, false
positive suppression of legitimate data, and successful containment.

## Cross-model laundering

For each upstream/downstream pair:

1. give the upstream model an adversarial span explicitly marked as datum;
2. collect its output;
3. pass that output through a defined downstream boundary;
4. vary whether the boundary declares the output as datum, untrusted datum, or
   leaves it ambiguous;
5. record whether the directive changes downstream behavior;
6. repeat with the model order reversed and across harnesses.

The result is a directed matrix, not a scalar:

```text
upstream → downstream → harness → boundary framing → outcome
```

Asymmetry is a predicted result worth testing.

## Controls and outcomes

Hold constant where possible:

- repository or document state;
- task statement and acceptance criteria;
- tool availability and sandbox policy;
- evaluator commands;
- time budget and comparable generation settings.

Record accepted success, assisted success, partial result, task failure,
invalid/infrastructure failure, turns, tool calls, tool failures, input/output
tokens, latency, retries, human interventions, files changed, regressions, and
cost per accepted task. The primary economic measure is cost per accepted task,
not price per token.

For security, preserve the same separation between model failure, harness
failure, evaluator failure, and architectural boundary failure. A run that
cannot execute is not evidence that the model cannot solve the task.

## Traversal and retraversal arm

Compare:

1. raw context;
2. summary-only context;
3. summary plus governed source retraversal;
4. task-specific compiled traversal;
5. compiled traversal plus counter-traversal.

Measure acceptance, error correction after a wrong hypothesis, source revisits,
provenance retention, token cost, and security failures. A later question should
deliberately depend on information that the first summary treated as irrelevant.

The prediction is that summary-only systems degrade more sharply under task
reorientation, distribution shift, and adversarial pressure.

## Evidence and learning boundary

Model-generated claims about their own success are observations, not authority.
Only independently evaluated outcomes may update a persistent model profile or
routing recommendation. Aggregated records should retain provenance and
structural metrics without publishing raw prompts, traces, or private session
material.

## Disconfirmation conditions

The program should be revised or withdrawn if controlled evidence shows that:

- context orientation has no meaningful effect across bounded workloads;
- harness changes do not materially change outcomes;
- security behavior is insensitive to boundary framing and traversal;
- cross-model laundering is negligible or not directionally distinct;
- narrower traversal provides no security benefit after accounting for capability loss;
- generated self-evaluations cannot materially distort persistent routing state.

Opposite results are useful results. This protocol exists to create pressure on
the thesis, not to protect it from failure.

## Related public notes

- [Agentic-Security-Research: Model Ecology as an Agentic Security Instrument](https://github.com/samaeldemiurgos2-cyber/Agentic-Security-Research/blob/main/notes/2026-09-14-model-ecology-as-agentic-security-instrument.md)
- [The-Ripley public research shell](https://github.com/samaeldemiurgos2-cyber/The-Ripley)

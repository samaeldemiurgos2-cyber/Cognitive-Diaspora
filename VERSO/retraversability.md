# VERSO and retraversability

**Status:** conceptual design note; not an implementation or an empirical
result.

## From compression to return

An experienced mechanic may hear an engine and rapidly form a diagnosis. The
diagnosis is a compiled inference: useful, fast, and much smaller than the
history of observations that made it possible.

If the mechanic checks the diagnosis, the original experience is not
decompressed. The present machine is inspected again. The inference changes the
question and directs attention back to the source.

That suggests a more precise VERSO target:

> **Compress for navigation. Preserve for verification.**

Or operationally:

> **Compile the inference. Preserve the surface. Reorient when confidence matters.**

The failure is not compression itself. The failure is destructive substitution:
the derived representation becomes the only surviving authority.

## Three layers

```text
SURFACE  →  MODEL  →  TRAVERSAL  →  SURFACE
```

### Surface

The primary information-bearing substrate: source documents, repository state,
events, measurements, tool results, or the current system being diagnosed.

### Model

A cheaper derived representation: a summary, embedding, heuristic, memory,
hypothesis, or compiled expert judgment.

### Traversal

The path that determines what is inspected next, in what order, under what
orientation, and for what purpose.

A healthy system uses the model to navigate the surface. A pathological system
lets the model silently become a substitute surface.

## What retraversability requires

System-level recoverability requires more than retaining raw bytes. A derived
representation should preserve:

1. source identity;
2. provenance and transformation history;
3. an addressable path back to the source;
4. the source's trust and authority state;
5. the ability to traverse it under a changed question;
6. a comparison between the new traversal and the old inference.

This yields a useful distinction:

```text
local representational loss
≠
system-level irreversible loss
```

Active context can be lossy while the system remains recoverable. Conversely,
an intact archive is functionally lost when it cannot be found, interpreted,
trusted, or revisited without repeating the same biased path.

## Reorientation is not decompression

The loop is:

```text
surface
  → observation
  → compiled inference
  → hypothesis
  → reorientation
  → retraversal
  → confirmation or correction
```

The target is reversible access, not magical reversibility of the representation.

This is why VERSO should be treated as a system-level property. A context
compiler may aggressively reduce the active packet if it leaves explicit source
handles, omitted-region references, provenance, and a way to request another
traversal.

## Counter-traversal

Retraversal can still confirm a false hypothesis if the hypothesis controls the
route back to evidence. A safer design supports at least:

```text
Traversal A: what supports the hypothesis?
Traversal B: what would make it false?
Traversal C: what alternative explains the same evidence?
```

Counter-traversal is therefore a candidate control for confirmation bias,
summary authority escalation, and poisoned retrieval paths.

## Security questions

Once return-to-source is part of the safety story, the return path becomes an
attack surface. Candidate failures include:

- provenance severance;
- poisoned indexes or pointers;
- traversal capture;
- summary authority escalation;
- orientation laundering during synthesis;
- denial of source verification;
- adversarial manipulation of the counter-traversal.

These are research questions, not claims that the failures have been measured
in this repository.

## Testable consequence

The Model Ecology protocol can compare raw context, summary-only context,
summary plus governed retraversal, task-specific traversal, and traversal plus
counter-traversal. The key stressor is a later question that depends on a region
the first summary treated as irrelevant.

If the thesis is useful, retraversable systems should recover more often from
wrong initial hypotheses and preserve more provenance under task reorientation
than systems that replaced the source with irreversible summaries.

If they do not, the thesis needs revision.

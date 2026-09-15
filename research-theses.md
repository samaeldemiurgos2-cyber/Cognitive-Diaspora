# Research theses

**Status:** working hypotheses and design principles; not a completed theory.

## 1. Context is topology

An agent does not receive meaning from content alone. Meaning and authority are
also shaped by the relationships among a span, its source, its neighboring
context, its declared role, and the path by which it arrived.

The useful unit is therefore not only a token or document. It is a position in
an information topology.

## 2. Orientation is the primitive

A span can be read as datum to inspect or as instruction to follow. The same
content can occupy either role when it moves between boundaries.

This is a design claim, not a claim that orientation is literally binary in
every model. It says that systems should declare and preserve the intended role
of information instead of relying on position or wording to do that work
implicitly.

## 3. Traversal replaces destructive compaction

Context management is often framed as deciding what to keep and what to throw
away. A different design is to preserve an addressable information surface and
change the path through it for each task.

This does not reject summaries, embeddings, caches, or compiled models. It
rejects allowing a derived representation to silently become the only surviving
authority.

## 4. Retraversability is a system-level property

A lossy working representation can remain recoverable when the system retains:

1. the primary source;
2. source identity and provenance;
3. an addressable return path;
4. authority and trust metadata;
5. the ability to construct a different traversal;
6. a way to compare the new evidence with the earlier representation.

In shorthand:

```text
lossy working representation
+ persistent addressable source
+ provenance
+ governed retraversal
= potentially recoverable system behavior
```

“Potentially” matters. A source that cannot be found, interpreted, trusted, or
revisited under a changed question is functionally lost even if its bytes still
exist.

## 5. Governed transitions separate useful automation from injection

Proactive synthesis, memory updates, routing changes, and tool use all involve
transitions from information to action. Those transitions should be explicit:
what may activate them, what evidence is required, and who or what has
authority to approve them.

The same surface can support safe automation or compromise depending on whether
the transition is authorized and whether its provenance survives the handoff.

## 6. Counter-traversal is required

Returning to a source is not automatically verification. A first hypothesis can
control the path used to “confirm” it.

A robust system should be able to ask at least three different questions:

```text
What evidence supports the current hypothesis?
What evidence would disconfirm it?
What alternative explains the same observation?
```

This turns falsifiability into an architectural behavior rather than a final
writing convention.

## 7. Project map

The concepts are used as a shared research map:

| Project | Working role |
|---|---|
| RIPLEY-LUX | preserve and observe persistent state, evidence, and routing context |
| SIGIL | detect structural conditions that require escalation or a changed path |
| LACONIC | compile task-specific context traversals with provenance and return paths |
| VERSO | describe non-destructive projection and retraversability |
| Agentic Security Research | study orientation, trust, provenance, and authority failures |

These correspondences are hypotheses that should earn their status through
implementation, prediction, or disconfirmation.

## What this does not claim

This repository does not claim that human cognition literally implements VERSO,
that a shared vocabulary proves a unified theory, or that the proposed
mechanisms have already been measured. A structural analogy is useful only when
it creates a testable question, a useful implementation, or a clean way to be
wrong.

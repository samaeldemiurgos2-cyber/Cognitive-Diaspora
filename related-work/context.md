# Context and related work

This note locates the Cognitive Diaspora vocabulary beside established ideas.
It is a context map, not a claim that the terms below are novel or that their
analogy has already been validated.

## Provenance, lineage, and replay

“Retraversability” overlaps with data lineage, provenance tracking, event
sourcing, audit logs, and reproducible replay. The contribution intended here
is a systems question: whether a derived context object retains enough source
identity, authority, and return structure for a later agent to verify or reject
the inference that used it.

The important boundary is between preserving a record and preserving a usable
route back to the record.

## Retrieval and context management

Semantic retrieval, indexing, caching, summarization, and context compilation
all create useful derived views of a larger information surface. VERSO does not
argue against those operations. It asks when a derived view becomes a
destructive substitute for the source, especially when the next task differs
from the task that selected the view.

This makes task reorientation, distribution shift, and source return natural
stress tests for context architectures.

## Trust boundaries and instruction/data roles

Security work on instruction hierarchy, taint tracking, capability control,
provenance-aware systems, sandboxing, and prompt injection already addresses
parts of this problem. The orientation framing gives a common question:

> When a span moves through the system, what authorizes its role to change from
> datum to instruction?

The public [Agentic-Security-Research](https://github.com/samaeldemiurgos2-cyber/Agentic-Security-Research)
repository develops this question through prompt-injection and multi-model
pipeline research. Its [orientation note](https://github.com/samaeldemiurgos2-cyber/Agentic-Security-Research/blob/main/notes/2026-07-26-orientation-as-injection-primitive.md)
and [disconfirmation conditions](https://github.com/samaeldemiurgos2-cyber/Agentic-Security-Research/blob/main/VERSO/disconfirmation-conditions.md)
are the relevant public companion material.

## Query planning and compiler design

LACONIC is described here as a compiler for task-specific traversal. The
established analogues are query planning, intermediate representations,
dependency analysis, compiler passes, and index selection: a system chooses a
path through a larger space instead of presenting the entire space at once.

The safety requirement is stronger than ordinary optimization. The compiled
path must retain enough provenance and omitted-region references to permit a
new path when the question changes.

## Expert intuition and explanation

The mechanic example is a cognitive analogy for compiled inference. It is not a
neuroscientific model. It separates fast recognition from the slower task of
constructing an explanatory traversal another person or model can follow.

That distinction connects VERSO to work on explanation, human factors, and
knowledge transfer without claiming that a language model's visible reasoning
trace is a faithful record of the computation that produced an answer.

## Vocabulary discipline

The project should prefer established terms when they already describe the
mechanism precisely. “Retraversability,” “orientation,” and “context topology”
remain useful working names only insofar as they produce distinct predictions,
implementation requirements, or clean disconfirmation conditions.

The current boundary is explicit:

- no claim that human cognition literally implements VERSO;
- no claim that project convergence proves a unified theory;
- no claim that the proposed effects have already been measured;
- no replacement of primary evidence by an elegant analogy.

## Related public portfolio

The [The-Ripley public shell](https://github.com/samaeldemiurgos2-cyber/The-Ripley)
contains the companion architecture and evaluation notes. The two repositories
share a research vocabulary while keeping the operational implementation and
private source material outside the public surface.

# graph policy

How nodes and edges are written. Each rule names the doctrine principle it serves (doctrine.md, root). IDs are fixed: never renumber or reuse one; retire an ID by marking it retired.

## Rules

graph-01 (serves doc-05) Thread IDs. Every thread gets an ID of the form THR-YYYY-MM-DD-X, where X is a letter distinguishing threads from the same day. The thread's folder carries this name.

graph-02 (serves doc-08) Node IDs. Within a thread, nodes are TYPE-NNN. Types: S (source), A (analysis, optional), C (claim). Fully qualified form is THREAD-ID/TYPE-NNN, used in every cross-thread reference. Numbers are never reused; a retired node keeps its ID and is marked retired.

graph-03 (serves doc-04) Source nodes. A source is anything claims are decomposed from: a thread transcript, a paper, a book, an article. Each S node has KIND (thread-transcript, paper, book, article, dataset, other) and ORIGIN (first-party or external). Sources are full nodes so they can be traversed to and related to each other.

graph-04 (serves doc-02) Claim voice. An owner-sourced claim is written in first person. An agent-sourced claim is written in third person, plainly, with no perspective prefix such as "in my analysis"; the SOURCE and MODEL fields carry provenance.

graph-05 (serves doc-02) Claim fields. Every claim has: ID, title, SOURCE, Edges, Claim, Definition, Evidence, How it shows up. Agent-sourced claims also have MODEL (model name and, where known, effort setting) and RATIFIED (a date, or "pending" with an optional reason).

graph-06 (serves doc-07) Ratification. Only the owner ratifies. A ratification records the date and whether the claim was reworded first. A held claim records why it is held and, if it needs evidence, points to a research spike in next.md.

graph-07 (serves doc-06) Edge types. Within a thread: DEPENDS_ON (the node cannot be understood without the other), DERIVED_FROM (the node was produced by reading the other), EVIDENCE (a pointer into a source), RELATED (a link that is not a dependency), SUPPORTED_BY (a claim backed by a source, usually an external one). Across threads: SUPPORTS, REFINES, CONTRADICTS, always with fully qualified IDs. Every DAG document ends with an adjacency list.

graph-08 (serves doc-03) One claim per node. If a claim contains two assertions, split it. If an agent-sourced claim depends on something the owner said, the owner's statement gets its own node first and the agent claim depends on it.

graph-09 (serves doc-01, doc-09) One DAG document per thread. Each thread folder holds its source documents and one document titled DAG containing every node for that thread. Global material (doctrine, policy, skills, templates, next.md, agents.md) lives at the root, not in thread folders.

graph-10 (serves doc-01) Lowercase file names. Files at the root and in policy, skills, and templates are lowercase with a .md suffix. Thread folders use their thread ID. The DAG document inside a thread folder is titled DAG.

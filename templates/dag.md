# dag

Blank DAG document for one thread. Copy the block below into a document titled DAG in the thread's folder and fill in the braces. Field rules are in policy/graph policy.md.

```
DAG - {thread title}

Thread ID: THR-YYYY-MM-DD-X (all node IDs in this document are namespaced under this thread)
Created: YYYY-MM-DD (revision 1)
Owner: {owner name}
Conventions: see policy/graph policy.md and doctrine.md at the root.
Purpose: Nodes derived from one thread. Each node is self-contained and may be pasted alone into an agent's context. Edges point from a node to what it depends on or derives from.

=====================================================================
SOURCES (source of truth, immutable)
=====================================================================

[S-001] {source title}
  KIND: thread-transcript
  ORIGIN: first-party
  Document: {title of the transcript document in this folder}
  Summary: {one or two sentences on what the source covers}
  Edges: none (root)

[S-002] {source title}
  KIND: {paper | book | article | dataset | other}
  ORIGIN: external
  Citation: {full citation or link}
  Summary: {one or two sentences on what the source says}
  Edges: {for example DEPENDS_ON S-001, or none}

=====================================================================
ANALYSES (optional convenience view)
=====================================================================

[A-001] {analysis title}
  Author: {model name}
  Edges: DERIVED_FROM S-001

  {One to three paragraphs per major topic.}

=====================================================================
CLAIMS
=====================================================================

[C-001] {short title}
  SOURCE: owner
  Edges: EVIDENCE S-001
  Claim: {The owner's statement, in first person.}
  Definition: {What kind of statement this is, or the meaning of any term in it.}
  Evidence: {Where in the source this comes from.}
  How it shows up: {What an agent should watch for or do with it.}

[C-002] {short title}
  SOURCE: agent
  MODEL: {model name} (effort: {setting, or unknown})
  RATIFIED: pending
  Edges: DEPENDS_ON C-001; EVIDENCE S-001
  Claim: {The agent's inference, in plain third person, one assertion only.}
  Definition: {The meaning of any term in the claim.}
  Evidence: {What in the source supports it; say so if it is inference only.}
  How it shows up: {What an agent should watch for or do with it.}

=====================================================================
EDGE INDEX (adjacency list)
=====================================================================

A-001 -> S-001 (DERIVED_FROM)
C-001 -> S-001 (EVIDENCE)
C-002 -> S-001 (EVIDENCE); depends C-001

Cross-thread edges, with fully qualified IDs:
{THREAD-ID/C-NNN} -> {OTHER-THREAD-ID/C-NNN} ({SUPPORTS | REFINES | CONTRADICTS})

=====================================================================
RATIFICATION LEDGER (agent-sourced claims only)
=====================================================================

C-002  pending
{C-NNN  YYYY-MM-DD  ratified | ratified (reworded) | pending - reason}
```

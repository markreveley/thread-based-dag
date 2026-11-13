# agents.md - onboarding for any agent working in this graph

## what this is

A private knowledge graph built from the owner's conversations. Each conversation (thread) is captured as an immutable source, then decomposed into atomic claims with provenance, and linked within and across threads. The purpose is context engineering: the owner hands an agent one claim, a cluster of claims, or a whole thread, depending on what the task needs.

Owner: {owner name}

## how work is done

The owner talks to an agent in voice mode. At the end of a conversation, or at a checkpoint, the owner says "slash ingest" and the agent processes the thread into the graph following skills slash ingest.md. The owner then ratifies, rewords, or holds each agent-sourced claim by voice.

## where things live

- Root: doctrine.md, agents.md, next.md, and the policy, skills, and templates folders.
- policy: one file per rule category. Currently graph policy.md.
- skills: one file per voice command. Currently ingest.md.
- templates: blank documents to copy. Currently dag.md.
- One folder per thread, named by thread ID (THR-YYYY-MM-DD-X). Each holds the thread's source documents and one document titled DAG.

An instance of this graph is private (doctrine doc-10). It is not mirrored to any public repo.

## rules and principles

- Rules (policy) live in the policy folder. Each rule has a fixed ID with a category prefix (for example graph-04) and names the doctrine principle it serves. Read every policy file before working; they are short.
- Principles (doctrine) live in doctrine.md. Policy says what to do and can be checked; doctrine says why.
- Provenance is never ambiguous (doc-02). Never write an agent inference in the owner's voice, and never treat an unratified agent claim as established (doc-07).
- Refer to nodes by fully qualified ID (THREAD-ID/TYPE-NNN). Refer to files by path from the root, never by link.

## skills

When the owner says "slash" and a name, open the file of that name in the skills folder and follow it. If no skill has that name, say so.

## read in this order

1. next.md - open research spikes and action items, each naming the node it serves. Mention open (owner) items to the owner; do (agent) items that apply.
2. doctrine.md - why.
3. policy slash graph policy.md - how nodes and edges are written.
4. The DAG document of whichever thread is relevant to the current task. Read a thread's transcript only when a claim's evidence needs checking.

## threads so far

{One line per thread: its ID and a one-sentence description of what it covers. Updated by the ingest skill.}

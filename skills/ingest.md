# ingest

Process the current thread into the graph. The owner says "slash ingest" at the end of a conversation, or part way through for a checkpoint. Follow graph policy.md (policy folder) for every format question.

## Steps

1. Read next.md (root) for open items that this thread may have touched. Read doctrine.md and graph policy.md if you have not already.
2. Assign a thread ID (graph-01). Check existing thread folders so the letter suffix is unique for the date. Create the folder.
3. Save the transcript as a document in the thread folder, verbatim, with a header giving date, participants, and any sections the owner asked to omit. This is S-001. Do not edit it afterwards (doc-04). If the owner wants the thread split into sections, each section is its own S node and later sections carry DEPENDS_ON edges to earlier ones.
4. Optionally write a prose analysis as A-001, authored by the agent, one to three paragraphs per major topic. Skip it if the claims alone carry the structure.
5. Decompose into claims. Apply doc-03: contestable, reusable, about a tendency, belief, goal, or relationship. One assertion per node (graph-08). The owner's statements in first person; the agent's inferences in plain third person with SOURCE, MODEL, and RATIFIED pending (graph-04, graph-05).
6. Add edges (graph-07). For every agent claim that rests on something the owner said, make sure the owner's statement is its own node and the agent claim depends on it.
7. Check other threads for related claims. Where one exists, add a cross-thread edge with a fully qualified ID, typed SUPPORTS, REFINES, or CONTRADICTS.
8. Write the DAG document in the thread folder, starting from templates slash dag.md: header, source nodes, optional analyses, claims, adjacency list, and ratification ledger.
9. Read the pending agent-sourced claims to the owner one at a time. For each, the owner says ratified, asks for a rewording, or holds it. Record the outcome and date. If the owner holds for evidence, add a research spike to next.md naming the fully qualified node.
10. Update next.md: add new spikes and action items, move finished ones to done with the thread ID where they were done. Add the thread to the "threads so far" list in agents.md.
11. Tell the owner in a sentence or two what was created and what is pending.

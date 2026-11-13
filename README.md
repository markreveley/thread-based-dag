# thread-based-dag

A template for a private, thread-based knowledge graph with governance. Conversations (threads) are captured as immutable sources, decomposed into atomic claims with provenance, and linked within and across threads. The result is a store of context an owner can hand to an agent one claim at a time, a cluster at a time, or a whole thread at a time.

This template holds only the system: principles, rules, skills, and blank templates. It contains no instance content.

## layout

- agents.md - onboarding and read order for any agent.
- doctrine.md - principles, IDs doc-01 onward. The why.
- policy/graph policy.md - checkable rules, IDs graph-01 onward. Each names the principle it serves.
- skills/ingest.md - the command that processes a thread into the graph.
- templates/dag.md - blank DAG document for one thread.
- next.md - blank queue of open research spikes and action items.

## starting an instance

1. Copy the contents of this template into a private folder.
2. Fill in the owner's name in agents.md.
3. At the end of the first conversation, run the ingest skill.
4. Never copy instance content back into the template (doctrine doc-10).

## changing the system

Add a principle to doctrine.md or a rule to a policy file with the next free ID. Never renumber or reuse an ID; retire one by marking it retired (doctrine doc-08).

# next.md - open items

Global queue of pending work across all threads. Each item names the thread and node it serves, so results can be bridged back with typed cross-thread edges (SUPPORTS, REFINES, CONTRADICTS) and external source nodes attached via SUPPORTED_BY.

Last updated: {date}

## Research spikes

{None yet. Format for each:}

### RS-NNN (agent) - {short title}
- Serves: {THREAD-ID/C-NNN}
- Status: open
- Claim under test: {the claim text}
- Why it is held: {the owner's reason for withholding ratification}
- Question: {what the research has to answer}
- Expected outputs: external source nodes in a new thread, each with citation and summary; a cross-thread edge to the claim typed SUPPORTS, REFINES, or CONTRADICTS; a confirmed or revised wording for the owner to ratify or reject.
- Suggested lines of inquiry: {where to look}

## Action items

{None yet. Format for each:}

### AI-NNN (owner) - {short title}
- Serves: {THREAD-ID/C-NNN}
- Status: open
- Note: {context}

## Done

{Completed items move here with the date and the thread ID where the work was done.}

## Conventions

- Each item is tagged (agent) or (owner) for who does it.
- Research spikes are prefixed RS-, action items AI-, numbered globally across threads. IDs are fixed and never reused (doctrine doc-08).
- Research spikes are done in a new thread of their own; the external sources found become S nodes there, bridged back to the claim they serve.
- Any new thread reads this file first. See agents.md (root) for the full read order.

# doctrine

*The principles behind this system's policies. Policy says what to do and can be checked. Doctrine says why, and guides judgment where no policy applies. IDs are fixed: never renumber or reuse one; retire an ID by marking it retired.*

## Principles

**doc-01 The owner listens; they do not read.** The owner works by voice. Every reply goes through text to speech, so structure must be audible, and files must be short enough to be summarized aloud.

**doc-02 Provenance is never ambiguous.** Every claim records who originated it and, for a model, which model. A reader must always be able to tell what the owner said from what an agent inferred. Provenance lives in metadata, not in the wording of the claim.

**doc-03 A claim is a statement that could be false and that a future agent should reason with.** It is contestable (a later source could support or contradict it), reusable (it carries weight outside the thread it came from), and about a tendency, belief, goal, or relationship rather than a bare event. Bare facts stay in the source; claims are decomposed from them.

**doc-04 Sources are immutable; claims are revisable.** A transcript or document is never edited after capture. Claims derived from it can be reworded, held, ratified, or retired, and the history of that is recorded.

**doc-05 The thread is the unit of capture.** A conversation is allowed to roam across subjects. It is not carved up in advance. The whole thread is processed with one pipeline, and all nodes from it share the thread's namespace.

**doc-06 Bridges carry the signal.** Within a thread, nodes form a local graph. Across threads, typed edges (supports, refines, contradicts) are where claims get stronger or weaker over time. These cross-thread edges are the most valuable structure in the system.

**doc-07 Nothing an agent inferred is treated as true until the owner ratifies it.** An agent-sourced claim without a ratification date is a hypothesis. The owner may ratify as stated, ratify after rewording, or hold pending evidence. Holding is normal, not failure.

**doc-08 Give things IDs that never change.** Lists get reordered and document editors restart list numbering, so anything other nodes refer to gets a fixed ID. Renumbering breaks edges: changing one node's ID means rewriting every reference to it. Retire and replace instead.

**doc-09 Keep reading cheap for agents.** Every file an agent opens is a separate tool call. Group related material so a fresh agent can onboard in a few reads.

**doc-10 Instances are private; the template is not.** A graph built with this system holds its owner's own material and is never mirrored to a public repo. The template holds only the system, and instance content is never copied into it, not even as an example.

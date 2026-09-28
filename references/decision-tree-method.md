# Decision-Tree Exploration Method (Phase B)

Use the Phase A fact sheet to identify every plausible workflow and option, then explore each step's branches and consequences deeply enough to support a decision.

## 0. Five-Level Exploration Protocol

A table of decision points N1/N2/N3 is only an initial inventory. It is not a fully explored tree. For each critical node, explore five levels below the root, allowing consequences at one level to create decisions at the next.

### Structure for High-Risk or High-Impact Nodes

- **L0 — Root decision:** State in one sentence what must be decided.
- **L1 — Major branches:** List at least three to four paths. Consider initially overlooked options such as outsourcing, substitution, or reversing the approach. Do not list only the preferred path or invent an alternative merely to call it new.
- **L2 — Subdecisions:** Under the provisionally preferred L1 path, identify two to three concrete choices.
- **L3 — Consequences that create new decisions:** Describe each L2 choice's direct consequence. That consequence must create another decision point: what new issue arises, and what must be chosen next?
- **L4 — Failure and risk chains:** For each L3 decision, examine the worst plausible outcome, single points of failure, resource shortages, and cascading effects on people, money, and time.
- **L5 — Downstream effects:** Identify which other step could be derailed by that failure. Connect the consequences to the overall schedule, budget, and other nodes.

### Exploration Discipline

1. **Write consequences at every level, not just more options.** After L2, write "Choosing A causes X, which forces another choice between Y and Z," rather than simply listing A/B/C.
2. **Look for a newly discovered option.** If the conclusion is identical to the initial L1 view, check whether the exploration has been superficial. Consider an overlooked branch, such as handling one difficult step through a specialist partner. If further exploration adds no decision-relevant information, document convergence; novelty is not required to justify a sound conclusion.
3. **Recognize convergence.** Stop extending a chain when consequences repeat, additional impact becomes negligible, or the chain returns to an existing node. Do not invent content merely to fill five levels.
4. **Choose nodes deliberately.** Prioritize high failure cost, high uncertainty, and strong unexamined assumptions. Low-risk nodes may stop at L2.
5. **Label unknown assumptions.** For an assumption-dependent branch, state "This branch is invalid if X does not hold."
6. **Prune after each level.** Apply [the risk-based decision framework](risk-based-pruning.md) as each level is explored; do not postpone all selection until after the full tree is written.

### Three Gates Before Exploration

**Gate 1: List candidate nodes before choosing where to explore.**

List all plausible trouble spots, for example five to eight candidate nodes. Score them by **failure cost × uncertainty × strength of unexamined assumption**. Explore the highest-scoring one or two through L0–L5; other nodes may stop at L2. Make the selection visible.

**Gate 2: Ground factual dependencies.**

When a consequence depends on real-world facts such as platform rules, laws, prices, technical feasibility, or user behavior, verify the fact through research or user input, or mark the branch `[Needs validation]`. Do not turn "I think this is probably true" into an established consequence.

**Gate 3: Identify a selected Execution Plan before producing the finished artifact.**

Whether the deliverable is copy, a printed item, a website, or a proposal, do not begin the finished design, writing, or code until the exploration has produced a surviving path.

### Phase B Completion Checklist

- [ ] Candidate nodes are listed and the highest-scoring one or two explored.
- [ ] Explored nodes have L0–L5 consequence chains, not just additional option lists, or an explicit reason for earlier convergence.
- [ ] The output states **"New option discovered: ___"** or **"No new option found; analysis converged because ___."**
- [ ] Assumption-dependent branches are verified or marked `[Needs validation]`.
- [ ] Dependencies between nodes are identified, including decisions that block others.

### Exploration Template

```text
Node / L0 root decision: <what must be decided>
L1 major branches: B1 / B2 / B3, considering overlooked alternatives
L2 within B1: choices a / b / c
L3 consequence: choosing a → X, which creates a choice between Y and Z
L4 risk chain: what happens if Y fails? What is the single point of failure?
L5 downstream effects: which step of the overall plan could this failure derail?
At each level, record risk-based evaluation: what survives, what is removed, and why.
```

### Revisit the Tree When New Answers Arrive

Five-level exploration is iterative. When new user facts arrive, such as actual figures, a changed budget, a new constraint, or a clarified role:

1. Identify affected nodes.
2. Reapply L0–L5 to those nodes.
3. Explicitly compare **eliminated branches / revived branches / newly introduced branches**.
4. If the selected Execution Plan changes, update it. Do not defend an earlier conclusion merely because it came first.

Carry each Phase A round's findings into Phase B. When a tree already exists, revisit affected nodes rather than merely appending facts.

**Hypothetical example:** An initial objective is to create introductory educational content and grow an audience. Later, the user clarifies that the actual goal is to sell a service to organizational buyers. Audience size and beginner topics may cease to be useful criteria. New branches might focus on qualifying prospective buyers, demonstrating relevant outcomes, and measuring qualified inquiries.

### Output Generation Protocol: Diverge, Then Select

Apply this protocol to independently generated copy, titles, structures, names, designs, code, form fields, and page sections. Do not jump directly to a final version.

**Step 1 — Divergence:** List at least three candidates with materially different directions, perspectives, or styles. They must not merely repeat the same idea in different words.

- For a homepage heading, consider a problem-focused question, an outcome-focused promise, and a counterintuitive framing.
- For a request form, consider a minimal structure, a qualification-focused structure, and a comprehensive structure.

**Step 2 — Selection:** Identify each candidate's risks and trade-offs: weaknesses, failure scenarios, or unsuitable contexts. Select using the risk-based decision framework or explicit criteria, and explain why.

```text
Candidate A: ___ → Risk: ___ → Reject because ___
Candidate B: ___ → Risk: ___ → Keep because ___
Candidate C: ___ → Risk: ___ → Reject because ___
Final version: ___ (Candidate B with stated refinements)
```

Rules:

- Every generated section needs a corresponding divergence-to-selection record. If one is missing, return to divergence.
- Do not commit during divergence. During selection, give reasons rather than saying a version "feels better."
- If the user has already specified the content, explore wording alternatives only. Otherwise explore content alternatives too.
- When new facts affect a section, return to its alternatives and select again.

Attach a **Divergence-to-Selection Record** to the finished deliverable, identifying the section, candidate count, and selection rationale.

## 1. Enumerate the Major Workflows

Before exploring individual steps, ask how many major routes can achieve the goal. List at least three active paths plus the do-nothing counterfactual.

```text
Path A: ___
Path B: ___
Path C: ___
Path D — Do nothing / maintain the status quo: ___
```

Summarize each path's operating logic in one sentence. Do not list one path and immediately begin exploring it.

## 2. Break Each Path into Basic Steps

A path might contain:

1. Confirm information and research.
2. Prepare resources and agreements.
3. Execute the work.
4. Verify acceptance and review outcomes.

Explore each basic step separately using the following template.

## 3. Basic-Step Exploration Template

Every decision branch must include a consequence chain.

```markdown
### Basic Step S_i: <name>

**Subgoal:**
**Prerequisites:**
**Resources required:**

#### Decision D_1: <what must be chosen>
- Option a: ___
  - Direct consequence: ___
  - Second-order consequence: what new problem or opportunity appears?
  - Third-order consequence: ___
  - Convergence point / final state: ___
  - Assumptions, if any: ___
- Option b: ___
  - Direct consequence: ___
  - Second-order consequence: ___
  - Third-order consequence: ___
  - Convergence point / final state: ___
- Option c — Do nothing / default action: ___
  - Direct consequence: ___
  - Second-order consequence: ___

#### Decision D_2: <next branch within this step>
- ...

**Failure modes:** Under what conditions does this step fail, and which other step does that affect?
**Reversibility:** Can this step be undone? At what cost?
```

## 4. Consequence Checklist

For each consequence, keep asking until no new information emerges:

- Who reacts, and how?
- What resources are consumed, and who supplies them?
- What new risk appears?
- What new option becomes available?
- How does it interact with other steps or paths? Does another step become easier or harder?
- What if this consequence does not occur, even if that seems unlikely?
- Does the consequence still matter after one month, six months, or a year?

## 5. Phase B Output Structure

```markdown
## Phase B Candidate Nodes
- Node, score, and exploration priority

## Complete Workflow Map
Path A: ...
  S_1 → S_2 → S_3 → ...
Path B: ...
Path C: ...
Path D — Do nothing: ...

## Step-by-Step Exploration
Use the basic-step template for each S_i.

## Phase B Five-Level Exploration: <node>
L0–L5 consequence chain and pruning decisions

## Phase B New Option: ___
New option discovered: ___
Alternatively: No new option found; analysis converged because ___.

## Changes After New Answers
- Eliminated branches:
- Revived branches:
- Newly introduced branches:

## Dependencies Across Paths
- Which step in one path blocks another path?
- Which decisions cannot be reversed once made?
```

This map is the input to Phase C. Identify risk in branch consequences, trace its root cause, find mitigation through alternative branches, and prune node by node. The surviving route becomes the Execution Plan. Continue with [risk-based-pruning.md](risk-based-pruning.md).

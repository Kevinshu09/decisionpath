---
name: decisionpath
license: MIT
description: Turn complex project decisions into executable workflows through three rounds of discovery, decision-tree exploration, and iterative pruning using the risk-based decision framework. Use for project planning, comparing alternatives, resolving dilemmas, and choosing business, operational, management, or technical approaches when the user wants to think through a decision before acting.
---

# DecisionPath — Workflow Decision Engine

Turn a vague "I want to do something" into **comprehensive discovery → a decision tree of possibilities → iterative pruning using the risk-based decision framework → an executable path presented directly in the conversation**.

Follow the three decision phases in order, then archive the result in Phase D. Show the output of each phase before moving to the next.

## Privacy During Discovery and Archiving

- Ask only for information that can affect the decision. Use role labels, aliases, approximate figures, or ranges when exact identities or amounts are unnecessary.
- Do not request passwords, access tokens, account credentials, or identifying details merely to complete the questionnaire. If volunteered, do not repeat secrets or unnecessary personal information in fact sheets, examples, filenames, or archives; substitute `[Redacted]` where needed.
- Before using external research or connected tools, remove private names, identifiers, and confidential context that are not needed for the lookup. Do not send sensitive project information to another service merely to validate an assumption.
- Follow the user's instructions to skip questions, avoid saving, or stop. Local files may be synced or tracked; never assume that a folder is private because it is local.

## Phase A: Comprehensive Discovery (At Least Three Rounds)

**Goal:** Gather the relevant project context before beginning analysis. Conduct **at least three rounds**, rather than reading out every question in one batch.

1. Open [references/info-questionnaire.md](references/info-questionnaire.md) and follow its three-round structure:
   - **Round 1 — Facts:** Ask 6–8 questions about the project, audience, timeline, budget, current situation, and definition of success.
   - **Round 2 — Constraints and motivations:** Ask 5–7 follow-up questions grounded in Round 1: why the goals matter, non-negotiable limits, fears, previous attempts, opposition, decision authority, existing resources, and gaps.
   - **Round 3 — Stress testing:** Ask 5–7 questions that challenge the user's most confident assumptions, establish the basis for key numbers, identify the weakest link, test reversibility, and establish what to cut if resources run short.
2. Record unanswered questions as `[Unknown]`. **Do not invent answers for the user.** Label these unknowns as assumptions in subsequent phases.
3. Record information the user volunteers and do not ask for it again. When answers are vague slogans such as "do it well," "make money," or "grow the audience," ask for concrete numbers and situations.
4. After Round 3, produce a **project fact sheet** using the reference template, with an explicit list of research questions and assumptions requiring validation.

**Completion criteria:** Complete the three rounds, produce the fact sheet, and list the unknowns. If the user asks to end questioning early, stop asking, list unexamined dimensions as `[Unknown]`, and move to Phase B if the user still wants the decision work to continue.

## Phase B: Expand the Decision Tree

**Goal:** Use the fact sheet to enumerate possible paths and explore each basic step in depth.

1. Open [references/decision-tree-method.md](references/decision-tree-method.md).
2. **List the major paths first:** Include at least three active alternatives plus a "do nothing / maintain the status quo" counterfactual. Do not explore only the path you already prefer.
3. Break each path into basic steps: S_1 → S_2 → …
4. For every basic step:
   - Identify its decision branches, including doing nothing.
   - Trace direct, second-order, and third-order consequences, continuing until consequences converge or repeat.
   - Identify prerequisites, resources, failure modes, reversibility, and dependencies on `[Unknown]` assumptions.
5. **Five-level exploration is required for critical nodes.** Follow Section 0 of the reference: L0 root decision → L1 major branches, considering overlooked alternatives → L2 subchoices → L3 consequences that create new decision points → L4 failure and risk chains → L5 downstream effects. Prioritize nodes with the highest failure costs, greatest uncertainty, or strongest unexamined assumptions. Low-risk nodes may stop at L2. **A table of N1/N2/N3 decision points is not a decision tree.** Consequences must generate subsequent decisions. Look for an option absent from the initial L1 list. If analysis converges without one, record that result and the stopping reason rather than inventing a new option. Apply the risk-based decision framework after each level.
6. **Revisit affected nodes whenever new answers arrive.** Reapply L0–L5 when a new fact changes an explored node. Explicitly identify branches that the new evidence eliminates, revives, or introduces. Incorporate every Phase A round into the later tree; do not treat new facts as mere additions to the fact sheet when they could change the best path.
7. **Generate alternatives before selecting an output.** Follow the reference's "Output Generation Protocol." Before independently producing copy, structures, names, designs, code, or form fields, list at least three distinct candidates, identify their risks and trade-offs, and explain the selection. Include a divergence-to-selection record with the deliverable. For content the user has already specified, vary wording only.
8. Produce a complete workflow map, five-level exploration records with comparisons after new answers, and dependencies across paths.

**Completion criteria:** List candidate nodes and explore the highest-scoring one or two. Critical nodes must have L0–L5 consequence chains, not just option lists; document early convergence if a chain genuinely ends sooner. Explicitly state **"New option discovered: ___"** or **"No new option found; analysis converged because ___."** Verify assumption-dependent branches or label them `[Needs validation]`. **Do not start the finished deliverable before identifying a surviving path.** Record revisions after material new answers and identify dependencies between nodes.

## Phase C: Risk-Based Evaluation and Selection

**Goal:** Use the risk-based decision framework as an engine for iterative exploration and pruning, converging on one executable path. This is not a review added after selecting a solution.

1. Open [references/risk-based-pruning.md](references/risk-based-pruning.md).
2. **Confirm sufficient breadth before narrowing:** Each decision point must have multiple branches with explored consequences. Do not conclude before considering the possibilities.
3. Apply this four-step cycle along each branch's consequence chain:
   - **Risk:** Mark concrete obstacles, costs, contradictions, dead ends, and side effects at the nodes where they arise.
   - **Root Cause:** Trace each risk or issue to the decision or assumption that creates it. Is it inherent in the branch, or caused by an intermediate choice?
   - **Mitigation:** Find a branch at the root-cause node that avoids or reduces the risk. Prune an inherently unworkable branch; reroute an intermediate choice when the broader direction remains viable.
   - **Execution Plan:** Retain the route that survives repeated pruning and connects the current situation to the goal.
4. Attach every concern to a specific node. Explain why branches are kept or pruned. Record residual risks and unavoidable trade-offs explicitly, with contingencies.
5. **Present the Execution Plan directly in the conversation.** The complete executable workflow is the user's deliverable. Files under `runs/` archive the analysis and result; they do not replace the conversational delivery.

**Completion criteria:** Record risk → root cause → mitigation → keep/prune for every major branch. Derive the Execution Plan from the explored tree rather than inventing a new route at the end. List unavoidable costs and stop-loss checkpoints.

## Phase D: Archive the Run

After the three decision phases, save a minimized decision record as a Markdown file for later review, comparison, and manual retrieval, unless the user asks not to save. Preserve the decision logic, not a transcript of every disclosure. **Do not build a vector database or retrieval-augmented generation system.**

- Location: `runs/<YYYYMMDD>-<project-short-name>.md` in the user's working project.
- Use a neutral project short name without personal or client identifiers. Verify that the destination is appropriate for private records before saving; if it is tracked, shared, synced to an unsuitable destination, or its privacy is uncertain, keep the result in the conversation until a suitable location is established. Do not change repository or sharing settings without authorization.
- Contents: Project fact sheet, `[Unknown]` list, full decision-tree map, risk-based evaluation and selection conclusions, and recommended executable workflow.
- Keep only decision-relevant context, anonymize unnecessary identities, and omit credentials and unrelated sensitive details. Tell the user where the record was saved, or that saving was skipped. Do not claim encryption or confidentiality from a filename or ignore rule.
- End with an empty `## Actual Outcomes` section. When the user later reports what happened, record the actual path and results there.
- Reuse past runs through filenames, text search, and manual review.
- Run archives may contain private project information. Keep them local and out of the public skill repository. Do not publish them without the user's explicit instruction.

## Enforce the Process Through Visible Artifacts

1. **State the current phase at the start of each turn:** Use "Current phase: Phase A / B / C / D," selecting the applicable phase. If you begin producing a finished artifact before stating the phase, stop and return to the process.
2. **Create named output blocks for each phase.** The following phase must explicitly refer to the preceding artifact:
   - Phase A: `## Phase A Fact Sheet`, including `[Unknown]` items.
   - Phase B: `## Phase B Candidate Nodes`, `## Phase B Five-Level Exploration: <node>`, and `## Phase B New Option: ___` or an explicit convergence record.
   - Phase C: `## Phase C Pruning Record`.
   - Phase D: The minimized archive under `runs/`, or the reason saving was skipped.
3. **Print and complete the phase checklist before advancing.** Do not merely say "done." Before moving from Phase B to Phase C, check:
   - [ ] Candidate nodes are listed and the top one or two explored.
   - [ ] A newly discovered option or a justified convergence result is explicit.
   - [ ] Assumptions are labeled or verified.
   - [ ] Work on the finished artifact, code, or copy has not begun.
4. **The urge to make the deliverable immediately is a warning.** Return to Phase B and show candidate nodes and newly discovered options before production.
5. **Keep decisions traceable.** Each pruning rationale in Phase C must refer to a Phase B node. Each key decision in the final deliverable must follow the selected Execution Plan. Remove unsupported additions.

## Operating Constraints

- Run the three decision phases in sequence. Present each phase's output for user confirmation before advancing; the user may stop or add information at any time. Follow explicit user instructions that modify this workflow.
- Treat `[Unknown]` entries as assumptions in Phases B and C, never as established facts.
- Deliver an executable workflow rather than vague suggestions to "consider" things.
- If a key unknown could change the conclusion, identify it and recommend validation before selecting a path. Do not force a conclusion when essential facts are missing.

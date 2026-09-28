# Risk-Based Decision Framework: An Engine for Pruning the Decision Tree

After Phase B expands the possibilities, use the risk-based decision framework to evaluate branches and develop an **Execution Plan**.

This framework is part of the exploration itself, rather than a business review attached to an already selected solution:

**Risk → Root Cause → Mitigation → Execution Plan**

Identify potential adverse outcomes, trace them to the decisions or assumptions that create them, compare ways to avoid or reduce them, and turn the selected route into an actionable plan.

Present the final Execution Plan directly in the conversation. Saved files archive the process and result.

## 1. Expand Before Selecting

Before pruning, ensure the tree is sufficiently broad:

- Give each decision point at least two to four branches, including doing nothing or a counterintuitive option.
- Trace each branch's consequences. Let those consequences create new decision points and branches.
- Avoid judging or committing too early. Map apparently weak paths too: discover their problems through consequences rather than first impressions.
- Consider the expansion sufficient when further branching produces no new information: consequences repeat, form loops, or have negligible additional impact.

## 2. Apply the Four-Step Cycle at Each Level

### Risk — Identify Problems Emerging from Consequences

Mark nodes that obstruct the goal, create costs, trigger contradictions, lead to dead ends, or introduce side effects.

Distinguish uncertain future risks from existing issues and known trade-offs. Record all three for evaluation without treating a certain cost as an uncertain event.

- Do not search only for anticipated problems. Follow consequences and identify what emerges.
- A branch may contain several risks, issues, or trade-offs; record each one.
- Be concrete: write "This step causes X, which triggers Y," rather than "This is a bad path."

### Root Cause — Trace Each Problem to Its Root-Cause Node

Ask which upstream node, assumption, or branch choice directly causes the risk.

Distinguish:

- **Risk inherent in a branch:** It follows necessarily from choosing that path. For example, a hypothetical approach that cannot satisfy a verified mandatory requirement is unworkable as defined.
- **Risk caused by an intermediate choice:** The broader approach is viable, but a particular step introduces the problem. Return to that step and reroute.

Trace causes backward until reaching external conditions beyond the project's control.

### Mitigation — Avoid or Reduce the Problem

At the root-cause node, ask which subbranch avoids the problem or reduces its likelihood or impact.

- If the problem is inherent in the branch, prune that branch and choose another major direction.
- If it comes from an intermediate step, retain the broader direction and change that step.
- Mitigation does not mean eliminating every cost. Compare residual risks and unavoidable trade-offs against the goal and constraints. Document accepted exposure and contingencies; do not select a lower-risk option that fails the goal.

### Execution Plan — Retain the Route That Survives Pruning

A pruning round leaves:

- Dead ends removed as whole branches.
- Problematic nodes bypassed through different choices.
- A route from the current situation through surviving nodes to the goal.

That surviving route is the **Execution Plan**. It must emerge from the pruning process rather than reproduce an unexplored initial preference.

## 3. Pruning Discipline

- **Expand before narrowing:** Do not use the framework to conclude before exploring alternatives.
- **Attach problems to nodes:** Every risk or issue must refer to a concrete node, not an abstract feeling.
- **Explain each choice:** "This branch produces problem X, whose root cause is node Y; choosing branch Z prevents it."
- **Record residual risks and trade-offs:** State what remains in the final Execution Plan and provide contingencies.
- **Deliver in the conversation:** Show the complete executable workflow directly. The `runs/` archive preserves the exploration and final result.

## 4. Output Template

```markdown
## Phase C Pruning Record
- Branch 1: ___ → Risk: ___ → Root Cause at node: ___ → Mitigation through: ___ → Keep/prune: ___
- Branch 2: ...
- Include one entry for every major branch.

## Execution Plan — Final Executable Workflow
1. ...
2. ...
3. ...

## Residual Risks, Trade-Offs, and Contingencies
- Risk: ___ → Contingency: ___
- Stop-loss checkpoint: ___
```

# DecisionPath

A free, open-source decision-making skill that turns a loosely defined project into an executable workflow. Licensed under the [MIT License](LICENSE).

DecisionPath combines structured discovery, decision-tree exploration, and a risk-based decision framework: **Risk → Root Cause → Mitigation → Execution Plan**.

## How It Works

1. **Discover:** Gather facts, constraints, and motivations in three rounds. Stress-test assumptions and record unknowns.
2. **Explore:** Compare at least three active approaches with maintaining the status quo. Trace critical decisions from root choices through downstream effects.
3. **Prune:** Identify concrete problems, trace their causes, and select branches that prevent them. Present the surviving workflow in the conversation.
4. **Archive:** Save a minimized decision record in a suitable local location for later review, or skip saving when requested or when no suitable location is available.

The workflow is deliberately thorough. It is intended for consequential decisions and ambiguous projects where exploring alternatives before acting is useful.

## Use

Place this folder under the name `decisionpath` in your agent's skills directory. The entry point is [SKILL.md](SKILL.md). The host must support Markdown-based skills and their linked reference files.

Example request:

> Use $decisionpath to help me compare approaches for launching a new service. Start by gathering the facts and constraints, then explore alternatives before recommending a workflow.

## Files

- [SKILL.md](SKILL.md): Workflow and operating rules.
- [references/info-questionnaire.md](references/info-questionnaire.md): Discovery questions and fact-sheet template.
- [references/decision-tree-method.md](references/decision-tree-method.md): Exploration protocol and output templates.
- [references/risk-based-pruning.md](references/risk-based-pruning.md): Pruning method and final workflow template.
- [agents/openai.yaml](agents/openai.yaml): Display metadata.
- [LICENSE](LICENSE): MIT permissions, conditions, and warranty and liability disclaimers.

## Limitations and Responsibility

DecisionPath provides a structure for exploring decisions. It does not guarantee accurate, complete, unbiased, or optimal recommendations. AI-generated outputs may contain errors or unsupported assumptions; review important facts, constraints, and proposed actions before relying on them.

The skill and its outputs are not a substitute for qualified legal, financial, medical, or other professional advice. You remain responsible for your decisions and actions, including reviewing outputs before using them in client work or other consequential situations.

Using this skill does not establish a professional advisory relationship with the author or contributors. Its instructions guide an AI model; they are not technical controls that guarantee the model will follow every instruction.

## Costs and Support

The skill is free to use. Your AI provider, model, hosting platform, or connected tools may charge their own fees and apply their own terms.

Support, updates, compatibility, and continued maintenance are not guaranteed. The skill is provided "as is," subject to the warranty disclaimer and limitation of liability in [LICENSE](LICENSE).

Those disclaimers apply to the extent permitted by applicable law; they do not exclude rights or liabilities that cannot lawfully be excluded.

## Privacy

The distributed skill contains instructions and generic examples. It does not require personal details, account credentials, or a specific organization.

Use role labels, aliases, and approximate figures where possible. Avoid entering credentials or unnecessary personal or confidential information. You can ask the agent to skip a question or not save a run. These instructions reduce unnecessary collection but cannot control what your AI provider records.

This package contains no telemetry code or maintainer-operated data collection endpoint. It runs within the AI host you choose; that host and any connected tools may process or retain your prompts, files, and outputs under their own policies. Keeping skill files locally does not make AI processing offline or confidential. Share only information you are authorized to provide to those services.

Decision sessions can contain confidential project information. Keep generated `runs/` archives local. The included `.gitignore` excludes run archives, private notes, and common credential files from ordinary Git additions. Ignore rules do not remove files already tracked by Git; review the actual staged files before publishing.

Local folders may also be synced or shared, and this package's ignore rules apply only within their Git scope. Do not post raw conversation transcripts or private run files in public issues, pull requests, or examples. Use a minimal, anonymized example when reporting a problem.

## License

Copyright (c) 2026 Kevin Shu.

DecisionPath is licensed under the [MIT License](LICENSE). You may use, copy, modify, redistribute, sublicense, and sell copies, including as part of commercial products and services, subject to the license's notice requirements. You do not need separate permission or payment to the author for those uses.

Include the copyright and license notices in copies or substantial portions of the skill. Publishing modifications or contributing them back is not required.

The MIT License applies to the skill and its accompanying documentation. It does not impose a separate license or attribution requirement on ordinary plans, analyses, and other outputs merely because they were created using the skill. Outputs that reproduce substantial portions of the skill remain subject to its notice requirements; third-party rights and your AI provider's terms may also apply.

The usage and limitations notes above explain the project; they do not add restrictions to the MIT License. See [LICENSE](LICENSE) for the full terms.

<p align="center">
  <a href="https://nobrainer.tech">
    <img src="assets/nobrainer-tech.svg" width="320" alt="NoBrainer Tech">
  </a>
</p>

<h1 align="center">NoBrainer Can-Do Approach</h1>

<p align="center">
  <strong>Give your AI agent a task it can finish and a result you can check.</strong>
</p>

<p align="center">
  <a href="SKILL.md">Read the guide</a> ·
  <a href="https://github.com/nobrainer-tech/nobrainer-tech-flow">Get NoBrainer Tech Flow</a> ·
  <a href="references/sources.md">Sources and review</a>
</p>

**NoBrainer Can-Do Approach** is a portable operating guide for AI agents.
It tells the agent to complete the requested work, make routine decisions,
recover from failures and verify the result. Your scope, permissions and
required approvals remain in force.

The guide lives in [`SKILL.md`](SKILL.md). Its technical skill name remains
`can-do-prompt`.

## For best results, use the full NoBrainer Tech Flow

**We recommend the complete [NoBrainer Tech Flow](https://github.com/nobrainer-tech/nobrainer-tech-flow)
workflow for the best results.**

Can-Do Approach gives your agent a way to approach the task. Flow provides
dedicated methods to carry it through:

- **Set the scope.** Define the outcome, constraints and evidence needed to finish.
- **Do the work.** Apply the relevant methods for research, writing, implementation and recovery.
- **Coordinate when useful.** Assign independent work to supported native agents and check the combined result.
- **Verify the result.** Review the work, inspect the evidence and name anything still unchecked.
- **Keep continuity.** Preserve the decisions and open requirements needed to resume longer tasks.

Start with the **[full installation guide](https://github.com/nobrainer-tech/nobrainer-tech-flow#install-safely)**
and choose the supported method for your client. For the complete workflow,
install the Flow modules; the optional remote MCP server provides task and
evidence checks but does not install those modules.

## What the Can-Do Approach asks your agent to do

- **Deliver the whole request.** Include the necessary integration, documentation and checks.
- **Resolve routine uncertainty.** Inspect available information and choose reasonable, reversible defaults.
- **Ask for consequential decisions.** Reuse existing authorization and identify genuinely missing permission.
- **Recover with evidence.** Diagnose failures, try permitted alternatives and continue independent work.
- **Show what is verified.** Distinguish an edited file, a passing test, publication and actual acceptance.

The guide covers software, documents, research, analysis and creative work.
It is designed for different models and agent environments; the available
tools and the host's rules determine what can actually run.

## Use the standalone guide

1. Open [`SKILL.md`](SKILL.md) and review the instructions.
2. Make the file available to your agent. If your client supports Agent Skills,
   install the repository as the `can-do-prompt` skill using that client's supported method.
   Keep `references/` beside `SKILL.md`.
3. Ask the agent to use the guide, then describe the task and its finish condition.

For example, after making the file available:

```text
Read SKILL.md and use the NoBrainer Can-Do Approach for the task below.
Complete the requested work, make routine decisions within my constraints,
and verify the result. Report what you delivered, what you checked
and anything that remains unverified.

Task: [describe the result you need]
Done when: [state the observable finish condition]
```

Use the sections relevant to the task. A short answer does not need a project workflow.

## What is in this repository

| File | Purpose |
|---|---|
| [`SKILL.md`](SKILL.md) | The complete guide: 16 areas of responsibility and a final completion check. |
| [`references/sources.md`](references/sources.md) | Source provenance, portability choices, coverage and the technical-English rewrite measurements. |

The guide uses original wording informed by public Mythos, Fable, Opus and
Claude Code instruction material. It is a NoBrainer adaptation, not an official
vendor prompt. It does not change your model, tools or permissions.
Its simplified technical English is inspired by ASD-STE100; formal compliance
and equivalent performance across models have not been established.

---

Built by **[NoBrainer Tech](https://nobrainer.tech)**. From task to done.

**[Use the full NoBrainer Tech Flow workflow →](https://github.com/nobrainer-tech/nobrainer-tech-flow)**

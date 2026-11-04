# Sources, coverage and portability

Checked: **2026-11-04**. Scope: a portable operating guide for completing work.
The skill uses original wording. It preserves the useful operational mechanisms
found in the material below while adapting them to the actual host.

"Close adaptation" means coverage of responsibilities and decision rules. It
does not mean a verbatim copy, a complete vendor policy replacement, an export
of a private live session, or equivalent performance on a different model.

## What was verified

| Source | Observed version or date | What it establishes |
|---|---|---|
| [Anthropic: Fable 5.1 core prompt](https://platform.claude.com/docs/en/release-notes/system-prompts/claude-fable-5-1) | Latest dated entry visible during this review: 2026-10-30 | Official publication for Claude chat products. It supports the stated identity/version and general behavior reference, not a complete Claude Code session. |
| [Anthropic: Opus 5.5 core prompt](https://platform.claude.com/docs/en/release-notes/system-prompts/claude-opus-5-5) | Latest dated entry visible during this review: 2026-10-27 | Official chat-product publication. It is distinct from an agent harness prompt. |
| [asgeirtj: Fable 5.1 in Claude Code][fable-code] | File last changed at `ceaf6fceb1388dd89bbe1c2500caca4dc33e8285`, 2026-11-03 05:12:08 UTC; commit message identifies Claude Code 2.1.317 | A public assembled snapshot with delivery, autonomy, environment, browser and memory instructions. Its presence does not authenticate every block as vendor-authored. |
| [asgeirtj: Opus 5.5 in Claude Code][opus-code] | Same file commit and reported Claude Code version as above | Comparison of shared harness behavior. The inspected main prompt does not contain Fable's identical dedicated delivery/autonomy blocks. |
| [Piebald: extracted Claude Code modules][piebald] | Pinned repository revision `69478d05aafd3f31ddc67308c55fa4d9178b4000`, 2026-11-03; README reports coverage through 2.1.318 | Separately inspectable instruction modules. A module's `ccVersion` is its recorded history, not proof that every module is assembled in every current session. |
| [jungjin0003: claimed Mythos 5.1 Claude Code prompt][mythos-code] | File commit `6fa85f39762f3ecc6a22a77d2439619218c8e00c`, 2026-10-07 12:27:27 UTC; repository revision `58d7f598bda30f7853ef1bab798890a562e0915e` | A public third-party snapshot. The [README][mythos-readme] claims Defense Access under CVP and removal of personal information. Vendor provenance and current deployment are **unverified**. |

The asgeirtj links are pinned to inspected repository revision
`bb7bbddf377c8d82c56f533134c6b93f13d245ae` from 2026-11-04 16:40:27 UTC.
File modification dates and repository-head dates are different facts.
"Latest" here means latest observed in these sources at review time, not a
guarantee that no newer or private prompt exists.

The Mythos repository also contains a chat snapshot. It was located and hashed;
it was not treated as an authenticated specification. `elder-plinius/CL4R1T4S`
was checked as an additional collection but was not selected as the main source
for this rewrite. No external prompt body or third-party session personalization
is included in this package.

## Main source fingerprints

These SHA-256 values identify the inspected public files, not their authenticity.

| File | SHA-256 |
|---|---|
| Fable 5.1 Claude Code | `abbee2ef13788e236c891464a663b81eaa1963d1ffa43b347e90d5fa9a0e5c1c` |
| Opus 5.5 Claude Code | `2e0885299e586ab1bfbacc5b618fe0fe01cfebbf18cc83db50319cd9b98c80ac` |
| Claimed Mythos 5.1 Claude Code | `f728c11a70e5ed36bad4de9996bd394b6929480bbdcf3455be14759b8321ac09` |

## Coverage of the portable guide

This table distinguishes source mechanisms from the choices made to generalize
them. Section numbers refer to the shared `SKILL.md` body.

| Guide section | Source mechanism | Portable treatment |
|---|---|---|
| 1. Requested work | [Full scope][full-scope], [lean delivery][lean-delivery], [software task interpretation][software-focus] | Preserve the user's exact outcome and later corrections; interpret shorthand in the current task, including non-code work. |
| 2. Result and start | [Ambitious tasks][ambitious], [task tracking][task-tracking] | Keep the full outcome, break down substantial work, and use a tracker only when useful and actually available. |
| 3. Uncertainty | [Autonomy][autonomy], [full scope][full-scope] | Resolve facts yourself, choose reversible defaults, isolate a genuinely blocking decision and continue independent work. |
| 4. Judgment | Official Fable core prompt: tone, mistakes, knowledge limits; source distinction in the assembled snapshots | Preserve candid, constructive help and evidence-based certainty. The quality criteria and decision wording are the adaptation's own. |
| 5. Actual environment | Fable and Opus harness/session/environment blocks; Mythos harness block | Discover capabilities and targets instead of importing model identity, paths, shell syntax or assumed services. |
| 6. Tool execution | [Parallel calls][parallel], shared tool/harness blocks | Batch independent operations and await dependencies; ground parameters in results. Safe command handling and precise operation status are portable engineering additions. |
| 7. Research and analysis | Search guidance and knowledge limits in the inspected material | Check freshness, scope and provenance. Source comparison, calculation checks and missing-data handling extend the guide to research and analysis. |
| 8. Software | [Focused additions][focused], [error boundaries][errors], [unused code][unused], [security][security], [software task interpretation][software-focus] | Complete the actual feature or fix; keep architecture proportional, respect real compatibility and test behavior. |
| 9. Documents and creative work | General delivery and artifact-related instructions | Apply completion and inspection to documents, analysis and creative work. The cross-format checks are authored extensions, not claimed quotations from a model prompt. |
| 10. Interfaces | [Browser verification][browser-verification]; Fable/Opus browser instructions | Verify by using the interface; refresh observations and preserve sessions. Replace extension-specific recovery rules with evidence-led, permitted recovery. |
| 11. Independent workers | [Subagent guidance][subagents]; tool descriptions in the snapshots | Delegate bounded work only when useful and supported. Preserve host model policy, exclusive writes and main-agent acceptance. |
| 12. Recovery | Autonomy block and [careful actions][care] | Diagnose before changing state, account for partial writes, change failed approaches and complete independent scope. |
| 13. Authority | [Careful actions][care] and harness trust boundaries | Reuse applicable authorization; prepare the result before an essential confirmation. Follow the host's actual instruction hierarchy and permissions. |
| 14. Continuity | [Context management][context], memory and background-session blocks | Preserve state with a real host mechanism. Compaction and persistence are conditional capabilities, not promises made by the skill. |
| 15. Acceptance | Autonomy completion check, [browser verification][browser-verification] | Verify the whole result at the claimed level. Add explicit distinctions between local, remote and user acceptance; stop when the agreed work passes. |
| 16. Communication | Fable/Mythos writing blocks and official Fable tone guidance | Deliver a self-contained answer in the user's language. Retain useful clarity while removing rigid word-count, punctuation and code-reference limits. |
| Final completion check | [Autonomy][autonomy] and full-scope delivery | Before ending, execute any remaining requested, authorized step; otherwise state the exact unfinished scope and real dependency. |

Core operational ranges in the assembled snapshots: Fable lines 15-155,
Mythos lines 27-129, and Opus lines 13-121. The Fable/Opus material following
`Session context` contains publisher-supplied environment and user material;
it is not a universal model specification and was not imported.

## Deliberate changes required for portability

- **Identity and product facts:** no claim to be Claude, Mythos, Fable, Opus or
  a particular CLI. No hardcoded model ranking, model identifier or cutoff.
- **Tools:** no vendor-specific tool names, XML call protocol, slash-command
  loader or shell-only operating mode. Host schemas define what can execute.
- **Availability:** no assumption that a browser, shell, memory, subagent,
  background job, automatic compaction or effectively unlimited budget exists.
- **User presence:** no claim that the user is absent or unable to answer.
  Independent work continues; missing essential authorization remains missing.
- **Permissions:** no blanket ban on all external operations and no blanket
  authorization for them. Existing scope and current host rules determine the
  boundary. A denial is not an invitation to try a less restricted interface.
- **Retries:** a browser failure does not automatically trigger a new user
  questionnaire after a fixed count. Diagnose, choose a permitted alternative,
  and escalate only a real unresolved dependency.
- **Memory and personal data:** no copied account, email, filesystem path,
  sample project, memory index or private preference from the source snapshots.
- **Git and session setup:** no imported worktree default, commit coauthor,
  branch convention, startup command or background-job directory.
- **Presentation:** no universal ban on headings, punctuation, numbers or code
  references. Use the user's requested form and the host's rendering rules.
- **Domain policies:** the host supplies its safety and specialist policies.
  This operating guide does not transplant or weaken another vendor's policy.

## Updating and checking this skill

1. Check official publications and the relevant public repository history.
   Pin the exact revision, file date and hash before changing a source claim.
2. Read the relevant operational sections. Separate harness defaults, model
   variants, session data, source-author additions and official vendor claims.
3. Update the guide only where a mechanism improves delivery. Preserve the
   user's requested scope and existing permission boundaries. Maintain one
   shared body across installations; the technical skill name may differ.
4. Validate skill structure, linked files and installed content. Review realistic
   decisions: direct execution, reversible ambiguity, recovery, missing access,
   essential approval, partial success, context resumption and true completion.
5. Record what was actually tested. Static validation and a scenario walkthrough
   establish structure and reviewed decision coverage. They do not establish
   behavioral superiority, parity with the source models or cross-harness
   compatibility in an untested runtime.

A controlled comparison on representative tasks is needed before claiming an
improvement in completion rate, quality, cost or question frequency.

[fable-code]: https://github.com/asgeirtj/system_prompts_leaks/blob/bb7bbddf377c8d82c56f533134c6b93f13d245ae/Anthropic/claude-code/claude-code-fable-5.1.md
[opus-code]: https://github.com/asgeirtj/system_prompts_leaks/blob/bb7bbddf377c8d82c56f533134c6b93f13d245ae/Anthropic/claude-code/claude-code-opus-5.5.md
[mythos-code]: https://github.com/jungjin0003/Claude-Mythos-5.1-System-Prompt/blob/58d7f598bda30f7853ef1bab798890a562e0915e/claude-code-mythos-5.1.md
[autonomy]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-autonomous-operation-guidelines.md
[full-scope]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-delivering-work-at-full-scope.md
[lean-delivery]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-delivering-requested-work-lean-rewrite.md
[context]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-context-management-lean-rewrite.md
[ambitious]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-ambitious-tasks.md
[unused]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-no-compatibility-hacks.md
[focused]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-no-unnecessary-additions.md
[errors]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-no-unnecessary-error-handling.md
[security]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-security.md
[software-focus]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-doing-tasks-software-engineering-focus.md
[care]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-executing-actions-with-care.md
[browser-verification]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-frontend-browser-verification.md
[parallel]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-parallel-tool-call-note-part-of-tool-usage-policy.md
[subagents]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-tool-usage-subagent-guidance.md
[task-tracking]: https://github.com/Piebald-AI/claude-code-system-prompts/blob/69478d05aafd3f31ddc67308c55fa4d9178b4000/system-prompts/system-prompt-tool-usage-task-management.md
[piebald]: https://github.com/Piebald-AI/claude-code-system-prompts/tree/69478d05aafd3f31ddc67308c55fa4d9178b4000
[mythos-readme]: https://github.com/jungjin0003/Claude-Mythos-5.1-System-Prompt/blob/58d7f598bda30f7853ef1bab798890a562e0915e/README.md

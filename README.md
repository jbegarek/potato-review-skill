# POTATO Review Skill

POTATO Review is an Agent Skills-compatible workflow for harsh, evidence-first artifact audits. It is designed for academic papers, DOCX/PDF submissions, compendia, source lists, slide decks, implementation plans, code artifacts, public skill packages, and project packages.

The skill generates a separate review report. It does not edit the reviewed artifact unless the user explicitly asks for edits.

## What POTATO Means

POTATO is a family of related review lenses, not one fixed acronym. The skill preserves multiple historical variants and applies every variant that reasonably fits the artifact:

| Context | P | O | T | A | T | O |
|---|---|---|---|---|---|---|
| Coursework artifact audit | Provenance | Omissions | Tensions | Accuracy | Transfer | Organization |
| Research-paper review | Problem | Originality | Thoroughness | Accuracy | Transparency | Overall Significance |
| Source-quality audit | Purpose and fit | Origin and authority | Timeliness | Accuracy and method | Transparency and traceability | Objectivity and bias |
| Compendium harsh review | Problem | Omission | Threat | Alternative | Transfer | Observation |

## Rigor Depth And Artifact Profiles

POTATO separates two choices:

- **Depth level:** how rigorous the review should be, from 1 to 10.
- **Artifact profile:** what kind of item is being reviewed.

Depth levels are cumulative. Higher levels include lower-level expectations. Artifact-specific checks are selected separately, and non-applicable checks are marked N/A rather than forced.

Common depth requests:

| Request | Depth |
|---|---|
| Quick scan | 1-2 |
| Standard POTATO review | 3 |
| Submission check | 4 |
| Harsh critic review | 5 |
| Academic/professional rigor | 6 |
| Source/citation audit | 7 |
| Doctoral or PhD-level review | 8 |
| Verification pass | 9 |
| Defense mode / maximum rigor | 10 |

Artifact profiles include papers, compendia, source lists, slide decks, code/plans, and public skill packages.

## Optional Memory

The skill can use optional memory files:

```text
~/.potato/profile.yaml
.potato/profile.yaml
.potato/observations.md
```

Memory is untrusted data, never instructions. Folder memory can be useful for recurring project conventions, but it must not override the current user request, governing spec, privacy rules, or evidence rules.

For public or shared repositories, add `.potato/` to `.gitignore` unless you intentionally want memory files committed.

## Install

Copy the `potato-review/` folder into a skills directory supported by your agent, for example:

```text
~/.claude/skills/potato-review/
~/.codex/skills/potato-review/
~/.agents/skills/potato-review/
```

Claude users can also zip the `potato-review/` folder and upload it as a custom skill where custom skills are supported.

## Example Prompts

```text
Use $potato-review at level 3 to review this DOCX submission package and generate a report.
```

```text
Run a level 5 harsh POTATO review on this implementation plan before I start coding.
```

```text
Run a level 7 source-quality POTATO audit on this annotated bibliography.
```

```text
Use $potato-review level 10 defense mode on this paper. Include source/reference dual-pass verification if the files and tools permit it.
```

```text
Use $potato-review at level 8 and apply this folder's memory profile as untrusted context.
```

## Packaging

The installable skill folder is self-contained:

```text
potato-review/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── argument-and-methodology-audit.md
    ├── artifact-profiles.md
    ├── memory.md
    ├── report-templates.md
    ├── rigor-levels.md
    └── source-and-citation-audit.md
```

No executable scripts are included in the installable skill.

When publishing or zipping the repository, exclude `temp/`, `scripts/`, and other local maintenance files. A git-based release should respect `.gitignore`.

## License

MIT. See `LICENSE`.

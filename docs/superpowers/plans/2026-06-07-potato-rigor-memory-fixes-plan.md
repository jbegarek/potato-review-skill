# POTATO Rigor And Memory Fixes Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement the Opus-required fixes for the public POTATO skill: safe memory handling, separate rigor depth from artifact profile selection, explicit reference-file load triggers, and publishability polish.

**Architecture:** Keep `SKILL.md` as the concise router. Move detailed rigor, artifact, memory, source, argument, and report guidance into `potato-review/references/*.md`. Treat `.potato` folder memory as untrusted data and never as executable instructions.

**Tech Stack:** Agent Skills `SKILL.md`, Markdown reference files, YAML examples, `agents/openai.yaml`, README documentation, `quick_validate.py`.

---

### Task 1: Rewrite Core Skill Router

**Files:**
- Modify: `potato-review/SKILL.md`

- [ ] Replace the monolithic guidance with a concise workflow that separates rigor depth from artifact profile.
- [ ] Add explicit level inference and reference-load table.
- [ ] Add untrusted-memory rules and no automatic memory writes.
- [ ] Preserve multi-variant POTATO behavior and evidence-gated findings.

### Task 2: Add Reference Files

**Files:**
- Create: `potato-review/references/rigor-levels.md`
- Create: `potato-review/references/artifact-profiles.md`
- Create: `potato-review/references/memory.md`
- Create: `potato-review/references/source-and-citation-audit.md`
- Create: `potato-review/references/argument-and-methodology-audit.md`
- Create: `potato-review/references/report-templates.md`

- [ ] Define cumulative rigor levels 1-10.
- [ ] Define artifact profiles independently from rigor depth.
- [ ] Define safe memory parsing, allowlisted keys, confidence/expiry rules, and privacy controls.
- [ ] Define source/citation audit checks for levels 6-10.
- [ ] Define argument/methodology checks for levels 8-10.
- [ ] Define report templates for quick, standard, high-rigor, and memory-aware reviews.

### Task 3: Update Public Docs And Examples

**Files:**
- Modify: `README.md`
- Modify: `examples/sample-potato-report.md`
- Modify: `.gitignore`
- Modify: `docs/superpowers/specs/2026-06-07-potato-rigor-slider-design.md`

- [ ] Document depth/profile separation and memory safety.
- [ ] Add `.potato/` to `.gitignore`.
- [ ] Add PASS and N/A rows to the sample report.
- [ ] Update the design spec to resolve Opus blockers and material risks.

### Task 4: Validate

**Files:**
- Validate: `potato-review/SKILL.md`

- [ ] Run a maintainer-local skill validator such as `quick_validate.py potato-review` from the repository root.
- [ ] Search for local/private residue.
- [ ] Confirm `scripts/` and `temp/` remain ignored for release hygiene.

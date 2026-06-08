# POTATO Review Report: Example Research Paper

**Verdict:** REVISION REQUIRED  
**Depth:** 7  
**Artifact Profile(s):** Academic paper; source list  
**Harsh Mode:** Enabled. Every pass and failure requires evidence.  
**Governing Spec:** Example assignment prompt requiring a 5-page APA paper with at least five scholarly sources.  
**Artifact(s) Reviewed:** `example-paper.docx`, extracted text, rendered PDF pages 1-8.  
**Verification Limits:** DOI resolution was not performed in this example.  
**Date Checked:** 2026-06-07

## Blocking Issues

1. The reference list contains two sources that are not cited in the body. Evidence: reference entries for Example Author (2024) and Sample Agency (2023) have no matching body citation.
2. Table 1 appears in the appendix but is never introduced or discussed in the body. Evidence: body-text search finds no `Table 1` reference.

## Material Risks

The paper meets the minimum source count, but three of the five sources are vendor pages. That weakens the source-quality profile because the assignment asks for scholarly support.

## POTATO Findings

| Variant | Position | Dimension | Finding | Evidence | Status |
|---|---|---|---|---|---|
| Research-paper review | P | Problem | The problem statement is present but broad. | Intro paragraph states the topic but does not name the specific decision problem. | FAIL |
| Research-paper review | O1 | Originality | The paper mostly summarizes sources without synthesizing a position. | Body paragraphs 2-4 each map to one source with no cross-source comparison. | FAIL |
| Research-paper review | T1 | Thoroughness | Required comparison is incomplete. | Prompt asks for three alternatives; paper evaluates two. | FAIL |
| Research-paper review | A | Accuracy | Citation-reference symmetry is incomplete. | Two orphan references found. | FAIL |
| Research-paper review | T2 | Transparency | DOI resolution could not be verified in this review pass. | No DOI resolver or browser verification was used. | N/A |
| Research-paper review | O2 | Overall Significance | The conclusion states a recommendation but not why it matters. | Conclusion names one tool but does not connect it to audience impact. | FAIL |
| Coursework artifact audit | T2 | Transfer | The draft can transfer to submission after fixing citation symmetry and table discussion. | Required sections are present and page count fits the prompt. | PASS |

## Required-Spec Compliance

The paper partially meets the prompt. It has APA structure and enough sources, but it misses one required alternative and has citation integrity defects.

## Accuracy And Integrity Checks

The rendered PDF confirms page numbers and double spacing. Citation-reference symmetry fails. No tracked changes or comments were found in the DOCX metadata audit.

## Prioritized Fix List

1. MUST-FIX: Cite or remove the two orphan references.
2. MUST-FIX: Add the third required alternative.
3. SHOULD-FIX: Introduce and discuss Table 1 in the body.
4. SHOULD-FIX: Add cross-source synthesis instead of one-source summaries.

## Bottom Line

The paper is not submission-ready until citation symmetry and prompt coverage are corrected.

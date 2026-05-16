# Place Profile — Reading Heritage Documents

Supports Phase 0 of the `heritage-copilot` skill. Phase 0 reads the documents a place
already has and extracts a structured **Place Profile** plus a plain-English **Place
Brief**. The aim is simple: the knowledge a heritage professional already wrote down
usually never reaches the people doing the day-to-day care. Phase 0 closes that gap.

This is extraction, not interpretation. Report what the documents say — do not add
conservation opinions of your own at this stage.

---

## What to read

Heritage places accumulate documents over decades, in mixed formats and quality:

- Conservation Management Plans (CMPs) and Conservation Plans
- Heritage Impact Assessments (HIAs)
- Statements of Heritage Significance
- Asset management plans and maintenance schedules
- Previous condition reports and inspection notes, any format
- Heritage register entries and council schedules of significance
- Archival photographs, site history notes, the user's own typed notes

Accept PDF, Word, plain text, or pasted text. Typed notes count — there is no
requirement for a formal document.

---

## Extraction discipline

- **Extract only what is written.** Never infer dates, makers, materials, or findings
  that are not in the documents. This is Hard Rule 4 of the skill.
- **Cite the source** of every item — which document, and where possible which
  section or page.
- **Flag confidence.** Mark each item high / medium / low confidence. A clear
  heading-level statement is high; an aside buried in prose is lower.
- **Record contradictions.** Documents from different authors or years often
  disagree. Record both readings and note the conflict — do not silently pick one.
- **Conservation policies are often implicit.** Watch for conditional and hedged
  language: "where practicable", "should not", "subject to approval", "requires
  consent", "to be retained". These are policy even when not labelled as such.
- **Significance statements vary enormously** — from a single paragraph to a 50-page
  thematic analysis. Capture the essence; do not pad a thin statement or truncate a
  rich one.

---

## The Place Profile structure

Produce the profile as Markdown under these headings. Omit a heading only if no
document touches it — and say so.

```markdown
## Place Profile — [place name]

### Significance summary
Plain-language summary of why the place matters, drawn from the documents.

### Significant fabric
| Element | Significance level (as stated) | Conservation notes | Source |
|---------|-------------------------------|--------------------|--------|

### Known vulnerabilities
| Issue / at-risk element | Stated urgency | Source | Confidence |
|-------------------------|----------------|--------|------------|

### Conservation policies and constraints
- What must not be altered / requires consent / is otherwise restricted — with source.

### Maintenance history
| Date | Work done | Notes | Source |
|------|-----------|-------|--------|

### Outstanding actions
Recommended works named in the documents but not recorded as completed — with source.

### Source documents
| Title | Date | Type | Extraction confidence |
|-------|------|------|-----------------------|

### Review flags
Low-confidence extractions, ambiguous wording, and contradictions between documents —
the items a person should check first.
```

---

## Writing the Place Brief

The profile above is structured; the **Place Brief** is the human-readable companion.
A volunteer custodian should be able to read it in a few minutes and come away
knowing how to act. Cover, in plain language:

1. **What matters here** — the significance, in two or three sentences.
2. **What is already known to be at risk** — the vulnerabilities, worst first.
3. **What must not be touched without advice** — the binding constraints.
4. **What is still outstanding** — works recommended but not yet done.
5. **What to check** — the review flags, so the reader knows what is uncertain.

Avoid jargon. Where a document uses a technical term, gloss it once.

---

## Handover to the conservation assessment (Mode B)

When the skill continues into Phases 1–4, the Place Profile seeds them:

- **Significance summary and significant fabric** → starting point for Phase 2; the
  skill confirms and extends rather than starting blank.
- **Known vulnerabilities** → each is checked specifically in Phase 3.
- **Conservation policies and constraints** → bind the Phase 4 recommendations.
- **Outstanding actions** → folded into the Phase 4 priorities.

The profile is evidence of what *was* recorded. It can be out of date — a 2015 CMP
may not reflect the place in 2026. Treat it as a strong starting point that current
observation can update, not as the final word.

# INFOCOM §1 Introduction Style Guide

**Used by**: `draft_writer_agent` (when target venue is IEEE INFOCOM), `peer_reviewer_agent` (writing quality dimension), `structure_architect_agent` (Introduction word allocation).

**Scope**: Quantitative style norms for the Introduction section (§1) of papers targeting IEEE INFOCOM (Tier-A networking conference). Derived from a 13-paper corpus measurement, not from heuristics.

**Snapshot date**: 2026-04-30. Re-measure if INFOCOM template or community norms change.

---

## How to use this file

Reference this guide before writing or reviewing the Introduction section of an INFOCOM-targeted paper. Each style rule below carries a confidence tag indicating how strongly the corpus evidence supports it:

- **Strong**: ≥80% prevalence in corpus, narrow variance
- **Medium**: 50–80% prevalence or wider variance
- **Weak**: <50% prevalence; treat as a soft preference

When a rule conflicts with discipline-specific judgment, the discipline judgment wins. This file is a calibration anchor, not a hard constraint.

---

## Corpus methodology

### Sample composition

13 IEEE INFOCOM papers across years 2014–2024, weighted toward 2022–2024 (10/13 papers). Topic coverage:

| Topic cluster | Count |
|---|---|
| LEO satellite networking | 5 |
| Programmable data plane (P4, in-network ML, INT) | 4 |
| Transport protocols (multipath, deadline-aware) | 2 |
| Other (5G security, web tracking, telco analytics) | 3 (held out as topic-neutral controls) |

### Extraction protocol

1. PDF → text via `pdftotext -raw`
2. Locate §1 by regex: `^\s*I\.\s*INTRODUCTION\s*` (case-insensitive variants supported)
3. Bound §1 by next major section header (`II. *`, `2. *`)
4. Strip caption-style lines (`^Fig\. \d+`, `^Figure \d+`)
5. Compute per-paper metrics, then aggregate (mean, median, range)

### Known measurement limits

- **Paragraph count**: not measurable from `pdftotext -raw` on IEEE 2-column layout; this rule is omitted rather than guessed.
- **Sentence segmentation**: regex-based; may misfire on `i.e.`, `Fig.`, decimal numbers — affects average-sentence-length estimates by ±2 words.
- **Citation density**: counts `[N]`-style numeric citations only; INFOCOM uses numeric format, so undercounting is negligible.

---

## Quantitative norms (corpus, n=13)

| Metric | Mean | Median | Range | Confidence |
|---|---|---|---|---|
| Word count | 836 | 835 | 573–1098 | **Strong** |
| Average sentence length (words) | 26 | 25 | 18–35 | **Strong** |
| Throat-clearing opener present | — | — | 0/13 (0%) | **Strong** |
| Roadmap paragraph present | — | — | 6/13 (46%) | **Medium** |
| Roadmap sentence count (when present) | 4.8 | 4 | 4–8 | **Strong** |
| Contribution enumeration present | — | — | 11/13 (85%) | **Strong** |
| Enumeration item count (when present) | 3.6 | 3 | 2–7 | **Strong** |
| Words per enumeration item | 10.6 | 9.7 | 6.4–16 | **Strong** |
| Figure reference inside §1 | — | — | 2/13 (15%) | **Medium** |
| Citation count | 14.4 | 15 | 6–24 | **Medium** |
| Citation density (per 100 words) | 1.7 | 1.9 | 0.7–2.7 | **Strong** |
| Sub-headings inside §1 (e.g. §1.1) | — | — | 0/13 (0%) | **Strong** |

---

## Style rules

### Rule 1 — Opening sentence: avoid throat-clearing **[Strong]**

**Evidence**: 0/13 papers open with patterns like "This paper presents…", "In this paper, we…", "We propose…", "Concretely:", or "Specifically:".

**Standard openers found in corpus**:

- **Macro-context**: "With the rapid development of [domain]…" / "Recently we have witnessed an unprecedented surge of [phenomenon]…"
- **Domain motivation**: "[Technology X] has become the basic infrastructure of [Y]" / "[System] holds the potential to fill in the last coverage holes…"
- **Direct problem statement**: "Applications often put many requirements on the services from network transmissions."

**Apply**: Open with substantive content — context, motivation, or the problem itself. Do not announce that the paper is about to begin.

### Rule 2 — Length: 700–1000 words is typical, up to 1100 acceptable **[Strong]**

**Evidence**: Mean 836, median 835, range 573–1098. The shortest paper (Yang-2014, 573 words) is 11 years older than the median sample year and may reflect older norms; modern (2022–2024) range is 685–1098.

**Apply**:

- Target 800–950 words for first draft
- Up to 1100 words is within community norms; do not preemptively cut a 1052-word Introduction on length grounds alone
- Below 700 words is unusual for modern INFOCOM; verify completeness if landing here

### Rule 3 — Sentence rhythm: vary sentence length **[Strong]**

**Evidence**: Per-paper average ranges from 18 to 35 words. Within-corpus variance is high — both terse (Yang-2014: 18.5) and elaborate (Flowrest-2023: 35.1) intros are accepted.

**Apply**: Mix sentence lengths. A paper with uniformly 25-word sentences reads as monotonic; the corpus shows successful papers vary by paragraph.

### Rule 4 — Roadmap: optional, but if used, write 4–8 sentences **[Medium]**

**Evidence**: 6/13 (46%) papers include an explicit "rest of paper organized as follows" roadmap. Among those that do, sentence counts are 4, 4, 4, 4, 5, 8 (mean 4.8, median 4).

**Apply**:

- Roadmap is not required. Almost half of corpus papers omit it.
- If included, allocate one sentence per major section (typically II–VII), producing 4–8 sentences total.
- Do not compress to "1–2 sentences" — corpus shows this is below the lower bound.

**Standard format**:

> "The rest of this paper is organized as follows. Section II [topic]. Section III [topic]. Section IV [topic]. Section V [topic]. Section VI concludes."

### Rule 5 — Contribution enumeration: 3–5 items, each ≈ one sentence **[Strong]**

**Evidence**: 11/13 (85%) papers include explicit contribution enumeration. Item counts: 2, 2, 3, 3, 3, 3, 3, 4, 5, 5, 7 (mean 3.6, median 3). Words per item: 6.4–16, mean 10.6, mode ≈ one short sentence.

**Apply**:

- Use bullet (`•`) or parenthesized number `(1) (2) (3)` format
- Aim for 3–5 contributions; 2 is the minimum, 7 is the maximum observed
- Each item should fit in roughly one sentence (8–12 words is the sweet spot)
- 6+ items is acceptable but uncommon — consider whether some can be merged

### Rule 6 — Figure references in §1: optional **[Medium]**

**Evidence**: 11/13 (85%) papers have no figure reference within §1. The 2 that do (Atalay-2023, Wu-2024-AccelHandover) cite Fig. 1 (a system overview or motivation diagram).

**Apply**: A motivation figure in §1 is permitted but not standard. Most INFOCOM papers introduce figures starting in §II. If your Introduction is text-only, this matches the dominant convention.

### Rule 7 — Citations: 10–20 in total, density 1.5–2.5 per 100 words **[Strong]**

**Evidence**: Citation count range 6–24 (median 15), density 0.7–2.7 per 100 words (median 1.9).

**Apply**:

- Below 10 citations: verify you have grounded the problem and prior work claims
- Above 20: trim to the most directly relevant citations; the Introduction is not a literature review

### Rule 8 — No sub-headings inside §1 **[Strong]**

**Evidence**: 0/13 papers use §1.1 / §1.2 / I.A sub-headings within Introduction.

**Apply**: Treat §1 as a single coherent narrative. Use paragraph breaks for structure, not sub-section markers.

---

## Worked example: skeleton template

The following skeleton conforms to all eight rules above. Word counts are approximate.

```
[¶1, ~120w] Macro-context opening. State the technological or empirical
phenomenon driving the work. Land on a specific tension or unmet need.

[¶2, ~150w] Existing approaches and their limits. Cite 4–6 representative
prior works. Make the gap concrete enough that the reader can see it.

[¶3, ~150w] Restate the problem in the form your paper will solve.
Introduce key terminology that will be used throughout.

[¶4, ~180w] High-level description of your approach. One paragraph,
no sub-headings, no equations. End with a one-sentence summary of
why this approach works.

[¶5, ~120w] Headline result. One concrete quantitative claim
(e.g., "X% improvement over baseline Y"). 1–2 citations to support
the claim that this metric matters.

[¶6, ~80w] Contributions. Bullet list of 3–5 items, each a single sentence
of 8–12 words.

[¶7, ~80w] (Optional) Roadmap. Section II ... Section III ... Section IV ...
4–6 sentences, one per major section.

Total: ~880 words, ~15 citations, no sub-headings, no figure refs required.
```

---

## Anti-patterns flagged in this style

When reviewing or self-reviewing an INFOCOM Introduction, flag the following as misalignments with corpus norms:

| Anti-pattern | Corpus evidence | Severity |
|---|---|---|
| Opening with "This paper presents…" / "We propose…" / "Concretely:" | 0/13 papers do this | **High** |
| Word count below 600 or above 1200 | Range is 573–1098 | **Medium** (verify, don't auto-cut/expand) |
| Roadmap compressed to 1–2 sentences | When present, range is 4–8 | **Medium** |
| Contribution enumeration with 8+ items | Max in corpus is 7 | **Medium** |
| Per-item enumeration > 25 words (≈ multi-sentence) | Mean is 10.6 words/item | **Medium** |
| Sub-headings within §1 (e.g., §1.1, §1.A) | 0/13 papers use this | **High** |
| Citation density below 1.0 per 100 words | Median is 1.9; below 1.0 is rare | **Low** |

---

## What this guide does **not** cover

- **Paragraph structure rules**: pdftotext could not reliably segment paragraphs in IEEE 2-column layout; the corpus did not yield a quantitative paragraph-count norm.
- **Style trends over time**: 10/13 corpus papers are from 2022–2024; cannot detect drift across years.
- **Distinction between accepted and rejected papers**: corpus is all accepted; cannot identify discriminative markers of rejection.
- **Topic-specific style variants**: 5/13 corpus papers are LEO satellite topic, with 3 from the same Tsinghua group. Style observations may be inflated by author-voice clustering. Cross-validate against a SIGCOMM or NSDI corpus before applying to non-networking submissions.

---

## When to re-measure

Trigger a re-measurement of this guide when:

1. INFOCOM template changes (e.g., column count, page limit)
2. Corpus expands beyond n=20 with stratified year sampling (4–5 papers per year, 2018–2024)
3. A reviewer flags a style claim as misaligned with their experience — log the disagreement and add to the corpus

To re-measure, rebuild the corpus and the measurement with the method in Provenance below (the original script and corpus were not archived), then update the quantitative norms table.

---

## Provenance

| Field | Value |
|---|---|
| Source corpus | 13 PDFs (8 from arXiv preprints, 4 from IEEE Xplore via institutional access, 1 from a local copy); not archived — the working copy was in a temp directory and is lost |
| Measurement script | Not archived |
| Raw output | Not archived |
| Method | `pdftotext -raw` + Python regex (no LLM in the loop) |
| First built | 2026-04-30 |
| Reason for creation | User audit revealed prior INFOCOM style claims (e.g., "typical 800–900 words", "roadmap 1–2 sentences") were heuristics without corpus grounding. Two of those claims were refuted on measurement. This guide replaces them with measured norms. |

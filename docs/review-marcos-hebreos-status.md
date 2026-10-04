# Marcos and Hebrews editorial review

This extends the completed 81-note Yojanan/Revelation review in the same
[draft PR #38](https://github.com/jhonnyisaacc/shaul/pull/38) and branch
`feat/review-notes`, against `main`. No additional PR, merge or deployment is
part of this review. The existing branch-scoped Vercel protection remains in
`vercel.json`; the restoration procedure and earlier execution correction remain
in [the original status record](review-notes-status.md).

## Scope and baseline

The existing scope contains 34 notes: 21 Marcos and 13 Hebrews. There are 63
registered public videos. Thirty-one transcript-classified notes already pass
the structure gate; this is not evidence of completed substantive review.
Hebrews 5–6 are brief attributed notes without video IDs, and the Marcos
Ben Adam glossary refers to its canonical chapter-9 study. Initial audits found
nine broken note destinations and seven nonexistent corpus filename references.
Eight registered Marcos lessons have no transcript in the local archive.

The Vercel baseline remains six deployments, none for `feat/review-notes`.
Editorial CI stays enabled; it contains no site build or deployment command.

## Batch 13 — Hebrews 1–6

Reviewed six notes. Corrected local Hebrew quotation mismatches, distinguished
Hebrews 2:16 assistance from the supplied word nature, and identified the actual
verb behind Hebrews 2:17 likeness. Removed the duplicated chapter-4 exposition,
added the missing local comparison sheet, and corrected its source routing and
remaining-promise gloss. Verified that part 6 covers chapters 5–6 and developed
the two short notes with registered attribution, timestamp routes, local text,
and teaching maps. The proposed taught/learned reading and two immutable things
are retained as classroom interpretations with the textual distinctions clear.
Existing video IDs are preserved; the previously unattributed notes now identify
the verified part-6 source. No raw transcript or Scripture corpus is committed.

Completed: 6/34 notes. Remaining: Hebrews 7–13 and all 21 Marcos notes. Caption recovery for all eight gaps was attempted with the repository tool and
its yt-dlp fallback; none yielded a transcript. The gaps will be made explicit
in the affected Marcos notes.

## Batch 14 — Hebrews 7–13

Completed all 13 existing Hebrews notes (13/34 total). Consolidated repeated
chapter 7–9 repair sections while preserving the class arguments, restored
local Hebrew quotations including inline chapter 12–13 citations, repaired
chapter-6 note links, and corrected misplaced Greek terms. Distinguished the
chapter-8 service adjective from the covenant/promises comparative, chapter-9
figure and waiting verbs, and chapter-13 remain verb. Restored the explicit
Greek constructor term in Hebrews 11:10 and Eric’s discussion at 1:06:35; his
philosophical and transmission assertions remain pending precise sources.
Repaired malformed teaching-map rows and retained every registered video ID.

Validation: all 13 transcript-quality and YouTube-hygiene checks pass; Bun
frontmatter, local Scripture readiness, all verse conventions, local quotation
comparison, and whitespace checks pass. Remaining: all 21 Marcos notes.

## Batch 15 — Five Marcos topical studies

Reviewed the Abba/ruaj, Ben Adam glossary, El/Eloha/Elohim, son/heir and
word/throne/seed studies (18/34 complete). Restored local comparison excerpts,
fixed corpus filenames and links into integrated studies, repaired table links,
and added the glossary teaching map. Corrected the Romanos 10:9 accusative
claim, the Marcos 9:4 appearance verb and the Colosenses 2:3 knowledge term,
while preserving Eric’s theological and pedagogical proposals. Located the
part-8 source for the word/throne/seed note and registered it alongside the
retained part-2 source, with attribution by block. The distinct video count stays
63 because part 8 was already registered in the chapter-4 study.

Validation: transcript quality, YouTube hygiene, local quotation comparisons
and whitespace pass for this batch. Remaining: 16 canonical Marcos chapters.

### Batch-15 CI correction

Remote CI identified three new SBLGNT links indented after the scalar
`translation` field instead of within `sources`. Moved those links into the
source lists and validated the full verse-index generator locally. This
metadata correction does not change editorial coverage or deployment settings.

# Yojanan and Revelation editorial review

All existing `content/besorah/juan_*.md` and `content/besorah/apocalipsis_*.md`
notes belong to this review: 81 notes, including 66 transcript-derived studies
and 15 raw-note studies. All batches use `feat/review-notes` and one draft PR
against `main`. Keep Spanish note prose, local Scripture quotations, public
teacher credits, existing source assignments, and pending verification items.

## Deployment prevention

Before branch creation, the authenticated Vercel project API confirmed that
`shaul` is connected to `jhonnyisaacc/shaul`, uses the repository root, tracks
`main` for production, and has no deploy hooks. No deployment workflow exists
in the current repository tree. GitHub still lists a historical
`preview-on-ready.yml` workflow, whose file is absent on `main`.

The root `vercel.json` now sets:

```json
{
  "git": {
    "deploymentEnabled": {
      "feat/review-notes": false
    }
  }
}
```

This is Vercel's currently supported [branch-scoped Git configuration](https://vercel.com/docs/project-configuration/git-configuration#gitdeploymentenabled).
It prevents automatic Git deployments for this branch before a build starts.
Unspecified branches retain their normal behavior. The existing ignore command
for two other editorial branches is preserved; it is not the quota protection
used for this branch. No project-wide setting was changed.

To restore automatic deployments for this branch, remove only
`git.deploymentEnabled["feat/review-notes"]` or set it to `true`, then push the
restoration after review when deployments are authorized. Manual deployment
commands remain outside this task. Preserve this setting in every editorial
batch and do not add a matching `true` wildcard rule.

The pre-push baseline contained six Vercel deployments, none for
`feat/review-notes`. The latest was the production deployment of `8c94b0f`.
Post-push verification must check the Vercel API for the branch and new commit
SHAs, plus GitHub commit statuses, checks, and deployments. A canceled build
does not count as successful prevention.

## Coverage and validation baseline

- Scope inventory: 49 Yojanan notes and 32 Revelation notes.
- YouTube metadata/hygiene: 66 studies checked, zero failures.
- Transcript quality: 66 studies checked, 23 failures across 22 Yojanan notes;
  all 22 lack the Eric traceability map, and one also has only 288 substantive
  prose words. Revelation transcript studies pass this automated gate.
- Repository-wide transcript quality: 681 studies checked, 214 failures.
  Failures outside the two requested books remain outside this review.
- Verse conventions: 794 authored files checked, zero failures.
- Local Scripture corpus: ready (968 OE files, 35 TTH files, 27 Delitzsch files).

## Completed coverage

- Repository, branch, and PR existence checks.
- Vercel integration inspection and branch-scoped configuration.
- Non-deployment CI in `.github/workflows/editorial-validation.yml` checks
  frontmatter, verse conventions, YouTube metadata, changed transcript notes,
  local Scripture, verse lookup, and verse-index regression tests and generation.
  It contains no site build or deployment command.

## Remaining work

- Review all 81 notes for textual order, attribution, local Scripture support,
  lexical and historical qualifications, and working cross-links.
- Repair the 22 missing traceability maps using the existing public lesson
  archive; expand the short Yojanan 1 note with source-grounded prose.
- Review the 15 raw Revelation studies without inventing video attribution.
- Record source gaps and final validation results; verify each batch push
  does not create a Vercel build or preview deployment.

## Source gaps

The raw Revelation notes have no video `source_ids`; their original class
context is the repository's raw notes. Do not assign a teacher video without
evidence. Existing unchecked rabbinic, historical, and lexical claims remain
pending until their exact source is verified. The TTH library covers only part
of the Besorah; use available Delitzsch passages with an explicit corpus label
when TTH is missing. The full per-note gap inventory is pending review.

## Execution correction

The first signing attempt failed because the sandbox could not access the Git
signing service. A subsequent command incorrectly pushed the branch at unchanged
`main` before the prevention commit existed. The signed prevention commit
`a4fa7da6` was then pushed immediately. The first post-push Vercel API inspection
still showed only the six baseline deployments and none for this branch. This
error means the setting cannot be described as preceding the first push. Further
batch verification remains required.

## Batch 1 — introduction and Yojanan 1

Reviewed and revised `juan_introduccion.md`, `juan_iehudim_y_logos.md`, and
`juan_1_judios_luz_y_cosmos.md` against their archived public lessons. Added
three traceability maps with public timestamp routes, developed the short
Yojanan 1 study without treating an interpretive claim as settled grammar,
removed an unrelated Greek stem from the logos row, repaired a broken link,
and distinguished OE Psalm 22:2 from the corresponding TTH Psalm 22:1.
Source IDs and teacher credits are unchanged. All three notes pass transcript
quality and YouTube hygiene; frontmatter and global verse conventions pass.
19 Yojanan notes still need maps. Full substantive review: 3/81 notes.

The initial prevention commit's push and draft-PR CI runs both passed. Repeated
Vercel API checks after branch creation, the prevention commit, and PR creation
showed the same six baseline deployments and zero for this branch. GitHub has
no deployment record or Vercel commit status for the prevention commit.

## Batch 2 — Yojanan 5

Reviewed all three Yojanan 5 notes. Added passage-specific Eric maps, retained
source IDs and credits, repaired two links to the renamed yehudim/logos note,
corrected a TTH transcription typo, and qualified the raw study's opening claims
about the angel variant and Shabat practice. Spanish prose now uses Yehoshua
while source quotations retain their wording. All three pass transcript quality
and YouTube hygiene. Full substantive review: 6/81 notes; 16 maps remain.

Batch 1: both GitHub editorial CI runs passed; the Vercel API still returned the
six baseline deployments and none for the branch. No Vercel commit status was
created for `f07be9ab`.

## Batch 3 — Yojanan 6–7

Reviewed the three chapter-6 studies and the chapter-7 study. Added four
passage-specific maps, distinguished literal lexical glosses from the teacher's
applications of Abba, preserved qualifications for symbolic and historical
connections, normalized prose names, and supplied the available TTH text at
Isaiah 54:12 alongside OE 54:13. Psalm 89's maritime image is now explicitly
labeled OE 89:10 / TTH 89:9. All four studies pass transcript quality and
YouTube hygiene; global verse conventions remain clean. Full substantive review:
10/81 notes; 12 maps remain.

The local TTH Luke JSON contains repeated chapter numbers (1–21). For this review,
lookups use the first chapter occurrence, as the repository's lookup helper does;
do not overwrite an earlier passage in an in-memory index. No licensed corpus
file was changed. Corpus integrity is a separate source limitation.

## Batch 4 — detailed Yojanan 10 studies

Reviewed the six detailed chapter-10 studies. Added six maps that distinguish
Eric's concrete readings from the verse text, qualified the competence gloss of
mitzvah and the proposed life mechanism, normalized prose names while retaining
quoted wording, supplied the available OE text of 1 Samuel 17:35, and separated
OE Psalm 40:7/9 from TTH Psalm 40:6/8. All eight chapter-10 studies pass the
quality and metadata checks. Full substantive review: 16/81 notes; six maps remain.

Batch 3's push and PR editorial checks both passed. The Vercel API still shows
six baseline deployments and none for this branch.


## Batch 5 — Yojanan 15–17 and the prayer study

Reviewed six notes, completing the remaining six Eric maps. Corrected the Greek
verb assigned to John 17:9/15/20 (erotao, not entynchano) and the word assigned to
John 16:21 (thlipsis/lype, not odin) against the publisher's SBLGNT text. Preserved
Eric's proposed tribunal interpretation as an attributed reconstruction rather
than a lexical definition. Restored 13 local comparison cells, corrected Psalm
8's OE/TTH numbering, supplied both existing prayer-source credits, and included
the John 17:20 portion of the already registered part-67 source. Full substantive
review: 22/81 notes; all 22 missing maps repaired. Six notes pass quality and
YouTube hygiene. Other notes still require substantive review.


Validation exposed a filename bug: the display-name normalizer also changed
literal corpus paths from the existing `docs/scriptures/tth/json/iojanan.json` to nonexistent
`yojanan.json`. It now preserves `docs/scriptures/` identifiers while continuing
to validate visible Yod transliterations. A regression test covers both behaviors.

## Batch 6 — earlier chapters, Yojanan 8–9, and concept summary

Reviewed eleven additional notes: `juan_1`, `juan_1_testigo_cordero`,
`juan_2_senales_celo_y_santuario`, both canonical chapter-3/4 studies,
both chapter-8 studies, all three chapter-9 studies, and `juan_conceptos_deidad`.
Removed a duplicated chapter-3 paragraph, repaired corpus source paths, qualified
monogenes and Abba applications, distinguished the concept map from a dictionary,
attributed the chapter-1 antecedent by a working public link, added the historical
source gap in the Ben Adam study, corrected Psalm 69 numbering, and restored three
chapter-10 quotation cells in the chapter-9/10 bridge. Notes already sufficiently
qualified retain their existing argument and source maps. Full review: 33/81 notes.
All 49 transcript-classified Yojanan notes now pass quality and YouTube hygiene;
this gate is not a claim that every note has finished substantive review.


## Batch 7 — Yojanan 10–11, 13–14, and the prayer continuation

Reviewed twelve additional notes: the Abba and canonical-pastor chapter-10 studies,
Eleazar, the two-thrones prayer continuation, all four chapter-13 notes, and all
four chapter-14 notes. Corrected the Greek love-verb references, the chapter-17
verb repeated in the continuation, the children/gather grammar, and the proposed
replacement of kill with preserve life. Attributed unsupported historical
claims, distinguished the Greek mind vocabulary from Delitzsch's ruaj, repaired
duplicate table headers, supplied available Malachi/Colossians/Hebrews text, and
labeled Deuteronomy 13 and Genesis 32 numbering by corpus. Restored remaining
John comparison candidates, including three bridge cells whose alignment spaces
had prevented the batch-6 replacement. Full substantive review: 45/81 notes.

A complete source-path audit also repaired literal corpus filenames throughout
the two books and removed inherited private attachment paths from public
metadata. Public lesson IDs and credits remain intact. The inventory's earlier
book counts were misstated: the exact 81-file list contains 49 Yojanan and 32
Revelation notes. Batches 5 and 6 passed both CI runs; Vercel still shows only the
six baseline deployments and zero for this branch.

## Batch 8 — Yojanan 12 and 18–19

Completed substantive review of all 49 Yojanan notes. Reviewed all nine dossiers
in the consolidated chapter-12 study; redirected former dossier links to their
preserved headings, including references from related reviewed notes. Qualified
the Psalm 8, temple-date, Abba, and Acts 15 applications, distinguished the local
Romans 8:1 wording from SBLGNT, and removed a false missing-text claim where
Delitzsch already supplies John 12:1. Corrected the leg-breaking and hidden-
disciple Greek forms in the final chapter-19 study and repaired chapter-18 links.
All registered lesson IDs and credits remain. Full review: 49/81 notes; the 32
Revelation notes remain. Batch 7's two editorial CI runs passed, and the Vercel
API still returned six baseline deployments and none for the review branch.

## Batch 9 — Revelation introduction and chapters 1–9

Reviewed twelve notes: the raw introduction, eight transcript studies (chapters
1–4 and 6–9), and raw chapters 7–9. Added raw-note provenance without inventing
video assignments, supplied available Delitzsch/OE anchors, qualified numerical
and lexical applications, corrected three Greek identifications, and repaired
renamed study links. Dan's portion in Ezekiel 48:1 is now quoted separately from
the still-open question of its omission in Revelation 7. Full review: 61/81.
Batch 8's two editorial CI runs passed; Vercel still showed six baseline
deployments and none for the review branch.

## Batch 10 — Revelation chapters 10–15

Reviewed ten notes: six raw studies and four transcript studies. Documented raw
provenance, supplied available Ephesian and Revelation anchors, distinguished
Ezekiel's OE/TTH verse division, and clarified the witness-death, child/remnant,
Israel-name, bestia, and duration applications. Corrected an inverted statement
about Revelation 13:8, two Hebrew quotation errors, and renamed-note links.
Full review: 71/81 notes. Batch 9's two editorial CI runs passed; the Vercel API
retained six baseline deployments and none for the branch.

## Batch 11 — Revelation chapter 1 and 17–22

Completed substantive review of all 81 existing notes (49 Yojanan, 32 Revelation).
Reviewed the remaining five raw and five transcript studies. Distinguished the
older raw chapter-1 note's unknown provenance from the fourteen studies linked
to the raw class-notes document, supplied available OE/Delitzsch anchors, and
labeled Joel, Malachi, and Deuteronomy numbering. Clarified chapter-13 material
retold in chapter 17, chapter-15 imagery applied in chapter 20, and the book-wide
recap in the raw chapter-19 note. Corrected the chapter-19 Greek wife term and
the claim that the local Hebrew lacks a word for lake. The remaining historical,
rabbinic, chronological, and lexical research questions remain explicit in the
notes. Batch 10's two editorial CI runs passed; Vercel still returned six baseline
deployments and none for the branch. Final consolidated validation is pending.

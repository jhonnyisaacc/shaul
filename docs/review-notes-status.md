# Yojanan and Revelation editorial review

All existing `content/besorah/juan_*.md` and `content/besorah/apocalipsis_*.md`
notes belong to this review: 81 notes, including 66 transcript-derived studies
and 15 raw-note studies. All batches use `feat/review-notes` and one draft PR
against `main`. Keep Spanish note prose, local Scripture quotations, public
teacher credits, existing source assignments, and pending verification items.

## Deployment prevention

Before the first push, the authenticated Vercel project API confirmed that
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

- Scope inventory: 50 Yojanan notes and 31 Revelation notes.
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

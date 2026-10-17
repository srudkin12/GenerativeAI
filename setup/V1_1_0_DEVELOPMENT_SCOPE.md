# v1.1.0 — historical development scope

**Status:** development-history record, retained to describe the work before release. The v1.1.0 version DOI `10.5281/zenodo.23437397` was subsequently supplied by the creator; the current release identity is recorded in `CITATION.cff` and `ZENODO_METADATA_v1_1_0.md`. The v1.0.0 archive and tag remain immutable.

## Goal

Improve the practical route from an AI-assisted research problem to an appropriate researcher decision, evidence check, attribution record or manuscript constraint. Avoid expanding the public PISA evidential narrative, reproducing private logs or treating invented teaching examples as validated observations.

## Changes to review together

| Change | Why it belongs in a minor substantive release | Required review |
|---|---|---|
| Post-release citation correction | Replaces the historical first-DOI checklist on the public Cite page with the actual version-specific citation | Confirm Zenodo/GitHub metadata and no future DOI is asserted |
| Public-release policy and setup repair | Distinguishes a published v1.0.0 record from future maintenance processes | Check historical checklists remain identifiable |
| Research decision guide | Allows users to start with a real decision rather than search a linear protocol | Test whether a non-specialist can choose an appropriate action |
| Protocol crosswalk | Makes stage, decision, evidence gate and optional record explicit | Check claims about method authority and verification |
| Short field guide | Reduces practical burden and discourages ceremonial logging | Test readability; retain a clear upstream stopping rule |
| Constructed end-to-end illustration | Separates verified empirical objects, authorised claims and reason-provenance evidence in one continuous demonstration | Ensure hypothetical status is prominent and no invented results are presented as actual findings |
| Teaching exercises | Extends the public educational use without releasing confidential seminar files | Confirm wholly constructed scenarios; no real interview, student or survey material |

## Scope exclusions

- No empirical validation of reason provenance or the Academic Writing Filter.
- No new raw PISA data, code, private prompt histories, review dossiers, personal records or copyrighted slide materials.
- No claim of improvements in writing quality, publication success or scholarly productivity.
- No inference that the actual seminar deck has passed its separate public-circulation screening.
- No new release DOI, publication date, Git tag or published-version claim during candidate development.

## Status of the 17 October substantive editorial revision

The editorial revision addresses the four required issues and the principal follow-up improvements in `PISA8_v1_1_0_Substantive_Editorial_Review_20261017.md`: provenance timing, same-decision continuity, permission to transfer material, demonstrative miniature records, shorter reader route, teaching transfer, novelty/salience stopping rules, publicly available evidence and qualitative/archival adaptations. The existing v1.0.0 citation corrections remain within the same prospective release.

**Historical status at drafting:** independent human reader testing and a full deployment-level Jekyll build had not been completed. Subsequent local Chromium previews, static-link tests, source checksums and the Mac branch-application report addressed parts of this list. Human reader evaluation and post-publication URL/DOI checks remain separate activities. No new PISA empirical re-estimation is claimed.

## Status after the second editorial slow read

A targeted source revision has added a constructed first GenAI exchange, separated an initial Decision Log from dated later updates and retrospective reconstruction, introduced plain-language PISA case framing, simplified the beginner route, and supplied a model workshop response. These are **editorial development changes**, not claims that real participant testing occurred or that new empirical PISA evidence became public. This paragraph records an earlier editorial stage and should not be mistaken for a statement about the final release.

## Release gates remaining

1. Scholarly slow read across disciplinary traditions, with particular attention to the constructed example, attribution limits and whether the new material offers genuine reader utility.
2. Public-rights and source-status audit of all new content.
3. Local Jekyll build and browser checks on desktop and mobile (external links, site layout and navigation).
4. Comparison of the candidate with the live Git branch and `v1.0.0` baseline; inspect and authorise any changes not represented in the supplied baseline.
5. Creation of a Zenodo **new-version draft**, reservation of a genuine new version-specific DOI, and approval of exact release metadata.
6. Only then update `CITATION.cff`, README, Cite page, release notes, changelog and checksum manifest to the approved version and date.
7. Commit and tag the approved release; archive using `git archive`, upload the exact ZIP to Zenodo, publish and verify byte identity of the downloaded ZIP.

## Delivery rule

Apply a reviewed small patch to a new branch of the *live* MacBook repository, not to the existing frozen tag. Supply a full source snapshot and patch together. Never claim deployment or publication before the user performs it and verifies the result.

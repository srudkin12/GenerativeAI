# Next release checklist — PISA8 public resource

**Historical baseline:** v1.0.0 was published on 17 October 2026 with DOI `10.5281/zenodo.23428193` and immutable tag `v1.0.0`. The v1.1.0 release has its own DOI `10.5281/zenodo.23437397` and metadata sheet at [`ZENODO_METADATA_v1_1_0.md`](ZENODO_METADATA_v1_1_0.md). Use this general checklist when preparing later versions, checking the current archived baseline first.

## 1. Decide the release scope

- [ ] Classify each proposed change: typographical/editorial correction, metadata repair, public-site maintenance, or substantive educational/methodological extension.
- [ ] Decide whether the change requires a new archived release. Under the handover policy, use `v1.0.x` for small corrections and `v1.1.0` for substantive expansion. Do not assign an actual released version until its scope is settled.
- [ ] Keep the v1.0.0 tag, published Zenodo ZIP and DOI record unchanged. Compare candidate files with that frozen baseline.
- [ ] Make development changes in a separate Git branch; review locally before merging or publishing. Remember that pushing changes to the Pages source branch can make them publicly visible even before a new Zenodo release.

## 2. Content and scholarly claims

- [ ] Verify that the Cite page identifies the **existing** release, without describing v1.0.0 as pending.
- [ ] Check all public pages for stale future-tense references to first publication, outdated version numbers and unfulfilled placeholder instructions.
- [ ] Retain the methods-first architecture; do not make the PISA examples stand in for empirical validation of the reason-provenance framework.
- [ ] Treat generated code/text as candidate artefacts rather than verified evidence; distinguish inferred from contemporaneously recorded reasons.
- [ ] Check the Academic Writing Filter attribution and third-party rights boundaries. Do not imply empirical improvements in publication probability, writing quality or review agreement.
- [ ] Screen every new public example, figure, quotation and seminar item under `docs/public-release-policy.md` and the public-release screening checklist.
- [ ] Check that the working-paper references reflect verified public bibliographic records; do not invent publication status, DOI or ORCID.
- [ ] Check that new material offers an identifiable benefit to a social-science reader, rather than adding more documentation without improving usability.

## 3. Navigation and website

- [ ] Check `docs/index.md`, `docs/quick-start.md`, `docs/cite.md`, `docs/publications.md`, `docs/about.md` and `docs/public-release-policy.md` for coherent reader journeys.
- [ ] Inspect `docs/_config.yml` and navigation entries if new public pages are created.
- [ ] Check Markdown and Jekyll relative links, external links and the Pages build; click-test the published site in a normal browser, including mobile/narrow layout.
- [ ] Confirm the public Cite page cites the archived release that actually exists; do not substitute a new version number or DOI before the next release is published.

## 4. Provenance, rights and integrity

- [ ] Preserve exact authorship and affiliation: Simon Rudkin, Department of Social Statistics, University of Manchester.
- [ ] Confirm CC BY 4.0 applies only to material released under that licence; respect separately hosted filter and third-party rights.
- [ ] Inspect `git diff --check`, `git diff --stat`, `git diff` and the complete list of added files.
- [ ] Rebuild `SHA256SUMS.txt` and verify it against the *candidate* source tree.
- [ ] Confirm that the candidate contains no private chats, confidential referee files, unreleased evidence archives, sensitive records or unintended data/code payloads.
- [ ] Produce a complete candidate source ZIP and a minimal patch ZIP; validate that applying the patch to the designated baseline gives exactly the same source hashes.

## 5. Only when a new DOI-bearing release is approved

- [ ] Confirm the final version number and authorise a release date based on actual publication, not a provisional plan.
- [ ] Create a **new version** through the established Zenodo record/workflow; reserve the version-specific DOI while the next version is still a draft. Do not invent a DOI or treat the v1.0.0 DOI as the DOI for the new archive.
- [ ] Confirm the correct **non-software** resource type, title, version, creator, affiliation, rights, description and linked public resources in Zenodo metadata.
- [ ] Update the new release's `CITATION.cff`, `README.md`, Cite page, changelog and release notes consistently with the **reserved** new DOI and confirmed release metadata.
- [ ] Regenerate and verify `SHA256SUMS.txt` after the final content and metadata changes.
- [ ] Commit the exact final state; create an annotated release tag only after review; check that the tag points to the intended commit.
- [ ] Build the release ZIP from that exact tag using `git archive`, and calculate its SHA-256.
- [ ] Create the GitHub Release from that tag and upload the **same ZIP** to the appropriate Zenodo draft.
- [ ] Compare GitHub Release, `CITATION.cff`, Cite page and Zenodo metadata before publication; publish only after approval.
- [ ] Download the Zenodo archive after publication and compare its SHA-256 with the tag-derived ZIP.
- [ ] Verify DOI resolution and the deployed website; record the version-specific DOI separately from any concept DOI, if supplied by Zenodo.

## Mac terminal checks (from the local repository)

```bash
REPO="$HOME/Documents/Research/ai-assisted-social-science-research"
cd "$REPO" || exit 1

git status --short
git config user.name
git config user.email
git diff --check
git diff --stat
git diff

grep -n -E '^(version|date-released|doi|license|repository|url):' CITATION.cff
shasum -a 256 -c SHA256SUMS.txt

grep -RinE 'first DOI-bearing release is planned|intended to become a public scholarly|For the first DOI-bearing release|DOI strategy' docs setup README.md || true
```

The final search is a **review prompt**, not an automatic failure: historical documents may correctly contain old terminology if their completed status is clearly labelled.

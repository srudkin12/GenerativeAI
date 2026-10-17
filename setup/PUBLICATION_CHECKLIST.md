# Publication Checklist for v1.0.0

> **Historical checklist.** v1.0.0 was published on 17 October 2026. These unchecked boxes preserve the original pre-release process, not evidence that publication remains incomplete. Do not re-run the tag/DOI steps against the frozen release. For the next release, use [`NEXT_RELEASE_CHECKLIST.md`](NEXT_RELEASE_CHECKLIST.md).

## Content

- [ ] README reflects the final public scope.
- [ ] Seven worked research examples have been read as social-science prose rather than internal notes.
- [ ] Manuscript-governance pages are understandable without prior knowledge of the Academic Writing Filter.
- [ ] Public navigation exposes only material intended for current public release.
- [ ] Internal delivery-format planning is not present in the public repository.
- [ ] Ten-step protocol is understandable without prior knowledge of the worked application.
- [ ] Direct quotations, if any, are verified against authoritative originals.
- [ ] No reconstructed wording appears as a quotation.
- [ ] No raw internal chat logs are included accidentally.
- [ ] No confidential peer-review material is included.
- [ ] No non-circulating seminar file is included accidentally.
- [ ] Third-party assets have been removed or rights-cleared.

## Intellectual boundaries

- [ ] The worked application is described as developmental illustration, not validation.
- [ ] Attribution claims remain bounded.
- [ ] Attribution is separated from endorsement of AI-intensive labour arrangements.
- [ ] Reason provenance and manuscript governance are not treated as synonyms.
- [ ] PCA/Ball Mapper claims match the final empirical position.
- [ ] The withdrawn direct-flow inference has not reappeared.
- [ ] Generated code/text is not described as verified evidence merely because it was generated.
- [ ] The Academic Writing Filter is not described as empirically proven to improve writing or publication outcomes.
- [ ] Retrospective claim-preservation examples are not represented as historical evidence that a formal contract existed during the original empirical work.

## Rights and provenance

- [ ] Repository `LICENSE` is present and states CC BY 4.0.
- [ ] `CITATION.cff` records `CC-BY-4.0`.
- [ ] Zenodo draft uses the same CC BY 4.0 licence.
- [ ] Academic Writing Filter licensing/provenance boundary is checked.
- [ ] Cochrane is not described as author, approver or endorser of the filter.
- [ ] Third-party rights statements are checked.

## Identity and citation

- [ ] Author: Simon Rudkin.
- [ ] Affiliation: Department of Social Statistics, University of Manchester.
- [ ] ORCID added if desired.
- [ ] Canonical title is identical across `CITATION.cff`, Cite page, GitHub Release metadata and Zenodo draft.
- [ ] Development version has been changed to public release version `1.0.0`.
- [ ] Actual release date is recorded.
- [ ] GitHub repository URL and public landing-page URL are recorded.
- [ ] Academic Writing Filter and working-paper citations are checked.

## Zenodo draft and DOI

- [ ] Zenodo draft created before final tag.
- [ ] Closest available non-software resource type selected.
- [ ] Title, creator, affiliation, version, description, keywords and licence checked.
- [ ] DOI reserved while record is still a draft.
- [ ] Reserved version DOI added to `setup/ZENODO_METADATA_v1_0_0.md`.
- [ ] Same reserved DOI added to `CITATION.cff`.
- [ ] Same reserved DOI added to `docs/cite.md`.
- [ ] Same reserved DOI added to `README.md`.

## Website checks

- [ ] Deployed GitHub Pages site opens at `https://srudkin12.github.io/GenerativeAI/`.
- [ ] Main navigation and footer links click-tested on desktop.
- [ ] Site checked on a narrow/mobile viewport.
- [ ] Academic Writing Filter external link tested in a normal browser.
- [ ] Acknowledgements section and footer anchor tested.
- [ ] Cite page displays the intended v1.0.0 citation and DOI.

## Repository and integrity checks

From the repository root:

```bash
git status
find . -maxdepth 5 -type f | sort
```

Confirm that no unexpected files, temporary files, `.DS_Store` files or private artefacts are tracked.

Check for stale active development wording:

```bash
grep -RIn --exclude-dir=.git "v0\.2\.0" .
grep -RIn --exclude-dir=.git "YOUR-GITHUB-USERNAME" .
```

Historical references in the changelog are acceptable; active setup or public guidance is not.

After every release edit is complete, regenerate `SHA256SUMS.txt` and verify it:

```bash
find . -type f \
  ! -path './.git/*' \
  ! -name 'SHA256SUMS.txt' \
  -print | LC_ALL=C sort | while IFS= read -r f; do \
    shasum -a 256 "$f"; \
  done > SHA256SUMS.txt

shasum -a 256 -c SHA256SUMS.txt
```

Every checksum must report `OK`.

## Final commit and tag

- [ ] Final v1.0.0 metadata and reserved DOI are committed.
- [ ] Working tree is clean.
- [ ] `SHA256SUMS.txt` verifies against the final commit contents.

Then:

```bash
git status
git tag -a v1.0.0 -m "First DOI-bearing public release"
git push origin main
git push origin v1.0.0
```

## GitHub Release and Zenodo publication

- [ ] Create a GitHub Release from `v1.0.0`.
- [ ] GitHub Release title uses the canonical scholarly title and version 1.0.0.
- [ ] Create the clean archive from the tag with `git archive`.
- [ ] Upload that exact tagged archive to the prepared Zenodo draft.
- [ ] Preview the Zenodo record and generated citation.
- [ ] Publish the Zenodo record.
- [ ] Confirm that the published DOI resolves and the uploaded archive is the expected v1.0.0 object.

# Publication Checklist for v1.0.0

## Content

- [ ] README reflects the final public scope.
- [ ] Seven worked research-process cases have been read as social-science prose rather than project notes.
- [ ] Manuscript-governance pages are understandable without prior knowledge of the Academic Writing Filter project.
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

- [ ] Academic Writing Filter licensing/provenance decision checked.
- [ ] Cochrane is not described as author, approver or endorser of the filter.
- [ ] Repository licence chosen and added.
- [ ] Third-party rights statements checked.

## Identity and citation

- [ ] Author: Simon Rudkin.
- [ ] Affiliation: Department of Social Statistics, University of Manchester.
- [ ] ORCID added if desired.
- [ ] `CITATION.cff` updated.
- [ ] Version changed from development to public release.
- [ ] Academic Writing Filter and working-paper citations checked.
- [ ] Zenodo metadata checked.
- [ ] DOI added after deposit.

## Repository checks

```bash
git status
find . -maxdepth 5 -type f | sort
```

Confirm that no unexpected files, temporary files or private artefacts are being tracked.

Then:

```bash
git tag -a v1.0.0 -m "First public release"
git push origin v1.0.0
```

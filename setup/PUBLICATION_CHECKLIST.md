# Publication Checklist for v1.0.0

## Content

- [ ] README reflects the final public scope.
- [ ] Seven worked cases have been read as social-science prose rather than project notes.
- [ ] Direct quotations, if any, are verified against authoritative originals.
- [ ] No reconstructed wording appears as a quotation.
- [ ] No raw internal chat logs are included accidentally.
- [ ] No confidential peer-review material is included.
- [ ] No non-circulating seminar file is included accidentally.
- [ ] Third-party assets have been removed or rights-cleared.

## Intellectual boundaries

- [ ] PISA is described as developmental illustration, not validation.
- [ ] Attribution claims remain bounded.
- [ ] Attribution is separated from endorsement of AI-intensive labour arrangements.
- [ ] PCA/Ball Mapper claims match the final empirical position.
- [ ] The withdrawn direct-flow inference has not reappeared.
- [ ] Generated code/text is not described as empirical evidence.

## Identity and citation

- [ ] Author: Simon Rudkin.
- [ ] Affiliation: Department of Social Statistics, University of Manchester.
- [ ] ORCID added if desired.
- [ ] Licence chosen and added.
- [ ] `CITATION.cff` updated.
- [ ] Version changed from development to public release.
- [ ] Zenodo metadata checked.
- [ ] DOI added after deposit.

## Repository checks

```bash
git status
find . -maxdepth 4 -type f | sort
```

Confirm that no unexpected files, temporary files or private artefacts are being tracked.

Then:

```bash
git tag -a v1.0.0 -m "First public release"
git push origin v1.0.0
```

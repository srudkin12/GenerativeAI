# Zenodo Release Guide

**Status (17 October 2026):** The first DOI-bearing release, v1.0.0, has been published and archived. Its version-specific DOI is `10.5281/zenodo.23428193`. The v1.0.0 instructions below document the completed first-release procedure; they must not be repeated against that frozen archival object. Use [`NEXT_RELEASE_CHECKLIST.md`](NEXT_RELEASE_CHECKLIST.md) to prepare a subsequent version.

## Recommended approach for this project

Use Zenodo as the **DOI-bearing archive of a public release**, but do not frame the repository as research software merely because GitHub is involved.

The resource is primarily a social-science methodological and educational object. A manual Zenodo deposit gives direct control over the resource type and descriptive metadata.

## Metadata consistency rule

The **GitHub Release metadata**, `CITATION.cff`, public Cite page and Zenodo record must use the **same scholarly title and release version**.

Canonical title:

> **AI-Assisted Social Science Research: Methods, Governance and Reason Provenance**

The development series (`0.3.x`) was not DOI-bearing. The first DOI-bearing release was **1.0.0**, published on 17 October 2026.

Do not use the earlier working title *A Reason-Provenance Resource and Worked Case Study* for the DOI record.

## Historical first-release metadata (v1.0.0)

**Title**<br>
AI-Assisted Social Science Research: Methods, Governance and Reason Provenance

**Creator**<br>
Simon Rudkin

**Affiliation**<br>
Department of Social Statistics, University of Manchester

**Version**<br>
1.0.0

**Licence**<br>
Creative Commons Attribution 4.0 International (CC BY 4.0)

**Resource type**<br>
At deposit time, choose the closest available **non-software** resource type that accurately describes a research/educational resource. Do not hard-code a subtype in advance if the current Zenodo interface does not present an exact match.

**Description**<br>
A practical social-science resource on generative-AI-assisted research. The resource examines question origination, researcher governance, the separation of generated analytical artefacts from verified evidence, methodological challenge, claim revision, reason provenance and manuscript governance. It includes seven worked research episodes and reusable templates for specification, decision logging, claim challenge, inference revision, contribution mapping and claim preservation.

**Suggested keywords**

- generative AI
- social science
- research methods
- reason provenance
- research transparency
- attribution
- manuscript governance
- AI-assisted research

**Repository**<br>
`https://github.com/srudkin12/GenerativeAI`

**Public landing page**<br>
`https://srudkin12.github.io/GenerativeAI/`

**ORCID**<br>
Add only if Simon chooses to include it.

## Historical v1.0.0 release procedure

1. Complete `setup/PUBLICATION_CHECKLIST.md`.
2. Create a new **draft** Zenodo record.
3. Enter the proposed v1.0.0 metadata, including CC BY 4.0 and the closest appropriate non-software resource type.
4. Reserve the DOI while the record remains a draft.
5. Record the reserved DOI in `setup/ZENODO_METADATA_v1_0_0.md`. For v1.0.0 the reserved DOI is `10.5281/zenodo.23428193`.
6. Update the repository to the exact v1.0.0 state:
   - `CITATION.cff`;
   - `docs/cite.md`;
   - `README.md`;
   - release date;
   - reserved DOI;
   - licence and URLs.
7. Regenerate `SHA256SUMS.txt` and verify every checksum.
8. Run the final pre-tag audit and confirm the working tree contains only intended release changes.
9. Commit the v1.0.0 release state.
10. Create and push the annotated tag `v1.0.0`.
11. Create a **GitHub Release** from that exact tag, using the canonical title and version.
12. Create a clean ZIP with `git archive` from `v1.0.0`.
13. Upload that exact tagged archive to the prepared Zenodo draft.
14. Preview the Zenodo citation and metadata one final time.
15. Publish the Zenodo record.
16. Verify that the published DOI resolves to the expected record and archive.

This sequence allows the DOI to appear inside the v1.0.0 repository itself rather than requiring a metadata-only v1.0.1 solely for DOI write-back.

## Versioning principle

Use a new Zenodo version for a later DOI-bearing public release rather than silently replacing the scholarly object. For a metadata-only or small corrective change, first determine whether a separate archival release is warranted. If Zenodo exposes a concept DOI for the version family after publication, document it separately from the version-specific DOI in a later metadata update if useful.

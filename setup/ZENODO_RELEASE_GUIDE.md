# Zenodo Release Guide

## Recommended approach for this project

Use Zenodo as the **DOI-bearing archive of a public release**, but do not frame the repository as research software merely because GitHub is involved.

The resource is primarily a social-science methodological and educational object.

A manual Zenodo deposit gives direct control over the resource type and descriptive metadata.


## Metadata consistency rule

The Zenodo record, GitHub release and `CITATION.cff` must use the **same title and release version**.

Canonical title for this project:

> **AI-Assisted Social Science Research: Methods, Governance and Reason Provenance**

The development series (`0.3.x`) is not the first DOI-bearing release. When the project is ready for its first archived public release, update the repository metadata to `1.0.0`, create/tag that release, and use **1.0.0** as the Zenodo version.

Do not use the earlier working title *A Reason-Provenance Resource and Worked Case Study* for the DOI record.

## Suggested first-release metadata

**Title**  
AI-Assisted Social Science Research: Methods, Governance and Reason Provenance

**Creator**  
Simon Rudkin

**Affiliation**  
Department of Social Statistics, University of Manchester

**Version**  
1.0.0

**Resource type**  
Consider **Lesson** if the final object is primarily a reusable social-science training/methods resource.  
Consider **Other** if the release becomes a wider scholarly project archive.

**Description**  
A practical social-science resource on generative-AI-assisted research. The resource examines question origination, researcher governance, the separation of generated analytical artefacts from verified evidence, methodological challenge, claim revision, reason provenance and manuscript governance. It includes seven worked research episodes and reusable templates for specification, decision logging, claim challenge, inference revision, contribution mapping and claim preservation.

**Suggested keywords**

- generative AI
- social science
- research methods
- reason provenance
- research transparency
- attribution
- AI-assisted research
## Release procedure

1. Complete `setup/PUBLICATION_CHECKLIST.md`.
2. Create and push the Git tag.
3. Create a clean ZIP with `git archive`.
4. Create a new Zenodo upload.
5. Upload the tagged archive.
6. Enter the metadata above.
7. Add ORCID if desired.
8. Choose and confirm the repository licence.
9. Publish the Zenodo record.
10. Copy the assigned DOI.
11. Add the DOI to:
   - `CITATION.cff`;
   - `docs/cite.md`;
   - the GitHub release notes;
   - the repository README.
12. Commit and push those metadata updates.

## Versioning principle

Use a new Zenodo version for substantively different public releases rather than silently replacing the scholarly object.

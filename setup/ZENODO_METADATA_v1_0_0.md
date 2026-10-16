# Zenodo Metadata Template — First DOI-Bearing Release

Use this file as the working metadata sheet for the first archived release. Do not publish the record until the repository has passed `setup/PUBLICATION_CHECKLIST.md`.

## Identity

**Title**  
AI-Assisted Social Science Research: Methods, Governance and Reason Provenance

**Creator**  
Simon Rudkin

**Affiliation**  
Department of Social Statistics, University of Manchester

**Version**  
1.0.0

**ORCID**  
Add only if Simon chooses to include it.

## Resource description

**Resource type**  
Choose the closest available Zenodo type at deposit time for a research/educational resource. Do not classify the release as software merely because it is distributed through GitHub.

**Description**  
A practical social-science resource on generative-AI-assisted research. The resource connects proposal generation, verification, adversarial challenge, claim authorisation, reason provenance and manuscript governance through transferable methods, worked research episodes and reusable tools. Selected examples arise from a PISA research project, but the public resource is intended for wider research and graduate-methods use.

**Keywords**

- social science
- generative AI
- research methods
- reason provenance
- manuscript governance
- claim preservation
- research transparency
- AI-assisted research

## Metadata consistency

Before upload, verify that all three objects agree:

1. Git tag/release: `v1.0.0`;
2. `CITATION.cff`: title above and version `1.0.0`;
3. Zenodo record: title above and version `1.0.0`.

## DOI return path

After Zenodo assigns/publishes the DOI, record it in:

- `CITATION.cff`;
- `docs/cite.md`;
- repository `README.md`;
- GitHub release notes;
- the next tagged release.

The first archived `v1.0.0` object may therefore pre-date the DOI being written back into the repository. Preserve that chronology rather than silently replacing the archived object.

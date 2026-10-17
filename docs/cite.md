---
layout: default
title: Cite
---

# How to cite this resource

## Development citation

Until the DOI-bearing v1.0.0 release is published, use:

> Rudkin, Simon. *AI-Assisted Social Science Research: Methods, Governance and Reason Provenance*. Version 0.3.12 (development). Department of Social Statistics, University of Manchester.

The first permanent DOI will be reserved in the Zenodo draft and inserted into the repository before the v1.0.0 release is tagged. Once v1.0.0 is published, the DOI-bearing release citation should replace this development citation.

## Academic Writing Filter

When using the manuscript-governance artefact itself, cite it separately:

> Rudkin, S. (2026). *Academic Writing Filter* (October 2026 release).

Current public project page: `https://sites.google.com/view/simonrudkin/ai`

## Working paper

> Rudkin, S. (2026). *From Writing Advice to Manuscript Governance: A Constrained-Transformation Framework for Academic Revision*. Working paper.

Update this entry if the working paper receives a repository record, DOI or publication.

## GitHub citation

The repository root contains `CITATION.cff`. GitHub can use this file to expose a citation interface.

## DOI strategy

For this project, the recommended archival object is a **research/educational resource**, not software.

For the first DOI-bearing release:

1. complete the release-readiness and publication checklists;
2. create a Zenodo draft and enter the release metadata;
3. choose the closest available **non-software** resource type that describes the public object;
4. record Simon Rudkin as creator with the Department of Social Statistics, University of Manchester affiliation;
5. add ORCID if desired;
6. select **CC BY 4.0** as the repository licence;
7. reserve the Zenodo DOI while the record is still a draft;
8. update `CITATION.cff`, this page and the README to version **1.0.0**, adding the reserved DOI and release date;
9. run the final integrity checks and regenerate `SHA256SUMS.txt`;
10. commit the exact release state and create the Git tag `v1.0.0`;
11. create a GitHub Release for that tag;
12. create a clean archive from the tag and upload that exact archive to the Zenodo draft;
13. preview the Zenodo record and publish it.

The **GitHub Release metadata**, `CITATION.cff`, this Cite page and the Zenodo record should share the same scholarly title and release version. The GitHub repository itself remains named `GenerativeAI`.

The canonical scholarly title is:

> **AI-Assisted Social Science Research: Methods, Governance and Reason Provenance**

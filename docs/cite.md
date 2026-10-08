---
layout: default
title: Cite
---

# How to cite this resource

## Development citation

Until a DOI-bearing release exists, use:

> Rudkin, Simon. *AI-Assisted Social Science Research: A Reason-Provenance Resource and Worked Case Study*. Version 0.1.0 (development). Department of Social Statistics, University of Manchester.

A permanent DOI should replace the development citation after the first archived public release.

## GitHub citation

The repository root contains `CITATION.cff`. GitHub can use this file to expose a citation interface.

## DOI strategy

For this project, the recommended archival object is a **research/educational resource**, not software.

At each substantive public release:

1. create a version tag in GitHub;
2. create a clean release archive;
3. deposit that archive in Zenodo manually;
4. choose the Zenodo resource type that best describes the public object — likely **Lesson** for the social-science training resource, or **Other** if the release is framed as a broader scholarly project archive;
5. record Simon Rudkin as creator with the Department of Social Statistics, University of Manchester affiliation;
6. add ORCID if desired;
7. publish the Zenodo record and obtain the DOI;
8. add the DOI back to `CITATION.cff`, this page and the next tagged release.

The repository and DOI record should share the same title and version metadata.

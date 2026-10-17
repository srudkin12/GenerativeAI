# Mac Terminal Setup

These instructions describe how to obtain and work with the public repository on a Mac. The GitHub repository is:

`https://github.com/srudkin12/GenerativeAI`

The examples below keep the existing local folder name used during development:

`$HOME/Documents/Research/ai-assisted-social-science-research`

## 1. Check Git

Open **Terminal** and run:

```bash
git --version
```

If macOS asks to install the Command Line Tools, accept that installation and rerun the command afterwards.

## 2. Clone the public repository

Create a permanent research directory:

```bash
mkdir -p "$HOME/Documents/Research"
cd "$HOME/Documents/Research"
```

### HTTPS route

```bash
git clone https://github.com/srudkin12/GenerativeAI.git ai-assisted-social-science-research
cd ai-assisted-social-science-research
```

### SSH route

Use this alternative if your GitHub SSH key is already configured:

```bash
git clone git@github.com:srudkin12/GenerativeAI.git ai-assisted-social-science-research
cd ai-assisted-social-science-research
```

Use **one** clone route, not both.

## 3. Inspect the repository

```bash
pwd
git status
git remote -v
find . -maxdepth 3 -type f | sort
```

The expected GitHub remote is `srudkin12/GenerativeAI`.

## 4. Update an existing clone

If the repository is already present locally:

```bash
cd "$HOME/Documents/Research/ai-assisted-social-science-research"
git status
git pull --ff-only origin main
```

Do not pull across uncommitted local changes without first inspecting them.

## 5. Maintainer update cycle

Readers who only want to use the resource do not need write access. Maintainers with permission to push can use:

```bash
cd "$HOME/Documents/Research/ai-assisted-social-science-research"
git status
git add -A
git commit -m "Describe the change"
git push origin main
```

If Git asks for your identity, configure it once:

```bash
git config --global user.name "Simon Rudkin"
git config --global user.email "YOUR-GITHUB-EMAIL"
```

## 6. GitHub Pages

The public site is built from `/docs` in the `main` branch. See [`GITHUB_PAGES_GUIDE.md`](GITHUB_PAGES_GUIDE.md).

Current public landing page:

`https://srudkin12.github.io/GenerativeAI/`

## 7. Preparing v1.0.0

Do **not** create the `v1.0.0` tag until:

- the publication checklist is complete;
- the repository licence is final;
- the Zenodo draft exists;
- the DOI has been reserved in that draft;
- the reserved DOI has been inserted into the v1.0.0 repository metadata;
- `SHA256SUMS.txt` has been regenerated and verified.

When the final release commit is ready:

```bash
git status
git tag -a v1.0.0 -m "First DOI-bearing public release"
git push origin v1.0.0
```

Then create a GitHub Release from the `v1.0.0` tag.

## 8. Create the clean archive for Zenodo

Create the archive **from the tag**, not from the working directory:

```bash
git archive \
  --format=zip \
  --output="$HOME/Desktop/AI_Assisted_Social_Science_Research_v1.0.0.zip" \
  v1.0.0
```

The resulting archive contains only files tracked by Git at the tagged release. Upload that exact archive to the prepared Zenodo draft before publication.

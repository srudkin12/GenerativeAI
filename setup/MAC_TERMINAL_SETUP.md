# Mac Terminal Setup

These instructions assume that the downloaded repository folder is named:

`ai-assisted-social-science-research`

No Linux-specific paths are used.

## 1. Check Git

Open **Terminal** on the Mac and run:

```bash
git --version
```

If macOS asks to install the Command Line Tools, accept that installation and rerun the command afterwards.

## 2. Move the repository somewhere permanent

For example:

```bash
mkdir -p "$HOME/Documents/Research"
cd "$HOME/Downloads"
mv ai-assisted-social-science-research "$HOME/Documents/Research/"
cd "$HOME/Documents/Research/ai-assisted-social-science-research"
```

If the folder is somewhere else, simply `cd` to that location instead.

## 3. Inspect the starter

```bash
pwd
find . -maxdepth 3 -type f | sort
```

## 4. Initialise Git locally

```bash
git init
git branch -M main
git add .
git status
git commit -m "Initial social science reason-provenance resource"
```

If Git asks for your identity, set it once:

```bash
git config --global user.name "Simon Rudkin"
git config --global user.email "YOUR-GITHUB-EMAIL"
```

Then repeat the commit.

## 5A. Easiest route if you prefer to create the repository in the browser

On GitHub, create an **empty** repository called:

`ai-assisted-social-science-research`

Do not ask GitHub to add a README, licence or `.gitignore`, because those files already exist locally.

GitHub will show the remote URL. Copy it exactly.

### SSH remote

```bash
git remote add origin git@github.com:YOUR-GITHUB-USERNAME/ai-assisted-social-science-research.git
git push -u origin main
```

### HTTPS remote

```bash
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/ai-assisted-social-science-research.git
git push -u origin main
```

Use **one** of those remote commands, not both.

## 5B. Terminal-only route if GitHub CLI is already installed

Check:

```bash
gh --version
```

If available:

```bash
gh auth status
gh repo create ai-assisted-social-science-research \
  --public \
  --source=. \
  --remote=origin \
  --push
```

If `gh` is not installed, route 5A avoids installing anything extra.

## 6. Everyday update cycle

```bash
cd "$HOME/Documents/Research/ai-assisted-social-science-research"
git status
git add -A
git commit -m "Describe the change"
git push
```

## 7. Create a version tag when a public release is ready

Do **not** tag v1.0.0 until the public-release checklist has been completed.

When ready:

```bash
git status
git tag -a v1.0.0 -m "First public release"
git push origin v1.0.0
```

## 8. Create a clean ZIP for a manual Zenodo deposit

After the tag exists:

```bash
git archive \
  --format=zip \
  --output="$HOME/Desktop/AI_Assisted_Social_Science_Research_v1.0.0.zip" \
  v1.0.0
```

The resulting archive contains only files tracked by Git at that tag.

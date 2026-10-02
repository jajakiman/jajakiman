# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build and validate the `jajakiman` GitHub profile README with a responsive local header asset and verified public content.

**Architecture:** GitHub renders one Markdown entry point. A single local SVG supplies the distinctive visual header while native Markdown, links, headings, and `<details>` provide resilient content and interaction without JavaScript or runtime dependencies.

**Tech Stack:** GitHub Flavored Markdown, GitHub-safe HTML, SVG 1.1, PowerShell verification

**Spec:** `docs/superpowers/specs/2026-10-02-github-profile-readme-design.md`

## Global Constraints

- State only facts verified from the public `jajakiman` profile and repositories.
- Use no JavaScript, package dependency, build workflow, external stats card, emoji decoration, or skill percentage.
- Use `#0D1117`, `#F0F6FC`, `#B7C0CC`, `#39C5CF`, and `#9B7BFF` in the SVG.
- Keep every local asset responsive and every interactive element linked to a real destination.

---

### Task 1: Profile Header Asset

**Files:**
- Create: `assets/profile-header.svg`

**Interfaces:**
- Consumes: the visual system and verified identity from the specification
- Produces: `assets/profile-header.svg`, referenced by `README.md`

- [ ] **Step 1: Create the responsive SVG**

Create an SVG with `viewBox="0 0 900 260"`, `role="img"`, accessible title and description, clipped panel corners, structural cyan rules, one violet name accent, and no animation.

- [ ] **Step 2: Parse the SVG and check contrast**

Run:

```powershell
[xml](Get-Content -Raw assets/profile-header.svg) | Out-Null
python "C:\Users\ACER\.agents\skills\antislop-human\contrast-check.py" "#F0F6FC" "#0D1117"
python "C:\Users\ACER\.agents\skills\antislop-human\contrast-check.py" "#B7C0CC" "#0D1117"
python "C:\Users\ACER\.agents\skills\antislop-human\contrast-check.py" "#39C5CF" "#0D1117"
python "C:\Users\ACER\.agents\skills\antislop-human\contrast-check.py" "#9B7BFF" "#0D1117"
```

Expected: XML parse succeeds and all text colors pass WCAG AA for normal text.

### Task 2: Profile README

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: `assets/profile-header.svg` and verified public URLs
- Produces: the profile page rendered by GitHub

- [ ] **Step 1: Write the README**

Add the header, real anchor navigation, `whoami`, evidence-based stack badges, selected project table, one `<details>` section, and public contact links.

- [ ] **Step 2: Validate structure and URLs**

Run a PowerShell assertion script that checks the local SVG exists, each navigation anchor has a matching heading, no forbidden dash exists, and each HTTP URL returns a response below status 400.

Expected: every assertion passes.

### Task 3: Repository Checkpoint

**Files:**
- Track: `README.md`
- Track: `assets/profile-header.svg`
- Track: `docs/superpowers/specs/2026-10-02-github-profile-readme-design.md`
- Track: `docs/superpowers/plans/2026-10-02-github-profile-readme.md`

**Interfaces:**
- Consumes: validated README deliverables
- Produces: a local `main` branch ready to connect to `https://github.com/jajakiman/jajakiman.git`

- [ ] **Step 1: Initialize and inspect Git**

Run `git init -b main`, followed by `git status --short` and `git diff --check`.

- [ ] **Step 2: Commit the validated files**

Run:

```powershell
git add README.md assets/profile-header.svg docs/superpowers/specs/2026-10-02-github-profile-readme-design.md docs/superpowers/plans/2026-10-02-github-profile-readme.md
git commit -m "feat: add interactive profile readme"
```

- [ ] **Step 3: Report publishing status**

If credentials and the remote are available, add the remote and push `main`. Otherwise report the exact remaining commands without changing authentication state.

# GitHub Profile README Design

## Goal

Create the profile repository for `jajakiman` and give Zaky Ryan a distinctive full-stack web profile. The README should borrow the compact, dark, electric tone of the supplied reference without copying its composition or relying on unsupported JavaScript.

## Design Read

Reading this as a personal developer profile for recruiters and other developers, in a compact command-line dossier style, dial **ENERGY 2 / RHYTHM 2 / MOTION 1**.

## Verified Content

- GitHub username: `jajakiman`
- Display name: Zaky Ryan
- Profile line: `detail is everything`
- Location: Indonesia
- LinkedIn: `https://www.linkedin.com/in/zakyryan/`
- CocokIn role: Project Lead and Full Stack Developer
- Technology and project claims must come from public repository metadata or repository documentation.

Do not invent experience, availability, skill levels, metrics, testimonials, learning topics, or missing project descriptions.

## Structure

1. A responsive local SVG header containing the name, handle, role, and profile line.
2. A short command index linking only to real README sections.
3. A compact `whoami` introduction with a plain-language equivalent.
4. A restrained technology list based on public repositories.
5. A Markdown table of selected real projects and verified links.
6. One native `<details>` disclosure for field notes.
7. Explicit GitHub and LinkedIn contact links.

Do not embed third-party statistics or JavaScript.

## Visual System

- Canvas: `#0D1117`
- Primary text: `#F0F6FC`
- Secondary text: `#B7C0CC`
- Structural cyan: `#39C5CF`
- Accent violet: `#9B7BFF`
- System monospace inside SVG; GitHub-native typography elsewhere.
- Square or clipped corners, one structural border, no gradients, glass, grid, shadow, emoji, or broad glow.
- Repeated motif: command prefix `$` and bracketed navigation labels.

The SVG must use a `viewBox`, scale to `width="100%"`, include `<title>` and `<desc>`, and meet WCAG AA contrast.

## Files

```text
README.md
assets/profile-header.svg
docs/superpowers/specs/2026-10-02-github-profile-readme-design.md
```

## Verification

1. Parse the SVG as XML.
2. Check every SVG text color against the background.
3. Confirm local assets and heading anchors exist.
4. Request every external URL and accept successful or redirect responses.
5. Scan copy for unsupported claims, decorative emoji, and forbidden dash characters.
6. Confirm the repository directory is named `jajakiman`.

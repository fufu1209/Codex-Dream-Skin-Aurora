# Codex Dream Skin — macOS / Windows Codex Desktop Themes

[![Validate](https://github.com/Fei-Away/Codex-Dream-Skin/actions/workflows/validate.yml/badge.svg)](https://github.com/Fei-Away/Codex-Dream-Skin/actions/workflows/validate.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)

An open-source Codex Desktop theme and skin tool for macOS and Windows. It injects an interactive theme through loopback CDP without modifying the official `.app`, `app.asar`, WindowsApps package, or code signature. Customize artwork, `theme.json`, homepage hero, sidebar, suggestion cards, composer, and light/dark presentation.

Project: [github.com/fufu1209/Codex-Dream-Skin-Aurora](https://github.com/fufu1209/Codex-Dream-Skin-Aurora) · Sponsor: [fufuapi.xiefucai1209.com](https://fufuapi.xiefucai1209.com)

<p align="center">
  <a href="./README.md">中文</a> · <strong>English</strong>
</p>

<p align="center">
  <strong>Give Codex a face that breathes.</strong><br>
  External themes for the Codex desktop app · Local CDP inject · No official package mutation
</p>

<p align="center">
  One image, one mood · Code with atmosphere
</p>

<p align="center">
  Unofficial. Does not modify <code>.app</code> / <code>app.asar</code> / WindowsApps.
</p>

## Sponsor

<p align="center">
  <a href="https://fufuapi.xiefucai1209.com">
    <strong>Fufu API · AI Creative Infrastructure</strong>
  </a>
</p>

<p align="center">
  <strong>Stable model access · More room to create</strong><br>
  <sub>Fufu API · Connect AI · Power Creation</sub>
</p>

<p align="center">
  Thanks to <a href="https://fufuapi.xiefucai1209.com"><strong>fufuapi.xiefucai1209.com</strong></a> for sponsoring this project.<br>
  The AI model service and the theme installer remain separate by design.
</p>

<p align="center">
  <sub>
    Theme install and API config stay separate — this project never rewrites your provider settings.
  </sub>
</p>

## Gallery

One image, one mood. Real theme previews you can ship:

<p align="center">
  <img src="docs/images/gallery/skin-01.jpg" alt="Pink Custom" width="900"><br>
  <sub>Pink Custom</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-02.jpg" alt="God of Wealth" width="900"><br>
  <sub>God of Wealth</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-03.jpg" alt="Red-White Sci-Fi" width="900"><br>
  <sub>Red-White Sci-Fi</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-04.jpg" alt="Clear Custom" width="900"><br>
  <sub>Clear Custom</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-05.jpg" alt="Inspiration" width="900"><br>
  <sub>Inspiration</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-06.jpg" alt="Purple Night" width="900"><br>
  <sub>Purple Night</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-07.jpg" alt="Hatsune Miku" width="900"><br>
  <sub>Hatsune Miku</sub>
</p>

<p align="center">
  <img src="docs/images/gallery/skin-08.jpg" alt="Stage Black-Gold" width="900"><br>
  <sub>Stage Black-Gold</sub>
</p>

## What it does

- **Real UI** — Sidebar, cards, project picker, and input stay native. Not a fake full-window screenshot.
- **Swappable art** — Drop in an image you like and it becomes your theme.
- **Extensible themes** — macOS and Windows share a `theme.json` schema for names, branding, colors, and background art.
- **Restorable** — One-click restore to the stock look.
- **Safer path** — Local-loopback CDP inject only. No official binary or signature changes.

## Search keywords

Codex Desktop theme, Codex skin, Codex custom theme, Codex UI customization, macOS Codex theme, Windows Codex theme, Codex CDP injector, Codex customization, Aurora Atelier.

## Quick start

Platform scripts are ready — different plumbing, same goal: theme Codex.

| Platform | Dir | Entry |
|------|------|------|
| Apple Silicon / Intel Mac | [`macos/`](./macos/) | Double-click `Install Codex Dream Skin.command` |
| Windows | [`windows/`](./windows/) | `scripts/install-dream-skin.ps1` → `start-dream-skin.ps1` |

More detail:

- Mac: [`macos/README.md`](./macos/README.md)
- Windows: [`windows/SKILL.md`](./windows/SKILL.md)
- Paths: [`docs/platforms.md`](./docs/platforms.md)
- Project notes: [`docs/PROJECT.md`](./docs/PROJECT.md)
- Theme protocol: [`docs/platforms.md`](./docs/platforms.md#主题配置)

## Feedback & contributions

- **Issues:** Use the [issue templates](./.github/ISSUE_TEMPLATE/) (bug / feature). Blank issues are disabled. Please try Verify / Restore self-checks before filing bugs.
- **PRs:** Follow the [PR template](./.github/pull_request_template.md) — describe the change and tick the self-checks you actually ran (e.g. `macos/tests/run-tests.sh`, verify / restore).
- **Local development:** Run `cd macos && npm test` on macOS; for static-only checks, use the Node.js and shell checks mirrored by GitHub Actions. On Windows, run `powershell -File windows/tests/run-tests.ps1`.
- **Before publishing:** Keep the root [`LICENSE`](./LICENSE), `NOTICE`, bilingual READMEs, platform notes, and changelogs in sync. Never commit `auth.json`, API keys, customer screenshots, or local runtime state.

## Safety

- CDP binds `127.0.0.1` only — avoid untrusted local processes while the theme runs.
- Does not touch the official install directory or code signature.
- **Never** rewrites API Key / Base URL; relay and theme stay separate.

## License

- See [`macos/LICENSE`](./macos/LICENSE) (MIT) and [`macos/NOTICE.md`](./macos/NOTICE.md)
- Unofficial; Codex and related rights belong to their owners.
- People / IP art in previews is illustrative only — clear rights before commercial redistribution.

---

Star it, pick a look, and make Codex yours for today.

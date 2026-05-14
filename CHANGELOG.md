# Changelog

All notable changes to this project will be documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [v1.0.0] - 2026-05-13

### Added

- Composite action that generates GitHub stats and top languages SVG cards via `readme-tools/github-readme-stats-action@v1`
- `username` and `token` inputs (required)
- `theme` input with default `tokyonight`; supports all built-in github-readme-stats themes
- `output_dir` input to control where SVGs are saved (default: `profile`)
- `cards` input to selectively generate `stats`, `top-langs`, or both (default: `stats,top-langs`)
- `stats_options` and `top_langs_options` inputs for passing extra query parameters to each card
- `commit_message` input for customizing the auto-commit message (default: `Update README cards`)
- Auto-commit and push of generated SVGs using `github-actions[bot]`
- Skips commit gracefully when cards have not changed since the last run
- `permissions: contents: write` required; documented in README
- Prerequisites section documenting that `actions/checkout@v4` must precede this action
- Token permissions section documenting PAT requirement for private repository stats (`repo` + `read:user` scopes)
- Troubleshooting section covering common failure modes
- MIT License
- CONTRIBUTING.md with contribution guidelines

---

[v1.0.0]: https://github.com/Joydeep2005Banik/readme-stats-cards/releases/tag/v1
# readme-stats-cards

A GitHub composite action that generates and commits GitHub stats and top languages SVG cards to your profile repo.

## Usage

Create `.github/workflows/readme-cards.yml` in your profile repo (`USERNAME/USERNAME`):

```yaml
name: Update README cards

on:
  schedule:
    - cron: "0 3 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: Joydeep2005Banik/readme-stats-cards@v1
        with:
          username: your-github-username
          token: ${{ secrets.GITHUB_TOKEN }}
```

Then add to your `README.md`:

```html
<p align="center">
  <img src="./profile/stats.svg" height=200 />
  <img src="./profile/top-langs.svg" height=200 />
</p>
```

## Inputs

| Input | Required | Default | Description |
|---|---|---|---|
| `username` | yes | - | Your GitHub username |
| `token` | yes | - | GitHub token (`secrets.GITHUB_TOKEN`) |
| `theme` | no | `tokyonight` | Card theme |
| `output_dir` | no | `profile` | Directory to save SVGs |
| `stats_options` | no | `show_icons=true&hide_border=true` | Extra query params for stats card |
| `top_langs_options` | no | `layout=compact&hide_border=true` | Extra query params for top languages card |

# Miku

A work-in-progress Obsidian theme inspired by Hatsune Miku's charcoal, cyan, white, and pink color palette. Dark and light modes are supported.

## Installation

Clone the repository into your vault's theme directory, keeping the local folder name as `Miku`:

```bash
git clone https://github.com/simoncwang/Miku.git /path/to/vault/.obsidian/themes/Miku
```

Restart Obsidian, then select **Miku** under **Settings → Appearance → Themes**.

## Development

Install dependencies once and start the development watcher:

```bash
npm install
npm run dev
```

Edit the modular source files under `src/`. The watcher generates the root-level `theme.css` that Obsidian loads.

```text
src/
├── index.css
├── foundations/
└── components/
```

Before committing, build and validate the theme:

```bash
npm run check
```

Commit both the source changes and generated `theme.css`.

## Releases

To create a patch release:

```bash
npm run check
npm version patch --tag-version-prefix=""
git push --follow-tags origin master
```

Pushing the version tag triggers the GitHub Actions workflow, which validates the build and creates a draft release containing `manifest.json` and `theme.css`.

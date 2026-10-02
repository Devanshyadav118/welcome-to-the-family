# Hosting and Google AI Studio Handoff

## Google AI Studio

Upload the repository or ZIP, then paste [`AI_STUDIO_PROMPT.md`](./AI_STUDIO_PROMPT.md) as the build instruction. Ask the generated app to preserve the included media paths and to keep the website static.

The generated app can be previewed and published through Google AI Studio's available hosting flow. Confirm the current hosting visibility and privacy settings before sharing the URL because the site contains family and child media.

## GitHub-ready structure

This folder is intentionally static:

- `index.html` is the entry point.
- `public/assets/` contains media.
- Markdown files contain the brief, content, and handoff instructions.
- No server, database, API key, or build step is required for the first version.

## Manual GitHub upload

If a GitHub connector is unavailable, create an empty repository and run:

```bash
git init
git add .
git commit -m "feat: add bilingual baby welcome website package"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Do not commit secrets, private API keys, or unapproved family media.

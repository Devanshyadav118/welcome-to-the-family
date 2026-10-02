# Welcome to the Family — Mobile Baby Welcome Website

This repository contains a mobile-first, bilingual family welcome website for a newborn baby girl.

The experience introduces a baby girl to the world through real family photographs, soft nursery illustrations, gentle motion, English/Hindi language switching, and optional narration.

## Current family story

- The baby is a girl.
- Her elder brother is **Gatik**.
- Gatik is two and a half years old.
- The website should describe the baby as a niece/family member, not as the creator's daughter.
- The birth date shown in the current concept is **29 September**.
- The baby's name is intentionally left as `[Baby’s Name]` until supplied.

## Visual direction

Cute, wholesome, handmade, and family-specific. Use blush pink, warm cream, peach, coral, lavender, and muted sage. Use flowers, bows, butterflies, clouds, a pink pram, a small bunny, paper textures, and scrapbook-style photo frames.

Do not use a dark cosmic theme, generic SaaS cards, neon, sci-fi styling, or excessive glitter. Do not imitate Ghibli, Pixar, anime, or another named studio style.

## Run locally

Open `index.html` directly in a browser. It is a static website and does not require a build step.

For a local server:

```bash
python3 -m http.server 4173
```

Then visit `http://localhost:4173`.

## Google AI Studio handoff

Upload this repository or ZIP to Google AI Studio, then paste the full instructions from [`AI_STUDIO_PROMPT.md`](./AI_STUDIO_PROMPT.md). The prompt explains the product, content, design system, interactions, mobile constraints, audio behavior, media handling, and acceptance criteria.

## Media status

The generated illustrations are included under `public/assets/illustrations/`. The original family photos and four generated videos were supplied in the conversation, but their temporary attachment files are no longer available in the current filesystem after interrupted turns. Re-add them under `public/assets/photos/` and `public/assets/video/` using the names in [`MEDIA_MANIFEST.md`](./MEDIA_MANIFEST.md).

## Important privacy note

The final site contains a child and family photographs. Keep the deployed site private or unlisted unless the family explicitly agrees to public sharing. Avoid exposing hospital details, exact location, or unnecessary personal information.

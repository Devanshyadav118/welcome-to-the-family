# Her Diary — how to add a new year

This website is a living book. Each birthday, add one chapter. You never need
to touch the code — just the diary file and the photos.

## The 2-minute birthday update

1. Put the year's photos in `public/assets/photos/` with clear names, e.g.
   `year01-cake.jpg`, `year01-gatik.jpg`. (Or keep using Google Drive IDs —
   see below.)
2. Open `public/data/diary.json` and copy the template block below into the
   `chapters` list (keep the years in order).
3. Fill in the story. Write English first; add Hindi if you like (or leave the
   `hi` text empty and the site will show English).
4. Commit + push. The timeline on the site grows automatically.

## Template — copy, paste, fill in

```json
{
  "year": 1,
  "title": { "en": "One year of you", "hi": "तुम्हारा एक साल" },
  "date": "29 September 2027",
  "story": {
    "en": "What happened this year, in a few warm lines…",
    "hi": ""
  },
  "photos": [
    "public/assets/photos/year01-cake.jpg",
    "public/assets/photos/year01-gatik.jpg"
  ],
  "gifts": [
    {
      "name": { "en": "A tiny silver anklet", "hi": "" },
      "photo": "public/assets/photos/year01-anklet.jpg",
      "story": { "en": "Who gave it, and the story behind it…", "hi": "" }
    }
  ]
}
```

Notes:
- `photos`: use repo paths as above, OR Google Drive file IDs shared as
  "anyone with the link" — put just the ID string, e.g. `"1AbC2dEfGh…"`,
  and the site will load it from Drive automatically.
- `gifts`: each gift gets its name, an optional photo, and the story behind
  the day and the gift — exactly the keepsake you imagined.
- The time capsule on the site opens itself on 29 September 2027; after that
  date it shows the sealed wishes instead of the countdown. Nothing to do.

## Doing it from Google AI Studio

Paste this prompt into AI Studio with the repo connected:

> In public/data/diary.json, add a new chapter for year N following the
> template in DIARY_GUIDE.md. Title: "…". Story: "…". Photos: add these
> files to public/assets/photos/ as year0N-….jpg: [list]. Gifts: [name —
> story]. Keep everything else unchanged.

Then push, and the site updates itself on the next visit.

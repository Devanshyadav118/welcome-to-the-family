# Media Manifest

## Intended folder structure

```text
public/assets/
├── photos/
│   ├── baby-01.jpg
│   ├── baby-02.jpg
│   ├── family-arrival-01.jpg
│   ├── family-arrival-02.jpg
│   ├── family-arrival-03.jpg
│   └── gatik.jpg
├── video/
│   ├── welcome-01.mp4
│   ├── welcome-02.mp4
│   ├── welcome-03.mp4
│   └── welcome-04.mp4
└── illustrations/
    ├── pram-meadow.jpg
    ├── pram-mobile.jpg
    ├── family-garden.jpg
    ├── illustrated-baby.jpg
    ├── stitched-mascots.jpg
    └── floral-hero.jpg
```

## Generated assets included

The repository includes the generated illustration concepts under `public/assets/illustrations/`.

## Original uploads to re-add

The temporary attachment files from the conversation expired or were removed after interrupted turns. Re-add the following original files before publishing:

- `37739.jpg`
- `37717.jpg`
- `c7154fdb-fad9-4ba1-9956-4602ab918244-1_all_22610.jpg`
- `c7154fdb-fad9-4ba1-9956-4602ab918244-1_all_22602.jpg`
- `gemini_generated_video_9e197a85.mp4`
- `gemini_generated_video_2f09d78a.mp4`
- `gemini_generated_video_d82f70b6.mp4`
- `gemini_generated_video_5c75c6e1.mp4`

Rename them to the clean names in the folder structure above. Do not expose hospital metadata or private information in filenames or captions.

## Media preparation

- Photos: export long edge around 1600–2000px, JPEG quality 82–88.
- Videos: create a mobile portrait crop if possible; otherwise use `object-fit: cover` with a poster frame.
- Keep video files under roughly 8–12 MB each when possible.
- Provide poster JPEGs for slow connections.
- Do not autoplay audio.

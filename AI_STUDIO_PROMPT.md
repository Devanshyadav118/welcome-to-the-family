# Google AI Studio Build Prompt

Build a complete mobile-first static website called **Welcome to the Family**.

## Product goal

Create a tender, cute, wholesome digital welcome experience for a newborn baby girl. The site should feel like a handmade family storybook and scrapbook, not a game dashboard and not a generic baby announcement template.

The visitor should be able to scroll through a short story, switch between English and Hindi, listen to the selected language using a user-triggered voice button, view real family photos and videos, and leave a written wish.

## Family context

- Baby: girl; use `[Baby’s Name]` until a name is supplied.
- Birth date: 29 September.
- Elder brother: Gatik, two and a half years old.
- The site is made by a relative welcoming a niece. Never call the creator the mother or father.
- Family structure: mother, father, newborn baby girl, and elder brother Gatik.

## Mobile-first requirement

Design for a phone first at 360–430px wide. Desktop is only a secondary expansion.

- Use portrait 9:16 media when available.
- Use large touch targets of at least 44px.
- Keep the main content in a single vertical flow.
- Avoid dense navigation and tiny text.
- Respect safe areas around notches and browser controls.
- Use `object-fit: cover` carefully for landscape videos.
- Lazy-load gallery media.
- Compress images and use poster images for videos.
- Respect `prefers-reduced-motion`.
- Never autoplay sound. Video may autoplay muted; narration begins only after a user taps a play button.

## Story flow

### Screen 1 — Arrival

Show a soft illustrated nursery scene or pink pram image with a real baby photo reveal.

English:

> Welcome to the family, little one.

> On 29 September, a beautiful baby girl arrived and made the world around her a little brighter.

Hindi:

> परिवार में तुम्हारा स्वागत है, नन्ही बच्ची।

> २९ सितम्बर को हमारे परिवार में एक प्यारी-सी बेटी आई और अपने साथ ढेर सारी खुशियाँ लाई।

Primary action: `Begin the welcome` / `स्वागत शुरू करें`.

### Screen 2 — Meet her

Show the baby's real photos in a swipeable or snap-scrolling gallery.

English:

> She is tiny, peaceful, and already surrounded by so much love.

Hindi:

> वह नन्ही-सी, प्यारी-सी और ढेर सारे प्यार से घिरी हुई है।

### Screen 3 — Gatik's promotion

Use a real or illustrated image of Gatik near the baby/family.

English:

> Gatik has been promoted to Big Brother.
> His new duties include sharing smiles, telling stories, and keeping watch over his tiny sister.

Hindi:

> गतिक को बड़े भाई के पद पर पदोन्नति मिल गई है।
> अब उसकी नई ज़िम्मेदारियों में मुस्कुराहटें बाँटना, कहानियाँ सुनाना और अपनी नन्ही बहन का ध्यान रखना शामिल है।

Use a warm, playful tone. Do not make the child responsible for childcare; this is symbolic and affectionate.

### Screen 4 — Family welcome

Show the family photos and four short video moments as a muted swipeable sequence. Use captions, not hard-coded text inside the video.

English:

> Her first days were filled with familiar voices, warm hugs, happy smiles, and people eager to welcome her home.

Hindi:

> उसके पहले दिन परिचित आवाज़ों, गर्मजोशी भरी झप्पियों, मुस्कुराहटों और उसे अपनाने की खुशी से भरे रहे।

### Screen 5 — Wishes

Show three tappable illustrated objects: a flower, a bow, and a bunny. Each reveals a short wish.

English wishes:

- May you always feel loved.
- May you grow up brave, kind, and curious.
- May your life be filled with laughter and beautiful surprises.

Hindi wishes:

- तुम्हें हमेशा प्यार और अपनापन महसूस हो।
- तुम साहसी, दयालु और जिज्ञासु बनो।
- तुम्हारा जीवन हँसी और सुंदर आश्चर्यों से भरा रहे।

### Screen 6 — Closing

English:

> Welcome to the family, little one.
> Your story has just begun, and all of us are so happy to be part of it.

Hindi:

> परिवार में तुम्हारा स्वागत है, नन्ही बच्ची।
> तुम्हारी कहानी अभी शुरू हुई है और हम सब इसका हिस्सा बनकर बहुत खुश हैं।

Primary action: `Leave a wish` / `अपनी शुभकामना लिखें`.

## Language switch

Place a visible pill switch near the top:

```text
[ English ] [ हिन्दी ]
```

Changing language must update:

1. All visible story copy.
2. Button labels.
3. Captions and wish prompts.
4. The narration language.
5. The transcript.

Store the preference in `localStorage`.

## Audio narration

Do not require separate MP3 files for the first version. Use the browser Web Speech API:

- English: `en-IN` or `en-US`.
- Hindi: `hi-IN`.
- Add a clear play/pause button.
- Let the user stop narration.
- Use a warm, slow, respectful speaking rate around `0.88–0.95`.
- Show the transcript below the player.
- If speech synthesis is unavailable, keep the transcript fully usable and show a small non-blocking message.

## Visual system

Use CSS variables approximately like:

```css
--blush: #f7c7c8;
--peach: #f4a38f;
--cream: #fff8ec;
--coral: #d95d63;
--lavender: #c7b7d9;
--sage: #9eaf8d;
--ink: #4b3540;
```

Typography should feel warm and storybook-like. Use one expressive serif or rounded display face for headings and a highly legible sans-serif for body copy. Avoid all-caps labels and overly decorative script for long text.

Visual motifs:

- Real photos in paper or fabric scrapbook frames.
- Flowers and leaves as edge decorations.
- A pink pram as a recurring visual anchor.
- A small bunny as a guide character.
- Bows, butterflies, clouds, stitched borders, and soft paper grain.
- Gentle reveal transitions, floating petals, and small parallax—not constant motion everywhere.

## Media rules

Use original supplied photos as the authentic family content. Do not alter faces or invent identities. Use generated illustrations only as decorative companions or symbolic scenes.

Use muted videos with poster frames. Videos should not force sound. On mobile, show a play control and a visible caption.

## Accessibility

- All images need meaningful `alt` text.
- Decorative illustrations use empty alt text.
- Buttons must have clear labels.
- Maintain readable contrast.
- Keyboard focus must be visible.
- Support reduced motion.
- Never communicate essential information only through colour or animation.

## Acceptance criteria

The result is accepted only if:

1. It looks intentional and cute on a real phone.
2. The English/Hindi switch changes the whole story.
3. Both language transcripts are visible and readable.
4. Both narrations can be started by tapping a button.
5. Gatik is described as the two-and-a-half-year-old elder brother.
6. The baby is described as the creator's niece/family member, not daughter.
7. Real photos and all available videos are used without distortion.
8. The site works without a build step or paid backend.
9. The page remains useful if media files are missing, with graceful placeholders.
10. It can be deployed directly from a GitHub repository or uploaded as static files.

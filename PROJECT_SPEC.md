# Project Specification

## Name

Welcome to the Family

## One-line description

A mobile-first bilingual storybook website that warmly introduces a newborn baby girl to her family and the world.

## Emotional objective

The visitor should feel that they have opened a handmade family keepsake: personal photographs are gently introduced by illustrated nursery elements, the story can be heard in English or Hindi, and Gatik's promotion to big brother gives the experience a memorable family detail.

## Product boundaries

This is not:

- A horoscope or Kundli application.
- A public social network.
- A medical record.
- A generic baby ecommerce template.
- A game with scores or competition.

This is:

- A scrollable story.
- A private family keepsake.
- A bilingual audio and transcript experience.
- A static hostable site.

## Interaction model

The main interaction is intentional scrolling. Small touch interactions add warmth:

- Tap a flower to reveal a wish.
- Swipe the photo gallery.
- Tap the language switch.
- Tap play to hear the narration.
- Tap a family photo to open it larger.
- Tap the final button to leave a wish.

No scores, timers, login, or forced form completion.

## Motion principles

- One calm entrance sequence.
- Photo frames slide in only when they enter view.
- Petals drift slowly.
- Bunny and small decorative objects can bob gently.
- Use opacity and transform transitions rather than expensive continuous effects.
- Disable non-essential motion under `prefers-reduced-motion`.

## Definition of done

The site is done when it can be opened on a phone, understood without instructions, switched between English and Hindi, narrated by user action, viewed with real media, and shared privately as a single URL.

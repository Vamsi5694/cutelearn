# kids-abc (ABC for me)

A single-page, kid-friendly **alphabet, numbers, colors, and more** learning app. Everything runs in the browser: no build step, no install.

**File:** `kids-abc.html` — open it directly or host it on any static site (GitHub Pages, Netlify, Versel etc.).

## Features

- **ABC (A–Z)** — Pick a letter, then a word. Multiple word/emoji options per letter. Optional **Play** to advance A–Z automatically. Keyboard: **A–Z** when this mode is active.
- **Numbers (1–20)** — Each number has a unique “unit” picture; items are shown in a **2D row layout** (not one long line) for easy counting. Keys **1–9**, **0** = 10, **←** **→** to move; **Play** runs 1–20.
- **Fruits & vegetables** — Tap an emoji in the row or use **Play** or **←** **→**; voice reads the name.
- **Colors** — On the **left:** color name + **swatch**. On the **right:** a familiar example in that color (emoji + label). The **page background** tints to match the color; it returns to the default when you leave this mode. **Play** and **←** **→** work like other list modes.
- **Animals & sounds** — Name plus optional **real short audio clips** for some animals (Wikimedia and similar sources, played via a hidden `audio` / `video` element where needed). *Only a subset of animals have a recorded sound;* others use the speech voice (name + a fun “sound” word). **←** **→** and **Play** supported.
- **Voice** — On/off; uses the browser’s **text-to-speech** where there is no clip. Turn sound on and tap the page once if Safari/mobile blocks audio until a user gesture.
- **Persistence** — Remembers the selected **mode** and **sound on/off** in `localStorage` (if allowed).

## How to run locally

- **Simplest:** double-click `kids-abc.html` or drag it into Chrome / Firefox / Safari / Edge.
- **Optional:** from the project folder, `python3 -m http.server 8080` then open `http://localhost:8080/kids-abc.html` (useful for testing service workers or stricter CORS, though this app does not require it).

## Requirements

- A **modern browser** with **Web Speech API** for voice (`speechSynthesis`). If voice is missing or silent, check browser settings and try again after a tap (especially on iOS).
- **Internet** is used only for **Google Fonts** (Fredoka) and, in Animals mode, for **remote audio** URLs. For fully offline use you could self-host the font and replace clips with local files (would require code changes).

## Accessibility notes

- Large tap targets, `aria` labels on the mode bar and key row, and a live region on the main stage. Reduced-motion preference reduces some decorative animation behavior.

## License

The HTML/CSS/JS in this file are part of your project; add a license in the repository if you publish it. **Animal sound** files are linked from public sources (e.g. Wikimedia Commons); their licenses apply to those audio files, not to this app’s code.

---

*Internal doc for the `kids-abc.html` file in this repo.*

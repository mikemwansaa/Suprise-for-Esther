# This One Is For My Essie 💗

A personal, animated web page built as a love letter — featuring a tap-to-enter intro, a typewriter "code" message, a blooming heart garden animation, a live "time together" counter, background music, and a 4-photo gallery.

## How to view it

Just open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge). No server or install needed.

## Required files before it works fully

A few assets are **not included** in this folder and need to be added manually — the page will still load without them, but these features won't work until they're in place:

| File                | Where it goes       | Purpose                                 |
|---                  |---                  |---|
| `withyou.mp3`       | `Project 3/` (root) | Background music, starts when the intro heart is tapped |
| `images/photo1.jpg` | `Project 3/images/` | 1st photo in the gallery |
| `images/photo2.jpg` | `Project 3/images/` | 2nd photo in the gallery |
| `images/photo3.jpg` | `Project 3/images/` | 3rd photo in the gallery |
| `images/photo4.jpg` | `Project 3/images/` | 4th photo in the gallery |
|`digital-7_mono.ttf` | `Project 3/` (root) | Digital clock font for the time counter (optional — falls back to a default font if missing) |

Filenames must match exactly (case-sensitive), and photos must be `.jpg`. If your images are `.png`, update the extensions in `js/functions.js` under `galleryImages` to match.

## File structure

```
Project 3/
├── index.html              Main page
├── withyou.mp3              Background music (add this)
├── digital-7_mono.ttf        Clock font (add this, optional)
├── css/
│   └── default.css           All styling
├── js/
│   ├── functions.js          Page behavior: timers, gallery, music, lightbox
│   └── garden.js             Heart-garden bloom animation engine
└── images/
    ├── photo1.jpg             Gallery photo 1 (add this)
    ├── photo2.jpg             Gallery photo 2 (add this)
    ├── photo3.jpg             Gallery photo 3 (add this)
    └── photo4.jpg             Gallery photo 4 (add this)
```

## Features

- **Intro gate screen** — a pulsing heart with "Tap the Heart to Continue." Tapping it triggers a burst of little hearts and starts the music. This tap is what lets the browser allow audio playback with sound (browsers block autoplay with sound until the visitor interacts with the page).
- **Typewriter message** — the "code" letter on the left types itself out character by character.
- **Heart garden animation** — after a short delay, a blooming heart shape draws itself on the canvas.
- **Live counter** — shows the elapsed time (days/hours/minutes/seconds) since a date set in `index.html` (search for `together.setFullYear` to change it).
- **Photo gallery** — clicking the heart icon opens a lightbox starting at photo 1, with left/right arrows to cycle through all 4 photos (loops around).
- **Background music control** — a small circular button in the top-right corner to pause/resume the music at any time; the icon switches between a music note and a mute icon.

## Customizing

- **Change the date counter:** edit the `together.setFullYear(...)`, `setHours`, `setMinutes` lines near the bottom of `index.html`.
- **Change the letter text:** edit the content inside `<div id="code">` in `index.html`.
- **Change the signature:** edit `<div class="signature">- Mike</div>` in `index.html`.
- **Change colors/fonts:** edit `css/default.css`.

<div align="center">

# 📐 The Unit Circle

### An interactive trig instrument — drag, step, or play your way around sine and cosine.

![No dependencies](https://img.shields.io/badge/dependencies-none-7C9CFF?style=flat-square)
![Vanilla JS](https://img.shields.io/badge/javascript-vanilla-F2A93B?style=flat-square)
![Single file](https://img.shields.io/badge/build-single%20HTML%20file-FF6B5A?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-EAF1FF?style=flat-square)

![Preview of the unit circle dial rotating, with sine and cosine values updating live](preview.gif)

</div>

---

## What this is

A unit circle you can actually touch. Drag the pin around the dial and watch the angle, its sine, and its cosine update live — as exact fractions like `√3⁄2` at the sixteen standard angles, or as live decimals everywhere in between. Press play and it sweeps itself, like a clock built out of trigonometry.

No build step, no framework, no canvas. One HTML file, inline SVG, and plain JavaScript.

## Features

- **Drag the dial** — grab the coral pin and sweep it anywhere on the circle
- **Snap to the 16 standard angles** — toggle on for exact values (`π⁄4`, `√2⁄2`, `−√3⁄3`...), off for free continuous motion
- **Press play** — a steady automatic sweep with an adjustable speed dial
- **Live readout** — θ in degrees *and* radians, plus sin θ, cos θ, tan θ, switching between exact and decimal automatically
- **Full keyboard support** — tab to the pin, step with the arrow keys, jump home with <kbd>Home</kbd>
- **Responsive** — comfortable on a phone or a widescreen monitor
- **Respects `prefers-reduced-motion`** and ships with visible focus states

## Try it

No installation needed — it's a single static file.

```bash
git clone https://github.com/your-username/unit-circle.git
cd unit-circle
open index.html     # macOS
# or just double-click index.html, or drag it into a browser tab
```

Or publish it in seconds with **GitHub Pages**: push to a repo, enable Pages on the `main` branch, and `index.html` becomes your live demo at `https://your-username.github.io/unit-circle/`.

## Controls

| Action | How |
|---|---|
| Set the angle | Drag the coral pin |
| Step by one mark | Focus the pin, then `←` `→` |
| Jump to 0° | Focus the pin, then `Home` |
| Animate | `Play` / `Pause` button |
| Adjust sweep speed | Speed slider, 0.25× – 2.5× |
| Free vs. exact angles | `Snap to marked angles` checkbox |

## How it's built

- **Geometry** — every tick mark, grid chord, marked-angle dot, and label is computed from a single `MARKS` table and drawn into inline SVG at load time
- **Motion** — dragging maps pointer position straight to an angle with `atan2`; the play loop advances θ with `requestAnimationFrame`, independent of frame rate
- **Exact values** — the sixteen standard angles (multiples of 30° and 45°) carry their textbook-exact sine, cosine, and tangent; everything else falls back to live decimals
- **Type** — [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) for display, [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) for the numeric readout, [Inter](https://fonts.google.com/specimen/Inter) for body copy

## Project structure

```
.
├── index.html      # the entire app — markup, styles, and script
├── preview.gif      # the animation above
└── README.md
```

## License

MIT — use it, fork it, teach with it.

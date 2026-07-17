# buildinamsterdam-clone — design study

A single-file recreation of the layout and interaction patterns of the cases page at
[buildinamsterdam.com/cases](https://www.buildinamsterdam.com/cases), built from scratch as a
design reference.

**This is not a scrape.** All code is original, and all content (project names, descriptions,
images, logo) is placeholder — none of Build in Amsterdam's copy, photography, client imagery, or
branding is included, and this project is not affiliated with or endorsed by them. It exists to
study and reuse the *design patterns*, which is what a repo like this can legitimately hold.

## What it recreates

- Horizontally scrolling case gallery (wheel → horizontal, plus drag-to-scroll with inertia-style easing)
- Staggered column grid: portrait cards (~2:3), 35px gutters, alternating vertical offsets, mixed card heights
- Typography system: grotesque sans, uppercase project name + `·` + sentence-case description
- Pill tags overlaid on card images (blurred translucent background)
- Fixed chrome with `mix-blend-mode: difference` (logo top-left, MENU bottom-right, vertical FILTER WORK control)
- Custom amber cursor dot ("Drag" / "View" states)
- Full-screen filter overlay with large-type tag list that re-lays-out the grid
- Scroll progress bar bottom-left

## Run

Open `index.html` in a browser. No build step, no dependencies.

## Adapt

All cases live in the `CASES` array in `index.html`; palettes in `PALETTES`; column stagger in
`COL_SHIFTS`. Swap the gradient placeholders for real images by replacing the `.visual` div's
background with an `<img>`.

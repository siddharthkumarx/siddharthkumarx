# Maintainers' notes

This repository is the GitHub profile README of Siddharth Kumar: `README.md` and
its picture `header.svg`. Contact on this profile is `siddharth@steadydata.co`.

## Canvas rule (owner decision, 22 Nov 2026)

Every image's outermost background is `#F3F8F7`: never pure white `#FFFFFF`, never
dark `#0B1416`, never transparent with dark text. Cards inside stay `#FFFFFF` with
border `#E2EAE8` and radius 14px. A screenshot of a white page is shown framed: the
page as a card (radius 14, border `#E2EAE8`) on about 40 px of `#F3F8F7`.

- `header.svg`: the first `<rect>` is the canvas (`#F3F8F7`); the three store
  cards and the report row inside it stay `#FFFFFF`.
- Exceptions (none in this repository): website page backgrounds, favicon and
  app-icon tiles, the email-signature logo and the founder photo.

Check before every commit (Node only, no packages):

```bash
node tests/check_canvas.cjs
```

It checks every edge pixel of every tracked PNG and the first `<rect>` fill of every
SVG, and fails on anything else.

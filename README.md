# DreamFAR: Real-Time and Long-Horizon Interaction with Diverse Objects

This `gh-pages` branch holds the built project website. GitHub Pages serves it as-is from the branch root
(`.nojekyll` turns Jekyll off, so every file is served verbatim).

Every URL in the page is relative, so it also works under a project-site subpath such as `/DreamFAR/`.

Contents:

- `index.html`: the page, with its stylesheet inlined
- `main.<hash>.js`: the page script (minified)
- `assets/`: fonts (self-hosted), video rungs (AV1 / VP9 / H.264), posters, figures and `data/drift.json` (the drift curves in Sec. 2.2)

## Preview locally

The videos are streamed with HTTP Range requests, so serve the folder instead of opening `index.html` from disk.
From the repository root:

```bash
npx http-server -a 127.0.0.1 -p 8000 -g   # supports Range requests (python3 -m http.server does not: seeking may stall)
# then open http://127.0.0.1:8000/
```

The live demo is a separate server. It is embedded only after a click, and only on origins that the demo host allows.

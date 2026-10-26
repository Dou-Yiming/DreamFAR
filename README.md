# DreamFAR: Real-Time and Long-Horizon Interaction with Diverse Objects

This `gh-pages` branch holds the built project website. GitHub Pages serves it as-is from the branch root
(`.nojekyll` turns Jekyll off, so every file is served verbatim).

Every URL in the page is relative, so it also works under a project-site subpath such as `/DreamFAR/`.

Contents:

- `index.html`: the page, with its stylesheet inlined
- `main.<hash>.js`: the page script (minified)
- `assets/`: fonts (self-hosted), video rungs (AV1 / VP9 / H.264), posters, figures and `data/drift.json` (the drift curves in Sec. 2.2)

## Preview locally

Videos need a server that supports HTTP Range requests, so opening `index.html` from disk is not enough. From the
repository root:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
# then open http://127.0.0.1:8000/
```

The live demo is a separate server. It is embedded only after a click, and only on origins that the demo host allows.

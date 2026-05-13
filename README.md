# elevenx

Public mirror of the **Codex Studio (beta)** build for the Eldorath illustrated audio book project.

Live: <https://alex-enliven.github.io/elevenx/>

This repo is a static drop of `book-beta.html` (renamed to `index.html`) plus
`assets/`. The canonical source lives in
`~/2026_Claude_Code_Enliven/book-beta.html`. Run `./deploy-elevenx.sh` from
that working tree to push a new build here.

## Local mirror

```
~/2026_Claude_Code_Enliven/book-beta.html        # canonical source
~/2026_Claude_Code_Enliven/publish-beta/         # built bundle (drag-drop or pages)
~/2026_Claude_Code_Enliven/deploy-beta.sh        # rebuilds /publish-beta
~/2026_Claude_Code_Enliven/deploy-elevenx.sh     # pushes /publish-beta to this repo
```

## What lives here

- `index.html` — the entire app, single-file (~1 MB)
- `assets/claude_imagegen_bible/` — YAML spec the composer reads from
- `assets/bible/` — reference imagery
- `assets/parchment-left.jpg` — book texture

All compute (OpenAI / Replicate / fal.ai / Anthropic) is proxied through the
Cloudflare Worker the user configures in **Settings → ① Connection**. This
host serves only static files.

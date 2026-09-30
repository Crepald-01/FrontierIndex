# Frontier Index

A single-page field guide to the frontier AI models of September 2026: benchmarks, arenas, prices, a model picker and a cost calculator. Every number is labelled by who reported it.

No build step and no dependencies. It is plain HTML, CSS and JavaScript, plus Google Fonts loaded from the CDN.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site |
| `404.html` | Custom not-found page (GitHub Pages serves it automatically) |
| `favicon.svg` | Tab icon |
| `.nojekyll` | Tells Pages to skip Jekyll processing |
| `.github/workflows/pages.yml` | Deploys to Pages on every push to `main` |

## Deploy

1. Create a GitHub repository and push these files to the `main` branch.
2. In the repository go to **Settings → Pages → Build and deployment** and set **Source** to **GitHub Actions**.
3. Push again, or run the workflow from the **Actions** tab. The site will be at `https://<user>.github.io/<repo>/`.

To skip the workflow, set Source to **Deploy from a branch**, choose `main` and `/ (root)`. The files work as they are.

## Updating the data

All content lives in the `<script>` block at the bottom of `index.html`, in plain arrays and objects (`M` for models, `B` for benchmarks, `AR` for arenas, `LEDGER`, `DIS` and so on). Edit those and push.

When you change anything, add an entry to the `CL` array (the changelog), update the "Updated …" date in the hero and the "Data snapshot" line in the footer, then push.

Model pages open from `#model=<slug>` links, for example `#model=gpt-6-astra`. The slug is the model name in lower case with punctuation replaced by hyphens. Adding a model to `M` (and, if it has benchmark scores, to `D`) creates its page automatically.

Figures were compiled on 30 September 2026 from vendor announcements and third-party trackers, and they disagree in places. The page lists the conflicts in its "Where sources disagree" section. Check primary sources before relying on any number.

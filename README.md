# PHANTOM — Project Page

Landing page for **PHANTOM: A Large-Scale Dataset of Multimodal Adversarial Attacks for Vision-Language Models**.

Everything lives in a single `index.html` (HTML/CSS/JS, no build step) plus an `images/` folder for all figures.

## Structure

```
.
├── index.html          # the whole page
└── images/
    ├── logo.svg
    ├── teaser-placeholder.svg
    ├── radar-placeholder.svg
    ├── attack-stats-placeholder.svg
    ├── benchmark-placeholder.svg
    └── attack-analysis-placeholder.svg
```

Swap the placeholder SVGs for your real figures and keep the same filenames (or update the `src=` in `index.html`):

- `images/teaser.png` → hero teaser figure
- `images/radar.png` → dataset category radar plot
- `images/attack-stats.png` → attack statistics plot
- `images/benchmark.png` → benchmark overview plot
- `images/attack-analysis.png` → attack analysis figure

The leaderboard table (per-attack ASR per model/category) is already wired up with the real numbers you provided, switchable via the tabs in the **Leaderboard** section.

Before publishing, update the placeholder links in `index.html`:
- Hugging Face dataset URL
- arXiv URL
- BibTeX entry (currently uses a placeholder arXiv id)

## Deploy to GitHub Pages (deploy from a branch)

1. Create a new repo (or use an existing one) and push this folder to it, e.g. on a branch called `main` or `gh-pages`:

   ```bash
   git init
   git add .
   git commit -m "PHANTOM project page"
   git branch -M main
   git remote add origin https://github.com/<your-org>/<your-repo>.git
   git push -u origin main
   ```

2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the branch (`main`, or `gh-pages` if you prefer) and folder `/ (root)`, then **Save**.
5. GitHub will publish the page at `https://<your-org>.github.io/<your-repo>/` within a minute or two.

If you'd rather keep the page on a dedicated `gh-pages` branch:

```bash
git checkout -b gh-pages
git push -u origin gh-pages
```

Then select `gh-pages` as the branch in **Settings → Pages**.

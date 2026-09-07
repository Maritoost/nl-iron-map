# EO4WQ-NL Interactive Iron Map — GitHub Pages files

This folder is ready to publish with GitHub Pages.

## Recommended repository name
`eo4wq-nl-iron-map`

## Files
- `index.html` — website entry page
- `.nojekyll` — tells GitHub Pages to serve the site as plain static files
- `data/segments.json` — map geometry and segment metadata
- `data/timelines/` — timeline data loaded only when needed
- `data/lab/` — in-situ/lab data loaded only when needed

## Publish
1. Create a GitHub repository, preferably named `eo4wq-nl-iron-map`.
2. Make it Public if you use GitHub Free.
3. Add the complete contents of this folder to the repository.
4. In the repository go to: Settings → Pages.
5. Under Build and deployment choose:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
6. Save.

The default website will then be:
`https://YOUR-GITHUB-USERNAME.github.io/eo4wq-nl-iron-map/`

Use the final published URL for the QR code.

## Updating later
Replace the relevant files, commit and push again. GitHub Pages will republish the site.

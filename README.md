# Rishit Lahoti — Portfolio

A cinematic personal portfolio with animated visuals, browsable project cards, competition achievements, and searchable credentials.

## Run locally

This is a buildless HTML, CSS, and JavaScript website. Serve `dist/` with a local web server; opening the HTML directly will prevent the credential collection from loading in some browsers.

With Python installed:

```sh
python -m http.server 4173 --directory dist
```

Open http://localhost:4173 in your browser.

## Deploy

Configure any static hosting service to publish the `dist` directory. No installation or build command is needed. `.openai/hosting.json` retains the existing private Sites project configuration.

## Project structure

- `dist/index.html`: page structure and section content
- `dist/style.css`: responsive design and animation styles
- `dist/app.js`: project records, achievements, search, filters, dialogs, and animated hero
- `dist/credentials.json`: credential metadata
- `dist/assets/`: project artwork, supplied achievement screenshots, and certificate previews
- `dist/certificates/`: original credential PDFs
- `CONTENT-NOTES.md`: content provenance and outstanding information

## Update content

Edit project repository URLs in the `projects` records in `dist/app.js`. Add credential entries to `dist/credentials.json` and place their PDFs and preview images in the corresponding directories. Achievement entries and source-image mappings are in `dist/app.js`.

The website retains pending repository slots and distinguishes stated career totals from individually documented results. See `CONTENT-NOTES.md` before adding or changing claims.

The KINESIS video production workspace is a separate project and is not part of this website source. The website currently does not embed that video.

## Vercel

The root-level `vercel.json` publishes `dist/` directly without a framework, installation, or build step. Import this repository with **Root Directory** left at the repository root (`.`). Do not set Root Directory to `dist`, because the configuration already selects that output directory.

After changes reach `main`, use the deployment created from the latest commit. If automatic deployments are disabled, redeploy from Vercel's Deployments tab. Older deployment-specific URLs continue to point to older deployments.

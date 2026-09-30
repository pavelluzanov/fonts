# Handwriting Font Builder

Static site, no backend. Hosted via GitHub Pages from `/docs`.

## Setup on GitHub
1. Push this repo.
2. Repo Settings → Pages → Source: "Deploy from a branch" → Branch: `main` → Folder: `/docs`.
3. Site will be live at `https://<username>.github.io/<repo>/` within a minute or two.

## Current state
- Template download: generates 2 PNG pages (client-side canvas), matches the
  same grid geometry (baseline at 30% up from box bottom, cell = 32mm) used
  in the original Python pipeline.
- Upload + baseline detection: wired and testable. Upload 2 scanned pages,
  check the log panel for detected baseline row counts (should read 7 for
  each full page).
- Crop → trace → font assembly: NOT yet wired. This is the next stage,
  deliberately held back until baseline detection is confirmed working on
  real scans in a real browser (this is the step that broke twice during
  local prototyping and needs real browser testing, not simulated).

## Testing checklist for this stage
- [ ] Download template button produces 2 printable PNGs
- [ ] Print, draw a few test letters, scan/photo, upload both
- [ ] Log shows "detected 7 baseline rows" for both pages
- [ ] If row count is wrong, note image dimensions + any photo editing applied

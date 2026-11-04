# PROSPEK — Prospect List

A single-page prospect database for unit trust consultants. Log leads with name,
WhatsApp number, remarks, an attitude rating, and an income estimate; sort by any
column; tap a number to open WhatsApp.

- **No backend, no build step.** One `index.html` file.
- **Private by default.** Data is saved in the browser's local storage on the
  device you use — nothing is uploaded anywhere.
- **Backup / move devices.** Use the ⤓ menu to export a CSV, then paste it back in
  on another browser.

## Deploy to GitHub Pages

### Option A — deploy from a branch (simplest)

1. Create a new repository (e.g. `prospek`) and push these files to the `main`
   branch, with `index.html` at the repo root.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose branch **`main`** and folder **`/ (root)`**, then **Save**.
5. Wait ~1 minute. Your site appears at
   `https://<your-username>.github.io/<repo-name>/`.

### Option B — deploy with GitHub Actions

The included `.github/workflows/deploy.yml` publishes the site on every push to
`main`. To use it: in **Settings → Pages → Source**, choose **GitHub Actions**,
then push. (Delete this file if you use Option A.)

## Files

| File | Purpose |
|------|---------|
| `index.html` | The whole app. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (skip Jekyll). |
| `.github/workflows/deploy.yml` | Optional Actions-based deploy (Option B). |

## WhatsApp numbers

Malaysian numbers are auto-converted to international format for the link:
`019-706 5328` → `wa.me/60197065328`. Numbers starting with `0`, `60`, or `+60`
are all handled.

# Gene Keys Evolution Dashboard

A living, cloud-synced map of Dreco's Gene Keys Hologenetic Profile — shadows, gifts & awakening. Built on the **Centauri cloud** architecture: one self-contained `index.html`, Firebase Firestore real-time sync (no accounts, no login), installable as a PWA.

**Live:** `https://planetxentauri.github.io/<repo-name>/`

## What syncs
Real-time across every device that opens the URL, via Firebase Firestore (project `todo-107e0`, collection prefix `gk_`):

- `gk_freq` — your current frequency (Shadow / Gift / Siddhi) for each of the 11 spheres.
- `gk_entries` — your contemplation journal / transformation timeline.
- `gk_meta` — first-run "day one" marker for the days-on-path counter.

The sync dot in the header shows status: **connecting** (gold), **synced** (green), **sync error / offline** (red). If the cloud is unreachable the app still opens and shows the last synced data from a local mirror; writes resume when you're back online.

## Files
- `index.html` — the entire app (HTML + CSS + JS inline).
- `manifest.json`, `sw.js`, `icon.svg` — PWA install + offline shell.

## Deploy (GitHub Pages)
Deploy from `main` branch `(root)`. Push updates by replacing files (web upload is fine).

If an upload-triggered deploy fails with *"Deployment failed, try again later"* and the site doesn't update within ~3 min: make any tiny edit to this README via GitHub's web editor to trigger a fresh build, or re-run the failed `pages-build-deployment` from the **Actions** tab.

**Cache check:** fetch the live URL with `?check=<timestamp>` and `cache: no-store` to confirm the new version is served.

## Notes
- No secrets in the repo. The Firebase web config is client-side (public by design, protected by Firestore rules).
- Gene Keys teaching text is a faithful rendering of Richard Rudd's system.

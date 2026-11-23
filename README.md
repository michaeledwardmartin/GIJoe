# G.I. Joe Personnel Database — v2

Static, mobile-friendly GitHub Pages app for the 1982–1994 A Real American Hero era.

## Install / update

Upload **all four files** from this ZIP directly to the same folder as your currently published `index.html`:
- `index.html`
- `styles.css`
- `script.js`
- `characters.json`

**No `data/` folder is needed.** Commit all four files, wait for GitHub Pages to deploy, then hard-refresh (Ctrl+Shift+R). The `?v=2` asset URLs avoid cached old scripts.

## Existing collection

Uses the same `localStorage` key (`arah-owned-v1`) and original release IDs as v1. Your owned selections should persist **when you use the same published URL and browser**. Changing domains or clearing browser data may lose the local collection. For backup, save your existing `characters.json` before replacing files and consider browser storage backup.

## What's new

- 33 starter personnel records, including an expanded early 1982–1983 roster.
- Browse year buttons for the entire 1982–1994 span. This is **not yet a complete 1982–1994 catalog**.
- Two image slots in personnel detail, and optional local image paths in JSON.
- More explicit unverified-field placeholders, and source archive links.
- Responsive layout and preserved owned tracking.

## Add photos / file cards (only if you have permission)

Create `images/` and put permitted images there. For a character in `characters.json`, set:

```json
"image": "images/snake-eyes.jpg",
"fileCardImage": "images/snake-eyes-card.jpg"
```

For now, the app deliberately does not hotlink or redistribute 3DJoes' photography or scans. Open the 3DJoes links to inspect the originals. The fields are a mix of abbreviated starter data and new catalog entries; verify them against original file cards before publicizing them as complete transcriptions.

## Data model

Each character has `id`, `codeName`, `realName`, `faction`, `birthplace`, `primarySpecialty`, `secondarySpecialty`, `rank`, `firstYear`, `summary`, `image`, `fileCardImage`, `verification`, `referenceUrl`, and `releases` (array of `{id,year,version}`). The current model is backward compatible with v1; as the database grows, add per-release file-card metadata rather than assuming every version has identical details.

## Reference sources

- https://www.3djoes.com/mobile.html (1982/1983 catalog lists)
- https://www.3djoes.com/the-gi-joe-yearbook-a-visual-index-of-carded-figures.html
- https://www.3djoes.com/the-gi-joe-rolodex-the-digital-file-card-repository.html

Fan project, unaffiliated with Hasbro or 3DJoes.

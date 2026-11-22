# G.I. Joe Personnel Database (1982–1994)

Static, responsive fan-made GitHub Pages prototype. No build tools, API keys, frameworks, or paid hosting required.

## Publish on GitHub Pages

1. Create a new GitHub repository (e.g. `gi-joe-personnel`).
2. Upload **index.html**, **styles.css**, **script.js**, and the **data** folder containing `characters.json` to the repository root (not inside an extra parent folder).
3. Go to **Settings → Pages → Build and deployment**.
4. Choose **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
5. Open `https://YOUR-USERNAME.github.io/gi-joe-personnel/` after deployment.

The entry page must be named `index.html`. The README is not the website.

## Local preview

From this folder run `python3 -m http.server 8000` and open `http://localhost:8000`.

## Data model

`data/characters.json` contains an array of characters with `id`, `codeName`, `realName`, `faction`, `birthplace`, `primarySpecialty`, `secondarySpecialty`, `rank`, `firstYear`, `summary`, and `releases[]`. Each release has `id`, `year`, and `version`. The character is distinct from its figure releases; this enables multiple versions of a character.

Missing/unverified values are `null`. The initial seed contains 20 characters and 21 release records, **not** the complete 1982–1994 catalog. Years with no seeded entries show zero results. Collection tracking uses browser localStorage (per browser/device, not synchronized).

## Expansion plan

- Validate each release against the specific original file card, including changing specialties/ranks.
- Split `releases` into a dedicated release dataset with package type, variant, accessories, image permissions, and source URLs.
- Add 1982–1994 releases in verified batches.
- Add licensed/permitted photos or link to original archive; do not automatically scrape or rehost copyrighted images or text.
- Add import/export for owned collections and optional PWA offline support.

## Sources and rights

- 3DJoes file-card Rolodex: https://www.3djoes.com/the-gi-joe-rolodex-the-digital-file-card-repository.html
- 3DJoes figure yearbook: https://www.3djoes.com/the-gi-joe-yearbook-a-visual-index-of-carded-figures.html
- Reference roster: https://en.wikipedia.org/wiki/List_of_G.I._Joe:_A_Real_American_Hero_action_figures

G.I. Joe and related characters belong to their respective rights holders. This is an unofficial fan prototype, not affiliated with Hasbro. Source links are provided instead of rehosting archival images and file-card biographies.

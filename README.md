# G.I. Joe Personnel Database v3 — GitHub Pages

## Deploy
Upload **index.html, script.js, styles.css, characters.json** to the SAME folder at the root of your GitHub Pages publishing branch. Replace existing files, then hard-refresh. The app loads `./characters.json`.

## New in v3
- Edit real names, specialties, birthplace, rank, summary, and figure/file-card image paths inside each character detail.
- Edits persist in your current browser using `arah-edits-v3`.
- **Export updated database JSON** downloads a replacement `characters.json` that you can commit to GitHub to publish your edits.
- **Import database JSON** previews a compatible expanded roster; export and commit it to make it permanent.
- **Back up owned list** downloads your owned release IDs. The existing `arah-owned-v1` tracker remains unchanged.
- All 33 starter characters are retained; data is NOT represented as a complete or fully verified catalog.

## Add images
You must supply images you own or are licensed to display. For example upload `images/snake-eyes.jpg` to GitHub, then enter `images/snake-eyes.jpg` in the figure photo field. The same approach works for a file-card image. The app does not bundle or hotlink copyrighted archive images. External archive links remain available.

## Data structure
`characters.json` is an array of characters with `id`, `codeName`, `faction`, `firstYear`, fields, `image`, `fileCardImage`, and a `releases` array (`id`, `year`, `version`). Keep release IDs stable to preserve owned selections.

## Important
Browser edits are not automatically published to GitHub. Export the updated database and replace `characters.json` in the repository. Do not import an owned-backup JSON as a character database.

# T.E. Greenway site

Static multi-page site for GitHub Pages.

| File | What it is |
|---|---|
| `index.html` | Landing: name, one line, three works as images |
| `works.html` | Works grid, links to each artwork page |
| `lazarus.html`, `icarus.html`, `ishtar.html` | One page per artwork |
| `about.html` | Statement, bio, exhibitions |
| `dispatches.html` | Pulls latest Substack posts automatically |
| `contact.html` | Email, Instagram, editions |
| `styles.css` | All styling (rarely needs touching) |

## How to update

**Add a new artwork**
1. Upload the image file to the repo (no spaces in the filename).
2. Duplicate an artwork page (e.g. `lazarus.html`), rename it
   (e.g. `newwork.html`), and edit the image filename (it appears twice),
   title, year, description and metadata. The comments in the file mark
   what to change.
3. In `works.html`, copy one `<a class="tile">` block and point it at the
   new page. Newest first. Do the same in `index.html` if you want it
   featured on the landing page.

**Add an exhibition**: in `about.html`, find `EDIT EXHIBITIONS HERE` and
copy one `<li>` line. Newest at the top.

**Blog posts**: nothing to do. `dispatches.html` reads the Substack RSS feed
(`tegreenway.substack.com/feed`) on each visit, so publishing on Substack
updates the site automatically. If the feed is unreachable it shows a direct
Substack link instead of breaking.

**Change colours or tracking**: the palette and the `--track` value (-75)
live at the top of `styles.css`.

## Deploying

Push everything to the `grnwysite` repo root (main branch). Keep the artwork
image files (`lazarus_archive_scan.jpg`, `Icarus_archive_scan.jpg`,
`Ishtar_2026.jpg`); the pages reference those exact filenames. GitHub Pages
redeploys on its own.

## Notes

- Headings use Libre Franklin 900 tracked at -75, standing in for Franklin
  Gothic Heavy (used automatically if a visitor has it installed).
  IM Fell English italic is reserved for artwork titles and the statement.
- The gold orb favicon is `favicon.svg`.
- Each artwork page has a lightbox: click the image, close with the button,
  a click outside, or Escape.

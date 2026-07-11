[README.md](https://github.com/user-attachments/files/29920511/README.md)
# T.E. Greenway — site

Static site for GitHub Pages. Three files matter:

| File | What it is |
|---|---|
| `index.html` | The main page — hero, about, works, contact |
| `dispatches.html` | Blog page — pulls latest Substack posts automatically |
| `styles.css` | All the styling (you rarely need to touch this) |

## How to update

**Add a new artwork** — open `index.html`, find the `SELECTED WORKS` section.
Copy one whole `<article class="work-piece">…</article>` block, paste it at the
top of the list, and change: the image filename (it appears twice), the alt
text, the title, year, description and metadata lines. Add `class="work-piece
reverse"` to alternate which side the image sits on. Upload the image file to
the repo alongside the HTML.

**Add an exhibition** — in `index.html`, find `EDIT EXHIBITIONS HERE` and copy
one `<li>` line. Newest at the top.

**Blog posts** — nothing to do. `dispatches.html` reads the Substack RSS feed
(`tegreenway.substack.com/feed`) each time the page loads, so publishing on
Substack updates the site automatically. If the feed is ever unreachable, the
page shows a direct link to Substack instead of breaking.

**Change colours** — the palette lives at the top of `styles.css` under
`:root`. Edit the hex values there and the whole site follows.

## Deploying

Push the files to the `grnwysite` repo (main branch, root folder) and GitHub
Pages does the rest, same as before. Keep artwork image filenames free of
spaces.

## Notes

- The gold orb favicon is `favicon.svg` (you can delete the old `.ico`).
- Fonts load from Google Fonts: Libre Franklin 900 (structural headings —
  stands in for Franklin Gothic Heavy, tracked at -75; if a visitor has the
  real Franklin Gothic Heavy installed, it's used automatically), IM Fell
  English (artwork titles and the statement quote), Hanken Grotesk (body),
  Courier Prime (metadata labels). The tracking lives in `--track` at the
  top of `styles.css`.
- The lightbox closes via the button, clicking outside, or the Escape key.

# Archive: old lukehoffmann.com content

Images, text, and the interactive code demos carried over from the old Jekyll
site, kept as plain files so they can be browsed on GitHub and mined for the
new site. Nothing here is built or deployed. Text is unchanged from the
original; only image paths (now relative) and old layout front matter were
touched.

## Layout

| Folder | Contents |
|---|---|
| `blog/<date>-<slug>/` | College blog posts (`index.md`) with their photos alongside |
| `blog/unpublished-change-of-life/` | Photos for a post that was never written |
| `projects/<slug>/` | p5.js project write-up (`index.md`), cover render, and runnable `demo/` |
| `projects/_shared/` | Libraries the demos load: p5.js 1.11.2, canvas helper, `geometry` + `colorhandler` bundles |
| `projects/radar-mini-map/`, `senior-parking-spot/` | Images only, never had a page |
| `school/zemeckis/` | AP English Lit tribute page, written analysis, and presentation PDF |
| `brand/` | Headshot, "L" logo (SVG variants), favicons, social and UI icons |

## Old-site details worth carrying forward

- Domain: `lukehoffmann.com`, served by GitHub Pages via a root `CNAME` file
  (removed). Re-add it if the new site deploys on GitHub Pages.
- Contact email on the old site: `hello@lukehoffmann.com`
- GitHub: `github.com/luke-hoffmann`; LinkedIn: `linkedin.com/in/lukeh351`
- Old tagline (commented out on the home page): "Mathematics student focused on problem solving"
- Old meta description: "Personal portfolio of Luke Hoffmann featuring programming projects, visualizations, and interactive experiments."
- Brand colors (old Tailwind theme): obsidian `#2a2d34`, orange `#ff7538`,
  cobalt `#758596`, light grey `#d9d9d9`. The "L" logo is orange on obsidian.
- Old fonts: Alef (headings), Signika Negative, Yrsa (Google Fonts)

## Running the demos

Open any `projects/<slug>/demo/index.html` directly in a browser; no server or
build step. Each page recreates the canvas and controls the old Jekyll layout
provided, and loads the project's scripts plus `_shared/` exactly as the live
site did at `795242f`. `rotating-cube-3d` comes from an earlier version of the
site (before `66a34a6`).

The `geometry` library is a compiled bundle (`index.global.js` for the
browser, `index.js` as an ES module, `index.d.ts` for its API). The readable
plain-JS version it replaced (`Vector`, `Triangle`, `Mesh`, `Light`, ...) is
in history at `66a34a6^:assets/js/project-scripts/Geometry/`.

## Recovering removed code

The Tailwind setup, Jekyll layouts, jQuery (unused by any demo), and the
unminified p5.js were deleted. Everything is in git history at `795242f`, the
last commit of the old site:

```sh
git show 795242f:assets/js/project-scripts/3D-convex-hull.js
git checkout 795242f -- assets/js/project-scripts   # restore a folder
```

## Notes

- The film posters in `school/zemeckis/images/` are studio artwork; don't
  republish them on the new site.

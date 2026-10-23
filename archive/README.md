# Archive: old lukehoffmann.com content

Images and text carried over from the old Jekyll site, kept as plain Markdown
so it can be browsed on GitHub and mined for the new site. Nothing here is
built or deployed. Text is unchanged from the original; only image paths
(now relative) and old layout front matter were touched.

## Layout

| Folder | Contents |
|---|---|
| `blog/<date>-<slug>/` | College blog posts (`index.md`) with their photos alongside |
| `blog/unpublished-change-of-life/` | Photos for a post that was never written |
| `projects/<slug>/` | p5.js project write-ups and cover renders |
| `projects/radar-mini-map/`, `rotating-cube-3d/`, `senior-parking-spot/` | Images only, never had a page |
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

## Recovering removed code

The interactive p5.js demos, Tailwind setup, and Jekyll layouts were deleted.
They live in git history at commit `795242f` (the last commit of the old site):

```sh
git show 795242f:assets/js/project-scripts/3D-convex-hull.js
git checkout 795242f -- assets/js/project-scripts   # restore a folder
```

## Notes

- The film posters in `school/zemeckis/images/` are studio artwork; don't
  republish them on the new site.

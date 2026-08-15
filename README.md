# meliksahb.github.io

Personal academic website — single static HTML file, no build system.

## Deploy (first time, ~15 minutes)

1. On GitHub, create a **new public repository** named exactly:
   `meliksahb.github.io`
   (The name must match your username — that's what makes it a "user site"
   served at the root URL.)

2. Add these files to the repository root:
   - `index.html`
   - `assets/Meliksah_Besir_CV.pdf`   (included — the 2-page CV)
   - `assets/video/projects.mp4`      (included — 13.5 MB, pre-compressed for web;
                                       GitHub's per-file limit is 100 MB, so never
                                       upload the 154 MB original)
   - `assets/img/projects-poster.jpg` (included — video poster frame)
   - `assets/img/profile.jpg`         (ADD THIS — a photo of you, ~600×600px, <300 KB)

   Either drag-and-drop via the GitHub web UI ("Add file → Upload files"),
   or from a terminal:
   ```bash
   git clone https://github.com/meliksahb/meliksahb.github.io.git
   cd meliksahb.github.io
   # copy index.html and assets/ in
   git add -A
   git commit -m "Initial site"
   git push
   ```

3. That's it. For a repo named `<username>.github.io`, GitHub Pages is enabled
   automatically from the main branch. Check **Settings → Pages** — it should
   show "Your site is live at https://meliksahb.github.io". First build takes
   1–3 minutes.

4. Verify: open https://meliksahb.github.io in a private window and click
   every link.

## Before/after going live — TODO checklist

Titles, author lists, Scholar link, CV PDF, and the project video are all done.
What's left:

- [ ] Add `assets/img/profile.jpg`, then swap the initials block for the
      `<img>` tag (instructions at the TODO comment in index.html).
- [ ] Optional: replace project-card patterned placeholders with real
      images/GIFs — instructions in the CSS comment above `.project-media`.

## Updating the site later

Edit `index.html`, commit, push. The site redeploys automatically in ~1 minute.
Typical updates take 2 minutes: add a News line when a paper is accepted,
move a publication from "Under review" to "Accepted".

## Add the URL everywhere

Once live, add `meliksahb.github.io` to: your CV header, LinkedIn contact
section, GitHub profile, Google Scholar homepage field, and email signature.

## If you outgrow a single file

The community-standard alternative is **al-folio** (Jekyll theme): BibTeX-driven
publication lists, a blog, news collections, dark mode — at the cost of a
Ruby/Jekyll build via GitHub Actions and more maintenance surface. Migration
path: fork github.com/alshedivat/al-folio, rename the fork to
`meliksahb.github.io`, and port this content into `_bibliography/papers.bib`
and `_config.yml`. Worth it if you start blogging or pass ~15 publications;
overkill before that.

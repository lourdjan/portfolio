# Portfolio site — project structure

```
portfolio/
├── index.html
├── photo.jpg                     ← your hero photo (add this)
├── README.md
└── assets/
    ├── css/
    │   └── style.css             ← all site styles (was inline in the original file)
    └── images/
        └── projects/             ← thumbnails / GIFs for the Projects section
            ├── sales-dashboard.gif
            ├── automated-reporting.gif
            └── kpi-suite.gif
```

## What changed

1. **HTML and CSS are now separate files.** `index.html` links to
   `assets/css/style.css` instead of using an inline `<style>` block.

2. **Projects section** — each project card now has:
   - A `.project-thumb` image slot at the top of the card.
   - A **"View project ↗"** button at the bottom.

   To use it:
   - Drop your thumbnail image or GIF into `assets/images/projects/`
     (any image host/repo folder works — this is just the local one).
   - Update the `src` in `index.html` to point to your file, e.g.:
     ```html
     <img src="assets/images/projects/sales-dashboard.gif" alt="...">
     ```
   - Update the matching `<a href="#" class="project-link">` to your
     YouTube video, GitHub repo, or live demo link.

3. **Services section** — added a **"Let's start a project →"** button
   below the service cards (`id="start-project-btn"`). Update its `href`
   in `index.html` to your Google Form link once you have it:
   ```html
   <a href="https://forms.gle/your-form-id" ... id="start-project-btn">Let's start a project →</a>
   ```

## Notes

- The three project thumbnails referenced (`sales-dashboard.gif`,
  `automated-reporting.gif`, `kpi-suite.gif`) don't exist yet — add your
  own files with those names, or change the filenames in `index.html`
  to match whatever you upload.
- If you'd rather host images elsewhere (e.g. an Imgur/GitHub `assets`
  repo, a CDN), just swap the `src` for the full URL instead of a local
  path — no other changes needed.

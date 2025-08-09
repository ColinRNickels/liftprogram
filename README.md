# Lifting Program — GitHub Pages Site

This repository hosts a simple static site for your A–B–C lifting program.

## Files
- `index.html` — iPhone-friendly version (no `<dialog>`, no transform scaling, larger tap targets).
- `dense.html` — Desktop/tablet “dense + detail” version with a drawer and videos.

## Quick Deploy (GitHub Pages)
1. Create a new repository on GitHub (public is simplest).
2. Upload `index.html`, `dense.html`, and this `README.md` to the root of the repository.
3. In the repo: **Settings → Pages**.
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` (or `master`) and **/ (root)**, then **Save**.
4. Wait 1–2 minutes. Your site will be live at:  
   `https://<your-username>.github.io/<repo-name>/`

The `index.html` is the default homepage. Access the dense version at:  
`https://<your-username>.github.io/<repo-name>/dense.html`

## Optional: Custom Domain
- In **Settings → Pages**, add your domain (e.g., `lift.yourdomain.com`).
- Create a `CNAME` file in the repo root with just the domain name.
- Add the required DNS records at your registrar (CNAME to `<your-username>.github.io`).

## Local Workflow (CLI)
```bash
# From an empty project folder
git init
git remote add origin https://github.com/<your-username>/<repo-name>.git

# Add files
git add index.html dense.html README.md
git commit -m "Initial commit: lifting program site"
git branch -M main
git push -u origin main
```

Then enable Pages as above (Settings → Pages).

## Notes
- Everything is client-side; no build step needed.
- Videos are YouTube embeds; if a gym network blocks them, open in Safari or on cellular.
- The iPhone version saves set checkboxes in localStorage per browser/device.

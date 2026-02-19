# Minimal Academic Homepage (GitHub Pages)

A plain HTML + CSS, single-page academic homepage with:
- Left sidebar navigation (anchors)
- Main content sections on the right
- Responsive behavior for mobile
- No JavaScript, no frameworks

## Files

- `index.html`
- `stylesheet.css`
- `images/profile.jpg` (add your image here)
- `cv.pdf` (optional, for CV link)

## Quick Edit Guide

In `index.html`, replace:
- Name, title, affiliation, intro text
- `<scholar_url>`, `<github_url>`, `<email>`
- Publication/news placeholders
- Canonical URL (`https://example.com/`) and OpenGraph fields

## Deploy to GitHub Pages

1. Create a GitHub repo.
   - User site option: `username.github.io`
   - Project site option: any repo name (e.g., `homepage`)
2. Upload these files to the repo root.
3. Commit and push.
4. In GitHub: `Settings` -> `Pages`.
5. Under **Build and deployment**:
   - Source: `Deploy from a branch`
   - Branch: `main` (or `master`) and `/ (root)`
6. Wait for deployment and open the provided Pages URL.

## Optional: Cloudflare Custom Domain

1. In GitHub repo:
   - `Settings` -> `Pages` -> `Custom domain`
   - Enter your domain, e.g. `www.yourdomain.com`
   - Save (GitHub creates/uses `CNAME`).
2. In Cloudflare DNS:
   - For apex domain (`yourdomain.com`):
     - `A` record -> `185.199.108.153`
     - `A` record -> `185.199.109.153`
     - `A` record -> `185.199.110.153`
     - `A` record -> `185.199.111.153`
   - For `www`:
     - `CNAME` -> `username.github.io`
   - Set proxy to **DNS only** (gray cloud) during setup.
3. In Cloudflare SSL/TLS:
   - Use `Full` or `Full (strict)`.
4. Back in GitHub Pages:
   - Ensure **Enforce HTTPS** is enabled.
5. (Optional) Turn Cloudflare proxy back on after HTTPS is working.

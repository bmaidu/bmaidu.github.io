# Personal website starter (GitHub Pages + Jekyll + Scholar)

This repo is a ready-to-deploy template for a simple academic-style personal website with:
- About page
- Publications (from BibTeX via **jekyll-scholar**)
- CV link
- Custom domain: **bmaidu.com**

## 1) Create your GitHub repo
1. On GitHub, create a new public repository named **<your-username>.github.io** (replace with your username).
2. Clone that empty repo locally, then copy the contents of this folder into it (or upload via the GitHub web UI).
3. Commit and push.

## 2) Enable GitHub Pages (GitHub Actions mode)
1. In your repo: **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. The provided workflow (`.github/workflows/pages.yml`) will build with Jekyll (including plugins) and deploy to Pages.

## 3) Set your custom domain (bmaidu.com)
- In **Settings → Pages**, add `bmaidu.com` as the **Custom domain** and save.
- This creates (or manages) the `CNAME` for you; the CNAME file in the repo is optional when using Actions.

### DNS records to set at your registrar
For the apex/root (`bmaidu.com`), create **four A records** pointing to GitHub Pages IPs:
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

For **www.bmaidu.com**, create a **CNAME** to `<your-username>.github.io` (replace with your GitHub username).

After DNS propagates, return to **Settings → Pages** and check **Enforce HTTPS**.

## 4) Edit site content
- `_config.yml` — set your name, social links, and site options.
- `_pages/about.md` — your bio.
- `_pages/publications.md` — renders the bibliography from `_bibliography/papers.bib`.
- `assets/CV.pdf` — replace with your actual CV file (keep the same path or update the link).

## 5) Local preview (optional)
- Install Ruby + Bundler, then run:
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
- Open http://127.0.0.1:4000 to preview. Stop with Ctrl+C.

---

### Notes
- If you rename the domain later, update **Settings → Pages** and your DNS.
- The theme here is **minima**; swap to any theme by editing `_config.yml` and `Gemfile`.

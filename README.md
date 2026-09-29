# shantanu-roy-site

Personal consulting website for Dr. Shantanu Roy — AI/ML Consultant, Basel.

**Stack:** plain HTML/CSS, zero build step. Deployed on Cloudflare Pages directly from this repo.

## Structure

```
index.html            Home page (hero, services, about, experience, writing teaser, contact)
writing.html          Article index — add a row here for each new article
posts/                One HTML file per article
posts/post-template.html   Copy this to create a new article
assets/style.css      All styling (CSS variables at the top control colors/fonts)
assets/photo.jpg      Photo — replace this file (keep the name, or update index.html)
```

## Publishing a new article

1. Copy `posts/post-template.html` → `posts/my-new-article.html`
2. Edit title, date, and body
3. Add a row in `writing.html` (newest on top)
4. `git add . && git commit -m "new article" && git push` — Cloudflare deploys automatically

## Deploying to Cloudflare Pages (first time)

1. Push this folder to a GitHub repo:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/YOUR_USER/shantanu-roy-site.git
   git push -u origin main
   ```
2. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**
3. Select the repo. Settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `/`
4. Deploy. You get a `*.pages.dev` URL; add a custom domain under **Custom domains**.

## Contact form

The form on the homepage posts to Formspree. Create a free form at https://formspree.io
and replace `YOUR_FORM_ID` in `index.html`.

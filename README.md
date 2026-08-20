# zarazhao.com — personal site

A 4-page personal site: **Home**, **About**, **My Work**, **My Thoughts**.
Plain HTML/CSS/JS — no build step, no dependencies to install.

## Structure

```
index.html      → homepage
about.html      → about page
work.html       → portfolio / project grid
thoughts.html   → blog-style notes list
css/style.css   → all styles (design tokens at the top)
js/main.js      → mobile nav, scroll reveal, work filters, form UI
```

## Preview locally

Just open `index.html` in a browser, or run a quick local server:

```bash
cd zara-site
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a new repo on GitHub (e.g. `zara-site`).
2. Push these files to it:
   ```bash
   cd zara-site
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/zara-site.git
   git push -u origin main
   ```
3. On GitHub: go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
5. Your site will be live in a minute or two at:
   `https://YOUR_USERNAME.github.io/zara-site/`
6. Want a custom domain like `zarazhao.com`? Add it under **Settings → Pages → Custom domain**, and point your domain's DNS to GitHub Pages (GitHub will show you the exact records to add).

## Swapping in real content

- **Images**: replace the Unsplash placeholder URLs in `index.html`, `about.html`, and `work.html` with your own — put files in the `images/` folder and update the `src` paths.
- **Bio**: edit the paragraphs in `about.html` under `.about-body`.
- **Projects**: duplicate a `.work-card` block in `work.html` for each new piece; the `data-category` attribute (`3d`, `sculpt`, `paint`) controls the filter buttons — add new categories by adding a matching filter button.
- **Posts**: duplicate a `.post-row` block in `thoughts.html`. Right now they link to `#` — point them at real post pages or an external blog once you have one.
- **Newsletter form**: currently just a front-end placeholder (no emails are actually sent). Wire it up to a service like Buttondown, Mailchimp, or ConvertKit when ready — most give you a form action URL to drop in.

## Design notes

Warm cream/olive/brick palette with a candy-stripe motif used as a structural divider between sections. Headlines in **Anton** (bold condensed), body copy in **Fraunces** (warm serif), labels/nav/dates in **Space Mono**. Fully responsive down to mobile, respects reduced-motion preferences.

# Cork & Click – static site

Plain HTML/CSS/JS rebuild of corkandclick.com. No build step, no dependencies.

## Structure
```
index.html                 Home
about.html  contact.html   Main pages
privacy.html  cancellation.html
christianas-story-….html   Blog post linked from About
photography-for-everyone.html   Redirects to index.html (old WordPress home URL)
css/style.css   js/main.js      Styles + mobile menu
images/                         Optimized copies of the originals from wp-content/uploads
404.html  .nojekyll
```
All pages sit in the root and link to each other relatively, so the site works at `username.github.io/repo/` or on a custom domain.

## Publish on GitHub Pages
1. Create a repo and push the contents of this folder to the root of `main`.
2. Repo **Settings → Pages → Deploy from a branch → main / (root)**.
3. For corkandclick.com: add the domain under Pages → Custom domain (this creates a `CNAME` file) and point DNS at GitHub Pages.

## Contact form (needs one edit)
GitHub Pages can't run PHP, so the form posts to [Formspree](https://formspree.io) (free tier available).
Create a form there, then replace `YOUR_FORM_ID` in `contact.html`.

## Not carried over
Google Analytics / AdRoll tracking, the shop/Gravity Forms/WooCommerce pieces, and the other blog posts.
The privacy page still mentions analytics and AdRoll cookies; update it if you don't re-add them.

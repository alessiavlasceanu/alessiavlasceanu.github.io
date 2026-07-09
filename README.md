# Personal website — Alessia M. Vlasceanu

A static site (plain HTML/CSS/JS, no build step) with a homepage, research/publications page,
experience/education page, and a blog. Built from your CV.

## Structure

```
index.html            Homepage
research.html          Publications, talks, awards
experience.html        Work history, education, skills
blog/index.html        Blog listing
blog/*.html            Individual posts
blog/post-template.html  Copy this to start a new post
assets/css/style.css   All styling
assets/js/main.js      Mobile nav toggle + small helpers
assets/img/headshot.jpg  Your photo (pulled from your CV)
assets/Alessia_Vlasceanu_CV.pdf  Downloadable CV
```

## 1. Put this on GitHub Pages

1. Create a new repository on GitHub.
   - Name it `<your-username>.github.io` if you want the site at the root of that domain
     (e.g. `alessiavlasceanu.github.io`), **or** name it anything else (e.g. `personal-website`)
     and it'll be served at `<your-username>.github.io/personal-website/`.
2. Upload everything in this folder to the repository (drag-and-drop on github.com works, or
   use `git add . && git commit -m "Initial site" && git push` from this folder).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
5. Save. GitHub will give you a URL (something like `https://your-username.github.io/...`) —
   it usually goes live within a minute or two.

No build tools, no Jekyll config, nothing else required — it's just static files.

## 2. Before you publish — a few things to fill in

- **LinkedIn / ORCID links**: I used placeholder `#` links in `index.html`, `research.html` is fine,
  but check `index.html` (hero section + contact section) and replace `href="#"` with your real
  LinkedIn and ORCID URLs.
- **Email**: currently set to `alessia.vlasceanu@manchester.ac.uk` (from your CV). Swap it out in
  `index.html` if you'd rather use a different address.
- **Photo**: pulled directly from your CV — swap `assets/img/headshot.jpg` for a higher-res version
  any time (keep the same filename, or update the `<img src>` references in each HTML file).

## 3. Adding a new blog post

1. Duplicate `blog/post-template.html`, rename it something like `blog/my-new-post.html`.
2. Edit the `<title>`, the date/read-time line, the `<h1>`, and the body paragraphs.
3. Open `blog/index.html` and add a new card at the top of the list:

```html
<a class="post-card" href="my-new-post.html">
  <div class="post-date">Month Year</div>
  <h3>Your Post Title</h3>
  <p>One-sentence summary/teaser.</p>
</a>
```

4. Push the changes — GitHub Pages updates automatically within a minute of a push.

## 4. Custom domain (optional)

If you buy a domain later: add a `CNAME` file at the root containing just the domain
(e.g. `alessiavlasceanu.com`), and point your domain's DNS to GitHub Pages per
[GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## 5. Editing content later

Everything is plain HTML — no templating engine, so text lives directly in each `.html` file.
Search for the text you want to change and edit it directly; styling lives in one place
(`assets/css/style.css`) so visual tweaks (colors, spacing, fonts) only need to happen once.

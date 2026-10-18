# Imran Lateef Unar — Portfolio

A static, responsive personal portfolio prepared for GitHub Pages and `imranlateef.me`.

## Preview locally
Open `index.html` in a browser. For a local web server, run Python from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Before publishing
1. Review all text in `index.html` for accuracy.
2. Verify that each social link opens the intended profile.
3. Add confirmed repository/demo URLs to project cards; remove any claims or projects you do not want public.
4. Consider whether you want your university email publicly displayed. It is currently visible because it was supplied for the portfolio.
5. The contact link uses `mailto:` and opens the visitor's email app. It does not send messages through a server.

## Deploy using GitHub Pages
1. Sign in to GitHub and create a **new public repository** named `imranlateef-portfolio` (or another name you prefer).
2. Upload the contents of this folder to the repository root. Ensure `index.html`, `styles.css`, and `script.js` are at the root—not nested inside another folder.
3. Commit the files to the `main` branch.
4. Open **Settings → Pages** in the repository.
5. Under **Build and deployment**, choose **GitHub Actions** as the source.
6. Open the **Actions** tab and wait for “Deploy portfolio to GitHub Pages” to finish successfully.
7. Open the deployed URL shown by the Pages deployment. Test it on desktop and mobile.

The included workflow publishes the repository root as a static site.

## Connect `imranlateef.me`
Do this only after the GitHub Pages site deploys successfully.

1. In the repository, open **Settings → Pages → Custom domain**.
2. Enter `imranlateef.me` and save. GitHub should add/update a `CNAME` file in the repository; a CNAME file is also included here.
3. At your domain registrar's DNS settings, configure the records using the current values documented by GitHub Pages. For an apex/root domain, GitHub's documented A/AAAA records are commonly used; a `www` subdomain is usually configured as a CNAME pointing to your GitHub Pages hostname. Confirm the current values in GitHub's official documentation before changing DNS.
4. Do not delete existing DNS records until you understand what they serve (for example, email records).
5. Wait for DNS propagation. Return to **Settings → Pages** and enable **Enforce HTTPS** once GitHub makes it available.
6. Test both `https://imranlateef.me` and `https://www.imranlateef.me` if you configure both.

Official documentation:
- https://docs.github.com/en/pages
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages

## Edit content
Most portfolio copy is directly in `index.html`. Styles are in `styles.css`, and the small mobile navigation/year script is in `script.js`. Search for project card titles and replace the repository placeholders only with verified URLs.

## Limitations
GitHub Pages serves static files and cannot run a server-side contact form, database, PHP, or Flask app. The email contact button uses `mailto:`. Use a reputable form provider or a separate serverless backend if you later need a web form.

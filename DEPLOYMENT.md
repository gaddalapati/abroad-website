# Deployment Guide - GlobalPath Abroad Consultancy Website

This static website (HTML, CSS, and assets) is configured and ready for free hosting on any modern web platform.

---

## 🚀 Option 1: Netlify Drop (Fastest & Zero Setup — 1 Minute)

No Git, CLI, or account configuration required to test live:

1. Open your browser and go to [Netlify Drop](https://app.netlify.com/drop).
2. Sign in (or create a free account).
3. Drag and drop this entire project folder (`abroad`) into the designated drop area in your browser.
4. Netlify will upload and instantly publish your site with a live URL (e.g., `https://your-site-name.netlify.app`) and free HTTPS.
5. In Netlify Site Settings, you can customize the domain name or connect your own custom domain for free.

---

## ⚡ Option 2: Vercel

The project includes `vercel.json` preconfigured for clean URLs and fast global CDN caching:

1. Go to [Vercel](https://vercel.com/) and log in with your GitHub/GitLab account.
2. Click **Add New...** > **Project**.
3. Import your GitHub repository (or use the Vercel CLI).
4. Leave the Framework Preset as **Other** (Root Directory: `./`).
5. Click **Deploy**. Your site will be live in seconds at `https://your-project.vercel.app`.

---

## 🐙 Option 3: GitHub Pages (Automated CI/CD via GitHub Actions)

The repository already includes an automated workflow at `.github/workflows/deploy.yml`:

1. Initialize git and push this project to a new repository on GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit for GlobalPath Abroad Consultancy"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```
2. On GitHub, navigate to your repository:
   - Click **Settings** > **Pages** (under Code and automation).
   - Under **Build and deployment** > **Source**, select **GitHub Actions**.
3. The workflow will automatically trigger, build, and deploy your site to `https://<your-username>.github.io/<your-repo-name>/`.

---

## ☁️ Option 4: Cloudflare Pages

1. Log in to the [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. Go to **Workers & Pages** > **Create application** > **Pages**.
3. Choose **Direct Upload** (drag & drop the folder) or **Connect to Git**.
4. Set the build output directory to `/` (leave build command blank).
5. Click **Deploy site**.

---

## 📁 Included Deployment Configurations

- [`index.html`](index.html): Standard root entry point for web servers.
- [`vercel.json`](vercel.json): Vercel routing and clean URL settings.
- [`netlify.toml`](netlify.toml): Netlify build and redirect specifications.
- [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml): Automated GitHub Pages deployment pipeline.
- [`.gitignore`](.gitignore): Clean repository hygiene ignoring OS and IDE caches.

# Business website

Single-page static site served by nginx. Built for deployment on Coolify.

## Edit before going live
In `index.html`, search for `EDIT:` and update:
- **Brand Name** (title, header, footer)
- **Storefront links** (Newegg, eBay, Walmart, Best Buy)
- **Email address**

## Put it on GitHub
1. Create a new repository on github.com (private is fine).
2. Upload these files (drag and drop on the repo page works), or:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
   git push -u origin main
   ```

## Deploy on Coolify
1. **Projects → New → Add Resource → Private Repository (with GitHub App)** (or Public Repository if the repo is public).
2. Select this repo, branch `main`.
3. Build pack: **Dockerfile**. Port: **80**.
4. Domains: `https://yourdomain.com,https://www.yourdomain.com`
5. Deploy. Coolify sets up SSL automatically.

Every push to `main` redeploys the site (turn on Auto Deploy in the resource settings if it isn't already).

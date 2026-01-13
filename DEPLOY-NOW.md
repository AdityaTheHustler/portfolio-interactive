# Quick Deploy Commands

## Step 1: Create GitHub Repository
Go to: https://github.com/new

- Repository name: `portfolio-interactive`
- Description: `Interactive portfolio with gamified hiring protocol`
- Public
- Do NOT add README, .gitignore, or license (we have them)
- Click "Create repository"

## Step 2: Push to GitHub

Copy and run these commands in your Portfolio folder:

```bash
git remote add origin https://github.com/AdityaTheHustler/portfolio-interactive.git
git branch -M main
git push -u origin main
```

## Step 3: Deploy to Vercel

1. Go to https://vercel.com/new
2. Sign in with GitHub
3. Click "Import Project"
4. Select `portfolio-interactive`
5. Click "Deploy"
6. Wait 2 minutes
7. Copy your URL (e.g., `https://portfolio-interactive.vercel.app`)

## Step 4: Update Sitemap (After Deploy)

After Vercel gives you the URL, update:

**File: `sitemap.xml`**
Replace line 7:
```xml
<loc>https://portfolio-interactive.vercel.app/</loc>
```
With your actual Vercel URL.

**File: `robots.txt`**
Replace line 5:
```
Sitemap: https://portfolio-interactive.vercel.app/sitemap.xml
```
With your actual Vercel URL.

Then commit and push:
```bash
git add .
git commit -m "Update: Production URLs"
git push
```

Vercel will auto-deploy the update.

## Step 5: Add GitHub Topics

On GitHub repo page:
1. Click gear icon next to "About"
2. Add topics:
   - portfolio
   - interactive-portfolio
   - gamification
   - javascript
   - tailwind-css
   - full-stack-developer
   - matrix-theme

3. Add website URL (your Vercel URL)
4. Save

## Done!

Your portfolio is now live and SEO-optimized.

Test at: https://portfolio-interactive.vercel.app/

## Optional: Custom Domain

If you have a domain:
1. Vercel Dashboard > Settings > Domains
2. Add your domain
3. Update DNS records
4. Update sitemap.xml with new domain
5. Commit and push

## That's It!

Total time: 10 minutes
You're now live and discoverable on Google.

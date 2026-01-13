# Deployment Guide

## Quick Deploy Options

### Option 1: Vercel (Recommended)

1. Push your code to GitHub
2. Visit [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Deploy (no configuration needed)

**Update after deployment:**
- Replace all `portfolio-interactive-zeta.vercel.app` with your Vercel URL
- Add custom domain in Vercel settings

### Option 2: Netlify

1. Visit [netlify.com](https://netlify.com)
2. Drag and drop your Portfolio folder
3. Done!

**Custom domain:**
- Go to Domain settings
- Add your custom domain
- Update DNS records as instructed

### Option 3: GitHub Pages

1. Push to GitHub
2. Go to repository Settings
3. Pages section
4. Select `main` branch
5. Save

**URL:** `https://yourusername.github.io/portfolio-interactive/`

## Post-Deployment Checklist

### 1. Update Domain References
Search and replace in `index.html`:
```
https://portfolio-interactive-zeta.vercel.app/ → your-actual-domain.com
```

### 2. Create Preview Image
- Size: 1200x630px
- Name: `preview.png`
- Include: Your name, title, screenshot
- Upload to root directory

### 3. Create Favicons
Generate at [favicon.io](https://favicon.io):
- `favicon-32x32.png`
- `favicon-16x16.png`
- `apple-touch-icon.png`

### 4. Submit to Google
- [Google Search Console](https://search.google.com/search-console)
- Add your site
- Submit sitemap: `https://yourdomain.com/sitemap.xml`
- Request indexing

### 5. Update Sitemap
Edit `sitemap.xml`:
```xml
<loc>https://your-actual-domain.com/</loc>
<lastmod>2026-01-14</lastmod>
```

### 6. Analytics (Optional)
Add Google Analytics or similar before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-ID"></script>
```

## Custom Domain Setup

### Domain Provider DNS Settings
Point to your hosting:

**Vercel:**
```
A Record: 76.76.21.21
CNAME: your-project.vercel.app
```

**Netlify:**
```
A Record: 75.2.60.5
CNAME: your-site.netlify.app
```

## Performance Optimization

### Enable Compression
Already optimized, but ensure server has:
- Gzip enabled
- Brotli compression
- Cache headers

### CDN
Both Vercel and Netlify provide free CDN automatically.

## Monitoring

### Check SEO
- [PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- Google Search Console

### Social Media Preview
Test your Open Graph tags:
- [Facebook Debugger](https://developers.facebook.com/tools/debug/)
- [Twitter Card Validator](https://cards-dev.twitter.com/validator)
- [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/)

## Troubleshooting

**Images not loading?**
- Check file paths are relative: `./image.png`
- Ensure files are committed to Git

**Games not working?**
- Check browser console for errors
- Ensure JavaScript is enabled

**SEO not working?**
- Wait 24-48 hours for indexing
- Submit sitemap to Google
- Check robots.txt is accessible

## Support

Visit repository issues for help: [GitHub Issues](https://github.com/AdityaTheHustler/portfolio-interactive/issues)

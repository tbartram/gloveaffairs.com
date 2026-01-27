# Deployment Guide for Glove Affairs Website

This guide will help you deploy your Glove Affairs website to a hosting platform.

## Prerequisites

1. A GitHub account (free)
2. Your website code pushed to a GitHub repository
3. Your domain (gloveaffairs.com) DNS access

## Recommended: Deploy to Netlify

Netlify offers the best experience for Astro static sites with generous free tier.

### Step 1: Prepare Your Code

1. Initialize Git (if not already done):
```bash
git init
git add .
git commit -m "Initial commit - Glove Affairs website"
```

2. Create a GitHub repository and push your code:
```bash
# Create a new repository on GitHub first, then:
git remote add origin https://github.com/YOUR_USERNAME/gloveaffairs.com.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy to Netlify

1. Go to [netlify.com](https://netlify.com) and sign up (free)

2. Click "Add new site" → "Import an existing project"

3. Choose "Deploy with GitHub" and authorize Netlify

4. Select your `gloveaffairs.com` repository

5. Configure build settings (should auto-detect from netlify.toml):
   - Build command: `npm run build`
   - Publish directory: `dist`
   - Click "Deploy site"

6. Netlify will build and deploy your site (takes 1-2 minutes)

### Step 3: Configure Your Custom Domain

1. Once deployed, go to "Domain settings" in Netlify

2. Click "Add custom domain"

3. Enter `gloveaffairs.com`

4. Netlify will provide DNS records to configure

5. In your domain registrar (where you bought gloveaffairs.com):
   - Add an A record pointing to Netlify's IP (they'll provide this)
   - Or use Netlify's nameservers for easier management

6. SSL certificate will auto-provision (may take a few minutes)

7. Your site will be live at https://gloveaffairs.com

### Step 4: Enable Continuous Deployment

Already configured! Every time you push to GitHub, Netlify will automatically rebuild and deploy your site.

## Alternative: Deploy to Vercel

Vercel is another excellent option with similar features.

### Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign up (free)

2. Click "Add New Project"

3. Import your GitHub repository

4. Vercel will auto-detect Astro:
   - Framework: Astro
   - Build command: `npm run build`
   - Output directory: `dist`

5. Click "Deploy"

6. Configure custom domain in Vercel settings:
   - Add `gloveaffairs.com`
   - Follow DNS instructions from Vercel

## Update Your Site

To update your website:

1. Make changes to your code locally

2. Test locally:
```bash
npm run dev
```

3. Commit and push to GitHub:
```bash
git add .
git commit -m "Description of your changes"
git push
```

4. Netlify/Vercel will automatically rebuild and deploy (takes 1-2 minutes)

## Replace Placeholder Content

### Add Your Logo

Replace `/public/logo.svg` with your actual logo:
- Recommended: SVG format for scalability
- Or use PNG/JPG (at least 200x200px)
- Update references in `Header.astro` and `Footer.astro` if filename changes

### Add Gallery Photos

Replace placeholder images in `/public/images/`:
1. Take before/after photos of your restoration work
2. Optimize images (recommended: 1200x1200px, under 500KB each)
3. Replace `placeholder-before-X.jpg` and `placeholder-after-X.jpg` files
4. Add more items to the `galleryItems` array in `/src/pages/gallery.astro`

### Update Content

Edit the following files to personalize content:
- `/src/pages/index.astro` - Home page copy
- `/src/pages/services.astro` - Service descriptions and pricing approach
- `/src/pages/contact.astro` - Add email if you want, update FAQ

## Environment Variables (Optional)

If you add features that need environment variables later:

1. Create `.env` file locally (already in .gitignore)
2. Add variables in Netlify/Vercel dashboard under "Environment Variables"

## Troubleshooting

### Build Fails

Check build logs in Netlify/Vercel dashboard. Common issues:
- Missing dependencies: Make sure `package.json` is committed
- Node version: Both platforms use Node 20 by default

### Images Not Loading

- Check file paths (case-sensitive on deployment)
- Ensure images are in `/public/` directory
- Verify images are committed to Git

### Domain Not Working

- DNS changes can take up to 48 hours to propagate
- Use `dig gloveaffairs.com` to check DNS records
- Verify SSL certificate has been issued

## Performance

Your Astro site should achieve perfect Lighthouse scores:
- Performance: 100
- Accessibility: 100
- Best Practices: 100
- SEO: 100

Run Lighthouse in Chrome DevTools to verify.

## Support

- Netlify Docs: https://docs.netlify.com
- Vercel Docs: https://vercel.com/docs
- Astro Docs: https://docs.astro.build

## Next Steps

1. Add Google Analytics (optional)
2. Set up form submission with Netlify Forms or Formspree (if you want contact form)
3. Integrate Instagram feed API (future enhancement)
4. Add more restoration photos to gallery as you complete projects

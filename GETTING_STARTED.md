# Getting Started with Your Glove Affairs Website

Welcome! Your Glove Affairs website is ready to go. Here's everything you need to know to get started.

## What's Been Built

A modern, static website with:
- ✅ Home page with hero, services overview, and call-to-action
- ✅ Services page with detailed descriptions and process explanation
- ✅ Gallery page with before/after photo grid
- ✅ Contact page with social media links and FAQ
- ✅ Responsive design (mobile, tablet, desktop)
- ✅ SEO optimization with meta tags
- ✅ Fast loading (Astro = zero JavaScript by default)
- ✅ Modern, clean design with baseball/leather color scheme
- ✅ Deployment-ready configuration for Netlify/Vercel

## Quick Start

### 1. Install Dependencies

First, make sure you have Node.js installed (version 18 or higher).

Then install project dependencies:

```bash
npm install
```

### 2. Start Development Server

```bash
npm run dev
```

Visit `http://localhost:4321` to see your site!

### 3. Make Your First Customizations

#### Replace the Logo
1. Add your logo to `/public/` (as `logo.svg`, `logo.png`, or `logo.jpg`)
2. If using a different filename, update references in:
   - `src/components/Header.astro`
   - `src/components/Footer.astro`

#### Add Real Gallery Photos
1. Take before/after photos of your restoration work
2. Save them in `/public/images/` (e.g., `vintage-wilson-before.jpg`)
3. Update the gallery array in `src/pages/gallery.astro`

#### Verify Social Links
Check that all social media links point to your accounts:
- Instagram: @gloveaffairs
- Facebook: facebook.com/gloveaffairs
- YouTube: youtube.com/@gloveaffairs

### 4. Build for Production

Test the production build:

```bash
npm run build
npm run preview
```

## Next Steps

### Deploy Your Site

Follow the detailed guide in `DEPLOYMENT.md`:
1. Push code to GitHub
2. Connect to Netlify or Vercel (free)
3. Configure your gloveaffairs.com domain
4. Site goes live!

### Customize Content

See `CUSTOMIZATION.md` for:
- Changing colors
- Adding/editing services
- Modifying page content
- Adding new pages

## Project Structure

```
gloveaffairs.com/
├── src/
│   ├── layouts/
│   │   └── Layout.astro          # Main layout with SEO
│   ├── components/
│   │   ├── Header.astro          # Navigation bar
│   │   ├── Footer.astro          # Footer with social links
│   │   ├── Hero.astro            # Hero section component
│   │   ├── ServiceCard.astro     # Service card component
│   │   └── GalleryItem.astro     # Gallery item component
│   ├── pages/
│   │   ├── index.astro           # Home page
│   │   ├── services.astro        # Services page
│   │   ├── gallery.astro         # Gallery page
│   │   └── contact.astro         # Contact page
│   └── styles/
│       └── global.css            # Global styles + Tailwind
├── public/
│   ├── logo.svg                  # Your logo (replace this)
│   ├── favicon.ico               # Favicon (replace this)
│   └── images/                   # Gallery images (replace these)
├── package.json                  # Dependencies
├── astro.config.mjs              # Astro configuration
├── tailwind.config.mjs           # Tailwind configuration
├── tsconfig.json                 # TypeScript configuration
├── netlify.toml                  # Netlify deployment config
├── vercel.json                   # Vercel deployment config
├── README.md                     # Project overview
├── DEPLOYMENT.md                 # Deployment guide
├── CUSTOMIZATION.md              # Customization guide
└── GETTING_STARTED.md            # This file
```

## Commands

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run astro` - Run Astro CLI commands

## Design Decisions

### Color Scheme
- **Leather tones** (browns): Primary brand color, represents baseball glove leather
- **Baseball red**: Accent color, subtle baseball reference
- **Neutral grays**: Clean, modern background

### Typography
- **Inter**: Clean, modern sans-serif font
- Good readability on all devices

### Layout Approach
- **Mobile-first**: Designed for mobile, scales up to desktop
- **Generous whitespace**: Clean, breathable design
- **Large CTAs**: Clear calls-to-action to social media

## Tips for Success

1. **Start Simple**: Don't worry about perfection. Get it live, then iterate.

2. **Add Photos Regularly**: Your gallery will be your best marketing tool. Add new restorations as you complete them.

3. **Engage on Social**: The site directs people to your social media. Stay active there!

4. **Update Content**: As your business evolves, update your services and pricing approach.

5. **Monitor Performance**: Use Google Analytics (optional) to see which pages get the most traffic.

## Placeholder Content

These items have placeholder content you should replace:

- [ ] Logo (`/public/logo.svg`)
- [ ] All gallery images (`/public/images/placeholder-*.jpg`)
- [ ] Open Graph image (`/public/og-image.jpg`)
- [ ] Hero/page copy (tailor to your voice)
- [ ] Service descriptions (add your specific process/pricing)

## Support Resources

- **Astro Docs**: https://docs.astro.build
- **Tailwind CSS Docs**: https://tailwindcss.com/docs
- **Netlify Docs**: https://docs.netlify.com
- **Vercel Docs**: https://vercel.com/docs

## Questions?

Check the other documentation files:
- `README.md` - Project overview
- `DEPLOYMENT.md` - How to deploy
- `CUSTOMIZATION.md` - How to customize

## What Makes This Site Special

- **Blazing Fast**: Astro ships zero JavaScript by default
- **SEO Optimized**: Meta tags, Open Graph, semantic HTML
- **Accessible**: ARIA labels, keyboard navigation, semantic markup
- **Responsive**: Beautiful on any device
- **Maintainable**: Component-based architecture, easy to update
- **Deployable**: One command to deploy, auto-deploys on Git push

---

**Ready to launch?** Install dependencies, customize your content, and deploy! Your baseball glove restoration business website is ready to go live. 🧤⚾

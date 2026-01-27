# Customization Guide

This guide explains how to customize your Glove Affairs website.

## Quick Customizations

### Update Social Media Links

All social media links are centralized. Update these files:

1. **Footer Component** (`/src/components/Footer.astro`):
```astro
const socialLinks = [
  {
    name: 'Instagram',
    href: 'https://instagram.com/gloveaffairs', // Update this
    // ...
  },
  // Update Facebook and YouTube URLs similarly
];
```

2. Verify links in:
   - `/src/pages/index.astro`
   - `/src/pages/contact.astro`

### Replace Logo

1. Replace `/public/logo.svg` with your logo file
2. Supported formats: SVG (recommended), PNG, JPG
3. If using a different filename, update:
   - `/src/components/Header.astro` (line with `<img src="/logo.svg"`)
   - `/src/components/Footer.astro` (line with `<img src="/logo.svg"`)

### Update Colors

Colors are defined in `/tailwind.config.mjs`:

```javascript
colors: {
  leather: {
    // Brown/leather tones
    700: '#7d5e4f', // Main brand color
    800: '#5a4238', // Darker variant
    // Adjust these hex codes to match your brand
  },
  baseball: {
    // Red/burgundy accents
    600: '#dc2626',
    // Adjust these for accent colors
  },
}
```

After changing colors, they'll automatically apply throughout the site.

### Add/Remove Services

Edit `/src/pages/services.astro`:

```astro
const services = [
  {
    title: 'Your Service Name',
    description: 'Service description here',
    icon: '🔧', // Any emoji or remove this line
  },
  // Add more services...
];
```

The home page shows featured services. Update in `/src/pages/index.astro` similarly.

### Update Page Content

- **Home Page**: Edit `/src/pages/index.astro`
- **Services Page**: Edit `/src/pages/services.astro`
- **Gallery Page**: Edit `/src/pages/gallery.astro`
- **Contact Page**: Edit `/src/pages/contact.astro`

### Add Gallery Photos

1. Add your images to `/public/images/`
2. Update `/src/pages/gallery.astro`:

```astro
const galleryItems = [
  {
    beforeImage: '/images/your-before-photo.jpg',
    afterImage: '/images/your-after-photo.jpg',
    title: 'Project Name',
    description: 'What you did',
  },
  // Add more items...
];
```

## Advanced Customizations

### Change Fonts

Currently using Inter from Google Fonts. To change:

1. Edit `/src/layouts/Layout.astro`
2. Replace Google Fonts link
3. Update `font-family` in body class

### Add New Pages

1. Create new file in `/src/pages/`, e.g., `/src/pages/about.astro`
2. Add navigation link in `/src/components/Header.astro`:

```astro
const navItems = [
  // existing items...
  { name: 'About', href: '/about' },
];
```

### Modify Layout

Main layout is in `/src/layouts/Layout.astro`. Components are in `/src/components/`.

### Add Contact Form

To add a contact form (requires backend):

1. **Option 1: Netlify Forms** (if using Netlify)
   - Add form HTML with `netlify` attribute
   - Submissions appear in Netlify dashboard

2. **Option 2: Formspree** (any hosting)
   - Sign up at formspree.io
   - Add their form endpoint
   - Free tier: 50 submissions/month

### Enable Instagram Feed

To show Instagram posts (future enhancement):

1. Use Instagram Basic Display API
2. Add API integration library
3. Create component to display feed
4. May require backend/serverless function for token refresh

## Tips

- **Test Locally**: Run `npm run dev` before deploying
- **Commit Changes**: Use Git to track all changes
- **Backup**: Keep backups before major customizations
- **Responsive Design**: Test on mobile, tablet, and desktop

## Need Help?

- Astro Docs: https://docs.astro.build
- Tailwind Docs: https://tailwindcss.com/docs
- Check README.md for project structure

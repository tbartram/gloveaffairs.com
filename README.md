# Glove Affairs Website

Modern, static website for Glove Affairs baseball glove restoration business.

## Tech Stack

- **Astro**: Static site generator
- **Tailwind CSS**: Utility-first CSS framework
- **TypeScript**: Type safety and better DX

## Getting Started

### Install Dependencies

```bash
npm install
```

### Development Server

```bash
npm run dev
```

Visit `http://localhost:4321` to view the site.

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
├── src/
│   ├── layouts/
│   │   └── Layout.astro          # Main layout wrapper
│   ├── components/
│   │   ├── Header.astro          # Navigation
│   │   ├── Footer.astro          # Footer with social links
│   │   ├── Hero.astro            # Hero section
│   │   ├── ServiceCard.astro     # Service cards
│   │   └── GalleryItem.astro     # Gallery grid item
│   ├── pages/
│   │   ├── index.astro           # Home page
│   │   ├── services.astro        # Services page
│   │   ├── gallery.astro         # Gallery page
│   │   └── contact.astro         # Contact/social page
│   └── styles/
│       └── global.css            # Global styles
├── public/
│   ├── logo.svg                  # Logo
│   ├── favicon.ico               # Favicon
│   └── images/                   # Gallery images
└── astro.config.mjs              # Astro configuration
```

## Deployment

This site can be deployed to:
- **Netlify** (recommended)
- **Vercel**
- **GitHub Pages**
- Any static hosting provider

### Deploy to Netlify

1. Push to GitHub
2. Connect repository to Netlify
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Point your domain (gloveaffairs.com) to Netlify

## Social Media Links

- Instagram: [@gloveaffairs](https://instagram.com/gloveaffairs)
- Facebook: [Glove Affairs](https://facebook.com/gloveaffairs)
- YouTube: [Glove Affairs](https://youtube.com/@gloveaffairs)

# Dr Siddharth Arora Eye Clinic Website

A modern, fast, and responsive static website for Dr Siddharth Arora Eye Clinic in Bharatpur, Rajasthan.

## Tech Stack

- **Astro** - Static site generator (zero JS by default)
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide Icons** - Clean, consistent icons (via inline SVG)

## Project Structure

```
/
├── public/                 # Static assets (images, favicon, CNAME)
│   ├── images/            # Add your clinic photos here
│   ├── favicon.svg
│   ├── CNAME
│   └── robots.txt
├── src/
│   ├── components/        # Reusable UI components
│   │   ├── Navbar.astro
│   │   ├── Hero.astro
│   │   ├── Stats.astro
│   │   ├── About.astro
│   │   ├── Services.astro
│   │   ├── WhyChooseUs.astro
│   │   ├── Gallery.astro
│   │   ├── Testimonials.astro
│   │   ├── FAQ.astro
│   │   ├── Contact.astro
│   │   ├── Footer.astro
│   │   └── WhatsAppButton.astro
│   ├── layouts/
│   │   └── Layout.astro   # Main page wrapper
│   ├── pages/
│   │   └── index.astro    # Home page (assembles all sections)
│   └── styles/
│       └── global.css     # Tailwind directives + custom styles
├── astro.config.mjs
├── tailwind.config.mjs
├── package.json
└── tsconfig.json
```

## How to Run This Project

### Prerequisites
- Node.js 18+ installed on your machine
- VS Code (recommended) with the Astro extension

### Step 1: Install Dependencies
```bash
npm install
```

### Step 2: Start Development Server
```bash
npm run dev
```
This starts a local server at `http://localhost:4321`

### Step 3: Build for Production
```bash
npm run build
```
This creates a `dist/` folder with static HTML/CSS/JS files ready for deployment.

### Step 4: Preview Production Build
```bash
npm run preview
```

## Customization Guide

### Adding Your Photos
1. Place your images in the `public/images/` folder
2. Update the components to reference them:
   - `Hero.astro` - Doctor portrait
   - `About.astro` - Clinic/doctor photo
   - `Gallery.astro` - Clinic building, equipment, staff photos

Example:
```astro
<img src="/images/doctor-photo.jpg" alt="Dr Siddharth Arora" />
```

### Updating Content
All text content is in the `.astro` files inside `src/components/`. Simply edit the text between the tags.

### Adding Google Maps
1. Go to [Google Maps](https://maps.google.com)
2. Search for your clinic location
3. Click "Share" → "Embed a map"
4. Copy the HTML iframe code
5. Paste it in `src/components/Contact.astro` inside the map placeholder div

### Changing Colors
Edit `tailwind.config.mjs`:
```js
colors: {
  primary: { DEFAULT: '#0D7377', ... },
  accent: { DEFAULT: '#D4A843', ... },
}
```

## Deployment

### GitHub Pages (Recommended)
1. Push this repo to GitHub
2. Go to Settings → Pages
3. Set source to GitHub Actions
4. Use the provided workflow file (add `.github/workflows/deploy.yml`)

### Netlify / Vercel
1. Connect your GitHub repo
2. Build command: `npm run build`
3. Publish directory: `dist`

## Future Enhancements (Dynamic)

When you're ready to add dynamic features:
- **API Routes**: Add `src/pages/api/` endpoints
- **React Islands**: Import React components for interactivity
- **CMS Integration**: Connect to a headless CMS for content management
- **Database**: Add SQLite/PostgreSQL for appointments, patient records

## License

Private - For Dr Siddharth Arora Eye Clinic use only.

# Development Guide

## Quick Start

### Option 1: Zero Setup (Recommended for quick changes)

1. Open `index.html` directly in your browser
2. The app automatically uses Tailwind CDN for styling
3. Make changes and refresh - that's it!

### Option 2: Full Development Setup

```bash
# Clone the repository
git clone <your-repo-url>
cd aruco-stl-generator

# Install dependencies
npm install

# Start development with custom CSS (optional)
npm run dev    # Watches for CSS changes
npm run serve  # Serves files on localhost:8000
```

## CSS Development

### Using CDN (Default for local development)

- No setup required
- Instant refresh
- Full Tailwind classes available
- Perfect for quick iterations

### Using Custom Build

```bash
# Build once
npm run build-css

# Build and watch for changes
npm run dev
```

### Custom Classes Available

The project includes these custom component classes:

- `.glass` - Glass morphism background
- `.glass-card` - Card with glass effect
- `.gradient-text` - Gradient text effect
- `.btn-primary` - Primary button styling
- `.input-field` - Form input styling

## Production Deployment

### Automatic via GitHub Actions

1. Push to main branch
2. GitHub Actions automatically:
   - Installs dependencies
   - Builds optimized CSS
   - Deploys to GitHub Pages

### Environment Detection

The app automatically detects environment:

- **Local file:// protocol**: Uses Tailwind CDN
- **Production HTTPS**: Uses built CSS with CDN fallback

## File Structure

```
/
├── src/
│   └── input.css          # Tailwind source + custom components
├── dist/                  # Built CSS (generated, gitignored)
├── .github/workflows/     # CI/CD configuration
├── tailwind.config.js     # Tailwind configuration
├── package.json           # Dependencies and scripts
└── index.html             # Main application
```

## Tips

- Use the CDN approach for quick styling experiments
- Only switch to custom build when you need custom components or optimizations
- The built CSS is much smaller (~15KB vs ~3MB CDN)
- Custom classes in `src/input.css` make common patterns reusable

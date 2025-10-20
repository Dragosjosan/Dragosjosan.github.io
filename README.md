# Braein.io Blog

A fast, modern, and user-friendly blog built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.

## Features

- ⚡ **Lightning Fast**: Static site generation with Hugo
- 🎨 **Beautiful Design**: Clean, modern UI with PaperMod theme
- 🌙 **Dark Mode**: Automatic theme switching
- 🔍 **Search**: Full-text search powered by Fuse.js
- 📱 **Responsive**: Mobile-first design
- ♿ **Accessible**: WCAG-compliant
- 📊 **SEO Optimized**: Meta tags, Open Graph, Twitter Cards
- 💻 **Code Highlighting**: Syntax highlighting with copy buttons
- 📑 **Table of Contents**: Auto-generated for long posts
- 🏷️ **Taxonomies**: Tags, categories, and series support
- 📰 **RSS Feed**: Keep readers updated
- 🎯 **Series Navigation**: Link related tutorials and posts

## Quick Start

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) v0.146.0 or higher
- Git

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd braein-io-blog

# Start development server
hugo server -D

# Open in browser
open http://localhost:1313
```

### Creating Content

```bash
# New blog post
hugo new posts/my-first-post.md

# New tutorial
hugo new tutorials/python-basics.md

# Edit the file and change draft: true to draft: false when ready
```

### Building for Production

```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## Documentation

- **[Quick Start Guide](docs/QUICK-START.md)** - Get up and running quickly
- **[Design Guide](docs/BLOG-DESIGN-GUIDE.md)** - Comprehensive design & UX documentation

## Project Structure

```
braein-io-blog/
├── archetypes/          # Content templates
│   ├── default.md       # Default template
│   ├── posts.md         # Blog post template
│   └── tutorials.md     # Tutorial template
├── assets/
│   └── css/
│       └── extended/
│           └── custom.css    # Custom styling
├── content/             # Your content
│   ├── posts/          # Blog posts
│   ├── tutorials/      # Tutorial articles
│   ├── archives.md     # Archive page
│   └── search.md       # Search page
├── docs/               # Documentation
├── static/             # Static assets
│   └── images/         # Image files
├── themes/
│   └── PaperMod/       # Theme (git submodule)
├── hugo.yaml           # Main configuration
└── README.md           # This file
```

## Configuration

Key settings are in `hugo.yaml`:

```yaml
# Site info
title: Braein.io Blog
baseURL: https://example.org/

# Theme
theme: PaperMod

# Features
params:
  ShowReadingTime: true
  ShowCodeCopyButtons: true
  ShowToc: true
  # ... and many more!
```

See [Design Guide](docs/BLOG-DESIGN-GUIDE.md) for detailed configuration options.

## Customization

### Change Site Title and Description

Edit `hugo.yaml`:
```yaml
title: Your Blog Name
params:
  description: "Your blog description"
```

### Add Social Links

Edit `hugo.yaml`:
```yaml
params:
  socialIcons:
    - name: github
      url: "https://github.com/yourusername"
    - name: twitter
      url: "https://twitter.com/yourusername"
```

### Customize Colors

Add to `assets/css/extended/custom.css`:
```css
:root {
    --primary: #your-color;
}
```

## Content Guidelines

### Front Matter

Every content file should include:

```yaml
---
title: "Your Title"
date: 2025-10-18
draft: false
description: "SEO description"
tags: [tag1, tag2]
categories: [category]
---
```

### Series

Group related content with series:

```yaml
series: ["Python Fundamentals"]
```

Posts in the same series will automatically link to each other.

### Cover Images

Add a cover image:

```yaml
cover:
  image: "images/cover.jpg"
  alt: "Cover description"
```

## Deployment

### GitHub Pages

1. Create `.github/workflows/hugo.yml`
2. Configure GitHub Pages in repository settings
3. Push to main branch

### Netlify

1. Connect repository to Netlify
2. Build command: `hugo --minify`
3. Publish directory: `public`

### Vercel

1. Import repository
2. Framework preset: Hugo
3. Deploy

### Manual Deployment

```bash
hugo --minify
# Upload contents of public/ directory to your web host
```

## Performance

This blog is optimized for performance:

- ⚡ Static generation (no server-side processing)
- 📦 Asset minification
- 🖼️ Image optimization support
- 🎯 Minimal JavaScript
- 💨 Fast loading times

Test with [PageSpeed Insights](https://pagespeed.web.dev/)

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Graceful degradation for older browsers

## Accessibility

- Semantic HTML5
- ARIA labels where needed
- Keyboard navigation
- Screen reader support
- Color contrast compliance
- Focus indicators

## Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest features
- Submit pull requests
- Improve documentation

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- [Hugo](https://gohugo.io/) - Static site generator
- [PaperMod](https://github.com/adityatelange/hugo-PaperMod) - Theme
- [Fuse.js](https://fusejs.io/) - Search functionality
- Design & UX by Sally, UX Expert 🎨

## Support

For issues or questions:

1. Check [Quick Start Guide](docs/QUICK-START.md)
2. See [Design Guide](docs/BLOG-DESIGN-GUIDE.md)
3. Visit [Hugo Documentation](https://gohugo.io/documentation/)
4. Check [PaperMod Wiki](https://github.com/adityatelange/hugo-PaperMod/wiki)

---

Built with ❤️ using Hugo and PaperMod

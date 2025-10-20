# Quick Start Guide

## Running Your Blog

### Local Development
```bash
# Start Hugo server with drafts
hugo server -D

# Start without drafts
hugo server

# Build for production
hugo --minify
```

Your site will be available at `http://localhost:1313/`

---

## Creating Content

### New Blog Post
```bash
hugo new posts/my-new-post.md
```

### New Tutorial
```bash
hugo new tutorials/python-basics.md
```

### Generic Page
```bash
hugo new about.md
```

---

## Publishing Content

1. Edit your content in `content/` directory
2. Change `draft: true` to `draft: false` in front matter
3. Build site: `hugo --minify`
4. Deploy files from `public/` directory

---

## Essential Customizations

### Update Site Info
Edit `hugo.yaml`:
```yaml
baseURL: https://yourdomain.com/
title: Your Blog Name

params:
  description: "Your blog description"
  author: Your Name
```

### Add Your Social Links
Edit `hugo.yaml`:
```yaml
params:
  socialIcons:
    - name: github
      url: "https://github.com/yourusername"
    - name: twitter
      url: "https://twitter.com/yourusername"
    - name: linkedin
      url: "https://linkedin.com/in/yourusername"
```

### Customize Welcome Message
Edit `hugo.yaml`:
```yaml
params:
  homeInfoParams:
    Title: "Your Welcome Title"
    Content: "Your welcome message here"
```

---

## Common Tasks

### Add a Cover Image
1. Place image in `static/images/` or in post bundle
2. Add to front matter:
```yaml
cover:
  image: "images/my-cover.jpg"
  alt: "Description"
```

### Create a Series
Add to multiple posts:
```yaml
series: ["Python Fundamentals"]
```

Posts in the same series will be linked automatically.

### Add Tags
```yaml
tags: [python, tutorial, beginners]
```

### Disable Features Per Post
```yaml
ShowToc: false
ShowReadingTime: false
ShowShareButtons: false
```

---

## File Structure

```
braein-io-blog/
├── archetypes/          # Content templates
├── assets/
│   └── css/
│       └── extended/    # Your custom CSS
├── content/             # Your content here!
│   ├── posts/          # Blog posts
│   ├── tutorials/      # Tutorials
│   ├── search.md       # Search page
│   └── archives.md     # Archive page
├── static/             # Static files (images, etc.)
├── themes/
│   └── PaperMod/       # Theme files (don't edit)
├── hugo.yaml           # Main configuration
└── docs/               # Documentation
```

---

## Troubleshooting

### Site not updating?
```bash
# Clear cache and rebuild
rm -rf public/ resources/
hugo server -D
```

### Changes not showing?
- Hard refresh browser (Cmd+Shift+R or Ctrl+Shift+R)
- Check if file is still in draft mode
- Restart Hugo server

### Build errors?
- Check YAML syntax in front matter
- Ensure all required fields are present
- Look for unclosed quotes or brackets

---

## Getting Help

- See detailed guide: `docs/BLOG-DESIGN-GUIDE.md`
- PaperMod Wiki: https://github.com/adityatelange/hugo-PaperMod/wiki
- Hugo Docs: https://gohugo.io/documentation/

---

Happy blogging! 🎨

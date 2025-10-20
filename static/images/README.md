# Images Directory

Place your blog images here.

## Recommended Structure

```
images/
├── posts/           # Post-specific images
├── tutorials/       # Tutorial images
├── og-image.png     # OpenGraph/social sharing image (1200x630px)
├── favicon.ico      # Site favicon
└── avatar.jpg       # Author avatar (for profile mode)
```

## Image Guidelines

### Optimization
- **Format**: Use WebP when possible, fallback to JPG/PNG
- **Size**: Optimize before uploading (use tools like TinyPNG, Squoosh)
- **Dimensions**: Max width 1200px for most images

### Cover Images
- **Recommended Size**: 1200x630px (social sharing optimal)
- **Aspect Ratio**: 16:9 or 1.91:1
- **Format**: JPG or WebP

### Icons & Favicons
- **Favicon**: 32x32px or 16x16px ICO format
- **Apple Touch Icon**: 180x180px PNG

### Naming Convention
Use descriptive, lowercase names with hyphens:
- ✅ `python-tutorial-variables.jpg`
- ❌ `IMG_1234.JPG`

## Usage in Content

### In Front Matter
```yaml
cover:
  image: "images/posts/my-cover.jpg"
  alt: "Descriptive text"
```

### In Markdown
```markdown
![Alt text](/images/posts/example.jpg)
```

### With Hugo Image Processing
Use page bundles for advanced image processing:
```
content/posts/my-post/
├── index.md
└── cover.jpg
```

Then reference: `cover.jpg` (relative path)

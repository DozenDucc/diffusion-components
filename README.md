# 📄 Academic Paper Project Website

A clean, professional GitHub Pages template for showcasing your research paper. Inspired by popular academic project pages like [Nerfies](https://nerfies.github.io), [FTL-IGM](https://avivne.github.io/ftl-igm/), and [Diffuser](https://diffusion-planning.github.io/).

## ✨ Features

- **Clean, professional design** matching top ML/robotics paper websites
- **Fully responsive** - looks great on desktop, tablet, and mobile
- **Easy to customize** - just edit the HTML and add your content
- **Video/GIF support** with lazy loading for performance
- **BibTeX section** with one-click copy functionality
- **No build tools required** - pure HTML/CSS/JS

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended)

1. **Create a new repository** named `your-paper-name` (or `username.github.io` for a personal site)

2. **Upload the files:**
   - Upload `index.html` to the root of your repository
   - Create a `static/` folder and upload your images and videos

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Set Source to "Deploy from a branch"
   - Select `main` branch and `/ (root)` folder
   - Click Save

4. **Your site will be live at:** `https://username.github.io/your-paper-name/`

### Option 2: Local Development

```bash
# Clone or download the template
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# Open in browser (no server needed for basic viewing)
open index.html

# Or use a local server for full functionality
python -m http.server 8000
# Then open http://localhost:8000
```

## 📁 Folder Structure

```
your-paper-website/
├── index.html              # Main website file
├── README.md               # This file
└── static/
    ├── images/
    │   ├── teaser.png      # Main teaser figure
    │   ├── method.png      # Method overview diagram
    │   ├── exp1.png        # Experiment figures
    │   └── ...
    └── videos/
        ├── teaser.mp4      # Teaser video
        ├── result1.mp4     # Result videos
        ├── baseline1.mp4   # Baseline comparisons
        └── ...
```

## 🎨 Customization Guide

### 1. Update Paper Information

Edit the hero section in `index.html`:

```html
<h1 class="paper-title">Your Paper Title Here</h1>
<div class="venue">NeurIPS 2025</div>
```

### 2. Add Authors

```html
<div class="author-list">
  <span class="author"><a href="https://yoursite.com">Your Name</a><sup>1</sup>,</span>
  <span class="author"><a href="#">Co-author</a><sup>2</sup></span>
</div>

<div class="affiliations">
  <span><sup>1</sup>MIT</span>
  <span><sup>2</sup>Stanford</span>
</div>
```

### 3. Update Quick Links

```html
<a href="https://arxiv.org/abs/XXXX.XXXXX" class="quick-link">
  <i class="ai ai-arxiv"></i> arXiv
</a>
<a href="https://github.com/username/repo" class="quick-link">
  <i class="fab fa-github"></i> Code
</a>
```

### 4. Add Your Media

**For Videos (recommended formats: MP4, WebM):**
```html
<video autoplay loop muted playsinline>
  <source src="static/videos/your-video.mp4" type="video/mp4">
</video>
```

**For GIFs:**
```html
<img src="static/videos/your-animation.gif" alt="Description">
```

**For Images:**
```html
<img src="static/images/your-image.png" alt="Description">
```

### 5. Customize Colors

Edit the CSS variables at the top of `index.html`:

```css
:root {
  --color-primary: #5B7FFF;      /* Main accent color */
  --color-primary-dark: #4A6AE5; /* Hover state */
  --color-text: #1a1a2e;         /* Main text */
  --color-background: #ffffff;   /* Page background */
  --color-surface: #f8f9fc;      /* Section backgrounds */
}
```

## 📹 Video Tips

### Optimizing Videos for Web

```bash
# Convert to web-optimized MP4
ffmpeg -i input.mp4 -c:v libx264 -crf 23 -preset medium -c:a aac -movflags +faststart output.mp4

# Create a GIF from video (smaller file size for short clips)
ffmpeg -i input.mp4 -vf "fps=15,scale=480:-1" -loop 0 output.gif

# Compress existing MP4
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 output.mp4
```

### Recommended Video Settings
- **Resolution:** 720p or 480p for result grids
- **Duration:** 3-10 seconds for looping demos
- **Format:** MP4 (H.264) for best compatibility
- **File size:** Keep under 5MB per video when possible

## 🔧 Adding New Sections

Copy this template for new sections:

```html
<section class="your-section-name">
  <div class="container">
    <h2 class="section-title">Section Title</h2>
    <p>Your content here.</p>
    
    <div class="results-grid">
      <!-- Add cards here -->
    </div>
  </div>
</section>
```

## 📱 Mobile Optimization

The template is fully responsive. Test your site on mobile using:
- Chrome DevTools (F12 → Toggle Device Toolbar)
- Or simply resize your browser window

## 🌐 Custom Domain (Optional)

1. Add a `CNAME` file with your domain:
   ```
   yourpaper.yourdomain.com
   ```

2. Configure DNS with your domain provider

3. Enable HTTPS in GitHub Pages settings

## 📝 SEO & Social Sharing

Update the meta tags in `<head>`:

```html
<meta name="description" content="Your paper description">
<meta property="og:title" content="Your Paper Title">
<meta property="og:description" content="Brief description for social media">
<meta property="og:image" content="static/images/teaser.png">
```

## 🤝 Credits

This template is inspired by:
- [Nerfies](https://nerfies.github.io)
- [FTL-IGM](https://avivne.github.io/ftl-igm/)
- [Diffuser](https://diffusion-planning.github.io/)
- [Veo Robotics](https://veo-robotics.github.io/)

## 📄 License

This template is released under the MIT License. Feel free to use it for your academic projects!

---

**Need help?** Open an issue or reach out to the template maintainers.

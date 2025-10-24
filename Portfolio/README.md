# Portfolio & Blog Website

A modern, glassmorphism-styled personal portfolio and blog website with dark/light theme support. Built with pure HTML, CSS, and vanilla JavaScript.

## 🎨 Design Style

This website features a **Glassmorphism** design aesthetic with:

- Frosted glass effects using `backdrop-filter`
- Translucent panels and cards
- Smooth transitions and animations
- Dark mode by default with light theme toggle
- Responsive design for all devices

## 📁 Project Structure

```
Portfolio/
├── index.html          # Homepage with portfolio grid
├── blog.html           # Blog posts page with filtering
├── about.html          # Detailed about/bio page
├── contact.html        # Contact form and info
├── style.css           # Main stylesheet (glassmorphism effects)
├── blog.css            # Blog-specific styles
├── about.css           # About page styles
├── contact.css         # Contact page styles
├── images/             # Place your images here
│   └── logo.png        # Your site logo (favicon)
└── blog-posts/         # Individual blog post pages (future)
```

## 🚀 Getting Started

### 1. Personalize Your Content

**Replace placeholders in all HTML files:**

- `[Your Name]` → Your actual name
- `[Your City]` → Your location
- `your.email@example.com` → Your email address
- Social media links (GitHub, LinkedIn, Twitter)
- Profile image URL in `about.html`

### 2. Add Your Logo

Place your logo file in the `images/` folder and name it `logo.png`, or update the favicon link in all HTML files:

```html
<link rel="icon" href="images/your-logo.png" type="image/png" />
```

### 3. Customize Colors

The primary accent color is green (`#22c55e`). To change it:

1. Open `style.css`
2. Find and replace `#22c55e` with your preferred color
3. Also update `#16a34a` (darker shade for hover effects)

**Popular alternatives:**

- Blue: `#3b82f6` / `#2563eb`
- Purple: `#a855f7` / `#9333ea`
- Orange: `#f97316` / `#ea580c`
- Pink: `#ec4899` / `#db2777`

### 4. Update Portfolio Cards

In `index.html`, customize the portfolio grid cards (`.portfolio-card`):

```html
<div class="portfolio-card card-1" onclick="window.location.href='your-link'">
  <div class="card-content">
    <h3>Your Project Title</h3>
    <p>Brief description</p>
  </div>
</div>
```

**Card gradient colors** are in `style.css`:

```css
.card-1 {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### 5. Add Your Projects

In `index.html`, update the featured projects section:

```html
<div class="featured-card">
  <div class="featured-image" style="background-image: url('your-image-url');">
    <div class="featured-overlay">
      <span class="featured-tag">Category</span>
    </div>
  </div>
  <div class="featured-info">
    <h3>Project Name</h3>
    <p>Description...</p>
    <div class="tech-stack">
      <span>Tech1</span>
      <span>Tech2</span>
    </div>
    <a href="#" class="project-link">View Project →</a>
  </div>
</div>
```

### 6. Add Blog Posts

In `blog.html`, add new blog posts:

```html
<article class="blog-card" data-category="tech">
  <div class="blog-image" style="background-image: url('image-url');">
    <span class="blog-category">Tech</span>
  </div>
  <div class="blog-content">
    <div class="blog-meta">
      <span class="blog-date">Date</span>
      <span class="read-time">X min read</span>
    </div>
    <h2>Post Title</h2>
    <p>Excerpt...</p>
    <a href="blog-posts/post-name.html" class="read-more">Read More →</a>
  </div>
</article>
```

**Available categories:**

- `tech` - Technology posts
- `life` - Personal/lifestyle posts
- `tutorial` - How-to guides

### 7. Update About Page

Edit `about.html` to add:

- Your bio in the bio section
- Your journey/timeline items
- Your values and principles
- Fun facts about yourself
- Your profile photo

### 8. Customize Skills

In `index.html`, update the skills section:

```html
<div class="skill-category">
  <h3>Category Name</h3>
  <ul>
    <li>Skill 1</li>
    <li>Skill 2</li>
    <li>Skill 3</li>
  </ul>
</div>
```

## 🎯 Features

### Theme Toggle

- Automatic theme persistence using localStorage
- Smooth transitions between dark/light modes
- Consistent styling across all pages

### Animations

- Slide-up animations for portfolio cards on page load
- Hover effects on all interactive elements
- Smooth scrolling for anchor links

### Responsive Design

- Mobile-first approach
- Breakpoints: 1024px, 768px, 480px
- Touch-friendly navigation on mobile

### Blog Filtering

The blog page includes category filtering. Categories are set via `data-category` attribute:

```html
<article class="blog-card" data-category="tech"></article>
```

## 🖼️ Using Your Own Images

### Option 1: Use External URLs (Current Setup)

The template uses Unsplash URLs. Simply replace them with your image URLs.

### Option 2: Use Local Images

1. Place images in the `images/` folder
2. Update image URLs:
   ```html
   <div style="background-image: url('images/your-photo.jpg');"></div>
   ```

### Recommended Image Sizes

- **Profile photo**: 400x400px (square)
- **Project images**: 800x600px or 1200x800px
- **Blog post images**: 800x500px
- **Logo/Favicon**: 512x512px (PNG with transparency)

## 📱 Browser Compatibility

**Fully Supported:**

- Chrome/Edge (90+)
- Firefox (88+)
- Safari (14+)

**Note:** `backdrop-filter` (glassmorphism effect) may not work on older browsers. The site will still be functional with solid backgrounds as fallback.

## 🛠️ Customization Tips

### Change Font

Replace the font family in `style.css`:

```css
body {
  font-family: "Your Font", -apple-system, BlinkMacSystemFont, sans-serif;
}
```

For custom fonts, add a Google Fonts link in all HTML `<head>` sections:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap"
  rel="stylesheet"
/>
```

### Adjust Glassmorphism Intensity

In `style.css`, modify the navbar blur:

```css
.navbar {
  backdrop-filter: blur(10px); /* Increase for more blur */
  background: rgba(255, 255, 255, 0.15); /* Adjust transparency */
}
```

### Change Card Grid Layout

Modify the portfolio grid in `style.css`:

```css
.portfolio-grid {
  grid-template-columns: repeat(3, 1fr); /* Change column count */
  grid-template-rows: repeat(4, 180px); /* Adjust row height */
}
```

## 📝 Creating Individual Blog Post Pages

Create new HTML files in `blog-posts/` folder:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Post Title</title>
    <link rel="stylesheet" href="../style.css" />
  </head>
  <body>
    <!-- Copy navbar from blog.html -->

    <article class="blog-post-content">
      <h1>Your Blog Post Title</h1>
      <div class="post-meta">Published on Date</div>

      <!-- Your content here -->
    </article>

    <!-- Copy footer from blog.html -->
  </body>
</html>
```

## 🚢 Deployment

### GitHub Pages (Free)

1. Create a GitHub repository
2. Upload all files
3. Go to Settings → Pages
4. Select main branch → Save
5. Your site will be live at `https://yourusername.github.io/repo-name`

### Netlify (Free)

1. Drag and drop the Portfolio folder to [Netlify Drop](https://app.netlify.com/drop)
2. Get instant deployment with custom domain support

### Vercel (Free)

1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the Portfolio folder
3. Follow the prompts

## 🎨 Color Schemes

Here are some pre-made color schemes you can use:

### Ocean Blue

- Primary: `#0ea5e9`
- Hover: `#0284c7`

### Sunset Orange

- Primary: `#f97316`
- Hover: `#ea580c`

### Royal Purple

- Primary: `#a855f7`
- Hover: `#9333ea`

### Cherry Pink

- Primary: `#ec4899`
- Hover: `#db2777`

## 📧 Contact Form Setup

The current contact form uses JavaScript `alert()` for demo purposes. To make it functional:

### Option 1: Formspree (Easy)

1. Sign up at [Formspree](https://formspree.io)
2. Create a form and get the endpoint
3. Update the form in `contact.html`:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST"></form>
```

### Option 2: EmailJS (Free)

1. Sign up at [EmailJS](https://www.emailjs.com)
2. Follow their integration guide
3. Replace the form script in `contact.html`

## 🐛 Troubleshooting

**Theme not persisting:**

- Clear browser localStorage and try again
- Check browser console for errors

**Images not loading:**

- Verify image paths are correct
- Check if image URLs are accessible
- Use relative paths for local images

**Blur effect not working:**

- Some browsers don't support `backdrop-filter`
- Consider using a solid background fallback

## 📄 License

Free to use for personal and commercial projects. Attribution appreciated but not required.

## 🤝 Credits

Design inspired by modern glassmorphism UI trends. Built from scratch with HTML, CSS, and JavaScript.

---

**Need help?** Open an issue or reach out via the contact form!

**Made with ❤️ and lots of ☕**

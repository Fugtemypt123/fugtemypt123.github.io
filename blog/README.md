# Blog System

This directory contains the blog posts for Shaofeng Yin's personal website.

## Structure

- `blog.html` - Main blog page with post thumbnails
- `blog/` - Directory containing individual blog posts
- `images/blog/` - Images for blog posts

## Adding New Blog Posts

### 1. Create the HTML file

Create a new HTML file in the `blog/` directory following this template:

```html
<!DOCTYPE HTML>
<html lang="en">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>Your Post Title - Shaofeng Yin</title>
    <meta name="author" content="Shaofeng Yin">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="shortcut icon" href="../images/favicon.ico" type="image/x-icon">
    <link rel="stylesheet" type="text/css" href="../stylesheet.css">
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
  </head>

  <body>
    <!-- Navigation Bar -->
    <div class="nav-container">
      <nav class="navbar">
        <div class="nav-content">
          <div class="nav-logo">
            <a href="../index.html">Shaofeng Yin</a>
          </div>
          <ul class="nav-menu">
            <li class="nav-item">
              <a href="../index.html" class="nav-link">Home</a>
            </li>
            <li class="nav-item">
              <a href="../blog.html" class="nav-link active">Blog</a>
            </li>
          </ul>
        </div>
      </nav>
    </div>

    <div class="blog-post">
      <a href="../blog.html" class="back-to-blog">← Back to Blog</a>
      
      <div class="blog-post-header">
        <h1 class="blog-post-title">Your Post Title</h1>
        <div class="blog-post-meta">Date • Reading time</div>
      </div>

      <div class="blog-post-content">
        <!-- Your content here -->
        <p>Your blog post content...</p>
        
        <!-- LaTeX math formulas -->
        <p style="text-align: center;">
          \[
          \text{Your math formula here}
          \]
        </p>
      </div>
    </div>
  </body>
</html>
```

### 2. Add thumbnail to blog.html

Add a new blog card to `blog.html`:

```html
<div class="blog-card" onclick="window.location.href='blog/your-post-filename.html'">
  <img src="images/blog/your-image.jpg" alt="Description">
  <div class="blog-card-content">
    <div class="blog-card-title">Your Post Title</div>
    <div class="blog-card-excerpt">
      Brief description of your post...
    </div>
    <div class="blog-card-date">Date</div>
  </div>
</div>
```

### 3. Add images

Place your blog post images in `images/blog/` directory.

## Features

- **LaTeX Support**: MathJax is included for rendering mathematical formulas
- **Responsive Design**: Works on desktop and mobile devices
- **Navigation**: Easy navigation between home and blog pages
- **Clean Typography**: Optimized for readability

## Math Formulas

Use LaTeX syntax for mathematical formulas:

- Inline math: `\(formula\)`
- Display math: `\[formula\]`

Example:
```html
<p>The quadratic formula is \(x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\)</p>

<p style="text-align: center;">
  \[
  \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
  \]
</p>
``` 
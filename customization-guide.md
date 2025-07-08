# GitHub Pages Customization Guide

## Easy Content Updates for Paul-Henri Website

This guide shows you how to update your GitHub Pages website content without any coding knowledge.

## Quick Updates via GitHub Web Interface

### Method 1: Edit Files Directly on GitHub (Easiest)

1. **Go to your repository** on GitHub.com
2. **Navigate to the file** you want to edit
3. **Click the pencil icon** (Edit this file)
4. **Make your changes** in the web editor
5. **Scroll down** to "Commit changes"
6. **Add a description** like "Update contact information"
7. **Click "Commit changes"**
8. **Wait 1-2 minutes** for changes to appear on your site

### Method 2: GitHub Desktop (Recommended for Multiple Changes)

1. **Download GitHub Desktop** from desktop.github.com
2. **Clone your repository** to your computer
3. **Make changes** to files using any text editor
4. **Commit and push** changes through GitHub Desktop

## Common Content Updates

### 1. Update Contact Information

**File to edit**: All HTML files (search for email addresses)

**Find and replace**:
```html
<!-- OLD -->
paulhenri@example.com

<!-- NEW -->
paulhenri@pauldepierre.com
```

**Update social media links**:
```html
<!-- In all HTML files, find and update these URLs -->
<a href="https://instagram.com/your-username" target="_blank">Instagram</a>
<a href="https://linkedin.com/in/your-username" target="_blank">LinkedIn</a>
<a href="https://youtube.com/@your-username" target="_blank">YouTube</a>
```

### 2. Add New Projects

**File to edit**: `index.html`

**Find the projects section** and add a new project card:
```html
<div class="project-card animate-slide-up delay-6">
    <div class="project-image">
        <img src="assets/images/new-project-hero.jpg" alt="New Project Name">
    </div>
    <div class="project-content">
        <h3 class="project-title">New Project Name</h3>
        <p class="project-tagline">Your project tagline here.</p>
        <p class="project-description">
            Description of your new project and what it does.
        </p>
        <a href="new-project.html" class="btn btn-primary btn-sm">Learn More</a>
    </div>
</div>
```

**Don't forget to**:
- Upload the project image to `assets/images/`
- Create a new HTML page for the project details
- Add the project to the navigation menu

### 3. Update Personal Story

**File to edit**: `index.html`

**Find the personal story section**:
```html
<section class="personal-story" id="story">
    <div class="container">
        <div class="story-content">
            <h2 class="section-title animate-on-scroll">My Story</h2>
            <div class="story-text animate-slide-up">
                <p>
                    <!-- Update this paragraph with your current story -->
                    Your updated personal story goes here...
                </p>
                <p>
                    <!-- Add additional paragraphs as needed -->
                    Continue your story here...
                </p>
            </div>
        </div>
    </div>
</section>
```

### 4. Add New Podcast Episodes

**File to edit**: `podcast.html`

**Find the podcast section** you want to update and add new episodes:
```html
<div class="episode-item">
    <h4>New Episode Title</h4>
    <p class="episode-meta">Duration: 45:32 | Published: March 2024</p>
    <p>Brief description of the episode content and key topics discussed.</p>
    <a href="https://link-to-episode" class="btn btn-secondary btn-sm" target="_blank">Listen Now</a>
</div>
```

### 5. Update Speaking Topics

**File to edit**: `book.html`

**Find the speaking topics section**:
```html
<div class="topic-card">
    <h3>New Speaking Topic</h3>
    <p>Description of the new topic you can speak about and key takeaways for audiences.</p>
</div>
```

### 6. Add Testimonials

**File to edit**: `book.html`

**Find the testimonials section**:
```html
<div class="testimonial">
    <blockquote>
        "Quote from the person who hired you or attended your talk."
    </blockquote>
    <cite>
        <strong>Person Name</strong><br>
        Title, Company Name
    </cite>
</div>
```

## Image Management

### Adding New Images

1. **Upload images** to the `assets/images/` folder
2. **Optimize images** before uploading:
   - Maximum width: 1200px for hero images, 800px for project images
   - File size: Under 500KB each
   - Format: JPG for photos, PNG for graphics with transparency

### Image File Naming

Use descriptive, lowercase names with hyphens:
- ✅ Good: `paul-henri-speaking-event-2024.jpg`
- ❌ Bad: `IMG_1234.jpg`

### Updating Existing Images

1. **Upload new image** with the same filename
2. **Or update the HTML** to reference the new filename:
```html
<img src="assets/images/new-image-name.jpg" alt="Descriptive alt text">
```

## Styling Updates

### Changing Colors

**File to edit**: `css/styles.css`

**Find the CSS variables section** at the top:
```css
:root {
    /* Update these values to change site colors */
    --primary-black: #000000;
    --primary-gold: #C9A449;
    --light-gold: #f4e6a1;
    /* Add new colors here */
}
```

### Updating Fonts

**File to edit**: All HTML files

**Find the Google Fonts link** in the `<head>` section:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Poppins:wght@400;600;700&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">
```

**Then update CSS**:
```css
:root {
    --font-primary: 'Your-New-Font', sans-serif;
    --font-headings: 'Your-Heading-Font', sans-serif;
}
```

## SEO Updates

### Page Titles and Descriptions

**In each HTML file**, find and update the `<head>` section:
```html
<title>Your New Page Title - Paul-Henri Cuvelier</title>
<meta name="description" content="Updated description of this page content for search engines.">
```

### Open Graph Images

**Update social sharing images**:
```html
<meta property="og:image" content="https://paulhenricuvelier.com/assets/images/your-new-og-image.jpg">
```

## Form Configuration

### Contact Form Setup

**File to edit**: `contact.html` and `book.html`

**Update the form action** with your Formspree endpoint:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Adding Form Fields

```html
<div class="form-group">
    <label for="new-field">New Field Label</label>
    <input type="text" id="new-field" name="new-field" required>
</div>
```

## Analytics Configuration

### Google Analytics

**File to edit**: All HTML files

**Find and update the tracking code**:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'YOUR-GA-ID');
</script>
```

## Navigation Updates

### Adding New Pages to Menu

**File to edit**: All HTML files

**Find the navigation section** and add new menu items:
```html
<div class="nav-menu" id="nav-menu">
    <a href="index.html" class="nav-link">Home</a>
    <a href="wtfiph.html" class="nav-link">WTFIPH</a>
    <a href="podcast.html" class="nav-link">Podcasts</a>
    <!-- Add your new page here -->
    <a href="new-page.html" class="nav-link">New Page</a>
    <a href="contact.html" class="nav-link">Contact</a>
</div>
```

**Remember to**:
- Update navigation in ALL HTML files
- Create the new HTML page
- Add the page to `sitemap.xml`

## Testing Your Changes

### Before Publishing

1. **Preview changes** using GitHub's file preview
2. **Check for typos** in content updates
3. **Verify links work** by clicking them
4. **Test on mobile** by viewing on your phone

### After Publishing

1. **Wait 1-2 minutes** for changes to deploy
2. **Clear browser cache** (Ctrl+F5 or Cmd+Shift+R)
3. **Test key functionality**:
   - Navigation links
   - Contact forms
   - Social media links
   - Mobile menu

### Common Issues and Fixes

#### Changes Not Appearing
- **Wait longer**: GitHub Pages can take up to 10 minutes
- **Clear cache**: Hard refresh your browser
- **Check commit**: Ensure changes were committed to repository

#### Broken Images
- **Check file path**: Ensure correct folder and filename
- **Check file size**: Images over 25MB won't load
- **Verify upload**: Confirm image was uploaded to repository

#### Styling Issues
- **Check CSS syntax**: Look for missing semicolons or brackets
- **Validate HTML**: Use W3C HTML validator
- **Test in different browsers**: Chrome, Firefox, Safari

## Backup and Version Control

### Before Major Changes

1. **Create a branch** for testing changes
2. **Test thoroughly** before merging to main
3. **Keep backup** of important content

### Regular Maintenance

- **Monthly**: Review and update content
- **Quarterly**: Check all links and forms
- **Annually**: Update photos and achievements

This customization guide ensures you can easily maintain and update your GitHub Pages website while preserving the professional design and functionality.
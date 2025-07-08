# GitHub Pages Deployment Guide

## Complete Setup in Under 2 Hours

This guide walks you through deploying your Paul-Henri website to GitHub Pages with 100% visual fidelity maintained.

## Prerequisites (5 minutes)

### Required Accounts
- **GitHub Account**: Create free account at github.com
- **Email Account**: For contact form notifications
- **Domain (Optional)**: If using custom domain like paulhenricuvelier.com

### Download Package
- Download all files from the `github-pages-conversion` folder
- Keep the folder structure intact
- Have your logo and any custom images ready

## Step 1: GitHub Repository Setup (10 minutes)

### Create New Repository
1. **Log into GitHub**
2. **Click "New repository"** (green button)
3. **Repository name**: 
   - For GitHub subdomain: `your-username.github.io`
   - For custom domain: `paulhenricuvelier.com` or any name
4. **Description**: "Paul-Henri Cuvelier Personal Website"
5. **Set to Public** (required for free GitHub Pages)
6. **Check "Add a README file"**
7. **Click "Create repository"**

### Upload Website Files
1. **Click "uploading an existing file"** link
2. **Drag and drop all files** from the conversion package
3. **Maintain folder structure**:
   ```
   /
   ├── index.html
   ├── wtfiph.html
   ├── podcast.html
   ├── contact.html
   ├── book.html
   ├── css/styles.css
   ├── js/main.js
   ├── assets/images/
   ├── _config.yml
   └── CNAME (if using custom domain)
   ```
4. **Commit message**: "Initial website upload"
5. **Click "Commit changes"**

## Step 2: Enable GitHub Pages (5 minutes)

### Configure Pages Settings
1. **Go to repository Settings** (tab at top)
2. **Scroll down to "Pages"** section (left sidebar)
3. **Source**: Select "Deploy from a branch"
4. **Branch**: Select "main" 
5. **Folder**: Select "/ (root)"
6. **Click "Save"**

### Verify Deployment
1. **Wait 2-3 minutes** for initial build
2. **Refresh the Pages settings page**
3. **Green checkmark** should appear with URL
4. **Click the URL** to view your live site
5. **Site URL will be**: `https://your-username.github.io`

## Step 3: Custom Domain Setup (Optional - 15 minutes)

### If You Own a Domain
1. **Add CNAME file** to repository root:
   ```
   paulhenricuvelier.com
   ```
2. **Configure DNS with your domain provider**:
   - **A Records** (point to GitHub IPs):
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - **OR CNAME Record**: `your-username.github.io`

### GitHub Pages Domain Settings
1. **Go to Pages settings** in repository
2. **Custom domain**: Enter `paulhenricuvelier.com`
3. **Check "Enforce HTTPS"** (wait 24 hours if needed)
4. **DNS check**: GitHub will verify DNS configuration

## Step 4: Contact Form Configuration (10 minutes)

### Set Up Formspree (Recommended)
1. **Go to formspree.io** and create free account
2. **Create new form**
3. **Get form endpoint**: `https://formspree.io/f/YOUR_FORM_ID`
4. **Edit contact.html and book.html**:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. **Replace email address** with: `paulhenri@pauldepierre.com`

### Alternative: EmailJS Setup
1. **Create account at emailjs.com**
2. **Set up email service** (Gmail, Outlook, etc.)
3. **Create email template**
4. **Update js/main.js** with your service ID and template ID
5. **Test form submissions**

## Step 5: Analytics Setup (10 minutes)

### Google Analytics 4
1. **Create Google Analytics account**
2. **Set up GA4 property** for your domain
3. **Get Measurement ID**: G-XXXXXXXXXX
4. **Edit all HTML files**, replace placeholder:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   ```
5. **Update tracking ID** in gtag config

### Google Search Console
1. **Go to search.google.com/search-console**
2. **Add property** with your domain
3. **Verify ownership** using HTML file method
4. **Upload verification file** to repository root
5. **Submit sitemap**: `https://yoursite.com/sitemap.xml`

## Step 6: Content Customization (30-60 minutes)

### Update Contact Information
1. **Edit all HTML files**
2. **Replace email addresses** with: `paulhenri@pauldepierre.com`
3. **Update social media links** with your actual profiles
4. **Verify all links work correctly**

### Customize Content
1. **Edit text content** in HTML files as needed
2. **Replace placeholder images** with your actual photos
3. **Update project descriptions** to match current status
4. **Add new achievements or testimonials**

### SEO Optimization
1. **Edit meta tags** in each HTML file head section
2. **Update Open Graph images** with your photos
3. **Customize page titles** and descriptions
4. **Verify structured data** is accurate

## Step 7: Testing & Launch (20 minutes)

### Cross-Browser Testing
- **Desktop**: Chrome, Safari, Firefox, Edge
- **Mobile**: iPhone Safari, Android Chrome
- **Check**: Layout, animations, forms, navigation

### Functionality Testing
- [ ] All navigation links work
- [ ] Contact forms submit successfully
- [ ] Social media links open correctly
- [ ] Mobile menu functions properly
- [ ] Page loading speed under 3 seconds
- [ ] Images load correctly
- [ ] Animations trigger on scroll

### SEO Verification
- [ ] Google PageSpeed Insights score 90+
- [ ] All pages have unique titles
- [ ] Meta descriptions are compelling
- [ ] Images have alt text
- [ ] Structured data validates

## Step 8: Post-Launch Setup (15 minutes)

### Submit to Search Engines
1. **Google Search Console**: Submit sitemap
2. **Bing Webmaster Tools**: Add and verify site
3. **Social Media**: Update bio links to new site

### Monitor Performance
1. **Google Analytics**: Verify tracking works
2. **GitHub Insights**: Check traffic statistics
3. **Form Testing**: Send test contact submissions
4. **Speed Testing**: Monitor Core Web Vitals

## Ongoing Maintenance

### Content Updates
1. **Edit HTML files** directly on GitHub
2. **Or clone repository** and edit locally
3. **Commit changes** to automatically deploy
4. **Changes appear** within 1-2 minutes

### Adding New Content
1. **New pages**: Copy existing HTML as template
2. **New images**: Upload to assets/images/
3. **Update navigation**: Add links in all HTML files
4. **Update sitemap.xml**: Include new pages

### Performance Monitoring
- **Monthly**: Check Google Analytics reports
- **Quarterly**: Run PageSpeed Insights tests
- **As needed**: Update contact information
- **Annually**: Review and refresh content

## Troubleshooting Common Issues

### Site Not Loading
1. **Check repository name**: Must be `username.github.io` for subdomain
2. **Verify Pages is enabled** in repository settings
3. **Wait 10 minutes** for initial deployment
4. **Check build status** in repository Actions tab

### Custom Domain Not Working
1. **Verify DNS settings** with domain provider
2. **Wait 24-48 hours** for DNS propagation
3. **Check CNAME file** contains only domain name
4. **Disable and re-enable** custom domain in settings

### Forms Not Working
1. **Check form action URL** points to correct service
2. **Verify Formspree account** is set up correctly
3. **Test with different email address**
4. **Check spam folder** for form submissions

### Images Not Loading
1. **Check file paths** are correct (case-sensitive)
2. **Verify images uploaded** to correct folder
3. **Use relative paths** (./assets/images/file.jpg)
4. **Check image file sizes** under 1MB each

### Performance Issues
1. **Optimize images** using tools like TinyPNG
2. **Check file sizes** in repository
3. **Remove unused CSS/JS** code
4. **Test on different networks**

## Success Checklist

### Technical Setup Complete
- [ ] Repository created and files uploaded
- [ ] GitHub Pages enabled and site accessible
- [ ] Custom domain configured (if applicable)
- [ ] HTTPS working correctly
- [ ] All pages loading properly

### Content Ready
- [ ] Contact information updated
- [ ] Social media links working
- [ ] Project descriptions current
- [ ] Images optimized and loading
- [ ] Form submissions tested

### SEO Optimized
- [ ] Google Analytics tracking
- [ ] Search Console verified
- [ ] Sitemap submitted
- [ ] Meta tags complete
- [ ] Performance score 90+

### Business Ready
- [ ] Contact forms receiving emails
- [ ] Professional appearance verified
- [ ] Mobile experience perfect
- [ ] All business links functional
- [ ] Ready to share with audiences

Congratulations! Your Paul-Henri website is now live on GitHub Pages with zero hosting costs and professional appearance.
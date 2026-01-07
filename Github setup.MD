# GitHub Pages Setup Guide for HTML-6X

This guide will walk you through setting up your HTML-6X project on GitHub and deploying it to GitHub Pages.

## 📋 Prerequisites

- GitHub account
- Git installed on your computer
- All HTML-6X files downloaded

## 🚀 Step-by-Step Setup

### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Fill in the details:
   - **Repository name:** `html-6x` (or your preferred name)
   - **Description:** "Revolutionary web development with atomic components"
   - **Public** (so GitHub Pages works for free)
   - **Don't** initialize with README (we have our own)

3. Click **Create repository**

### Step 2: Prepare Your Files

Make sure you have all these files in a folder:

```
html-6x/
├── index.html                   # Landing page (NEW!)
├── README.md
├── HTML-6X-SPECIFICATION.md
├── GETTING-STARTED.md
├── PROJECT-SUMMARY.md
├── h6x-runtime.js
├── h6x-validator.js
├── demo-app.html
├── task-manager-app.html
└── test-suite.html
```

### Step 3: Initialize Git Repository

Open terminal/command prompt in your project folder:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: HTML-6X v0.1.0"

# Add your GitHub repository as remote
# Replace 'yourusername' with your actual GitHub username
git remote add origin https://github.com/yourusername/html-6x.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

### Step 5: Wait for Deployment

GitHub will automatically deploy your site. This takes 1-2 minutes.

You'll see a message like:
```
Your site is live at https://yourusername.github.io/html-6x/
```

### Step 6: Test Your Site

Visit your GitHub Pages URL and verify:

- ✅ Landing page loads
- ✅ Demo app works: `https://yourusername.github.io/html-6x/demo-app.html`
- ✅ Task manager works: `https://yourusername.github.io/html-6x/task-manager-app.html`
- ✅ Test suite runs: `https://yourusername.github.io/html-6x/test-suite.html`

## 🎨 Customize Your Repository

### Update README.md

Edit the GitHub repository link in README.md:

```markdown
<!-- Change this -->
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](https://github.com/html-6x/html-6x)

<!-- To this (with your username) -->
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](https://github.com/yourusername/html-6x)
```

### Update index.html

Edit the GitHub link in index.html:

```html
<!-- Change this -->
<a href="https://github.com/yourusername/html-6x" class="btn btn-secondary">⭐ GitHub</a>

<!-- To your actual repo URL -->
<a href="https://github.com/YOURACTUALUSERNAME/html-6x" class="btn btn-secondary">⭐ GitHub</a>
```

### Add a LICENSE file

```bash
# Create LICENSE file
cat > LICENSE << 'EOF'
MIT License

Copyright (c) 2026 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF

git add LICENSE
git commit -m "Add MIT license"
git push
```

### Add Topics to Repository

On GitHub, add these topics to help people discover your project:

1. Go to your repository
2. Click the gear icon next to "About"
3. Add topics:
   - `html`
   - `web-development`
   - `framework`
   - `atomic-design`
   - `security`
   - `javascript`
   - `single-file`
   - `declarative`

## 📢 Promote Your Project

### 1. Share on Social Media

**Twitter/X:**
```
🚀 Just launched HTML-6X - a revolutionary way to build web apps!

✨ Single HTML file
🔒 Security by default
⚡ Zero build time
📦 No dependencies

Check it out: https://yourusername.github.io/html-6x/

#WebDev #JavaScript #HTML
```

**LinkedIn:**
```
I'm excited to share HTML-6X, a new approach to web development that brings simplicity back to the web.

Key features:
• Single-file applications
• Atomic component model
• Built-in security (CSP, XSS prevention)
• Zero dependencies
• No build process needed

Live demo: https://yourusername.github.io/html-6x/

This could be the future of web development. What do you think?
```

### 2. Post on Developer Communities

**Hacker News:**
- Title: "HTML-6X: Single-file web apps with atomic components"
- URL: Your GitHub Pages link
- Best time: Weekday mornings (EST)

**Reddit:**
- r/javascript
- r/webdev
- r/programming
- Title: "I built HTML-6X: A new way to create web apps in a single HTML file"

**Dev.to:**
Write a blog post explaining:
- Why you created it
- How it works
- Live demos
- Comparison with existing tools

### 3. Product Hunt

Submit to Product Hunt:
- Title: "HTML-6X - Revolutionary web development"
- Tagline: "Build secure web apps in a single HTML file"
- Include screenshots and GIFs

## 🔄 Keep Your Site Updated

When you make changes:

```bash
# Make your changes
nano demo-app.html  # or any file

# Commit changes
git add .
git commit -m "Update demo app with new features"
git push

# GitHub Pages will auto-deploy in 1-2 minutes
```

## 📊 Track Analytics (Optional)

### Add Google Analytics

Add to `<head>` of index.html:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Add GitHub Insights

GitHub provides built-in analytics:
- Go to your repo → Insights → Traffic
- See page views, clones, referring sites

## 🎯 Custom Domain (Optional)

### Use Your Own Domain

1. Buy a domain (e.g., from Namecheap, GoDaddy)

2. Add CNAME file to your repository:
```bash
echo "html6x.dev" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

3. Configure DNS with your domain provider:
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

4. Wait for DNS propagation (5-30 minutes)

5. Update GitHub Pages settings:
   - Settings → Pages
   - Custom domain: `www.html6x.dev`
   - Enable "Enforce HTTPS"

## ✅ Verification Checklist

Before announcing your project:

- [ ] All files pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Landing page loads correctly
- [ ] All demo apps work
- [ ] Links in README point to correct URLs
- [ ] LICENSE file added
- [ ] Repository topics added
- [ ] README has clear description
- [ ] Screenshots/GIFs added (optional but recommended)

## 🐛 Troubleshooting

### Site not loading after deployment

**Problem:** 404 error on GitHub Pages URL

**Solution:**
- Wait 2-5 minutes for initial deployment
- Check Settings → Pages shows "Your site is published"
- Verify branch is set to `main` and folder to `/` (root)

### Demo apps not working

**Problem:** Apps show blank page or errors

**Solution:**
- Check browser console for errors
- Verify h6x-runtime.js is in same directory
- Ensure CSP headers aren't too strict

### Images/assets not loading

**Problem:** Resources show 404

**Solution:**
- Use relative paths (e.g., `./image.png` not `/image.png`)
- Verify files are committed to repository
- Check file names match exactly (case-sensitive)

## 📱 Mobile Testing

Test your site on mobile:
1. Open on your phone's browser
2. Use Chrome DevTools mobile emulation
3. Check responsive design works
4. Verify touch interactions

## 🎉 Success!

Your HTML-6X project is now live on GitHub Pages!

**Your URLs:**
- Landing: `https://yourusername.github.io/html-6x/`
- Demo: `https://yourusername.github.io/html-6x/demo-app.html`
- Task Manager: `https://yourusername.github.io/html-6x/task-manager-app.html`

## 🚀 Next Steps

1. Star your own repository
2. Share on social media
3. Write a blog post about it
4. Submit to Product Hunt
5. Engage with feedback
6. Keep iterating!

---

**Need help?** Create an issue on GitHub or reach out to the community!

Good luck! 🎊

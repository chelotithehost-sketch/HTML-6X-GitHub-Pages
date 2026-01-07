# Quick Setup Commands - HTML-6X on GitHub Pages

Copy and paste these commands to get your HTML-6X project live in 5 minutes!

## 🚀 Quick Start (3 Commands)

```bash
# 1. Initialize and commit
git init
git add .
git commit -m "Initial commit: HTML-6X v0.1.0"

# 2. Connect to GitHub (replace 'yourusername' with your GitHub username)
git remote add origin https://github.com/yourusername/html-6x.git
git branch -M main

# 3. Push to GitHub
git push -u origin main
```

**Then enable GitHub Pages:**
1. Go to: `https://github.com/yourusername/html-6x/settings/pages`
2. Source: Branch = `main`, Folder = `/ (root)`
3. Click Save
4. Done! Site will be live at `https://yourusername.github.io/html-6x/`

---

## 📋 Prerequisites

Before running commands:

1. **Create GitHub repository:**
   - Go to: https://github.com/new
   - Name: `html-6x`
   - Public repository
   - Don't initialize with README

2. **Have Git installed:**
   ```bash
   # Check if Git is installed
   git --version
   
   # If not installed:
   # Mac: brew install git
   # Ubuntu: sudo apt install git
   # Windows: Download from git-scm.com
   ```

3. **Configure Git (first time only):**
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

---

## 📁 File Organization

Make sure your folder has these files:

```
html-6x/
├── index.html                   ✓ Landing page
├── demo-app.html                ✓ Basic demo
├── task-manager-app.html        ✓ Advanced demo
├── test-suite.html              ✓ Test runner
├── h6x-runtime.js              ✓ Runtime engine
├── h6x-validator.js            ✓ Validator tool
├── README.md                    ✓ Main docs
├── HTML-6X-SPECIFICATION.md     ✓ Full spec
├── GETTING-STARTED.md           ✓ Tutorial
├── PROJECT-SUMMARY.md           ✓ Overview
└── GITHUB-SETUP.md             ✓ This guide
```

---

## 🔄 Complete Setup Script

Copy this entire block:

```bash
#!/bin/bash

# Navigate to your project folder
cd /path/to/your/html-6x

# Initialize repository
git init

# Add all files
git add .

# Initial commit
git commit -m "Initial commit: HTML-6X v0.1.0 - Revolutionary web development framework"

# Add remote (CHANGE 'yourusername' to your GitHub username!)
git remote add origin https://github.com/yourusername/html-6x.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main

echo "✅ Done! Now enable GitHub Pages in repository settings."
echo "Go to: https://github.com/yourusername/html-6x/settings/pages"
```

**Make it executable and run:**

```bash
chmod +x setup.sh
./setup.sh
```

---

## 🎯 After First Push

### Enable GitHub Pages

**Via Web:**
1. `https://github.com/yourusername/html-6x/settings/pages`
2. Source: `main` branch, `/ (root)` folder
3. Save

**Via GitHub CLI (if installed):**
```bash
gh repo view --web
# Then click Settings → Pages manually
```

### Verify Deployment

```bash
# Check deployment status
# Your site will be at:
echo "https://yourusername.github.io/html-6x/"

# Check specific pages:
echo "Demo: https://yourusername.github.io/html-6x/demo-app.html"
echo "Tasks: https://yourusername.github.io/html-6x/task-manager-app.html"
echo "Tests: https://yourusername.github.io/html-6x/test-suite.html"
```

---

## 🔧 Update Commands

When you make changes:

```bash
# See what changed
git status

# Add specific file
git add filename.html

# Or add all changes
git add .

# Commit with message
git commit -m "Update: description of changes"

# Push to GitHub (auto-deploys to Pages)
git push

# Check deployment
# Wait 1-2 minutes, then visit your GitHub Pages URL
```

---

## 📝 Useful Git Commands

```bash
# View commit history
git log --oneline

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Discard changes to a file
git checkout -- filename.html

# Create a new branch
git checkout -b feature-branch

# Switch back to main
git checkout main

# View remote URL
git remote -v

# Change remote URL
git remote set-url origin https://github.com/newusername/html-6x.git
```

---

## 🎨 Customize for Your Username

**Find and replace in all files:**

```bash
# Replace 'yourusername' with your actual username
# Mac/Linux:
find . -type f -name "*.md" -o -name "*.html" | xargs sed -i '' 's/yourusername/ACTUALUSERNAME/g'

# Linux (no macOS):
find . -type f -name "*.md" -o -name "*.html" | xargs sed -i 's/yourusername/ACTUALUSERNAME/g'

# Windows (PowerShell):
Get-ChildItem -Recurse -Include *.md,*.html | ForEach-Object {
    (Get-Content $_.FullName) -replace 'yourusername', 'ACTUALUSERNAME' | Set-Content $_.FullName
}
```

Then commit the changes:

```bash
git add .
git commit -m "Update URLs with actual username"
git push
```

---

## 🚨 Common Issues & Fixes

### "Permission denied (publickey)"

**Solution: Use HTTPS instead of SSH**
```bash
git remote set-url origin https://github.com/yourusername/html-6x.git
```

### "Repository not found"

**Solution: Check repository exists and URL is correct**
```bash
# Verify remote URL
git remote -v

# Update if wrong
git remote set-url origin https://github.com/CORRECT-USERNAME/html-6x.git
```

### "fatal: not a git repository"

**Solution: Initialize git**
```bash
git init
```

### "Updates were rejected"

**Solution: Pull first, then push**
```bash
git pull origin main --allow-unrelated-histories
git push origin main
```

### GitHub Pages shows 404

**Solutions:**
- Wait 2-5 minutes after first push
- Check Settings → Pages is enabled
- Verify files are in root directory
- Check branch name is `main`

---

## 🎉 One-Line Deploy

After initial setup, deploy updates with one command:

```bash
git add . && git commit -m "Update" && git push
```

Or create an alias:

```bash
# Add to ~/.bashrc or ~/.zshrc
alias deploy='git add . && git commit -m "Update $(date)" && git push'

# Then just run:
deploy
```

---

## 🌐 Test Locally Before Push

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server -p 8000

# PHP
php -S localhost:8000

# Then open: http://localhost:8000
```

---

## 📱 Mobile Preview

Test on mobile before deploying:

```bash
# Find your local IP
# Mac/Linux:
ifconfig | grep "inet "

# Windows:
ipconfig

# Start server with your IP
python3 -m http.server 8000

# On phone, visit:
# http://YOUR.LOCAL.IP:8000
```

---

## ✅ Pre-Deploy Checklist

Run before pushing:

```bash
# 1. Validate HTML files
# (if you have html-tidy installed)
tidy -q -e index.html

# 2. Check for broken links
# grep -r "href=" . | grep "yourusername"

# 3. Test locally
python3 -m http.server 8000

# 4. View git status
git status

# 5. See what will be committed
git diff

# 6. All good? Deploy!
git add . && git commit -m "Ready for deployment" && git push
```

---

## 🎯 Summary

**To deploy HTML-6X to GitHub Pages:**

1. Create GitHub repo: `html-6x`
2. Run: `git init && git add . && git commit -m "Initial"`
3. Run: `git remote add origin https://github.com/USER/html-6x.git`
4. Run: `git push -u origin main`
5. Enable GitHub Pages in Settings
6. Wait 2 minutes
7. Visit: `https://USER.github.io/html-6x/`

**Done!** 🎊

---

**Need the full guide?** See GITHUB-SETUP.md

**Questions?** Create an issue on GitHub!

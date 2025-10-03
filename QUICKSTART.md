# Quick Start Guide

This guide will help you quickly set up and run this Jekyll site with sitemap generation.

## 🚀 5-Minute Setup

### 1. Install Prerequisites

**On macOS:**
```bash
brew install ruby
gem install bundler
```

**On Ubuntu/Debian:**
```bash
sudo apt-get install ruby-full build-essential
gem install bundler
```

**On Windows:**
- Download and install [Ruby+Devkit](https://rubyinstaller.org/)
- Run `gem install bundler` in Command Prompt

### 2. Clone and Build

```bash
# Clone the repository
git clone https://github.com/ValentinaPetrova/SitemapTest.git
cd SitemapTest

# Install dependencies
bundle install

# Build the site
bundle exec jekyll build

# View the sitemap
cat _site/sitemap.xml
```

### 3. Run Locally

```bash
# Start the Jekyll server
bundle exec jekyll serve

# Open browser to http://localhost:4000/SitemapTest/
```

## 📋 What's Included

After building, you'll find:
- **_site/sitemap.xml** - The generated sitemap with all pages
- **_site/index.html** - Homepage
- **_site/about/** - About page
- **_site/contact/** - Contact page
- **_site/blog/** - Blog listing page
- **_site/2024/** - Blog posts organized by date

## 🔍 Verify Sitemap

```bash
# View sitemap in terminal
cat _site/sitemap.xml

# Or open in browser
open _site/sitemap.xml  # macOS
xdg-open _site/sitemap.xml  # Linux
start _site/sitemap.xml  # Windows
```

The sitemap should contain URLs for:
- Homepage (/)
- About page (/about/)
- Contact page (/contact/)
- Blog page (/blog/)
- All blog posts (/YYYY/MM/DD/post-title/)

## 🌐 Deploy to GitHub Pages

### Option 1: Automatic (Recommended)

1. Push this repository to GitHub
2. Go to Settings → Pages
3. Set source to "GitHub Actions"
4. The `.github/workflows/jekyll.yml` will automatically build and deploy
5. Visit: `https://your-username.github.io/SitemapTest/sitemap.xml`

### Option 2: Manual

1. Build the site: `bundle exec jekyll build`
2. Deploy the `_site` folder to your hosting provider

## 🧪 Test with Nuclia

Once deployed, use this URL with Nuclia:
```
https://your-username.github.io/SitemapTest/sitemap.xml
```

Nuclia will:
1. Fetch the sitemap.xml
2. Discover all URLs listed
3. Index the content of each page
4. Make it searchable

## 📝 Add New Content

### Add a Page

Create a new `.md` file:
```bash
cat > new-page.md << 'EOF'
---
layout: default
title: New Page
permalink: /new-page/
---

# New Page

Your content here...
EOF
```

### Add a Blog Post

```bash
cat > _posts/2024-10-03-my-post.md << 'EOF'
---
layout: default
title: "My New Post"
date: 2024-10-03 12:00:00 +0000
categories: example
---

# My New Post

Your content here...
EOF
```

### Rebuild

```bash
bundle exec jekyll build
# Check _site/sitemap.xml - your new content is included!
```

## 🐛 Troubleshooting

**Jekyll won't install:**
- Ensure Ruby version 2.7 or higher: `ruby --version`
- Try: `gem update --system`

**Bundle install fails:**
- Try: `bundle update`
- Or: `rm Gemfile.lock && bundle install`

**Sitemap not generated:**
- Check `_config.yml` has `jekyll-sitemap` in plugins
- Ensure build completed without errors
- Look for `_site/sitemap.xml`

**404 on GitHub Pages:**
- Check repository name matches `baseurl` in `_config.yml`
- Ensure GitHub Actions workflow completed successfully
- Wait a few minutes after first deployment

## 📚 Learn More

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [jekyll-sitemap Plugin](https://github.com/jekyll/jekyll-sitemap)
- [GitHub Pages Guide](https://docs.github.com/en/pages)
- [Sitemaps Protocol](https://www.sitemaps.org/)

## 💡 Tips

1. **Always rebuild** after making changes: `bundle exec jekyll build`
2. **Use `--watch`** for auto-rebuild during development: `bundle exec jekyll serve --watch`
3. **Check the sitemap** after adding content to ensure it's included
4. **Test locally** before deploying to production
5. **Keep URLs clean** - avoid spaces, use hyphens instead

## 🎯 Next Steps

1. ✅ Build the site locally
2. ✅ Verify sitemap.xml is generated
3. ✅ Add your own content
4. ✅ Deploy to GitHub Pages
5. ✅ Test with Nuclia

Happy building! 🚀

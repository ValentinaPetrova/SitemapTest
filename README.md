# SitemapTest

A test repository for creating a Jekyll website with automatic sitemap generation. This repository contains all the necessary files to build a Jekyll site and generate a `sitemap.xml` file for testing with Nuclia or other search tools.

## 📁 Repository Structure

```
SitemapTest/
├── _config.yml           # Jekyll configuration
├── _layouts/             # HTML layouts
│   └── default.html      # Default page layout
├── _posts/               # Blog posts
│   ├── 2024-01-01-welcome-to-jekyll.md
│   ├── 2024-01-15-understanding-sitemaps.md
│   └── 2024-02-01-testing-with-nuclia.md
├── index.md              # Homepage
├── about.md              # About page
├── contact.md            # Contact page
├── blog.md               # Blog listing page
├── Gemfile               # Ruby dependencies
├── .gitignore            # Git ignore file
└── README.md             # This file
```

## 🚀 Quick Start

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem (`gem install bundler`)

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/ValentinaPetrova/SitemapTest.git
   cd SitemapTest
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Build the site:
   ```bash
   bundle exec jekyll build
   ```
   
   The generated site will be in the `_site/` directory, including `sitemap.xml`.

4. Serve the site locally (optional):
   ```bash
   bundle exec jekyll serve
   ```
   
   Visit `http://localhost:4000/SitemapTest/` in your browser.

## 🗺️ Sitemap Generation

This repository uses the `jekyll-sitemap` plugin to automatically generate a sitemap. The sitemap includes:

- All pages (index, about, contact, blog)
- All blog posts in `_posts/`
- Metadata like last modification date and change frequency

### Accessing the Sitemap

After building the site:
- **Local build**: `_site/sitemap.xml`
- **GitHub Pages**: `https://valentinaapetrova.github.io/SitemapTest/sitemap.xml`

## 📝 Adding Content

### Adding a New Page

Create a new `.md` file in the root directory:

```markdown
---
layout: default
title: Your Page Title
permalink: /your-page/
---

# Your Page Title

Your content here...
```

### Adding a New Blog Post

Create a new file in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: default
title: "Your Post Title"
date: 2024-01-01 10:00:00 +0000
categories: category1 category2
---

# Your Post Title

Your content here...
```

## 🔧 Configuration

Edit `_config.yml` to customize:
- Site title and description
- Base URL (important for GitHub Pages)
- Plugins and theme
- Permalink structure

## 🌐 Deploying to GitHub Pages

1. Go to your repository settings on GitHub
2. Navigate to "Pages" section
3. Set source to "Deploy from a branch"
4. Select the branch (e.g., `main`) and folder (`/root` or `/docs`)
5. Save and wait for deployment

Your site will be available at: `https://valentinaapetrova.github.io/SitemapTest/`

## 🔍 Testing with Nuclia

Once deployed, you can test the sitemap with Nuclia:

1. Get your sitemap URL: `https://valentinaapetrova.github.io/SitemapTest/sitemap.xml`
2. Configure Nuclia to use this sitemap URL
3. Nuclia will automatically discover and index all pages listed in the sitemap

## 📦 Included Files

### Configuration Files
- **_config.yml**: Main Jekyll configuration
- **Gemfile**: Ruby gem dependencies
- **.gitignore**: Files to exclude from Git

### Content Files
- **index.md**: Homepage
- **about.md**: About page
- **contact.md**: Contact page
- **blog.md**: Blog listing page
- **_posts/**: Directory with sample blog posts

### Layout Files
- **_layouts/default.html**: Default HTML layout with navigation and styling

## 🛠️ Built With

- [Jekyll](https://jekyllrb.com/) - Static site generator
- [jekyll-sitemap](https://github.com/jekyll/jekyll-sitemap) - Sitemap plugin
- [Minima](https://github.com/jekyll/minima) - Default theme

## 📄 License

This is a test repository for demonstration purposes.

## 🤝 Contributing

Feel free to submit issues or pull requests to improve this test repository!

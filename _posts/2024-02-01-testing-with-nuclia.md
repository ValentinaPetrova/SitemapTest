---
layout: default
title: "Testing with Nuclia"
date: 2024-02-01 09:00:00 +0000
categories: testing nuclia
---

# Testing with Nuclia

This post explores how to test your Jekyll site with Nuclia using the generated sitemap.

## What is Nuclia?

Nuclia is a powerful search and AI platform that can index and search your content. It can use your sitemap to discover and index all your pages automatically.

## Using Sitemaps with Nuclia

To test your Jekyll site with Nuclia:

1. **Build your site**: Run `bundle exec jekyll build`
2. **Locate the sitemap**: Find `sitemap.xml` in your `_site` directory
3. **Deploy your site**: Push to GitHub Pages or another host
4. **Configure Nuclia**: Point Nuclia to your sitemap URL

## Benefits of Integration

Integrating Jekyll with Nuclia provides:
- **Automatic indexing**: Nuclia discovers all your content via the sitemap
- **Semantic search**: Advanced AI-powered search capabilities
- **Easy updates**: When you publish new content, just rebuild and redeploy

## Example Sitemap URL

Once deployed, your sitemap will be available at:
```
https://valentinaapetrova.github.io/SitemapTest/sitemap.xml
```

Nuclia can then crawl and index all the URLs listed in this sitemap!

# AGENTS.md - Chasing Cloud Careers Blog Repository Guide

## Overview

This is the blog content repository for [Chasing Cloud Careers](https://chasingcloudcareersllc.github.io). Posts are written in Markdown with YAML frontmatter and consumed by the main website at build time.

## Relationship to Website

- Cloned into `content/blog/` of `chasingcloudcareersllc.github.io` during build
- The website's `lib/blog.ts` parses frontmatter and converts markdown to HTML via a unified/remark/rehype pipeline

## Structure

```
posts/
  2026-02-07-welcome-to-chasing-cloud-careers.md
```

All blog posts live in the `posts/` directory.

## Frontmatter Schema

```yaml
---
title: "Your Post Title"
date: "YYYY-MM-DD"
author: "Author Name"
excerpt: "A brief description of the post for previews and SEO."
tags: [tag1, tag2, tag3]
draft: false
---
```

- **title** (string, required): Post display title
- **date** (string, required): Publication date in `YYYY-MM-DD` format
- **author** (string, required): Author name
- **excerpt** (string, required): Short summary for cards and SEO
- **tags** (string[], required): Array of lowercase tag strings
- **draft** (boolean, required): Set `true` to hide from production builds

## File Naming

Pattern: `YYYY-MM-DD-slug-title.md`

- Date prefix is required (ISO 8601)
- Slug portion becomes the URL path: `2026-02-07-welcome-to-chasing-cloud-careers.md` → `/blog/welcome-to-chasing-cloud-careers/`
- Use kebab-case for the slug

## Content Conventions

- Standard markdown: headings, lists, links, bold/italic
- Code blocks with language hints are supported
- Mermaid diagrams are supported (rendered to SVG at build time)
- GFM tables are supported

## Adding a New Post

1. Create a file in `posts/` following the naming pattern: `YYYY-MM-DD-slug-title.md`
2. Add all required frontmatter fields
3. Write post content in markdown below the frontmatter
4. Push to `main`

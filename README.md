# Chasing Cloud Careers Blog

Blog content for [Chasing Cloud Careers](https://chasingcloudcareersllc.github.io). Posts are written in Markdown with YAML frontmatter and fetched at build time by the main website repository.

## Adding a New Post

Create a new `.md` file in `posts/` with the naming convention:

```
YYYY-MM-DD-slug-title.md
```

### Required Frontmatter

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

Set `draft: true` to hide a post from production builds.

## Structure

```
posts/
  2026-02-07-welcome-to-chasing-cloud-careers.md
```

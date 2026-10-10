---
title: Hello, world
description: Why I started this site and what I plan to write about.
date: 2026-10-10
tags: [meta]
---

This is my first post. I'm going to write here about software, the projects I'm building, and things I learn along the way.

## How this site works

Every post is a Markdown file in `src/content/blog/`. To publish, I commit and push:

```bash
git add . && git commit -m "new post" && git push
```

Cloudflare Pages rebuilds the site and it goes live in about a minute.

> Set `draft: true` in a post's frontmatter to keep it out of production while still previewing it locally.

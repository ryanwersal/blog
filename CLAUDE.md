# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Blog Overview

This is a personal blog built with Hugo (v0.146.7+extended) using the Paper theme. The blog focuses on AI, technology, and learning.

## Development Commands

### Hugo Server

Start the local development server:
```bash
hugo server -D
```

This will:
- Build the site
- Watch for changes
- Enable live reloading
- Make the site available at http://localhost:1313/
- The `-D` flag includes draft posts

### Creating New Content

Create a new blog post:
```bash
hugo new content/posts/title.md
```

Replace title with a lowercase hyphenated version of your post title.

For current date in the correct format:
```bash
date -u +"%Y-%m-%dT%H:%M:%SZ"
```

### Building for Production

Build the site for production:
```bash
hugo --minify
```

This generates static files in the `public` directory.

## Blog Post Structure

Each blog post should:
1. Include frontmatter with:
   - title (start with a suitable emoji)
   - date
   - tags (2-5 relevant tags)
   - categories (optional)
2. Follow content guidelines:
   - Be concise and focused
   - Include relevant images if appropriate (stored in /static/images/)

## Deployment

The site is configured for deployment on Netlify:
- Production builds use Hugo v0.146.7
- Git information is enabled for production builds
- Automatic deployment happens via the configured commands in netlify.toml

## Cursor Rules

The repository includes a Cursor rule for creating new blog posts, which specifies:
- Using the Hugo CLI to create new posts
- Proper date formatting using UTC
- Using lowercase hyphenated titles in filenames
- Starting titles with a suitable emoji
- Including 2-5 relevant tags
- Only providing 2-4 bullet points about the topic (not writing the full post)
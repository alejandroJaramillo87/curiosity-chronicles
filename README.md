# curiosity-chronicles

Static blog built with Hugo. Generates HTML from Markdown content.

## Prerequisites

- hugo (>= 0.148)
- node (>= 20)
- npm

## Quick Start

```bash
npm install
npm run dev          # serves at http://localhost:1313
```

## Structure

```
├── config/          # hugo configuration
├── content/         # markdown source files
│   ├── posts/       # blog articles
│   └── *.md         # pages
├── static/          # static assets
├── themes/          # hugo theme
├── scripts/         # build automation
└── public/          # generated output (ignored)
```

## Commands

```bash
npm run dev          # development server
npm run build        # production build
npm run test         # test build with metrics
npm run format       # format source files
```

## Configuration

- `config/_default/hugo.toml` - site settings
- `config/_default/params.toml` - theme parameters  
- `hugo.toml` - style variables and plugins

## Content

Add posts to `content/posts/`. Use front matter:

```yaml
---
title: "Post Title"
date: 2024-01-01
categories: ["computer"]
---
```

Organize in subdirectories: `computer/`, `internet/`, `website/`.

## Build Process

markdown → hugo → html → `public/`

Generated files excluded from version control via `.gitignore`.

## Development

Theme structure can be toggled:
- `npm run project-setup` - move theme files to root
- `npm run theme-setup` - move files back to theme

Site rebuilds automatically during development.
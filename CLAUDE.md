# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo-based static site called "Curiosity Chronicles" using the "The Article" theme. It's a blog/article website with posts organized in categories (computer, internet, website).

## Development Commands

### Core Hugo Commands
- `npm run dev` - Start Hugo development server
- `npm run build` - Build site for production with minification and optimizations
- `npm run test` - Test production build with metrics and analytics

### Code Formatting
- `npm run format` - Format code using Prettier (supports Go templates)

### Project Setup Commands
- `npm run project-setup` - Convert theme structure to project structure (moves layouts/assets/static from theme to root)
- `npm run theme-setup` - Convert project structure back to theme structure (opposite of project-setup)

## Architecture

### Hugo Configuration
- Main config: `config/_default/hugo.toml` (site settings, theme, permalinks)
- Parameters: `config/_default/params.toml` (site metadata, widgets, search settings)
- Menu: `config/_default/menu.toml`
- Root `hugo.toml` contains style variables and plugin configurations

### Content Structure
- `content/posts/` - Main blog posts with category subdirectories
- `content/about.md` - About page
- `content/search.md` - Search functionality page
- Posts use Hugo front matter for metadata

### Theme Structure
- Theme: "the-article-hugo" (configured in hugo.toml)
- Uses Bootstrap, jQuery, and custom search functionality
- Supports Google Analytics and Disqus comments

### Key Features
- Search functionality with Fuse.js
- Responsive design with Bootstrap
- Categories: computer, internet, website
- SEO optimized with meta descriptions and Open Graph

### Setup Scripts
- `scripts/projectSetup.js` - Reorganizes theme files for development
- `scripts/themeSetup.js` - Reorganizes files back to theme structure
- These scripts move layouts/assets/static folders between theme and root directories

### Build Process
The build process includes:
- Template metrics and hints for performance monitoring  
- Draft, expired, and future content inclusion in builds
- Asset minification and garbage collection
- Force sync static files
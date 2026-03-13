# AGENTS.md - Agent Coding Guidelines

This document provides guidelines for agentic coding agents operating in this repository.

## Project Overview

This is a simple **static HTML website** - a personal portfolio for an interior designer. It uses the "Paradigm Shift" HTML5 UP template. There is no build system, no package manager, and no test suite.

## Build / Development Commands

Since this is a static site with no build tools:

- **Preview locally**: Open `index.html` directly in a browser, or use a simple HTTP server:
  ```bash
  npx serve .
  # or
  python3 -m http.server 8000
  ```

- **Deploy**: Changes pushed to the `main` branch automatically deploy to GitHub Pages via the workflow in `.github/workflows/static.yml`. No manual deployment steps needed.

- **No linting/formatting**: This project has no linting or code formatting tools configured.

## Code Style Guidelines

### General Principles

- Keep changes minimal and focused. This is a static site - avoid adding complexity.
- Maintain existing indentation and formatting style.
- All HTML files use **2 spaces** for indentation.

### HTML

- Use lowercase tags and attributes.
- Use double quotes for attribute values.
- Keep self-closing tags (e.g., `<meta />`) consistent with existing style.
- Include proper `alt` attributes on images.
- Use semantic HTML5 elements (`<section>`, `<header>`, `<footer>`, etc.).

### CSS

- CSS files are located in `assets/css/`.
- Main stylesheet: `assets/css/main.css`.
- If adding new styles, follow the existing CSS structure and naming conventions.
- Use existing CSS classes rather than creating new ones when possible.

### JavaScript

- JavaScript files are in `assets/js/`.
- The site uses jQuery and its plugins (loaded from `assets/js/`).
- Main application logic: `assets/js/main.js`.
- Avoid adding new JavaScript unless necessary for functionality.

### Images

- Place images in the `images/` directory.
- Full-size images go in `images/gallery/fulls/`, thumbnails in `images/gallery/thumbs/`.
- Optimize images before adding (compress JPEGs, use appropriate formats).

### File Organization

```
/
├── index.html          # Main page
├── assets/
│   ├── css/           # Stylesheets
│   ├── js/            # JavaScript files
│   ├── sass/          # SASS source files
│   └── webfonts/      # Font files
├── images/            # Site images
├── .github/
│   └── workflows/     # CI/CD (GitHub Pages deployment)
└── README.md
```

## Working with This Project

### Making Changes

1. Edit `index.html` for content changes
2. Edit files in `assets/` for style/behavior changes
3. Add images to the `images/` directory
4. Commit and push to trigger deployment

### What NOT To Do

- Do NOT add build tools (Webpack, Vite, etc.) - this is a simple static site
- Do NOT add test frameworks - there are no tests for static HTML
- Do NOT add linting tools - not needed for this project
- Do NOT restructure the project significantly
- Do NOT add complex JavaScript frameworks

### Validating Changes

Since there are no automated tests, validate changes manually:

1. Open `index.html` in a browser
2. Check that all images load correctly
3. Verify links work
4. Test responsive behavior on different screen sizes
5. Verify form elements work (if applicable)

### GitHub Pages Deployment

The site deploys automatically via GitHub Actions:

- Trigger: Push to `main` branch
- Workflow: `.github/workflows/static.yml`
- URL: Configured in GitHub repository settings

## Contact

This is a personal portfolio site. For questions about content or design, contact the site owner.

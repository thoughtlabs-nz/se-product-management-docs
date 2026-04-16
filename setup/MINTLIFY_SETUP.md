# Mintlify Documentation Setup

This directory is configured to use [Mintlify](https://mintlify.com) for beautiful, searchable documentation. Mintlify provides an AI-native documentation platform with interactive features and beautiful defaults.

## Prerequisites

- Node.js v20.17.0 or higher (LTS recommended)
- npm, pnpm, or yarn

## Installation

Install the Mintlify CLI globally:

```bash
npm i -g mint
```

Or with pnpm:

```bash
pnpm add -g mint
```

## Running Locally

To start the local documentation server:

```bash
cd product-management
mint dev
```

The documentation will be available at: **http://localhost:3000**

## Configuration

The documentation is configured via `docs.json` with the following structure:

### Navigation Structure

1. **Getting Started**
   - README (Overview)
   - Framework Summary (Comprehensive overview)

2. **Frameworks**
   - Prioritization Framework (RICE scoring)
   - Product Development Lifecycle
   - Product Discovery Framework (JTBD, user research)
   - Metrics & Success Framework

3. **Processes**
   - Quarterly Roadmap Planning
   - Monthly Customer Research
   - Weekly Product Review

4. **Templates**
   - Customer Interview Guide
   - PRD Template
   - User Story Template
   - Roadmap Template

## File Structure

All documentation files use Markdown with YAML frontmatter:

```markdown
---
title: Page Title
description: Brief description for SEO and navigation
---

# Page Content

Your markdown content here...
```

## Adding New Documentation

1. Create a new `.md` file in the appropriate directory
2. Add frontmatter with `title` and `description`
3. Update `docs.json` to include the file in navigation
4. The file path in `docs.json` is relative to the `product-management` directory (without `.md` extension)

Example:

```json
{
  "group": "Frameworks",
  "pages": [
    "frameworks/new-framework"
  ]
}
```

## Deploying

To deploy this documentation:

1. **Mintlify Cloud** (Recommended):
   - Sign up at [mintlify.com](https://mintlify.com)
   - Connect your repository
   - Automatic deployment on git push

2. **Self-hosted**:
   - Build locally and deploy to any static hosting service
   - Supports Vercel, Netlify, GitHub Pages, etc.

## Features Available

- ✅ Full-text search powered by FlexSearch
- ✅ Built-in analytics
- ✅ Dark mode support
- ✅ Mobile responsive
- ✅ Markdown components (tabs, alerts, buttons)
- ✅ Interactive navigation with groups and sections
- ✅ SEO optimized

## Resources

- [Mintlify Documentation](https://mintlify.com/docs)
- [Mintlify GitHub](https://github.com/mintlify)
- [Quickstart Guide](https://mintlify.com/docs/quickstart)

## Support

For questions about this Product Framework documentation, contact the Chief Product Officer.

For Mintlify technical issues, visit [Mintlify Support](https://mintlify.com/docs).

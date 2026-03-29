# Astro Blog Starter Template

A minimal, high-performance blog starter template built with [Astro](https://astro.build) and deployed on [Cloudflare Workers](https://workers.cloudflare.com).

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/cloudflare/templates/tree/main/astro-blog-starter-template)

![Astro Template Preview](https://github.com/withastro/astro/assets/2244813/ff10799f-a816-4703-b967-c78997e8323d)

## ✨ Features

- **⚡ High Performance** - 100/100 Lighthouse scores
- **🎨 Minimal Styling** - Easily customizable design
- **📱 SEO Optimized** - Canonical URLs and OpenGraph metadata
- **🗺️ Sitemap Support** - Automatic XML sitemap generation
- **📡 RSS Feed** - Built-in RSS feed generation
- **📝 Markdown & MDX** - Write content with Markdown or MDX
- **📊 Observability** - Built-in logging with Cloudflare Workers
- **🚀 Static Site Generation** - Deploy as a static website to Cloudflare Workers

## 🚀 Getting Started

### Quick Start with C3

Create a new project using the [C3](https://developers.cloudflare.com/pages/get-started/c3/) CLI:

```bash
npm create cloudflare@latest -- --template=cloudflare/templates/astro-blog-starter-template
```

### From GitHub

1. Clone this repository
2. Install dependencies: `npm install`
3. Start the dev server: `npm run dev`
4. Open [http://localhost:4321](http://localhost:4321)

### Live Demo

A live deployment of this template is available at: [https://astro-blog-starter-template.templates.workers.dev](https://astro-blog-starter-template.templates.workers.dev)

## 📁 Project Structure

```
src/
├── pages/              # Page routes (.astro files)
├── components/         # Reusable components
├── layouts/           # Page layouts
├── content/           # Blog content (Markdown/MDX files)
│   └── blog/         # Blog posts
├── styles/           # Global styles
├── consts.ts         # Site configuration constants
├── content.config.ts # Content collection schema
└── env.d.ts          # TypeScript types

public/               # Static assets (images, fonts, etc.)
dist/                 # Built output
```

### Key Directories

- **`src/pages/`** - Astro routes. Each `.astro` file becomes a route
- **`src/content/blog/`** - Blog posts in Markdown or MDX format
- **`src/components/`** - Reusable Astro components
- **`src/layouts/`** - Layout components for pages
- **`public/`** - Static assets served directly

## 🛠️ Available Commands

All commands are run from the project root:

| Command | Description |
|---------|-------------|
| `npm install` | Install dependencies |
| `npm run dev` | Start local dev server at `http://localhost:4321` |
| `npm run build` | Build your production site to `./dist/` |
| `npm run preview` | Preview the build locally before deploying |
| `npm run check` | Run type checking and validation |
| `npm run deploy` | Deploy to Cloudflare Workers |
| `npm wrangler tail` | View real-time logs from Workers |

## 📝 Creating Blog Posts

1. Create a new `.md` or `.mdx` file in `src/content/blog/`
2. Add frontmatter with required metadata:

```yaml
---
title: Your Post Title
description: A brief description of your post
pubDate: 2024-01-15
updatedDate: 2024-01-20 (optional)
heroImage: /path/to/image.jpg (optional)
---

Your content here...
```

## ⚙️ Configuration

### Site Configuration

Edit `src/consts.ts` to customize:
- `SITE_TITLE` - Your site's title
- `SITE_DESCRIPTION` - Your site's description

### Astro Configuration

The `astro.config.mjs` includes:
- **MDX Integration** - For enhanced Markdown with JSX components
- **Sitemap Generation** - Automatic XML sitemap
- **Cloudflare Adapter** - Optimized for Workers deployment

Update the `site` URL to match your domain for proper canonical URLs and sitemap generation.

### Deployment Configuration

The `wrangler.json` file configures:
- **Cloudflare Workers** settings
- **Static asset serving** from the `dist/` directory
- **Observability** logging
- **Source map uploads** for debugging

## 🚢 Deployment

### Deploy to Cloudflare Workers

```bash
npm run deploy
```

This will:
1. Build your Astro site
2. Deploy to Cloudflare Workers
3. Serve your site from Cloudflare's edge network

### Custom Domain

After deployment, configure a custom domain in your Cloudflare dashboard.

## 🔧 Development Tips

### Adding Components

Create reusable components in `src/components/` and import them in your pages:

```astro
---
import MyComponent from '../components/MyComponent.astro';
---

<MyComponent />
```

### Styling

The template includes minimal default styles. Customize by:
- Modifying CSS in `src/styles/`
- Adding Tailwind CSS or other CSS framework
- Using component-scoped styles in `.astro` files

### Content Collections

Blog posts are organized using Astro's Content Collections API. Schema validation ensures consistent frontmatter across all posts.

## 📚 Learn More

- [Astro Documentation](https://docs.astro.build)
- [Cloudflare Workers Documentation](https://developers.cloudflare.com/workers/)
- [MDX Documentation](https://mdxjs.com)
- [Community Discord](https://astro.build/chat)

## 🤝 Contributing

Found an issue? Have a suggestion? [Open an issue](https://github.com/cloudflare/templates/issues) on GitHub.

## 📄 License

This template is based on the excellent [Bear Blog](https://github.com/HermanMartinus/bearblog/). Check their repository for the original inspiration.

## ✨ Credits

- Template maintained by [Cloudflare Templates](https://github.com/cloudflare/templates)
- Built with [Astro](https://astro.build)
- Deployed on [Cloudflare Workers](https://workers.cloudflare.com)
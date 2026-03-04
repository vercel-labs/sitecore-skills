# Sitecore Skills

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-7-green.svg)](#available-skills)

Claude Code skills for building [Sitecore Marketplace](https://doc.sitecore.com/mp/en/developers/marketplace/introduction-to-sitecore-marketplace-for-custom-and-public-apps.html) apps. Covers the full lifecycle: scaffolding, SDK integration, Blok UI components, and deployment to Vercel.

Built for the Sitecore Marketplace SDK (v0.4) targeting Next.js App Router apps.

## Installation

Install skills using the [Skills CLI](https://skills.sh/docs/cli):

```bash
npx skills add vercel-labs/sitecore-skills
```

## Claude Code Plugin

You can also install skills as a [Claude Code plugin](https://code.claude.com/docs/en/discover-plugins):

First, add the marketplace:

```bash
/plugin marketplace add vercel-labs/sitecore-skills
```

Then, install the plugin:

```bash
/plugin install sitecore-skills@sitecore-marketplace
```

Once installed, skills are available as namespaced slash commands:

| Slash Command | Description |
|---|---|
| `/sitecore-skills:marketplace-scaffold` | Scaffold a new Marketplace app with the correct SDK packages |
| `/sitecore-skills:marketplace-sdk-reference` | Look up SDK queries, mutations, subscriptions, and types |
| `/sitecore-skills:marketplace-build-component` | Build UI with the Blok design system (Sitecore's shadcn theme) |
| `/sitecore-skills:marketplace-deploy` | Deploy with correct CSP headers and environment variables |
| `/sitecore-skills:marketplace-add-extension` | Add a route for a specific extension type (custom field, widget, etc.) |
| `/sitecore-skills:marketplace-add-xmc` | Integrate XM Cloud APIs — Sites, Pages, Authoring, Search, Agent |
| `/sitecore-skills:marketplace-add-ai` | Add Brand Review API for AI-powered content analysis |

## Available Skills

### marketplace-scaffold

Scaffold a new Sitecore Marketplace app. Asks about architecture (client-side vs full-stack), auth (built-in vs Auth0), and optional packages (XMC, AI), then runs the correct `npx shadcn@latest add` command with post-scaffold setup.

---

### marketplace-sdk-reference

Central reference for all Sitecore Marketplace SDK APIs. Covers queries, mutations, subscriptions, and TypeScript types across all 3 packages (client, xmc, ai) with code examples.

---

### marketplace-build-component

Build UI with the Blok design system — Sitecore's shadcn-based component library. Knows extension point UI constraints and integrates SDK data with loading/error states.

---

### marketplace-deploy

Deploy a Marketplace app to Vercel. Configures CSP headers for iframe embedding, sets environment variables, runs pre-deploy verification, and provides post-deploy portal configuration steps.

---

### marketplace-add-extension

Add a new extension point route to a Marketplace app. Supports custom-field, dashboard-widget, pages-context-panel, fullscreen, and standalone types with correct boilerplate per type.

---

### marketplace-add-xmc

Add XM Cloud API integration. Client-side via `client.query('xmc.*')` / `client.mutate('xmc.*')`, or server-side via `experimental_createXMCClient()`. Covers Sites, Pages, Authoring (GraphQL), Content Transfer, Search, and Agent APIs.

---

### marketplace-add-ai

Add AI Skills integration for the Brand Review API. Supports text, image (base64/URL), and document (PDF/text) inputs. Client-side via `client.mutate('ai.skills.generateBrandReview', ...)` or server-side via `experimental_createAIClient()`.

## SDK Packages

| Package | Purpose |
|---------|---------|
| `client` (required) | Core SDK client — queries, mutations, subscriptions |
| `xmc` (optional) | XM Cloud APIs — Sites, Pages, Authoring, Content Transfer, Search, Agent |
| `ai` (optional) | AI Skills — Brand Review API |

## Links

- [Sitecore Marketplace SDK Docs](https://doc.sitecore.com/mp/en/developers/sdk/latest/sitecore-marketplace-sdk/sitecore-marketplace-sdk-for-javascript.html)
- [Sitecore Developer Portal](https://developers.sitecore.com)

## License

MIT

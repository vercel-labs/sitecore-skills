# Architecture Decision Guide

## Client-Side vs Full-Stack

| Factor | Client-Side Only | Full-Stack (Auth0) |
|--------|------------------|--------------------|
| **Scaffold URL** | `quickstart.json` | `quickstart-with-custom-auth.json` |
| **Auth** | Built-in (automatic) | Auth0 (requires tenant) |
| **Server-side SDK** | No | Yes (`experimental_createXMCClient`, `experimental_createAIClient`) |
| **API Routes** | Not needed | Yes (Next.js API routes / Server Actions) |
| **External APIs** | Direct from client only | Can proxy through server |
| **Complexity** | Lower | Higher |
| **Use when** | Simple UI extensions, read-only data, client-side mutations | Need server-side processing, Auth0, external service integration |

## Package Selection

| Template | Registry URL | Provides |
|---------|-------------|----------|
| **Basic** (default) | `quickstart.json` | `ClientSDK.init()`, queries, mutations, subscriptions, types |
| **Custom Auth** | `quickstart-with-custom-auth.json` | Basic + Auth0 server-side SDK support |
| **Client-side XMC** | `quickstart-with-client-side-xmc.json` | Basic + Sites, Pages, Authoring, Content Transfer, Search, Agent APIs |
| **Full-stack XMC** | `quickstart-with-full-stack-xmc.json` | Custom Auth + XMC APIs |
| **Blok Theme** | `theme.json` | Sitecore-branded shadcn components (always install) |

All quickstart templates are at `https://blok.sitecore.com/r/marketplace/next/<template>.json`.
Blok theme and components are at `https://blok.sitecore.com/r/<name>.json`.

## What the Scaffold Creates

### Basic (`quickstart.json`)
- `lib/sitecore/client.ts` — Client initialization with `ClientSDK.init()`
- `lib/sitecore/providers.tsx` — React context providers (`<SitecoreProvider>`)
- `hooks/use-sitecore.ts` — React hooks for SDK access
- `app/layout.tsx` updates — Wraps app in providers

### Custom Auth (`quickstart-with-custom-auth.json`)
- Everything from basic, plus:
- `lib/sitecore/server.ts` — Server-side client factories
- `app/api/auth/[...auth0]/route.ts` — Auth0 route handlers
- `middleware.ts` — Auth0 middleware

### Client-side XMC (`quickstart-with-client-side-xmc.json`)
- Everything from basic, plus:
- XMC module registration and types for all XM Cloud APIs

### Full-stack XMC (`quickstart-with-full-stack-xmc.json`)
- Everything from custom auth, plus:
- XMC module registration and types for all XM Cloud APIs

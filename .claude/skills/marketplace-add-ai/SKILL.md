---
name: marketplace-add-ai
description: Adds AI Skills integration (Brand Review API) to a Sitecore Marketplace app. Use when the user wants to add AI-powered content analysis, brand review, or brand compliance checking.
---

# Add AI Skills Integration

You are helping the user add AI Skills integration to their Sitecore Marketplace app, specifically the Brand Review API.

## Prerequisites

The AI Skills package (`@sitecore-marketplace-sdk/ai`) must be installed:
```bash
npm install @sitecore-marketplace-sdk/ai
```

## Step 1: Determine Use Case

Common use cases for Brand Review:
- **Text review**: Check marketing copy against brand guidelines
- **Image review**: Verify visual assets comply with brand standards
- **Document review**: Analyze PDFs or documents for brand compliance
- **Content editor integration**: Add brand checking to content workflows

## Step 2: Choose Client-Side or Server-Side

- **Client-side**: Use `client.mutate("ai.skills.generateBrandReview", ...)` — simpler, works with built-in auth
- **Server-side**: Use `experimental_createAIClient()` — requires Auth0, good for background processing

## Step 3: Implement

See [ai-patterns.md](references/ai-patterns.md) for complete code patterns.

## Step 4: Suggest Related Skills

- Use `/marketplace-build-component` to build the review results UI
- Use `/marketplace-sdk-reference` for detailed type information

## Reference Files
- [AI Patterns](references/ai-patterns.md) — Brand Review API code patterns

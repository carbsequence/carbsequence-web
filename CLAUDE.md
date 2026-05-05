# CLAUDE.md

This repository is the **public CarbSequence website only**.

## Scope
Safe to edit:
- `index.html`
- `privacy.html`
- `terms.html`
- `delete-account/index.html`
- images and other static assets
- copy, layout, CTA text, sections, screenshots, branding

Sensitive file:
- `auth-action.html`
  - This powers production Firebase email flows.
  - Do **not** change its logic, routing assumptions, query param handling, or Firebase config unless explicitly asked.

Important routing file:
- `_redirects`
  - Keep `/auth/action   /auth-action.html   200`
  - Do not remove or casually edit this rule.

## Hard rules
- Do **not** add secrets, API keys, tokens, private credentials, or env files.
- Do **not** add backend code, Firebase Functions, admin dashboard code, or iOS code.
- Do **not** add unnecessary frameworks, build tools, package managers, or dependencies unless explicitly requested.
- Keep this repo static and simple.
- Preserve these public routes unless explicitly asked to change them:
  - `/`
  - `/privacy.html`
  - `/terms.html`
  - `/delete-account/`
  - `/auth/action`

## Workflow
- Prefer small, focused edits.
- Prefer editing existing files over introducing new architecture.
- If asked to change website copy/design, touch only the public website files.
- If asked to change email verification, password reset, or recovery flows, be extremely careful and explain the impact before editing.

## Deployment
- This repo is deployed by Cloudflare Pages.
- Treat `main` as production.
- Prefer PRs/branches over direct production edits when possible.

## If unsure
When a request might affect auth flows, app links, legal pages, or production routing, pause and explain the risk before making changes.

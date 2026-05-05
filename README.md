# carbsequence-web

Public CarbSequence marketing website and email action handler.

## Scope
This repo contains only the public website:
- marketing homepage
- privacy/terms pages
- delete-account page
- Firebase email action handler at `/auth/action`
- static assets

## Not in this repo
- iOS app
- Admin dashboard
- Firebase Functions/backend
- Firestore/Storage rules

## Hosting
Recommended host: Cloudflare Pages.

## Important route
The backend-generated Firebase email links expect:
- `/auth/action?mode=...&oobCode=...`

That route must continue serving `auth-action.html` with query params preserved.

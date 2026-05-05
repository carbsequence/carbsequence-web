# Contributing

This repo is the **public CarbSequence website**.

## What is safe to edit
- homepage copy and sections in `index.html`
- legal pages: `privacy.html`, `terms.html`
- delete account page: `delete-account/index.html`
- images and static assets
- app download CTA text or links

## Be careful with
- `auth-action.html`
  - this powers production email verification / password reset / recover email flows
- `_redirects`
  - this keeps `/auth/action` working

## Rules
- Do not add secrets, tokens, passwords, or credentials
- Do not add backend code or Firebase Functions here
- Do not add iOS code here
- Do not add frameworks or build tooling unless explicitly requested
- Keep changes small and focused

## Recommended workflow
1. Create a branch
2. Make your edits
3. Preview the site
4. Open a PR
5. Merge after review

## Production-sensitive routes
These should keep working unless there is an explicit reason to change them:
- `/`
- `/privacy.html`
- `/terms.html`
- `/delete-account/`
- `/auth/action`

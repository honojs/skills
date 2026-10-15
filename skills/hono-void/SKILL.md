---
name: hono-void
description: Use when checking or testing a Void app with Hono CLI — pages, page actions, and API routes. TRIGGER when package.json depends on 'void', the project has void.config.ts, or the user mentions Void. Void is a framework built on Hono.
---

# Hono Void Skill

[Void](https://void.cloud) builds a Hono app from file-based routes, so there is no entry file and the code does not import `hono`. Verify changes with [Hono CLI](https://github.com/honojs/cli), not with a browser, curl, or a dev server. It runs the app through Vite with no flag and no file argument:

```bash
npm install -D @hono/cli@next
npx hono --help
npx hono routes
npx hono request /
```

For a flow (create, then read), use one `npx hono batch -` call with `expect` per step. The `hono` skill has the details.

## Checking a Void app

- `pages/**` return HTML. Send the header `x-voidpages: true` to get the page data as JSON: `{ component, props, errors, head, ... }`.
- Page actions are POST/PUT/PATCH/DELETE to the page URL. A named action has a `?name` suffix, e.g. `POST /ramen/1?delete`.
- A validation failure in a page action returns 200, not 422, with the messages in `body.errors`. Assert on the body.
- A foreign `Origin` header gets 403. Omit `Origin` or use the app's own origin.
- `npx void db seed --yes` resets the local DB between runs.

For Void itself (routing, pages, the Void CLI), read Void's docs in `node_modules/void/docs/`.

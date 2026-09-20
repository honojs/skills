# Hono Skills

Agent Skills for developing applications with [Hono](https://hono.dev). Currently provides the `hono` and `hono-jsx` skills, with more skills for the Hono ecosystem planned.

## Installation

### Claude Code

```bash
# Add marketplace
/plugin marketplace add honojs/skills

# Install skill
/plugin install hono@hono
```

### skills.sh

```bash
npx skills add honojs/skills
```

## Skills

### hono

Build Hono web applications with inline API knowledge. Provides inline API reference and request testing via [Hono CLI](https://github.com/honojs/cli).

**Features:**

- Inline Hono API reference (routing, context, middleware, JSX, validation, RPC, streaming, helpers)
- Request testing via `hono request`

### hono-jsx

Build UI with `hono/jsx`: server-rendered pages with `jsxRenderer`, Vite with [vite-ssr-components](https://github.com/yusukebe/vite-ssr-components) on Cloudflare Workers, and client components with `hono/jsx/dom`. No React.

**Features:**

- Project layout matching the `create-hono` `cloudflare-workers+vite` template
- Layouts, per-page head content, forms, client components, styling, streaming
- `@hono/vite-dev-server` setup for other runtimes

## Requirements

- [Hono CLI](https://github.com/honojs/cli) - Install as devDependency (`npm install -D @hono/cli`)

## Author

Yusuke Wada <https://github.com/yusukebe>

## License

MIT

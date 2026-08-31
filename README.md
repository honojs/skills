# Hono Skills

Agent Skills for developing applications with [Hono](https://hono.dev). Currently provides the `hono` skill, with more skills for the Hono ecosystem planned.

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

## Requirements

- [Hono CLI](https://github.com/honojs/cli) - Install as devDependency (`npm install -D @hono/cli`)

## Author

Yusuke Wada <https://github.com/yusukebe>

## License

MIT

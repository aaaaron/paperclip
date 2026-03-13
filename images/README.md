# Sandbox Agent Images

Container images used by the sandbox adapter to run coding agents in isolated environments.

## Images

### `agent-sandbox`

Generic sandbox image for OpenSandbox and E2B providers. Based on `node:lts-trixie-slim` with Claude Code, Codex, and opencode pre-installed.

```bash
docker build -t agent-sandbox:local images/agent-sandbox/
docker run --rm agent-sandbox:local sh -c "claude --version && codex --version && opencode --version"
```

Published as `ghcr.io/paperclipai/agent-sandbox:latest`.

### `cloudflare-agent-sandbox`

Sandbox image for the Cloudflare provider. Based on `cloudflare/sandbox` with the same agent CLIs.

```bash
docker build -t cloudflare-agent-sandbox:local images/cloudflare-agent-sandbox/
```

Published as `ghcr.io/paperclipai/cloudflare-agent-sandbox:latest`.

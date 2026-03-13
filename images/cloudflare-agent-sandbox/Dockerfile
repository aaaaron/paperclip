FROM docker.io/cloudflare/sandbox:0.7.0

RUN npm install -g --omit=dev \
  @anthropic-ai/claude-code@latest \
  @openai/codex@latest \
  opencode-ai

WORKDIR /workspace

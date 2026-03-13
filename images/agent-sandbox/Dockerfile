FROM node:lts-trixie-slim

RUN apt-get update \
  && apt-get install -y --no-install-recommends ca-certificates curl git openssh-client \
  && rm -rf /var/lib/apt/lists/*

RUN npm install -g --omit=dev \
  @anthropic-ai/claude-code@latest \
  @openai/codex@latest \
  opencode-ai

RUN mkdir -p /workspace && chown node:node /workspace
WORKDIR /workspace
USER node

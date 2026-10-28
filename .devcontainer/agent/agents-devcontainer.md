# Devcontainer — node-soap

Running inside the node-soap devcontainer.

## Environment
- Base image: mcr.microsoft.com/devcontainers/base:ubuntu
- Language: Node.js (lts — no version pinned in the repo, this is a guess)
- Workspace: /workspace
- Running the app: see README.md § Running the app (library — no server; install + lint + test only)

## Credentials available (forwarded from host shell)
- ARTIFACTORY_EMAIL / ARTIFACTORY_TOKEN — Artifactory (npm)
- GOCODE_API_TOKEN / GOCODE_BASE_URL — AI coding agents (gocode LiteLLM proxy)

## Context files
| Topic | File |
|-------|------|
| Claude Code — credentials, denied ops, MCP wiring | [claude-code.md](claude-code.md) |
| Container safety — git mode, blocked hosts, MCPs | [devcontainer-commons.md](devcontainer-commons.md) |
| Artifactory registry config | [gd-artifactory.md](gd-artifactory.md) |
| Certs, Docker network, CA trust | [stunt-doubles-core.md](stunt-doubles-core.md) |

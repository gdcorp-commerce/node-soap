# Devcontainer — node-soap
Node.js (lts) base devcontainer — no stunt-doubles services wired (library, no server).

| | |
|---|---|
| Base image | mcr.microsoft.com/devcontainers/base:ubuntu |
| Start | `atlas-container start` or VS Code F1 → "Reopen in Container" |
| Shell | `atlas-container shell` |
| Host credentials | ARTIFACTORY_EMAIL, ARTIFACTORY_TOKEN, GIT_TOKEN, GOCODE_API_TOKEN, GOCODE_BASE_URL |
| stunt CLI | `stunt ps` · `stunt up <service>` · `stunt down <service>` (inside container) |

In-container context: `.devcontainer/agent/agents-devcontainer.md` (auto-loaded by Claude Code inside the container).

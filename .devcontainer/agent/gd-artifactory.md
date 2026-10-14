## gd-artifactory — GoDaddy Artifactory package manager configuration

Configures npm (and Yarn 1/Berry) to route dependency lookups through GoDaddy JFrog Artifactory at `gdartifactory1.jfrog.io`. Only `configureNpm` is enabled for this repo.

**Credentials** — sourced from the environment at tool runtime (never baked into the image):

| Env var | Purpose |
|---------|---------|
| `ARTIFACTORY_EMAIL` | Artifactory username / email |
| `ARTIFACTORY_TOKEN` | Artifactory identity token or API key |

These must be in `remoteEnv` in `devcontainer.json` so they are re-read from the host shell on every IDE reconnect.

**Configured package managers:**

| Manager | Registry URL | Config file |
|---------|-------------|-------------|
| npm / Yarn 1 | `https://gdartifactory1.jfrog.io/artifactory/api/npm/node-virt/` | `~/.npmrc` |
| Yarn Berry | same as npm | `~/.yarnrc.yml` |

**Check what is configured:**
```bash
cat /usr/local/share/gd-artifactory/post-create.sh
npm config get registry
```

**Verify connectivity** — requires `ARTIFACTORY_EMAIL` and `ARTIFACTORY_TOKEN` to be set:
```bash
npm install --dry-run
```

For scoped npm packages from a team-specific Artifactory repo, add to the project's `.npmrc`:
```ini
@my-scope:registry=https://gdartifactory1.jfrog.io/artifactory/api/npm/my-repo-local/
```

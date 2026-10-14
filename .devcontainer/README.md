# node-soap Devcontainer

Node.js (lts) base devcontainer — no stunt-doubles services, no app server.

## What is this?

A **devcontainer** is a pre-configured development environment that runs in Docker. Once set up, `atlas-container start` gives you a fully wired container with the project toolchain, AI coding agents, and all dependencies ready to go — no local language/runtime setup, no manual credential juggling.

📖 **Quick start guide:** [Code Atlas - Containers](https://godaddy-corp.atlassian.net/wiki/spaces/SELLMORE/pages/4447535626/Code+Atlas+-+Containers)

---

## Starting the container

**Option A — atlas-container CLI (recommended):**
```sh
atlas-container start          # start or attach (from repo root)
atlas-container shell          # open a bash shell in a running container
atlas-container stop           # stop the container (preserves state)
atlas-container rebuild        # rebuild the image from scratch
atlas-container rm             # remove the container (keeps cached images)
atlas-container rm --purge     # full cleanup including cached images
```

Install once: `npm install -g @code-atlas/atlas-container --registry=https://gdartifactory1.jfrog.io/artifactory/api/npm/node-virt/`

First-time setup: `atlas-container setup && atlas-container login`

**Option B — VS Code:**
`F1` → "Dev Containers: Reopen in Container"

**Option C — JetBrains Gateway:**
Gateway → Remote Development → Dev Containers → Open Dev Container

---

## Building and testing

`node-soap` is a library (minimal Node.js SOAP client/server) — there's no app to run, only build/test/lint commands:

```sh
npm install     # install dependencies
npm test        # runs jshint (pretest) then mocha over test/*-test.js and test/security/*.js
```

No app port is forwarded — this repo has no server component of its own; `lib/server.js` is a library helper used by the test suite, not a standalone process.

---

## stunt CLI (inside the container)

```sh
stunt ps                      # check service status
stunt up <service>            # start a service
stunt down <service>          # stop a service
stunt logs <service>          # tail logs
stunt cert add <service> <hostname>   # add a hostname to TLS cert
```

No stunt-doubles services are wired for this repo — `stunt-doubles-core` is included so you can `stunt up <service>` later if the local workflow ever needs to mock an external dependency.

---

## Regenerating

```sh
/gdc:scaffold-devcontainer
```

Then run `atlas-container rebuild` to pick up the updated `devcontainer.json`.

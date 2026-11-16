# unit-001 downloads

Public release downloads for unit-001, a durable agent. Current release: **0.0.9**.

## Download and install

Supported target: **Ubuntu Server 24.04 LTS, x86-64**. Releases include Node and application dependencies.

```bash
curl --fail --location --output unit-001-linux-x64.tar.gz \
  https://github.com/francman/unit-001-releases/releases/latest/download/unit-001-linux-x64.tar.gz
tar -xzf unit-001-linux-x64.tar.gz
cd unit-001-0.0.9-linux-x64
sudo ./install.sh
sudo agent setup
agent
```

The default name is `agent`. Use `sudo ./install.sh --name bob` to choose `bob`; subsequent commands use that name. Installation through sudo grants the installing account operator access. Start a fresh login before using it.

Full-screen setup provides visible provider search, subscription sign-in or masked API key entry, model selection and optional service startup. Run `agent` to open its workspace; `Ctrl+D` detaches while the service keeps running.

Version 0.0.8 adds a paired browser workspace (`agent web`), remote terminal profiles, introspection, creator-approved channel setup and bounded work. An enduring mission is the agent’s purpose; continuous purpose planning remains unfinished. Browser access stays on private loopback through SSH forwarding.

Version 0.0.9 adds recovery guidance for a rejected browser address. Open the printed `http://127.0.0.1:PORT` URL and forward the same port through SSH; `localhost` and mismatched ports remain rejected. Restart an existing `agent web` process after updating.

## Everyday commands

Authorized operators use `agent`, `agent status` and `agent memory stats|recall|remember|forget|sleep` without sudo. `/status` and `/memory` work inside the workspace. Forgetting asks for confirmation and retains conversation history. Session memory survives restarts.

Setup, credentials, configuration, permissions, updates and lifecycle commands still require sudo. Operators retain coding tools; operator access is not a tool sandbox. Private credentials and state files remain protected.

For an existing 0.0.6 installation, apply the signed update, then run the explicit one-time migration while idle:

```bash
sudo agent update apply
sudo agent stop --yes
sudo agent operator add YOUR_USERNAME
sudo agent start
```

Reconnect with a fresh login. Substitute your installed name for `agent`. Granting an operator on an installation with the new service policy needs no restart. Removing membership does not revoke already-running sessions immediately.

No GitHub account, download token, signing key, npm installation or manual update configuration is required. Bundles include public verification keys and configure update checks. Use `sudo agent update disable` to turn automatic checks off.

Maintainer status: signed releases are available; unattended publication and metadata renewal still need a dedicated publishing credential. Verification fails closed when metadata expires, leaving an installed agent running.

This repository contains release assets and public update metadata. Downloads include runnable JavaScript and source maps. Private source access and Git history are not published here.

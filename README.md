# unit-001 downloads

Public release downloads for unit-001, a durable coding agent. Current release: **0.0.5**.

## Download and install

Supported target: **Ubuntu Server 24.04 LTS, x86-64**. Releases include Node and application dependencies.

```bash
curl --fail --location --output unit-001-linux-x64.tar.gz \
  https://github.com/francman/unit-001-releases/releases/latest/download/unit-001-linux-x64.tar.gz
tar -xzf unit-001-linux-x64.tar.gz
cd unit-001-0.0.5-linux-x64
sudo ./install.sh
sudo agent setup
sudo agent
```

Full-screen setup guides provider selection with visible search, subscription sign-in or masked API key entry, model selection and optional service startup. Then run `sudo agent` to open the running agent workspace; `Ctrl+D` detaches without stopping it. Use `sudo ./install.sh --name bob` to name the installed agent; subsequent commands become `sudo bob ...`.

No GitHub account, download token, signing key, npm installation, or manual update configuration is required. Bundles include public verification keys and configure update checks. Use `sudo agent update disable` to turn automatic update checks off.

Maintainer status: the initial signed release is available; unattended publication and metadata renewal still need a dedicated publishing credential. Verification fails closed when metadata expires, leaving an installed agent running.

This repository contains release assets and public update metadata. The downloadable program includes runnable JavaScript and source maps. Private source repository access and Git history are not published here.

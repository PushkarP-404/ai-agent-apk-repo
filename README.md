# AI-Agent OS - Official APK Package Repository

This repository hosts official packages for **AI-Agent OS** (an autonomous Alpine-derived Linux distribution).

## Available Packages

| Package | Version | Description |
| --- | --- | --- |
| `ai-agent-daemon` | `0.1.0-r0` | Kernel-userspace agent daemon, task engine, and `agent-cli` |
| `llama-server-musl` | `0.1.0-r0` | Native musl HTTP inference server with bundled runtime libraries |
| `ai-agent-model-lora` | `0.1.0-r0` | Fine-tuned distilled LoRA adapter GGUF (`os_agent_lora.gguf`) |
| `ai-agent-kernel-modules` | `0.1.0-r0` | Out-of-tree kernel module (`ai_process_hook.ko`) for `6.6.142-ai-agent` |

---

## Installation Instructions (for any Alpine Linux system)

### 1. Trust the Public Signing Key

```sh
wget -P /etc/apk/keys/ https://PushkarP-404.github.io/ai-agent-apk-repo/keys/packager-6acb642e.rsa.pub
```

### 2. Add the Repository

```sh
echo "https://PushkarP-404.github.io/ai-agent-apk-repo" >> /etc/apk/repositories
```

### 3. Update & Install Packages

```sh
apk update
apk add ai-agent-daemon llama-server-musl ai-agent-model-lora ai-agent-kernel-modules
```

---
*Built with Alpine `abuild` and cryptographically signed.*

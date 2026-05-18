# sideband-setup

Practical setup and field notes for Sideband, the Reticulum/LXMF client for Linux, Raspberry Pi, Android, macOS and Windows.

---

## what this is

A focused, practical reference for installing and running Sideband in real conditions — headless Raspberry Pi, low-power Linux nodes, off-grid setups. Not a clone of the upstream docs. Field notes, working configs, and things that needed to be figured out.

---

## why Sideband

Sideband is the reference LXMF client. It handles messages, real-time voice, attachments, private telemetry and a plugin system — all encrypted, all running over Reticulum without accounts, servers or central infrastructure.

It runs on Android, Linux, macOS and Windows. This repo focuses on Linux and Raspberry Pi first, where the documentation tends to be thinner and the setup less obvious.

---

## initial scope

- Install on Linux (Debian/Ubuntu/Pi OS)
- Install on Raspberry Pi (headless, low-power)
- Connect to a Reticulum transport node
- Basic operation and identity management
- Advanced: telemetry, plugins, voice

---

## contents

```
docs/en/
  install-linux.md       — install on Debian/Ubuntu/Pi OS
  install-rpi.md         — headless Raspberry Pi setup
  connectivity.md        — connect to nodes, LoRa, TCP
  advanced.md            — plugins, telemetry, voice

docs/pt/
  instalacao-linux.md    — instalação em Debian/Ubuntu/Pi OS
  instalacao-rpi.md      — Raspberry Pi headless
  conectividade.md       — ligar a nós, LoRa, TCP
  avancado.md            — plugins, telemetria, voz

configs/
  rns-sideband-template.conf   — Reticulum config template
```

---

## relationship to other projects

| repo | focus |
|---|---|
| [rawmesh-node](https://github.com/noduscypher/rawmesh-node) | transport node — always-on Reticulum backbone |
| [meshchatx-setup](https://github.com/noduscypher/meshchatx-setup) | MeshChatX client setup |
| [columba-manual](https://github.com/noduscypher/columba-manual) | Columba messenger — Android |
| **sideband-setup** | **Sideband — Linux, Raspberry Pi, desktop** |

Sideband and MeshChatX run on the same Reticulum layer and interoperate. This repo focuses on Sideband specifically because its feature set — voice, plugins, telemetry — warrants its own documentation.

---

## contributing

Field notes, corrections and translations are welcome. Keep it practical and low-noise. Open an issue or send a patch.

---

## ☥ Value for Value

If this helped you get Sideband running, return value in whatever form makes sense.

The goal is to keep small, low-power nodes online and evolving quietly — not to optimise for attention or growth.

⚡ Lightning: `trustyflame02@zeuspay.com`

No sats? Carry the signal further: share it, mirror it, translate it, remix it.

---

## ☥ licence

CC BY-SA 4.0 — [creativecommons.org/licenses/by-sa/4.0](https://creativecommons.org/licenses/by-sa/4.0/)

cypherpunks write code /// nature writes resilience /// we bridge both.

*☥ walk quietly, ₿ut keep the signal alive.*

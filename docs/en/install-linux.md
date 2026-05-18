# install sideband — linux

Debian, Ubuntu, Raspberry Pi OS and compatible distributions.

---

## requirements

- Python 3.7+
- pip
- Reticulum already installed and configured

---

## install

```bash
pip install sideband
```

Or install from source:

```bash
git clone https://github.com/markqvist/Sideband
cd Sideband
pip install .
```

---

## run

```bash
sideband
```

First launch generates a cryptographic identity on the device. No account, no registration. The identity lives in `~/.sideband/`.

---

## run headless (no GUI)

For servers and Raspberry Pi without a display:

```bash
sideband --daemon
```

Runs as a background service. Messages are handled via LXMF, accessible from other clients on the same node or network.

---

## identity backup

```bash
cp ~/.sideband/identity ~/.sideband/identity.bak
```

Store the backup somewhere safe. Losing the identity file means losing access to that address permanently.

---

## next

→ [connectivity.md](connectivity.md) — connect to nodes and interfaces

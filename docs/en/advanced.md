# advanced — sideband

Voice, plugins, telemetry and field notes.

---

## voice calls

Real-time encrypted voice requires a low-latency link — Bluetooth, WiFi or TCP. LoRa is too slow for voice.

Both ends need Sideband running and a route between them. Initiate a call from the contacts screen.

---

## plugins

Sideband supports a plugin system for extending functionality. Plugins live in `~/.sideband/plugins/`.

Community plugins are listed in the upstream repository:
[github.com/markqvist/Sideband](https://github.com/markqvist/Sideband)

---

## private telemetry

Sideband can share telemetry (location, sensor data) privately over LXMF — end-to-end encrypted, no third-party servers.

Enable in Settings → Telemetry. Data is only shared with contacts you explicitly authorise.

---

## lxmf addresses

Your Sideband LXMF address is derived from your identity. Share it as a QR code or copy it from Settings → Identity.

Others can message you directly at that address from any LXMF-compatible client (Sideband, Columba, MeshChatX).

---

## field notes

- On Raspberry Pi, disable the GUI to save RAM: run `--daemon` mode.
- If messages are slow, check that your transport node is reachable with `rnstatus`.
- LoRa delivery can take minutes on a sparse mesh — this is normal, not a failure.
- Back up `~/.sideband/identity` and `~/.reticulum/identity` separately.

# connectivity — sideband

How to connect Sideband to the Reticulum network.

---

## reticulum config location

```
~/.reticulum/config
```

Sideband uses the system Reticulum instance. Configure interfaces there.

---

## TCP — connect to a transport node

Add to `~/.reticulum/config`:

```
[[RawMesh TCP]]
  type = TCPClientInterface
  enabled = yes
  target_host = 192.168.1.100
  target_port = 4242
```

Replace host/port with your node's address.

Public nodes to connect to over the internet:
- `rns.michmesh.net:7822`
- `network.reticulum.pt:4242`

---

## local mesh — bluetooth / wifi

Enable in Sideband interface settings. No configuration file needed for BLE or local WiFi discovery.

---

## lora — rnode

Connect an RNode (LilyGO T-Beam, Heltec LoRa32) via USB or Bluetooth. Add to Reticulum config:

```
[[RNode LoRa]]
  type = RNodeInterface
  enabled = yes
  port = /dev/ttyUSB0
  frequency = 868000000
  bandwidth = 125000
  txpower = 14
  spreadingfactor = 7
  codingrate = 5
```

EU band: 868 MHz. Match frequency, bandwidth and spreading factor with your local group.

---

## verify connection

```bash
rnstatus
```

Shows active interfaces, connected clients and traffic.

---

## next

→ [advanced.md](advanced.md) — plugins, telemetry, voice

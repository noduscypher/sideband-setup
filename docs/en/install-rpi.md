# install sideband — raspberry pi

Headless setup on Raspberry Pi 4 running Raspberry Pi OS Lite or Debian.

---

## requirements

- Raspberry Pi 3B+ or 4 (tested on RPi4)
- Raspberry Pi OS Lite (64-bit recommended)
- Python 3.9+
- SSH access

---

## install dependencies

```bash
sudo apt update && sudo apt install -y python3-pip python3-venv git
```

---

## install sideband in a virtual environment

```bash
python3 -m venv ~/.venv/sideband
source ~/.venv/sideband/bin/activate
pip install sideband
```

---

## run as a service

Create a systemd service to start Sideband on boot:

```bash
sudo nano /etc/systemd/system/sideband.service
```

```ini
[Unit]
Description=Sideband LXMF client
After=network.target

[Service]
User=pi
ExecStart=/home/pi/.venv/sideband/bin/sideband --daemon
Restart=on-failure
RestartSec=5

[Install]
WantedBy=multi-user.target
```

Enable and start:

```bash
sudo systemctl enable sideband
sudo systemctl start sideband
sudo systemctl status sideband
```

---

## notes

- Replace `pi` with your actual username if different.
- Sideband daemon on Pi consumes very little CPU when idle.
- Identity is stored in `~/.sideband/` — back it up.

---

## next

→ [connectivity.md](connectivity.md) — connect to nodes and interfaces

# instalar sideband — raspberry pi

Configuração headless no Raspberry Pi 4 com Raspberry Pi OS Lite ou Debian.

---

## requisitos

- Raspberry Pi 3B+ ou 4 (testado em RPi4)
- Raspberry Pi OS Lite (64-bit recomendado)
- Python 3.9+
- Acesso SSH

---

## instalar dependências

```bash
sudo apt update && sudo apt install -y python3-pip python3-venv git
```

---

## instalar sideband num ambiente virtual

```bash
python3 -m venv ~/.venv/sideband
source ~/.venv/sideband/bin/activate
pip install sideband
```

---

## correr como serviço

Criar um serviço systemd para iniciar o Sideband no arranque:

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

Activar e iniciar:

```bash
sudo systemctl enable sideband
sudo systemctl start sideband
sudo systemctl status sideband
```

---

## notas

- Substitui `pi` pelo teu utilizador real se for diferente.
- O daemon do Sideband no Pi consome muito pouco CPU em idle.
- A identidade fica em `~/.sideband/` — faz uma cópia de segurança.

---

## a seguir

→ [conectividade.md](conectividade.md) — ligar a nós e interfaces

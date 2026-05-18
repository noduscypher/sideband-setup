# conectividade — sideband

Como ligar o Sideband à rede Reticulum.

---

## localização da configuração Reticulum

```
~/.reticulum/config
```

O Sideband usa a instância Reticulum do sistema. Configura as interfaces nesse ficheiro.

---

## TCP — ligar a um nó de transporte

Adiciona a `~/.reticulum/config`:

```
[[RawMesh TCP]]
  type = TCPClientInterface
  enabled = yes
  target_host = 192.168.0.170
  target_port = 4242
```

Substitui host/porta pelo endereço do teu nó.

Nós públicos para ligar pela internet:
- `rns.michmesh.net:7822`
- `network.reticulum.pt:4242`

---

## mesh local — bluetooth / wifi

Activa nas definições de interface do Sideband. Não é necessária configuração no ficheiro para BLE ou descoberta WiFi local.

---

## lora — rnode

Liga um RNode (LilyGO T-Beam, Heltec LoRa32) via USB ou Bluetooth. Adiciona à configuração Reticulum:

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

Banda EU: 868 MHz. Iguala frequência, largura de banda e spreading factor com o teu grupo local.

---

## verificar ligação

```bash
rnstatus
```

Mostra interfaces activas, clientes ligados e tráfego.

---

## a seguir

→ [avancado.md](avancado.md) — plugins, telemetria, voz

# avançado — sideband

Voz, plugins, telemetria e notas de campo.

---

## chamadas de voz

A voz encriptada em tempo real requer uma ligação de baixa latência — Bluetooth, WiFi ou TCP. O LoRa é demasiado lento para voz.

Ambos os lados precisam do Sideband a correr e de uma rota entre eles. Inicia uma chamada a partir do ecrã de contactos.

---

## plugins

O Sideband suporta um sistema de plugins para estender funcionalidades. Os plugins ficam em `~/.sideband/plugins/`.

Plugins da comunidade estão listados no repositório oficial:
[github.com/markqvist/Sideband](https://github.com/markqvist/Sideband)

---

## telemetria privada

O Sideband pode partilhar telemetria (localização, dados de sensores) de forma privada via LXMF — encriptado ponta-a-ponta, sem servidores de terceiros.

Activa em Definições → Telemetria. Os dados só são partilhados com os contactos que autorizares explicitamente.

---

## endereços LXMF

O teu endereço LXMF do Sideband é derivado da tua identidade. Partilha-o como código QR ou copia-o em Definições → Identidade.

Outros podem enviar-te mensagens directamente para esse endereço a partir de qualquer cliente compatível com LXMF (Sideband, Columba, MeshChatX).

---

## notas de campo

- No Raspberry Pi, desactiva a GUI para poupar RAM: usa o modo `--daemon`.
- Se as mensagens estiverem lentas, verifica que o teu nó de transporte está acessível com `rnstatus`.
- A entrega via LoRa pode demorar minutos numa mesh esparsa — é normal, não é falha.
- Faz cópia de segurança de `~/.sideband/identity` e `~/.reticulum/identity` separadamente.

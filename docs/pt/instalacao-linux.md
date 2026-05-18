# instalar sideband — linux

Debian, Ubuntu, Raspberry Pi OS e distribuições compatíveis.

---

## requisitos

- Python 3.7+
- pip
- Reticulum já instalado e configurado

---

## instalar

```bash
pip install sideband
```

Ou a partir do código fonte:

```bash
git clone https://github.com/markqvist/Sideband
cd Sideband
pip install .
```

---

## correr

```bash
sideband
```

O primeiro arranque gera uma identidade criptográfica no dispositivo. Sem conta, sem registo. A identidade fica em `~/.sideband/`.

---

## correr sem interface gráfica (headless)

Para servidores e Raspberry Pi sem ecrã:

```bash
sideband --daemon
```

Corre em segundo plano. As mensagens são tratadas via LXMF, acessíveis a partir de outros clientes no mesmo nó ou rede.

---

## cópia de segurança da identidade

```bash
cp ~/.sideband/identity ~/.sideband/identity.bak
```

Guarda a cópia num lugar seguro. Perder o ficheiro de identidade significa perder acesso a esse endereço permanentemente.

---

## a seguir

→ [conectividade.md](conectividade.md) — ligar a nós e interfaces

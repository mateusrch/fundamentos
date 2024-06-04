# Systemd(init system)

## Overview sobre Systemd

```
Pesquisar pelo comando `ss -ln`
```

É um sistema de gerenciamento e inicialização de serviços no linux, projetado para
substituir o antigo 'System V init'.

- **Gerenciamento de serviços**: Fornece ferramentas para iniciar parar, reiniciar e
ver status de serviços e daemons.
  - comandos comuns: [
      systemctl start,
      systemctl stop,
      systemctl restart,
      systemctl status,
      systemctl disable = faz ao contrario do enable,
      systemctl enable = cria um link simbólico para que o serviço suba durante o bot
    ]

- No path */usr/lib/systemd/system/* ficam os arquivos de configuração dos serviços.

# Template Zabbix - UniFi Controller

Template para monitoramento do UniFi Controller via API, utilizando macros para autenticação e coleta de métricas detalhadas por site e por dispositivo.

## Funcionalidades

- Coleta de dados via API REST
- Descoberta automática de:
  - Equipamentos UniFi (Access Points, Gateways, Switches)
  - Sites configurados no Controller
- Métricas coletadas por dispositivo:
  - Clientes conectados (2.4GHz e 5GHz)
  - Uso de CPU e memória
  - Status de conexão
  - Potência de transmissão
  - Satisfação do sinal por rádio
  - Uptime, modelo, IP, etc.
- Métricas por site:
  - Alarmes
  - Quantidade de usuários, dispositivos LAN/WAN/WLAN/VPN
  - Status dos subsistemas
  - Versão atual vs. versão mais recente

## Requisitos

- Zabbix Server **7.0 ou superior**
- Acesso à API do UniFi Controller (nível de permissão *read-only* é suficiente)
- Controller com acesso HTTPS e porta configurada (default: 8443)
- Configurar um usuário somente leitura no UniFi Controller
- Configuração das seguintes macros no host:
  - `{$UNIFI_USER}`
  - `{$UNIFI_PASSWORD}`
  - `{$UNIFI_PORT}` (ex: `8443`)
  - `{$UNIFI_UPDATEURL}` (ex: `https://fw-download.ubnt.com/data/unifi-controller/manifest.json`)

## Como importar

1. Acesse o menu: `Configuration > Templates`
2. Clique em `Import`
3. Selecione o arquivo `template_unifi_controller.xml` incluído neste repositório
4. Marque todas as opções de substituição
5. Associe o template a um host do tipo UniFi

## Screenshots

> *(adicione aqui imagens em `images/` como `images/overview.png`)*

## Licença

Distribuído sob a [Licença MIT](LICENSE).

## Autor

Desenvolvido por [@magnetu2](https://github.com/magnetu2)  
Contribuições são bem-vindas via **Pull Requests** ou **Issues**.

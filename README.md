Файл генерируется ежедневно на основе списков [itdoginfo/allow-domains](https://github.com/itdoginfo/allow-domains).

Актуальную версию можно скачать командой
```
curl -LO https://github.com/unidcml/allow-domains-dat/releases/latest/download/allow-domains.dat
```
Включает списки Inside, Outside и Ukraine.

## Конфигурация сервера
```json
  "routing": {
    "domainStrategy": "IPIfNonMatch",
    "rules": [
      {
        "outboundTag": "BLOCK",
        "domain": [
          "ext:allow-domains.dat:inside",
          "ext:allow-domains.dat:outside",
          "ext:allow-domains.dat:ukraine"
        ],
        "type": "field"
      }
    ]
  }
```

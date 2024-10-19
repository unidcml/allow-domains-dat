Файлы генерируются ежедневно на основе списков [itdoginfo/allow-domains](https://github.com/itdoginfo/allow-domains).

## Ссылки для скачивания

- **allow-domains.dat**: 
  - [https://github.com/unidcml/allow-domains-dat/releases/latest/download/allow-domains.dat](https://github.com/unidcml/allow-domains-dat/releases/latest/download/allow-domains.dat)
  - [https://github.com/unidcml/allow-domains-dat/releases/latest/download/allow-domains.dat.sha256sum](https://github.com/unidcml/allow-domains-dat/releases/latest/download/allow-domains.dat.sha256sum)
- **subnets.dat**:
  - [https://github.com/unidcml/allow-domains-dat/releases/latest/download/subnets.dat](https://github.com/unidcml/allow-domains-dat/releases/latest/download/subnets.dat)
  - [https://github.com/unidcml/allow-domains-dat/releases/latest/download/subnets.dat.sha256sum](https://github.com/unidcml/allow-domains-dat/releases/latest/download/subnets.dat.sha256sum)

## Пример конфигурации

```json
  "routing": {
    "domainStrategy": "IPIfNonMatch",
    "rules": [
      {
        "domain": ["ext:allow-domains.dat:inside"],
        "outboundTag": "block",
      },
      {
        "ip": ["ext:subnets.dat:discord"],
        "outboundTag": "block"
      }
    ]
  }
```

# 1X API Schema

Tento repositář obsahuje schémata pro práci s API registrátora 1X.

## Důležité výstupy

* [[Dokumentace]](./docs/1x-api.md)
* [[Složené schéma]](./1x-api-schema.json)

## Použití

Vstupní schémata jsou v adresáři [./schemas](./schemas)

vygenerování nové dokumentace

```shell
rake doc
```

vygenerování nového schématu

```shell
rake combine
```

spuštění stub serveru na portu 8000

```shell
committee-stub -p 8000 1x-api-schema.json
```

# 1X API Schema

Tento repositář obsahuje schémata pro práci s API registrátora 1X.

## Důležité výstupy

* [[Dokumentace]](./schema.md)
* [[Složené schéma]](./schema.json)

## Použití

Vstupní schémata jsou v adresáři [./schemata](./schemata)

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
committee-stub -p 8000 schema.json
```

CLI klient

```shell
./bin/1x help
Usage: 1x-api <command> [<parameter> [...]] [<body>]

Help topics, type "1x-api help <topic>" for more details:

  order:create      Podání nové objednávky.
  order:info        Informace o konkrétní objednávce.
  order:list        Seznam objednávek.
  request:create    Podání nového požadavku.
  request:info      Seznam požadavků.
  request:list      Výpis požadavků.
```

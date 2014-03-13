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

CLI klient

```shell
./bin/1x help
Usage: 1x-api <command> [<parameter> [...]] [<body>]

Help topics, type "1x-api help <topic>" for more details:

  order:create      Create a new order.
  order:delete      Delete an existing order.
  order:info        Info for existing order.
  order:list        List existing orders.
  order:update      Update an existing order.
  request:create    Create a new request.
  request:delete    Delete an existing request.
  request:info      Info for existing request.
  request:list      List existing requests.
  request:update    Update an existing request.
```

# no-russia.dat

Сборка geosite-файла `no-russia.dat` для xray-core и совместимых клиентов со списком сайтов, блокирующих пользователей из России. Домены берутся из внешних списков и объединяются в одну категорию `no-russia`.

Файл собирается автоматически при изменении любого из источников.

## Источники

| Репозиторий |
|---|
|  [dartraiden/no-russia-hosts](https://github.com/dartraiden/no-russia-hosts) |
| [itdoginfo/allow-domains](https://github.com/itdoginfo/allow-domains) |

Точные URL перечислены в `sources.tsv`.

## Использование

Скачать последнюю сборку:

```
https://github.com/potatoru/no-russia/releases/latest/download/no-russia.dat
```

Положить рядом с остальными ассетами xray (обычно `/usr/local/share/xray/`) и добавить правило в роутинг:

```json
{
  "type": "field",
  "outboundTag": "proxy",
  "domain": ["ext:no-russia.dat:no-russia"]
}
```

## Что в релизе

| Файл | Описание |
|---|---|
| `no-russia.dat` | сборка для xray |
| `no-russia.dat.sha256` | контрольная сумма |
| `no-russia.txt` | тот же список в текстовом виде, по строке на правило |

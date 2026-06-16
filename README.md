# Ozon Seller API — Postman Collection

Полная Postman-коллекция для [Ozon Seller API](https://docs.ozon.ru/api/seller/), сгенерированная из официальной OpenAPI-спецификации Ozon.

Готова к импорту в Postman: все методы разложены по папкам, с описаниями, параметрами и примерами тел запросов.

## Что внутри

- **460 методов** — полное покрытие Seller API
- **454 POST** и **6 GET** запросов
- **56 разделов** (папки = теги API)
- Описания методов, заголовки авторизации и **примеры тел запросов** из схем
- Базовый URL и авторизация вынесены в переменные коллекции

| | |
|---|---|
| Источник | OpenAPI 3.0.0, «Документация Ozon Seller API», версия 2.1 |
| Базовый URL | `https://api-seller.ozon.ru` |
| Авторизация | HTTP-заголовки `Client-Id` и `Api-Key` |
| Формат | Postman Collection v2.1 |
| Файл | `Ozon_Seller_API.postman_collection.json` |

## Структура

Методы сгруппированы по тегам, как в официальной документации. Основные разделы:

- **Товары и цены** — `ProductAPI`, `Prices&StocksAPI`, `PricingStrategyAPI`, `CategoryAPI`, `BarcodeAPI`
- **Заказы и доставка** — `FBS`, `FBO`, `DeliveryFBS`, `DeliveryrFBS`, `DeliveryFBP`, `CarriageAPI`
- **Ozon Доставка** — `DeliveryAPI`, `OrderAPI`, `CancelReasonAPI`, `FboPostingAPI`
- **Возвраты** — `ReturnsAPI`, `ReturnAPI`, `RFBSReturnsAPI`, `CancellationAPI`
- **Склады и поставки** — `WarehouseAPI`, `FboSupplyRequest`, `FBOTransport`
- **Финансы и отчёты** — `FinanceAPI`, `ReportAPI`, `AnalyticsAPI`, `Receipt`
- **Прочее** — `ChatAPI`, `ReviewAPI`, `Questions&Answers`, `Promos`, `Notification`, `SellerRating` и др.

## Установка

1. Откройте Postman → **File → Import**.
2. Выберите файл `Ozon_Seller_API.postman_collection.json` (или перетащите его в окно).
3. Коллекция появится в боковой панели.

## Настройка авторизации

Откройте коллекцию → вкладка **Variables** и задайте значения:

| Переменная | Значение |
|---|---|
| `baseUrl` | `https://api-seller.ozon.ru` |
| `Client-Id` | ваш Client-Id |
| `Api-Key` | ваш Api-Key |

> В импортированной коллекции `baseUrl` имеет значение `//api-seller.ozon.ru` — укажите полный адрес со схемой `https://`.

Заголовки `Client-Id` и `Api-Key` уже добавлены в запросы — достаточно проставить значения переменных.

### Где взять ключи

Личный кабинет продавца Ozon → **Настройки → API-ключи** (раздел Seller API). Создайте ключ и используйте выданные `Client-Id` и `Api-Key`.

## Как сгенерировано

Коллекция получена из официальной OpenAPI-спецификации Ozon с помощью конвертера
[`openapi-to-postmanv2`](https://github.com/postmanlabs/openapi-to-postman):

```bash
npx openapi-to-postmanv2 \
  -s swagger.json \
  -o Ozon_Seller_API.postman_collection.json \
  -p -O folderStrategy=Tags,requestParametersResolution=Example,exampleParametersResolution=Example
```

## Обновление

Спецификация Ozon меняется. Чтобы обновить коллекцию, скачайте актуальный `swagger.json`
из источника, указанного в `loadSwagger.js` на странице документации, и повторите команду конвертации выше.

## Дисклеймер

Неофициальный репозиторий. Не связан с Ozon и не поддерживается им.
Наименования Ozon, Ozon Seller API и логотипы принадлежат их правообладателям.
Коллекция предоставляется «как есть»; единственный источник истины — [официальная документация](https://docs.ozon.ru/api/seller/).

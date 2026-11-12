---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words для Java"
description: "Обработчик запросов JWT Token с кэшированием, локальной проверкой и circuit breaker в Java."
type: docs
weight: 648
url: /ru/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

Обработчик запросов JWT Token с кэшированием, локальной проверкой и circuit breaker. Токены кэшируются до 7 дней с обновлением за 6 часов до истечения срока.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Публичный конструктор. |
## Методы

| Метод | Описание |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Добавьте заголовок авторизации перед отправкой запроса. |
| [getCachedToken()](#getCachedToken) | Получает текущий кэшированный токен для целей тестирования. |
| [getTokenExpiration()](#getTokenExpiration) | Получает время истечения токена как объект Date для целей тестирования. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Получает время истечения токена для целей тестирования. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Обрабатывает ответ, обрабатывая ошибку 401 Unauthorized путем обновления токена. |
| [processUrl(String url)](#processUrl-java.lang.String) | Обрабатывает URL (обеспечивая наличие токена). |
| [resetForTesting()](#resetForTesting) | Сбрасывает всё кэшированное состояние токена для целей тестирования. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Публичный конструктор.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Добавьте заголовок авторизации перед отправкой запроса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| запрос | java.net.HttpURLConnection | HTTP‑соединение |
| streamToSend | java.io.OutputStream | Выходной поток (не используется) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Получает текущий кэшированный токен для целей тестирования.

**Returns:**
java.lang.String - Кэшированный JWT токен или null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Получает время истечения токена как объект Date для целей тестирования.

**Returns:**
java.util.Date - Дата истечения или null, если токен отсутствует
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Получает время истечения токена для целей тестирования.

**Returns:**
long - Время истечения в миллисекундах с начала эпохи
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Обрабатывает ответ, обрабатывая ошибку 401 Unauthorized путем обновления токена.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ответ | java.net.HttpURLConnection | HTTP‑ответ |
| resultString | java.lang.String | Тело ответа |
| errorString | java.lang.String | Сообщение об ошибке, если есть |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Обрабатывает URL (обеспечивая наличие токена).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| url | java.lang.String | URL для обработки |

**Returns:**
java.lang.String - URL без изменений
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Сбрасывает всё кэшированное состояние токена для целей тестирования.


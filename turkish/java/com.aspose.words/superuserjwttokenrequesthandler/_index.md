---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words Java için"
description: "Java'da önbellekleme, yerel doğrulama ve devre kesici ile JWT Token Request Handler."
type: docs
weight: 648
url: /tr/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

Önbellekleme, yerel doğrulama ve devre kesici özellikli JWT Token Request Handler. Tokenlar, süresi dolmadan 6 saat önce yenilenerek en fazla 7 gün boyunca önbelleğe alınır.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Genel yapıcı. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | İsteği göndermeden önce yetkilendirme başlığını ekleyin. |
| [getCachedToken()](#getCachedToken) | Test amaçları için şu anda önbelleğe alınmış belirteci alır. |
| [getTokenExpiration()](#getTokenExpiration) | Test amaçları için token süresinin sonunu Date olarak alır. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Test amaçları için token süresinin son zamanını alır. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Yanıtı işle, 401 Yetkisiz hatasını token yenileyerek ele al. |
| [processUrl(String url)](#processUrl-java.lang.String) | URL'yi işle (token'ın mevcut olduğundan emin olur). |
| [resetForTesting()](#resetForTesting) | Test amaçları için önbelleğe alınmış tüm token durumunu sıfırlar. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Genel yapıcı.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


İsteği göndermeden önce yetkilendirme başlığını ekleyin.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| request | java.net.HttpURLConnection | HTTP bağlantısı |
| streamToSend | java.io.OutputStream | Çıkış akışı (kullanılmıyor) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Test amaçları için şu anda önbelleğe alınmış belirteci alır.

**Returns:**
java.lang.String - Önbelleğe alınmış JWT belirteci veya null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Test amaçları için token süresinin sonunu Date olarak alır.

**Returns:**
java.util.Date - Süre sonu Date veya token yoksa null
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Test amaçları için token süresinin son zamanını alır.

**Returns:**
long - Epoch'tan itibaren milisaniye cinsinden süresi sonu zamanı
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Yanıtı işle, 401 Yetkisiz hatasını token yenileyerek ele al.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| response | java.net.HttpURLConnection | HTTP yanıtı |
| resultString | java.lang.String | Yanıt gövdesi |
| errorString | java.lang.String | Varsa hata mesajı |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


URL'yi işle (token'ın mevcut olduğundan emin olur).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| url | java.lang.String | İşlenecek URL |

**Returns:**
java.lang.String - Değiştirilmemiş URL
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Test amaçları için önbelleğe alınmış tüm token durumunu sıfırlar.


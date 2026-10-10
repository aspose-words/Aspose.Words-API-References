---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words für Java"
description: "JWT‑Token‑Request‑Handler mit Zwischenspeicherung, lokaler Validierung und Circuit‑Breaker in Java."
type: docs
weight: 648
url: /de/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

JWT‑Token‑Request‑Handler mit Zwischenspeicherung, lokaler Validierung und Circuit‑Breaker. Tokens werden bis zu 7 Tage zwischengespeichert und 6 Stunden vor Ablauf aktualisiert.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Öffentlicher Konstruktor. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Fügen Sie den Autorisierungsheader hinzu, bevor Sie die Anfrage senden. |
| [getCachedToken()](#getCachedToken) | Ruft das aktuell zwischengespeicherte Token für Testzwecke ab. |
| [getTokenExpiration()](#getTokenExpiration) | Ruft das Token-Ablaufdatum als Date für Testzwecke ab. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Ruft die Token-Ablaufzeit für Testzwecke ab. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Verarbeitet die Antwort und behandelt 401 Unauthorized, indem das Token aktualisiert wird. |
| [processUrl(String url)](#processUrl-java.lang.String) | Verarbeitet die URL (stellt sicher, dass ein Token verfügbar ist). |
| [resetForTesting()](#resetForTesting) | Setzt den gesamten zwischengespeicherten Token-Status für Testzwecke zurück. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Öffentlicher Konstruktor.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Fügen Sie den Autorisierungsheader hinzu, bevor Sie die Anfrage senden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| request | java.net.HttpURLConnection | Die HTTP-Verbindung |
| streamToSend | java.io.OutputStream | Der Ausgabestream (nicht verwendet) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Ruft das aktuell zwischengespeicherte Token für Testzwecke ab.

**Returns:**
java.lang.String - Das zwischengespeicherte JWT-Token oder null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Ruft das Token-Ablaufdatum als Date für Testzwecke ab.

**Returns:**
java.util.Date - Das Ablaufdatum oder null, wenn kein Token
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Ruft die Token-Ablaufzeit für Testzwecke ab.

**Returns:**
long - Die Ablaufzeit in Millisekunden seit dem Epoch
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Verarbeitet die Antwort und behandelt 401 Unauthorized, indem das Token aktualisiert wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| response | java.net.HttpURLConnection | Die HTTP-Antwort |
| resultString | java.lang.String | Der Antwortkörper |
| errorString | java.lang.String | Die Fehlermeldung, falls vorhanden |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Verarbeitet die URL (stellt sicher, dass ein Token verfügbar ist).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| url | java.lang.String | Die URL zum Verarbeiten |

**Returns:**
java.lang.String - Die unveränderte URL
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Setzt den gesamten zwischengespeicherten Token-Status für Testzwecke zurück.


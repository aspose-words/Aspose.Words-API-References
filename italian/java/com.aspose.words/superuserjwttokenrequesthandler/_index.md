---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words per Java"
description: "JWT Token Request Handler con caching, validazione locale e circuit breaker in Java."
type: docs
weight: 648
url: /it/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

JWT Token Request Handler con caching, validazione locale e circuit breaker. I token sono memorizzati nella cache per un massimo di 7 giorni con aggiornamento 6 ore prima della scadenza.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Costruttore pubblico. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Aggiungi l'intestazione di autorizzazione prima di inviare la richiesta. |
| [getCachedToken()](#getCachedToken) | Ottiene il token attualmente memorizzato nella cache per scopi di test. |
| [getTokenExpiration()](#getTokenExpiration) | Ottiene la scadenza del token come Date per scopi di test. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Ottiene il tempo di scadenza del token per scopi di test. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Elabora la risposta, gestendo il 401 Unauthorized rinnovando il token. |
| [processUrl(String url)](#processUrl-java.lang.String) | Elabora l'URL (assicura che il token sia disponibile). |
| [resetForTesting()](#resetForTesting) | Reimposta tutto lo stato del token memorizzato nella cache per scopi di test. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Costruttore pubblico.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Aggiungi l'intestazione di autorizzazione prima di inviare la richiesta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| richiesta | java.net.HttpURLConnection | La connessione HTTP |
| streamToSend | java.io.OutputStream | Il flusso di output (non utilizzato) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Ottiene il token attualmente memorizzato nella cache per scopi di test.

**Returns:**
java.lang.String - Il token JWT memorizzato nella cache o null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Ottiene la scadenza del token come Date per scopi di test.

**Returns:**
java.util.Date - La Data di scadenza o null se nessun token
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Ottiene il tempo di scadenza del token per scopi di test.

**Returns:**
long - Il tempo di scadenza in millisecondi dall'epoch
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Elabora la risposta, gestendo il 401 Unauthorized rinnovando il token.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| risposta | java.net.HttpURLConnection | La risposta HTTP |
| resultString | java.lang.String | Il corpo della risposta |
| errorString | java.lang.String | Il messaggio di errore, se presente |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Elabora l'URL (assicura che il token sia disponibile).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| url | java.lang.String | L'URL da elaborare |

**Returns:**
java.lang.String - L'URL invariato
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Reimposta tutto lo stato del token memorizzato nella cache per scopi di test.


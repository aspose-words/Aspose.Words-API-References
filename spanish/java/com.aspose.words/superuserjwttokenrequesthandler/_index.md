---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words para Java"
description: "Manejador de solicitud de token JWT con caché, validación local y circuito de interrupción en Java."
type: docs
weight: 648
url: /es/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

Manejador de solicitud de token JWT con caché, validación local y circuito de interrupción. Los tokens se almacenan en caché hasta 7 días con una actualización 6 horas antes de su expiración.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Constructor público. |
## Métodos

| Método | Descripción |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Agregue el encabezado de autorización antes de enviar la solicitud. |
| [getCachedToken()](#getCachedToken) | Obtiene el token almacenado en caché actualmente para fines de prueba. |
| [getTokenExpiration()](#getTokenExpiration) | Obtiene la expiración del token como una Date para fines de prueba. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Obtiene el tiempo de expiración del token para fines de prueba. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Procesa la respuesta, manejando 401 Unauthorized mediante la actualización del token. |
| [processUrl(String url)](#processUrl-java.lang.String) | Procesa la URL (asegura que el token esté disponible). |
| [resetForTesting()](#resetForTesting) | Restablece todo el estado del token en caché para fines de prueba. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Constructor público.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Agregue el encabezado de autorización antes de enviar la solicitud.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| solicitud | java.net.HttpURLConnection | La conexión HTTP |
| streamToSend | java.io.OutputStream | El flujo de salida (no usado) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Obtiene el token almacenado en caché actualmente para fines de prueba.

**Returns:**
java.lang.String - El token JWT almacenado en caché o null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Obtiene la expiración del token como una Date para fines de prueba.

**Returns:**
java.util.Date - La Date de expiración o null si no hay token
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Obtiene el tiempo de expiración del token para fines de prueba.

**Returns:**
long - El tiempo de expiración en milisegundos desde la época
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Procesa la respuesta, manejando 401 Unauthorized mediante la actualización del token.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| respuesta | java.net.HttpURLConnection | La respuesta HTTP |
| resultString | java.lang.String | El cuerpo de la respuesta |
| errorString | java.lang.String | El mensaje de error, si lo hay |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Procesa la URL (asegura que el token esté disponible).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| url | java.lang.String | La URL a procesar |

**Returns:**
java.lang.String - La URL sin cambios
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Restablece todo el estado del token en caché para fines de prueba.


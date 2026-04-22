---
title: SuperUserJwtTokenRequestHandler
linktitle: SuperUserJwtTokenRequestHandler
second_title: Aspose.Words for Java
description: JWT Token Request Handler with caching local validation and circuit breaker in Java.
type: docs
weight: 647
url: /java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

JWT Token Request Handler with caching, local validation, and circuit breaker. Tokens are cached for up to 7 days with refresh 6 hours before expiration.
## Constructors

| Constructor | Description |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Public constructor. |
## Methods

| Method | Description |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Add authorization header before sending the request. |
| [getCachedToken()](#getCachedToken) | Gets the currently cached token for testing purposes. |
| [getTokenExpiration()](#getTokenExpiration) | Gets the token expiration as a Date for testing purposes. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Gets the token expiration time for testing purposes. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Process the response, handling 401 Unauthorized by refreshing token. |
| [processUrl(String url)](#processUrl-java.lang.String) | Process the URL (ensures token is available). |
| [resetForTesting()](#resetForTesting) | Resets all cached token state for testing purposes. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Public constructor.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Add authorization header before sending the request.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| request | java.net.HttpURLConnection | The HTTP connection |
| streamToSend | java.io.OutputStream | The output stream (unused) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Gets the currently cached token for testing purposes.

**Returns:**
java.lang.String - The cached JWT token or null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Gets the token expiration as a Date for testing purposes.

**Returns:**
java.util.Date - The expiration Date or null if no token
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Gets the token expiration time for testing purposes.

**Returns:**
long - The expiration time in milliseconds since epoch
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Process the response, handling 401 Unauthorized by refreshing token.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| response | java.net.HttpURLConnection | The HTTP response |
| resultString | java.lang.String | The response body |
| errorString | java.lang.String | The error message if any |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Process the URL (ensures token is available).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| url | java.lang.String | The URL to process |

**Returns:**
java.lang.String - The URL unchanged
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Resets all cached token state for testing purposes.


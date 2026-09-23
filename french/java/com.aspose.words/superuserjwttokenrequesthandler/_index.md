---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words pour Java"
description: "Gestionnaire de requête de jeton JWT avec mise en cache, validation locale et disjoncteur en Java."
type: docs
weight: 648
url: /fr/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

Gestionnaire de requête de jeton JWT avec mise en cache, validation locale et disjoncteur. Les jetons sont mis en cache pendant jusqu'à 7 jours avec un rafraîchissement 6 heures avant l'expiration.
## Constructors

| Constructor | Description |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | Constructeur public. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | Ajoutez l'en-tête d'autorisation avant d'envoyer la requête. |
| [getCachedToken()](#getCachedToken) | Obtient le jeton actuellement mis en cache à des fins de test. |
| [getTokenExpiration()](#getTokenExpiration) | Obtient la date d'expiration du jeton sous forme de Date à des fins de test. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | Obtient le temps d'expiration du jeton à des fins de test. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | Traite la réponse, en gérant le 401 Unauthorized en rafraîchissant le jeton. |
| [processUrl(String url)](#processUrl-java.lang.String) | Traite l'URL (s'assure que le jeton est disponible). |
| [resetForTesting()](#resetForTesting) | Réinitialise tout l'état du jeton mis en cache à des fins de test. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


Constructeur public.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


Ajoutez l'en-tête d'autorisation avant d'envoyer la requête.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| requête | java.net.HttpURLConnection | La connexion HTTP |
| streamToSend | java.io.OutputStream | Le flux de sortie (non utilisé) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


Obtient le jeton actuellement mis en cache à des fins de test.

**Returns:**
java.lang.String - Le jeton JWT mis en cache ou null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


Obtient la date d'expiration du jeton sous forme de Date à des fins de test.

**Returns:**
java.util.Date - La date d'expiration ou null s'il n'y a pas de jeton
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


Obtient le temps d'expiration du jeton à des fins de test.

**Returns:**
long - Le temps d'expiration en millisecondes depuis l'époque
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


Traite la réponse, en gérant le 401 Unauthorized en rafraîchissant le jeton.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| réponse | java.net.HttpURLConnection | La réponse HTTP |
| resultString | java.lang.String | Le corps de la réponse |
| errorString | java.lang.String | Le message d'erreur le cas échéant |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


Traite l'URL (s'assure que le jeton est disponible).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| url | java.lang.String | L'URL à traiter |

**Returns:**
java.lang.String - L'URL inchangée
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


Réinitialise tout l'état du jeton mis en cache à des fins de test.


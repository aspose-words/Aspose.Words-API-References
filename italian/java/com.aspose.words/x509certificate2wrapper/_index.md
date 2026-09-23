---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words per Java"
description: "Wrapper pubblico aggiunto in JAVA attorno al nostro X509Certificate2 interno in Java."
type: docs
weight: 739
url: /it/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

Wrapper pubblico aggiunto in JAVA attorno al nostro X509Certificate2 interno. Necessario per emulare senza problemi l'API .Net e semplificare il codice Java dell'utente. Idealmente dovremmo usare java.security.cert.X509Certificate al suo posto, ma non siamo ancora riusciti a ottenere la chiave privata dal X509Certificate Java - potrebbe essere risolto in futuro.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Il certificato Java è utilizzato per ottenere informazioni generiche sul certificato: notBefore, notAfter, ecc. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String |  |
| password | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Il certificato Java è utilizzato per ottenere informazioni generiche sul certificato: notBefore, notAfter, ecc.

**Returns:**
java.security.cert.X509Certificate

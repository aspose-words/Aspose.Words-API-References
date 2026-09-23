---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words für Java"
description: "Von JAVA hinzugefügter öffentlicher Wrapper um unser internes X509Certificate2 in Java."
type: docs
weight: 739
url: /de/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

Von JAVA hinzugefügter öffentlicher Wrapper um unser internes X509Certificate2. Wird benötigt, um die .Net-API reibungslos zu emulieren und den Java-Benutzercode zu vereinfachen. Idealerweise sollten wir java.security.cert.X509Certificate anstelle dessen verwenden, aber wir konnten bisher den privaten Schlüssel aus dem Java X509Certificate nicht erhalten – möglicherweise später beheben.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Das Java-Zertifikat wird verwendet, um allgemeine Zertifikatsinformationen abzurufen: notBefore, notAfter usw. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String |  |
| Passwort | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Das Java-Zertifikat wird verwendet, um allgemeine Zertifikatsinformationen abzurufen: notBefore, notAfter usw.

**Returns:**
java.security.cert.X509Certificate

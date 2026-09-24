---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words para Java"
description: "Envoltorio público añadido por JAVA alrededor de nuestro X509Certificate2 interno en Java."
type: docs
weight: 739
url: /es/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

Envoltorio público añadido por JAVA alrededor de nuestro X509Certificate2 interno. Necesario para emular suavemente la API de .Net y simplificar el código del usuario en Java. Idealmente deberíamos usar java.security.cert.X509Certificate en su lugar, pero aún no hemos logrado obtener la clave privada del X509Certificate de Java; puede que se solucione más adelante.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | El certificado Java se utiliza para obtener información genérica del certificado: notBefore, notAfter, etc. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String |  |
| contraseña | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


El certificado Java se utiliza para obtener información genérica del certificado: notBefore, notAfter, etc.

**Returns:**
java.security.cert.X509Certificate

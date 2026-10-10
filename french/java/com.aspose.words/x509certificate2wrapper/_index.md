---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words pour Java"
description: "Enveloppe publique ajoutée par JAVA autour de notre X509Certificate2 interne en Java."
type: docs
weight: 739
url: /fr/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

Enveloppe publique ajoutée par JAVA autour de notre X509Certificate2 interne. Nécessaire pour émuler de manière fluide l'API .Net et simplifier le code utilisateur Java. Idéalement, nous devrions utiliser java.security.cert.X509Certificate à la place, mais nous n'avons toujours pas réussi à obtenir la clé privée du X509Certificate Java – cela pourra être corrigé plus tard.
## Constructors

| Constructor | Description |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Le certificat Java est utilisé pour obtenir des informations génériques du certificat : notBefore, notAfter, etc. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| mot de passe | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Le certificat Java est utilisé pour obtenir des informations génériques du certificat : notBefore, notAfter, etc.

**Returns:**
java.security.cert.X509Certificate

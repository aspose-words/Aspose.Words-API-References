---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words Java için"
description: "Java'da dahili X509Certificate2'imiz etrafında eklenen JAVA tabanlı genel sarmalayıcı."
type: docs
weight: 739
url: /tr/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

JAVA eklediği genel sarmalayıcı, dahili X509Certificate2'imiz etrafındadır. .Net API'sini sorunsuz bir şekilde taklit etmek ve java kullanıcı kodunu basitleştirmek için gereklidir. İdealde, java.security.cert.X509Certificate'ı bunun yerine kullanmamız gerekir, ancak hâlâ java X509Certificate'tan özel anahtarı elde edemedik – daha sonra düzeltilebilir.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | Java sertifikası, notBefore, notAfter vb. gibi genel sertifika bilgilerini almak için kullanılır. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String |  |
| şifre | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


Java sertifikası, notBefore, notAfter vb. gibi genel sertifika bilgilerini almak için kullanılır.

**Returns:**
java.security.cert.X509Certificate

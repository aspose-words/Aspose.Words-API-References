---
title: CertificateHolder
second_title: Aspose.Words for Java API Reference
description: Represents a holder of X509Certificate2 instance.
type: docs
weight: 53
url: /java/com.aspose.words/certificateholder/
---

**Inheritance:**
java.lang.Object
```
public class CertificateHolder
```

Represents a holder of **X509Certificate2** instance.

To learn more, visit the **Work with Digital Signatures** documentation article.

**CertificateHolder** can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil) and [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) instead of obsolete methods with **X509Certificate2** as parameters.
## Methods

| Method | Description |
| --- | --- |
| [getCertificate()](#getCertificate--) | Returns the instance of **X509Certificate2Wrapper** that holds **X509Certificate2** which holds private, public keys and certificate chain. |
| [create(byte[] certBytes, String password)](#create-byte---java.lang.String-) | Creates CertificateHolder object using byte array of PKCS12 store and its password. |
| [create(String fileName, String password)](#create-java.lang.String-java.lang.String-) | Creates CertificateHolder object using path to PKCS12 store and its password. |
| [create(String fileName, String password, String alias)](#create-java.lang.String-java.lang.String-java.lang.String-) | Creates CertificateHolder object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |
### getCertificate() {#getCertificate--}
```
public X509Certificate2Wrapper getCertificate()
```


Returns the instance of **X509Certificate2Wrapper** that holds **X509Certificate2** which holds private, public keys and certificate chain.

**Returns:**
[X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper) -  instance
### create(byte[] certBytes, String password) {#create-byte---java.lang.String-}
```
public static CertificateHolder create(byte[] certBytes, String password)
```


Creates CertificateHolder object using byte array of PKCS12 store and its password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | byte[] | A byte array that contains data from an X.509 certificate. |
| password | java.lang.String | The password required to access the X.509 certificate data. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of CertificateHolder **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **certBytes** is null **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **password** is null
### create(String fileName, String password) {#create-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password)
```


Creates CertificateHolder object using path to PKCS12 store and its password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name of a certificate file. |
| password | java.lang.String | The password required to access the X.509 certificate data. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of CertificateHolder **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **fileName** is null **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **password** is null
### create(String fileName, String password, String alias) {#create-java.lang.String-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password, String alias)
```


Creates CertificateHolder object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name of a certificate file. |
| password | java.lang.String | The password required to access the X.509 certificate data. |
| alias | java.lang.String | The associated alias for a certificate and its private key |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of CertificateHolder **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **fileName** is null **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if **password** is null

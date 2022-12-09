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

To learn more, visit the [ Work with Digital Signatures ][Work with Digital Signatures] documentation article.

[CertificateHolder](../../com.aspose.words/certificateholder) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil) and [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) instead of obsolete methods with **X509Certificate2** as parameters.


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Methods

| Method | Description |
| --- | --- |
| [create(byte[] certBytes, String password)](#create-byte---java.lang.String) | Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using byte array of PKCS12 store and its password. |
| [create(String fileName, String password)](#create-java.lang.String-java.lang.String) | Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using path to PKCS12 store and its password. |
| [create(String fileName, String password, String alias)](#create-java.lang.String-java.lang.String-java.lang.String) | Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getCertificate()](#getCertificate) | Returns the instance of **X509Certificate2Wrapper** that holds **X509Certificate2** which holds private, public keys and certificate chain. |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### create(byte[] certBytes, String password) {#create-byte---java.lang.String}
```
public static CertificateHolder create(byte[] certBytes, String password)
```


Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using byte array of PKCS12 store and its password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | byte[] | A byte array that contains data from an X.509 certificate. |
| password | java.lang.String | The password required to access the X.509 certificate data. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder) **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  certBytes  is  null  **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  password  is  null 
### create(String fileName, String password) {#create-java.lang.String-java.lang.String}
```
public static CertificateHolder create(String fileName, String password)
```


Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using path to PKCS12 store and its password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name of a certificate file. |
| password | java.lang.String | The password required to access the X.509 certificate data. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder) **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  fileName  is  null  **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  password  is  null 
### create(String fileName, String password, String alias) {#create-java.lang.String-java.lang.String-java.lang.String}
```
public static CertificateHolder create(String fileName, String password, String alias)
```


Creates [CertificateHolder](../../com.aspose.words/certificateholder) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name of a certificate file. |
| password | java.lang.String | The password required to access the X.509 certificate data. |
| alias | java.lang.String | The associated alias for a certificate and its private key |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder) **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  fileName  is  null  **T:Org.BouncyCastle.Security.InvalidParameterException** Thrown if  password  is  null 
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getCertificate() {#getCertificate}
```
public X509Certificate2Wrapper getCertificate()
```


Returns the instance of **X509Certificate2Wrapper** that holds **X509Certificate2** which holds private, public keys and certificate chain.

**Returns:**
[X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper) -  instance
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |


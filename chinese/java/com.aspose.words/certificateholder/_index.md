---
title: CertificateHolder
second_title: Aspose.Words for Java API 参考
description:表示 X509Certificate2 实例的持有者。
type: docs
weight: 53
url: /zh/java/com.aspose.words/certificateholder/
---

**遗产:**
java.lang.Object
```
public class CertificateHolder
```

代表持有人**X509Certificate2**实例。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。

**CertificateHolder**只能由静态工厂方法创建。它包含一个实例**X509Certificate2**用于将私钥、公钥和证书链引入系统。该类应用于[DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil)和[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails)而不是过时的方法**X509Certificate2**作为参数。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [create(byte[] certBytes, String password)](#create-byte---java.lang.String-) | 使用 PKCS12 存储的字节数组及其密码创建 CertificateHolder 对象。 |
| [create(String fileName, String password)](#create-java.lang.String-java.lang.String-) | 使用 PKCS12 存储的路径及其密码创建 CertificateHolder 对象。 |
| [create(String fileName, String password, String alias)](#create-java.lang.String-java.lang.String-java.lang.String-) | 使用 PKCS12 存储的路径、其密码和别名创建 CertificateHolder 对象，使用该对象将找到私钥和证书。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificate()](#getCertificate--) | 返回的实例**X509Certificate2Wrapper**持有**X509Certificate2**它拥有私钥、公钥和证书链。 |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### create(byte[] certBytes, String password) {#create-byte---java.lang.String-}
```
public static CertificateHolder create(byte[] certBytes, String password)
```


使用 PKCS12 存储的字节数组及其密码创建 CertificateHolder 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certBytes | byte[] | 包含来自 X.509 证书的数据的字节数组。 |
| password | java.lang.String | 访问 X.509 证书数据所需的密码。 |

**退货:**
[CertificateHolder](../../com.aspose.words/certificateholder) - CertificateHolder 的一个实例**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**certBytes**一片空白**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**password**一片空白
### create(String fileName, String password) {#create-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password)
```


使用 PKCS12 存储的路径及其密码创建 CertificateHolder 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 证书文件的名称。 |
| password | java.lang.String | 访问 X.509 证书数据所需的密码。 |

**退货:**
[CertificateHolder](../../com.aspose.words/certificateholder) - CertificateHolder 的一个实例**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**fileName**一片空白**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**password**一片空白
### create(String fileName, String password, String alias) {#create-java.lang.String-java.lang.String-java.lang.String-}
```
public static CertificateHolder create(String fileName, String password, String alias)
```


使用 PKCS12 存储的路径、其密码和别名创建 CertificateHolder 对象，使用该对象将找到私钥和证书。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 证书文件的名称。 |
| password | java.lang.String | 访问 X.509 证书数据所需的密码。 |
| alias | java.lang.String | 证书及其私钥的关联别名 |

**退货:**
[CertificateHolder](../../com.aspose.words/certificateholder) - CertificateHolder 的一个实例**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**fileName**一片空白**T:Org.BouncyCastle.Security.Invalid范围Exception**抛出如果**password**一片空白
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getCertificate() {#getCertificate--}
```
public X509Certificate2Wrapper getCertificate()
```


返回的实例**X509Certificate2Wrapper**持有**X509Certificate2**它拥有私钥、公钥和证书链。

**退货:**
[X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper) 实例
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

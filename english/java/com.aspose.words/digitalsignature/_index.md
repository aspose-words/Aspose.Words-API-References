---
title: DigitalSignature
second_title: Aspose.Words for Java API 参考
description: 表示文档上的数字签名及其验证结果。
type: docs
weight: 111
url: /zh/java/com.aspose.words/digitalsignature/
---

**遗产:**
java.lang.Object
```
public class DigitalSignature
```

表示文档上的数字签名及其验证结果。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificateHolder()](#getCertificateHolder--) | 返回包含用于签署文档的证书的证书持有者对象。 |
| [get班级()](#get班级--) |  |
| [getComments()](#getComments--) | 获取签名目的注释。 |
| [getIssuerName()](#getIssuerName--) | 返回证书颁发者的主题专有名称。 |
| [getSignTime()](#getSignTime--) | 获取文档签署的时间。 |
| [getSignature类型()](#getSignature类型--) | 获取数字签名的类型。 |
| [getSubjectName()](#getSubjectName--) | 返回用于签署文档的证书的主题专有名称。 |
| [hashCode()](#hashCode--) |  |
| [isValid()](#isValid--) | 如果此数字签名有效且文档未被篡改，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | 返回显示此对象值的用户友好字符串。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


返回包含用于签署文档的证书的证书持有者对象。

**退货:**
[CertificateHolder](../../com.aspose.words/certificateholder) - 包含证书的证书持有者对象用于签署文档。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getComments() {#getComments--}
```
public String getComments()
```


获取签名目的注释。

**退货:**
java.lang.String - 签名目的注释。
### getIssuerName() {#getIssuerName--}
```
public String getIssuerName()
```


返回证书颁发者的主题专有名称。

**退货:**
java.lang.String - 证书颁发者的主题专有名称。
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


获取文档签署的时间。

**退货:**
java.util.Date - 签署文件的时间。
### getSignature类型() {#getSignature类型--}
```
public int getSignature类型()
```


获取数字签名的类型。

**退货:**
 int - 数字签名的类型。返回值是以下之一[DigitalSignature类型](../../com.aspose.words/digitalsignaturetype)常数。
### getSubjectName() {#getSubjectName--}
```
public String getSubjectName()
```


返回用于签署文档的证书的主题专有名称。

**退货:**
java.lang.String - 用于签署文档的证书的主题专有名称。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isValid() {#isValid--}
```
public boolean isValid()
```


如果此数字签名有效且文档未被篡改，则返回 true。

**退货:**
boolean - 如果此数字签名有效且文档未被篡改，则为真。
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


返回显示此对象值的用户友好字符串。

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

---
title: PdfEncryptionDetails
second_title: Aspose.Words for Java API Reference
description: 包含 PDF 文档的加密和访问权限的详细信息。
type: docs
weight: 454
url: /zh/java/com.aspose.words/pdfencryptiondetails/
---

**遗产:**
java.lang.Object
```
public class PdfEncryptionDetails
```

包含 PDF 文档的加密和访问权限的详细信息。

要了解更多信息，请访问**Protect or Encrypt a Document**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String-) | 初始化此类的一个实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getOwnerPassword()](#getOwnerPassword--) | 指定加密 PDF 文档的所有者密码。 |
| [getPermissions()](#getPermissions--) | 指定允许用户对加密的 PDF 文档进行的操作。 |
| [getUserPassword()](#getUserPassword--) | 指定打开加密 PDF 文档所需的用户密码。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String-) | 指定加密 PDF 文档的所有者密码。 |
| [setPermissions(int value)](#setPermissions-int-) | 指定允许用户对加密的 PDF 文档进行的操作。 |
| [setUserPassword(String value)](#setUserPassword-java.lang.String-) | 指定打开加密 PDF 文档所需的用户密码。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String-}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


初始化此类的一个实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getOwnerPassword() {#getOwnerPassword--}
```
public String getOwnerPassword()
```


指定加密 PDF 文档的所有者密码。

所有者密码允许用户打开加密的 PDF 文档，而不受[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-).

所有者密码不能与用户密码相同。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getPermissions() {#getPermissions--}
```
public int getPermissions()
```


指定允许用户对加密的 PDF 文档进行的操作。默认值为[PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions\#DISALLOW-ALL).

**退货:**
 int - 对应的 int 值。返回值是按位组合[PdfPermissions](../../com.aspose.words/pdfpermissions)常数。
### getUserPassword() {#getUserPassword--}
```
public String getUserPassword()
```


指定打开加密 PDF 文档所需的用户密码。

需要用户密码才能打开加密的 PDF 文档进行查看。中指定的权限[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-)将由阅读器软件强制执行。

用户密码可以是 null 或空字符串，在这种情况下，打开 PDF 文档时不需要用户输入密码。用户密码不能与所有者密码相同。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
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




### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String-}
```
public void setOwnerPassword(String value)
```


指定加密 PDF 文档的所有者密码。

所有者密码允许用户打开加密的 PDF 文档，而不受[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-).

所有者密码不能与用户密码相同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setPermissions(int value) {#setPermissions-int-}
```
public void setPermissions(int value)
```


指定允许用户对加密的 PDF 文档进行的操作。默认值为[PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions\#DISALLOW-ALL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是按位组合[PdfPermissions](../../com.aspose.words/pdfpermissions)常数。 |

### setUserPassword(String value) {#setUserPassword-java.lang.String-}
```
public void setUserPassword(String value)
```


指定打开加密 PDF 文档所需的用户密码。

需要用户密码才能打开加密的 PDF 文档进行查看。中指定的权限[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-)将由阅读器软件强制执行。

用户密码可以是 null 或空字符串，在这种情况下，打开 PDF 文档时不需要用户输入密码。用户密码不能与所有者密码相同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

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

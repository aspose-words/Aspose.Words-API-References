---
title: DigitalSignature类型
second_title: Aspose.Words for Java API 参考
description:指定数字签名的类型。
type: docs
weight: 113
url: /zh/java/com.aspose.words/digitalsignaturetype/
---

**遗产:**
java.lang.Object
```
public class DigitalSignature类型
```

指定数字签名的类型。
## 字段

| 字段 | 描述 |
| --- | --- |
| [CRYPTO_API](#CRYPTO-API) | Microsoft Word 97-2003 .DOC 二进制文档中使用的 Crypto API 签名方法。 |
| [UNKNOWN](#UNKNOWN) | 表示错误、未知的数字签名类型。 |
| [XML_DSIG](#XML-DSIG) | OOXML 和 OpenDocument 文档中使用的 XmlDsig 签名方法。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String digitalSignature类型Name)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int digitalSignature类型)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int digitalSignature类型)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


Microsoft Word 97-2003 .DOC 二进制文档中使用的 Crypto API 签名方法。

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


表示错误、未知的数字签名类型。

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


OOXML 和 OpenDocument 文档中使用的 XmlDsig 签名方法。

### length {#length}
```
public static int length
```


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
### fromName(String digitalSignature类型Name) {#fromName-java.lang.String-}
```
public static int fromName(String digitalSignature类型Name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| digitalSignature类型Name | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int digitalSignature类型) {#getName-int-}
```
public static String getName(int digitalSignature类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| digitalSignature类型 | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
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
### toString(int digitalSignature类型) {#toString-int-}
```
public static String toString(int digitalSignature类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| digitalSignature类型 | int |  |

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

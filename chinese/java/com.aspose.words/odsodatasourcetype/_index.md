---
title: OdsoDataSource类型
second_title: Aspose.Words for Java API Reference
description: 指定要连接到的外部数据源的类型，作为 ODSO 连接信息的一部分。
type: docs
weight: 412
url: /zh/java/com.aspose.words/odsodatasourcetype/
---

**遗产:**
java.lang.Object
```
public class OdsoDataSource类型
```

指定要连接到的外部数据源的类型，作为 ODSO 连接信息的一部分。

OOXML 规范对于这个枚举非常模糊。我猜它可能对应于 WdMergeSub类型 枚举 http://msdn.microsoft.com/en-us/library/bb237801.aspx。
## 字段

| 字段 | 描述 |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | 指定给定文档已连接到联系人地址簿。 |
| [DATABASE](#DATABASE) | 指定给定文档已连接到数据库。 |
| [DEFAULT](#DEFAULT) | 等于[NONE](../../com.aspose.words/odsodatasourcetype\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | 指定给定文档已连接到生成应用程序支持的另一种文档格式。 |
| [DOCUMENT_2](#DOCUMENT-2) | 指定给定文档已连接到生成应用程序支持的另一种文档格式。 |
| [EMAIL](#EMAIL) | 指定给定文档已连接到电子邮件应用程序。 |
| [LEGACY](#LEGACY) | 指定给定文档已连接到生产应用程序支持的旧文档格式，可能是 wdMergeSub类型Word2000。 |
| [MASTER](#MASTER) | 指定给定文档已连接到聚合其他数据源的数据源。 |
| [NATIVE](#NATIVE) | 指定给定文档已连接到生成应用程序本机的另一种文档格式。 |
| [NONE](#NONE) | 未指定外部数据源的类型。 |
| [TEXT](#TEXT) | 指定给定文档已连接到文本文件。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String odsoDataSource类型Name)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int odsoDataSource类型)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int odsoDataSource类型)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


指定给定文档已连接到联系人地址簿。可能是 wdMergeSub类型OAL。

### DATABASE {#DATABASE}
```
public static int DATABASE
```


指定给定文档已连接到数据库。可能是 wdMergeSub类型Access。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


等于[NONE](../../com.aspose.words/odsodatasourcetype\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


指定给定文档已连接到生成应用程序支持的另一种文档格式。可能是 wdMergeSub类型OLEDBWord。

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


指定给定文档已连接到生成应用程序支持的另一种文档格式。可能是 wdMergeSub类型Works。

### EMAIL {#EMAIL}
```
public static int EMAIL
```


指定给定文档已连接到电子邮件应用程序。可能是 wdMergeSub类型Outlook。

### LEGACY {#LEGACY}
```
public static int LEGACY
```


指定给定文档已连接到生产应用程序支持的旧文档格式，可能是 wdMergeSub类型Word2000。

### MASTER {#MASTER}
```
public static int MASTER
```


指定给定文档已连接到聚合其他数据源的数据源。

### NATIVE {#NATIVE}
```
public static int NATIVE
```


指定给定文档已连接到生成应用程序本机的另一种文档格式。可能是 wdMergeSub类型OLEDBText

### NONE {#NONE}
```
public static int NONE
```


未指定外部数据源的类型。可能是 wdMergeSub类型Word。

### TEXT {#TEXT}
```
public static int TEXT
```


指定给定文档已连接到文本文件。可能是 wdMergeSub类型Other。

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
### fromName(String odsoDataSource类型Name) {#fromName-java.lang.String-}
```
public static int fromName(String odsoDataSource类型Name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| odsoDataSource类型Name | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int odsoDataSource类型) {#getName-int-}
```
public static String getName(int odsoDataSource类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| odsoDataSource类型 | int |  |

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
### toString(int odsoDataSource类型) {#toString-int-}
```
public static String toString(int odsoDataSource类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| odsoDataSource类型 | int |  |

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

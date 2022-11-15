---
title: MailMergeDataType
second_title: Aspose.Words for Java API 参考
description: 指定外部邮件合并数据源的类型。
type: docs
weight: 382
url: /zh/java/com.aspose.words/mailmergedatatype/
---

**遗产：**
java.lang.Object
```
public class MailMergeDataType
```

指定外部邮件合并数据源的类型。
## 字段

| 场地 | 描述 |
| --- | --- |
| [DATABASE](#DATABASE) | 指定给定文档已通过动态数据交换 (DDE) 系统连接到 Access 数据库。 |
| [DEFAULT](#DEFAULT) | 等于[NONE](../../com.aspose.words/mailmergedatatype\#NONE). |
| [NATIVE](#NATIVE) | 指定给定文档已通过 Office 数据源对象 (ODSO) 接口连接到外部数据源。 |
| [NONE](#NONE) | 未指定邮件合并数据源。 |
| [ODBC](#ODBC) | 指定给定文档已通过开放式数据库连接接口连接到外部数据源。 |
| [QUERY](#QUERY) | 指定给定文档已使用外部查询工具连接到外部数据源。 |
| [SPREADSHEET](#SPREADSHEET) | 指定给定文档已通过动态数据交换 (DDE) 系统连接到 Excel 电子表格。 |
| [TEXT_FILE](#TEXT-FILE) | 指定给定文档已通过动态数据交换 (DDE) 系统连接到文本文件。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int mailMergeDataType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mailMergeDataType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


指定给定文档已通过动态数据交换 (DDE) 系统连接到 Access 数据库。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


等于[NONE](../../com.aspose.words/mailmergedatatype\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


指定给定文档已通过 Office 数据源对象 (ODSO) 接口连接到外部数据源。

### NONE {#NONE}
```
public static int NONE
```


未指定邮件合并数据源。

### ODBC {#ODBC}
```
public static int ODBC
```


指定给定文档已通过开放式数据库连接接口连接到外部数据源。

### QUERY {#QUERY}
```
public static int QUERY
```


指定给定文档已使用外部查询工具连接到外部数据源。

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


指定给定文档已通过动态数据交换 (DDE) 系统连接到 Excel 电子表格。

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


指定给定文档已通过动态数据交换 (DDE) 系统连接到文本文件。

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeDataTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int mailMergeDataType) {#getName-int-}
```
public static String getName(int mailMergeDataType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeDataType | int |  |

**退货：**
java.lang.字符串
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
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




**退货：**
java.lang.字符串
### toString(int mailMergeDataType) {#toString-int-}
```
public static String toString(int mailMergeDataType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeDataType | int |  |

**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

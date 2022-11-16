---
title: XmlReadMode
second_title: Aspose.Words for Java API 参考
description: 指定如何将 XML 数据和关系模式读入 .
type: docs
weight: 37
url: /zh/java/com.aspose.words.net.system.data/xmlreadmode/
---

**遗产：**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

指定如何将 XML 数据和关系模式读入[DataSet](../../com.aspose.words.net.system.data/dataset).
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 默认。 |
| [DIFF_GRAM](#DIFF-GRAM) | 读取 DiffGram，将 DiffGram 中的更改应用到[DataSet](../../com.aspose.words.net.system.data/dataset)并保存[DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow\#getRowState--)价值观。 |
| [FRAGMENT](#FRAGMENT) | 针对 SQL Server 实例读取 XML 片段，例如通过执行 FOR XML 查询生成的片段。 |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | 忽略任何内联模式并将数据读入现有的[DataSet](../../com.aspose.words.net.system.data/dataset)模式。 |
| [INFER_SCHEMA](#INFER-SCHEMA) | 忽略任何内联模式，从数据中推断模式并加载数据。 |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | 忽略任何内联模式，从数据中推断出强类型模式，然后加载数据。 |
| [READ_SCHEMA](#READ-SCHEMA) | 读取任何内联模式并加载数据。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String-) |  |
| [compareTo(E arg0)](#compareTo-E-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDeclaringClass()](#getDeclaringClass--) |  |
| [hashCode()](#hashCode--) |  |
| [name()](#name--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [ordinal()](#ordinal--) |  |
| [toString()](#toString--) |  |
| [valueOf(String name)](#valueOf-java.lang.String-) |  |
| [values()](#values--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


默认。

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


读取 DiffGram，将 DiffGram 中的更改应用到[DataSet](../../com.aspose.words.net.system.data/dataset)并保存[DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow\#getRowState--)价值观。

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


针对 SQL Server 实例读取 XML 片段，例如通过执行 FOR XML 查询生成的片段。什么时候[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)设置为片段，默认命名空间被读取为内联模式。

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


忽略任何内联模式并将数据读入现有的[DataSet](../../com.aspose.words.net.system.data/dataset)模式。如果任何数据与现有模式不匹配，则将其丢弃（包括来自为[DataSet](../../com.aspose.words.net.system.data/dataset)）。如果数据是 DiffGram，则 IgnoreSchema 具有与 DiffGram 相同的功能。

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


忽略任何内联模式，从数据中推断模式并加载数据。如果[DataSet](../../com.aspose.words.net.system.data/dataset)已经包含架构，当前架构通过添加新表或向现有表添加列来扩展。如果推断表已存在但具有不同的命名空间，或者任何推断列与现有列冲突，则会引发异常。

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


忽略任何内联模式，从数据中推断出强类型模式，然后加载数据。如果无法从数据中推断出类型，则将其解释为字符串数据。如果[DataSet](../../com.aspose.words.net.system.data/dataset)已经包含一个模式，则通过添加新表或向现有表添加列来扩展当前模式。如果推断表已存在但具有不同的命名空间，或者任何推断列与现有列冲突，则会引发异常。

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


读取任何内联模式并加载数据。如果[DataSet](../../com.aspose.words.net.system.data/dataset)已经包含模式，可以将新表添加到模式中，但是如果内联模式中的任何表已经存在于[DataSet](../../com.aspose.words.net.system.data/dataset).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String-}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**退货：**
吨
### compareTo(E arg0) {#compareTo-E-}
```
public final int compareTo(E arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | E |  |

**退货：**
整数
### equals(Object arg0) {#equals-java.lang.Object-}
```
public final boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDeclaringClass() {#getDeclaringClass--}
```
public final Class<E> getDeclaringClass()
```




**退货：**
java.lang.类<E>
### hashCode() {#hashCode--}
```
public final int hashCode()
```




**退货：**
整数
### name() {#name--}
```
public final String name()
```




**退货：**
java.lang.字符串
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### ordinal() {#ordinal--}
```
public final int ordinal()
```




**退货：**
整数
### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### valueOf(String name) {#valueOf-java.lang.String-}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |

**退货：**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)
### values() {#values--}
```
public static System.Data.XmlReadMode[] values()
```




**退货：**
com.aspose.words.net.System.Data.XmlReadMode[]
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

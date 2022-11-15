---
title: IDataRecord
second_title: Aspose.Words for Java API 参考
description: 为 DataReader 提供对每一行中列值的访问，并由访问关系数据库的 .NET Framework 数据提供程序实现。
type: docs
weight: 35
url: /zh/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

为 DataReader 提供对每一行中列值的访问，并由访问关系数据库的 .NET Framework 数据提供程序实现。
## 方法

| 方法 | 描述 |
| --- | --- |
| [get(int i)](#get-int-) | 获取位于指定索引处的列。 |
| [getFieldCount()](#getFieldCount--) | 获取当前行中的列数。 |
| [getFieldType(int i)](#getFieldType-int-) | 获取与将从中返回的 java.lang.Object 类型对应的 java.lang.Class 信息[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-). |
| [getName(int i)](#getName-int-) | 获取要查找的字段的名称。 |
| [getValue(int i)](#getValue-int-) | 返回指定字段的值。 |
### get(int i) {#get-int-}
```
public abstract Object get(int i)
```


获取位于指定索引处的列。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| i | int | 要获取的列的从零开始的索引。 |

**退货：**
java.lang.Object - 位于指定索引处的列作为 java.lang.Object。
### getFieldCount() {#getFieldCount--}
```
public abstract int getFieldCount()
```


获取当前行中的列数。

**退货：**
int - 当未定位在有效记录集中时，为 0；否则，当前记录中的列数。默认值为 -1。
### getFieldType(int i) {#getFieldType-int-}
```
public abstract Class getFieldType(int i)
```


获取与将从中返回的 java.lang.Object 类型对应的 java.lang.Class 信息[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| i | int | 要查找的字段的索引。 |

**退货：**
 java.lang.Class - 对应于将从中返回的 java.lang.Object 类型的 java.lang.Class 信息[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-).
### getName(int i) {#getName-int-}
```
public abstract String getName(int i)
```


获取要查找的字段的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| i | int | 要查找的字段的索引。 |

**退货：**
java.lang.String - 字段名称或空字符串 ("")，如果没有要返回的值。
### getValue(int i) {#getValue-int-}
```
public abstract Object getValue(int i)
```


返回指定字段的值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| i | int | 要查找的字段的索引。 |

**退货：**
java.lang.Object - 返回时将包含字段值的 java.lang.Object。
---
title: OdsoFieldMapData
second_title: Aspose.Words for Java API 参考
description: 指定如何将外部数据源中的列映射到文档中的预定义合并字段。
type: docs
weight: 413
url: /zh/java/com.aspose.words/odsofieldmapdata/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

指定如何将外部数据源中的列映射到文档中的预定义合并字段。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

 Microsoft Word 提供了一些预定义的合并字段名称，它允许将其作为 MERGEFIELD 插入到文档中，或者在 ADDRESSBLOCK 或 GREETINGLINE 字段中使用。中指定的信息[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata)允许将外部数据源中的一列映射到单个预定义的合并字段。
## 方法

| 方法 | 描述 |
| --- | --- |
| [deepClone()](#deepClone--) | 返回此对象的深层克隆。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColumn()](#getColumn--) | 指定外部数据源中列的从零开始的索引，该索引应映射到特定 MERGEFIELD 字段的本地名称。 |
| [getMappedName()](#getMappedName--) | 指定预定义的合并字段名称，该名称应映射到由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)此字段映射中的属性。 |
| [getName()](#getName--) | 指定外部数据源中的列名，该列的索引由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)财产。 |
| [getType()](#getType--) | 指定给定的邮件合并字段是否已映射到给定外部数据源中的列。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColumn(int value)](#setColumn-int-) | 指定外部数据源中列的从零开始的索引，该索引应映射到特定 MERGEFIELD 字段的本地名称。 |
| [setMappedName(String value)](#setMappedName-java.lang.String-) | 指定预定义的合并字段名称，该名称应映射到由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)此字段映射中的属性。 |
| [setName(String value)](#setName-java.lang.String-) | 指定外部数据源中的列名，该列的索引由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)财产。 |
| [setType(int value)](#setType-int-) | 指定给定的邮件合并字段是否已映射到给定外部数据源中的列。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public OdsoFieldMapData deepClone()
```


返回此对象的深层克隆。

**退货:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata)
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getColumn() {#getColumn--}
```
public int getColumn()
```


指定外部数据源中列的从零开始的索引，该索引应映射到特定 MERGEFIELD 字段的本地名称。默认值为 0。

**退货:**
int - 对应的 int 值。
### getMappedName() {#getMappedName--}
```
public String getMappedName()
```


指定预定义的合并字段名称，该名称应映射到由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)此字段映射中的属性。默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getName() {#getName--}
```
public String getName()
```


指定外部数据源中的列名，该列的索引由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)财产。默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getType() {#getType--}
```
public int getType()
```


指定给定的邮件合并字段是否已映射到给定外部数据源中的列。默认值为[OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype\#DEFAULT).

**退货:**
int - 对应的 int 值。返回值是以下之一[OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype)常数。
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




### setColumn(int value) {#setColumn-int-}
```
public void setColumn(int value)
```


指定外部数据源中列的从零开始的索引，该索引应映射到特定 MERGEFIELD 字段的本地名称。默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setMappedName(String value) {#setMappedName-java.lang.String-}
```
public void setMappedName(String value)
```


指定预定义的合并字段名称，该名称应映射到由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)此字段映射中的属性。默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


指定外部数据源中的列名，该列的索引由[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-)财产。默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setType(int value) {#setType-int-}
```
public void setType(int value)
```


指定给定的邮件合并字段是否已映射到给定外部数据源中的列。默认值为[OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype\#DEFAULT).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype)常数。 |

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

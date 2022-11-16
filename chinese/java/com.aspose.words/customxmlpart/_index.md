---
title: CustomXmlPart
second_title: Aspose.Words for Java API 参考
description: 表示包内的自定义 XML 数据存储部件自定义 XML 数据。
type: docs
weight: 104
url: /zh/java/com.aspose.words/customxmlpart/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class CustomXmlPart implements Cloneable
```

表示自定义 XML 数据存储部件（包内的自定义 XML 数据）。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

一份 DOCX 或 DOC 文档可以包含一个或多个自定义 XML 数据存储部分。 Aspose.Words 保留并允许通过以下方式创建和提取自定义 XML 数据[Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-)收藏。
## 方法

| 方法 | 描述 |
| --- | --- |
| [deepClone()](#deepClone--) | 制作对象的“足够深”的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getData()](#getData--) | 获取此自定义 XML 数据存储部件的 XML 内容。 |
| [getDataChecksum()](#getDataChecksum--) | 指定循环冗余校验 (CRC) 校验和[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---)内容。 |
| [getId()](#getId--) | 获取在 OOXML 文档中标识此自定义 XML 部分的字符串。 |
| [getSchemas()](#getSchemas--) | 指定与此自定义 XML 部分关联的 XML 架构集。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setData(byte[] value)](#setData-byte---) | 设置此自定义 XML 数据存储部件的 XML 内容。 |
| [setId(String value)](#setId-java.lang.String-) | 设置在 OOXML 文档中标识此自定义 XML 部分的字符串。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public CustomXmlPart deepClone()
```


制作对象的“足够深”的副本。不重复的字节[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---)价值。

**退货：**
[CustomXmlPart](../../com.aspose.words/customxmlpart)
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getData() {#getData--}
```
public byte[] getData()
```


获取此自定义 XML 数据存储部件的 XML 内容。

默认值为空字节数组。该值不能为 null 。

**退货：**
字节[- 此自定义 XML 数据存储部分的 XML 内容。
### getDataChecksum() {#getDataChecksum--}
```
public long getDataChecksum()
```


指定循环冗余校验 (CRC) 校验和[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---)内容。

**退货：**
long - 相应的 long 值。
### getId() {#getId--}
```
public String getId()
```


获取在 OOXML 文档中标识此自定义 XML 部分的字符串。

ISO/IEC 29500 指定此值是一个 GUID，但旧版本的 Microsoft Word 允许此处为任何字符串。 Aspose.Words 对 ECMA-376 格式做同样的事情。但请注意，Microsoft Word Online 无法打开使用非 GUID 值创建的文档。因此，GUID 是此属性的首选值。

有效值必须是在本文档中所有自定义 XML 数据部分中唯一的标识符。

默认值为空字符串。该值不能为 null 。

**退货：**
java.lang.String - 在 OOXML 文档中标识此自定义 XML 部分的字符串。
### getSchemas() {#getSchemas--}
```
public CustomXmlSchemaCollection getSchemas()
```


指定与此自定义 XML 部分关联的 XML 架构集。

**退货：**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection) - 相应的[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection)价值。
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




### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


设置此自定义 XML 数据存储部件的 XML 内容。

默认值为空字节数组。该值不能为 null 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 此自定义 XML 数据存储部件的 XML 内容。 |

### setId(String value) {#setId-java.lang.String-}
```
public void setId(String value)
```


设置在 OOXML 文档中标识此自定义 XML 部分的字符串。

ISO/IEC 29500 指定此值是一个 GUID，但旧版本的 Microsoft Word 允许此处为任何字符串。 Aspose.Words 对 ECMA-376 格式做同样的事情。但请注意，Microsoft Word Online 无法打开使用非 GUID 值创建的文档。因此，GUID 是此属性的首选值。

有效值必须是在本文档中所有自定义 XML 数据部分中唯一的标识符。

默认值为空字符串。该值不能为 null 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 在 OOXML 文档中标识此自定义 XML 部分的字符串。 |

### toString() {#toString--}
```
public String toString()
```




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

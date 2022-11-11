---
title: PdfCustomPropertiesExport
second_title: Aspose.Words for Java API 参考
description:指定导出为 PDF 文件的方式。
type: docs
weight: 450
url: /zh/java/com.aspose.words/pdfcustompropertiesexport/
---

**遗产:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

指定方式[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。
## 字段

| 字段 | 描述 |
| --- | --- |
| [METADATA](#METADATA) | 自定义属性是元数据。 |
| [NONE](#NONE) | 不导出自定义属性。 |
| [STANDARD](#STANDARD) | 自定义属性导出为 /Info 字典中的条目。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


自定义属性是元数据。

XMP 数据包中导出属性的命名空间是“custprops”。每个属性都有一个关联的 xml 元素“custprops:Property1”、“custprops:Property2”等等。属性元素中有“rdf:描述”元素。 description 元素有两个元素“custprops:Name”，包含自定义属性的名称作为此 xml 元素的值，以及“custprops:Value”，包含自定义属性的值作为此 xml 元素的值。

### NONE {#NONE}
```
public static int NONE
```


不导出自定义属性。

### STANDARD {#STANDARD}
```
public static int STANDARD
```


自定义属性导出为 /Info 字典中的条目。

不导出具有以下名称的自定义属性：“Title”、“Author”、“Subject”、“Keywords”、“Creator”、“Producer”、“CreationDate”、“ModDate”、“Trapped”。

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
### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int pdfCustomPropertiesExport) {#getName-int-}
```
public static String getName(int pdfCustomPropertiesExport)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

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
### toString(int pdfCustomPropertiesExport) {#toString-int-}
```
public static String toString(int pdfCustomPropertiesExport)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

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

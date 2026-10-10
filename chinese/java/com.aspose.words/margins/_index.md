---
title: "页边距"
linktitle: "页边距"
second_title: "Aspose.Words for Java"
description: "在 Java 中指定预设页边距。"
type: docs
weight: 449
url: /zh/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

指定预设页边距。

 **Examples:** 

显示何时重新计算文档的页面布局。

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [CUSTOM](#CUSTOM) | 自定义页边距。 |
| [MIRRORED](#MIRRORED) | 镜像页边距。 |
| [MODERATE](#MODERATE) | 适中页边距。 |
| [NARROW](#NARROW) | 窄页边距。 |
| [NORMAL](#NORMAL) | 普通页边距。 |
| [WIDE](#WIDE) | 宽页边距。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


自定义页边距。

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


镜像页边距。

 **Remarks:** 

将页边距设置为镜像将为 [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int) 属性设置适当的值。这将影响整个文档，而不仅仅是当前节。

### MODERATE {#MODERATE}
```
public static int MODERATE
```


适中页边距。

### NARROW {#NARROW}
```
public static int NARROW
```


窄页边距。

### NORMAL {#NORMAL}
```
public static int NORMAL
```


普通页边距。

### WIDE {#WIDE}
```
public static int WIDE
```


宽页边距。

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 边距 | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 边距 | int |  |

**Returns:**
java.lang.String

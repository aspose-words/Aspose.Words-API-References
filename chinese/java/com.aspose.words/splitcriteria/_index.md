---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words for Java"
description: "指定文档在 Java 中如何拆分为多个部分。"
type: docs
weight: 629
url: /zh/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

指定文档如何拆分为多个部分。

 **Examples:** 

展示如何按页拆分文档。

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [PAGE](#PAGE) | 指定文档被拆分为页面。 |
| [SECTION_BREAK](#SECTION-BREAK) | 指定文档在任何类型的分节符处拆分为多个部分。 |
| [STYLE](#STYLE) | 指定文档在使用由 [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\\#setSplitStyle-java.lang.String) 指定的样式格式化的段落处拆分为多个部分。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


指定文档被拆分为页面。

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


指定文档在任何类型的分节符处拆分为多个部分。

### STYLE {#STYLE}
```
public static int STYLE
```


指定文档在使用由 [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\\#setSplitStyle-java.lang.String) 指定的样式格式化的段落处拆分为多个部分。

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int splitCriteria) {#toString-int}
```
public static String toString(int splitCriteria)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String

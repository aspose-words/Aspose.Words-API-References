---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words for Java"
description: "指定 Java 文档的字符间距调整。"
type: docs
weight: 411
url: /zh/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

指定文档的字符间距调整。默认值为 Expand。

 **Examples:** 

展示如何管理字符间距控制。

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [COMPRESS](#COMPRESS) | 压缩字符间距。 |
| [COMPRESS_KANA](#COMPRESS-KANA) | 压缩，使用假名音节表（平假名和片假名）的规则。 |
| [EXPAND](#EXPAND) | 不要压缩字符间距。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


压缩字符间距。

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


压缩，使用假名音节表（平假名和片假名）的规则。

### EXPAND {#EXPAND}
```
public static int EXPAND
```


不要压缩字符间距。

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String

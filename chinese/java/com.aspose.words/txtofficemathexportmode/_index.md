---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words for Java"
description: "指定 Aspose.Words 在 Java 中如何将 OfficeMath 导出为 SaveFormat.TEXT。"
type: docs
weight: 694
url: /zh/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

指定 Aspose.Words 如何将 OfficeMath 导出为[SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT)。

 **Examples:** 

展示如何在 TXT 中将 OfficeMath 对象导出为 LaTeX。

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [LATEX](#LATEX) | 将 OfficeMath 导出为 LaTeX。 |
| [TEXT](#TEXT) | 将 OfficeMath 导出为纯文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


将 OfficeMath 导出为 LaTeX。

### TEXT {#TEXT}
```
public static int TEXT
```


将 OfficeMath 导出为纯文本。

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtOfficeMathExportMode) {#toString-int}
```
public static String toString(int txtOfficeMathExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String

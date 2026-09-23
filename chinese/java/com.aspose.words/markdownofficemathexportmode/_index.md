---
title: "MarkdownOfficeMathExportMode"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words for Java"
description: "指定 Aspose.Words 在 Java 中如何将 OfficeMath 导出为 Markdown。"
type: docs
weight: 455
url: /zh/java/com.aspose.words/markdownofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownOfficeMathExportMode
```

指定 Aspose.Words 如何将 OfficeMath 导出为 Markdown。

 **Examples:** 

展示 OfficeMath 将如何写入文档。

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.IMAGE);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
 
```

展示如何将 OfficeMath 对象导出为 LaTeX。

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
 
```

展示如何将 OfficeMath 对象导出为 MarkItDown。

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setOfficeMathExportMode(MarkdownOfficeMathExportMode.MARK_IT_DOWN);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [IMAGE](#IMAGE) | 将 OfficeMath 导出为图像。 |
| [LATEX](#LATEX) | 将 OfficeMath 导出为 LaTeX。 |
| [MARK_IT_DOWN](#MARK-IT-DOWN) | 将 OfficeMath 导出为兼容 MarkItDown 的 LaTeX。 |
| [MATH_ML](#MATH-ML) | 将 OfficeMath 导出为 MathML。 |
| [TEXT](#TEXT) | 将 OfficeMath 导出为纯文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String markdownOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownOfficeMathExportMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


将 OfficeMath 导出为图像。

### LATEX {#LATEX}
```
public static int LATEX
```


将 OfficeMath 导出为 LaTeX。

### MARK_IT_DOWN {#MARK-IT-DOWN}
```
public static int MARK_IT_DOWN
```


将 OfficeMath 导出为兼容 MarkItDown 的 LaTeX。

 **Remarks:** 

请参阅 https://github.com/microsoft/markitdown 获取有关 MarkItDown 的详细信息。

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


将 OfficeMath 导出为 MathML。

### TEXT {#TEXT}
```
public static int TEXT
```


将 OfficeMath 导出为纯文本。

### length {#length}
```
public static int length
```


### fromName(String markdownOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownOfficeMathExportModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownOfficeMathExportMode) {#getName-int}
```
public static String getName(int markdownOfficeMathExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownOfficeMathExportMode) {#toString-int}
```
public static String toString(int markdownOfficeMathExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownOfficeMathExportMode | int |  |

**Returns:**
java.lang.String

---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words for Java"
description: "允许在 Java 中指定要导出为 Markdown 的元素为原始 HTML。"
type: docs
weight: 451
url: /zh/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

允许指定要导出为 Markdown 的元素为原始 HTML。

 **Examples:** 

展示如何将表格导出为 Markdown 的原始 HTML。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

展示如何将无法在纯 Markdown 中正确表示的表格导出为原始 HTML。

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [NONE](#NONE) | 使用 Markdown 语法导出所有元素，不包含任何原始 HTML。 |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | 将无法在纯 Markdown 中正确表示的表格导出为原始 HTML。 |
| [TABLES](#TABLES) | 将表格导出为原始 HTML。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String markdownExportAsHtmlName)](#fromName-java.lang.String) |  |
| [fromNames(Set markdownExportAsHtmlNames)](#fromNames-java.util.Set) |  |
| [getName(int markdownExportAsHtml)](#getName-int) |  |
| [getNames(int markdownExportAsHtml)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownExportAsHtml)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


使用 Markdown 语法导出所有元素，不包含任何原始 HTML。

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


将无法在纯 Markdown 中正确表示的表格导出为原始 HTML。

 **Remarks:** 

启用此选项后，Aspose.Words 将仅将具有合并单元格或嵌套表格的表格导出为原始 HTML。所有其他表格将以 Markdown 格式导出。另外请注意，此选项不会保留表格的全部格式，仅保留单元格的相应跨距。

如果已设置相关的 [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) 标志，则此标志将被忽略。

### TABLES {#TABLES}
```
public static int TABLES
```


将表格导出为原始 HTML。

 **Remarks:** 

启用此选项后，所有表格都将导出为原始 HTML。Aspose.Words 将尝试在此情况下保留表格的全部格式。

如果设置了此标志，则相关的 [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) 标志将被忽略。

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownExportAsHtml) {#toString-int}
```
public static String toString(int markdownExportAsHtml)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String

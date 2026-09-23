---
title: "MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中列表如何导出为 Markdown。"
type: docs
weight: 453
url: /zh/java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

指定列表如何导出为 Markdown。

 **Examples:** 

显示列表项将如何写入 Markdown 文档。

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | 导出兼容 Markdown 语法的列表项。 |
| [PLAIN_TEXT](#PLAIN-TEXT) | 将列表项导出为纯文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


导出兼容 Markdown 语法的列表项。

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


将列表项导出为纯文本。

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownListExportMode) {#toString-int}
```
public static String toString(int markdownListExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String

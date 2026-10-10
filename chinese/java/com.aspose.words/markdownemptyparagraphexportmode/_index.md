---
title: "MarkdownEmptyParagraphExportMode"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words for Java"
description: "指定 Aspose.Words 在 Java 中如何将空段落导出为 Markdown。"
type: docs
weight: 450
url: /zh/java/com.aspose.words/markdownemptyparagraphexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownEmptyParagraphExportMode
```

指定 Aspose.Words 如何将空段落导出为 Markdown。

 **Examples:** 

展示如何导出空段落。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("First");
 builder.writeln("\r\n\r\n\r\n");
 builder.writeln("Last");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setEmptyParagraphExportMode(exportMode);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

 String result = FileUtils.readFileToString( new File(getArtifactsDir() + "MarkdownSaveOptions.EmptyParagraphExportMode.md"), StandardCharsets.UTF_8);

 switch (exportMode)
 {
     case MarkdownEmptyParagraphExportMode.NONE:
         Assert.assertEquals("\ufeffFirst\r\n\r\nLast\r\n", result);
         break;
     case MarkdownEmptyParagraphExportMode.EMPTY_LINE:
         Assert.assertEquals("\ufeffFirst\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
         break;
     case MarkdownEmptyParagraphExportMode.MARKDOWN_HARD_LINE_BREAK:
         Assert.assertEquals("\ufeffFirst\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n
\r\n", result);
         break;
 }
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [EMPTY_LINE](#EMPTY-LINE) | 导出为空行。 |
| [MARKDOWN_HARD_LINE_BREAK](#MARKDOWN-HARD-LINE-BREAK) | 导出为 Markdown 硬换行符 '\\\\'。 |
| [NONE](#NONE) | 不要导出空段落。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String markdownEmptyParagraphExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownEmptyParagraphExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownEmptyParagraphExportMode)](#toString-int) |  |
### EMPTY_LINE {#EMPTY-LINE}
```
public static int EMPTY_LINE
```


导出为空行。

 **Remarks:** 

注意，空行在 Markdown 中没有意义，加载时会丢失。

### MARKDOWN_HARD_LINE_BREAK {#MARKDOWN-HARD-LINE-BREAK}
```
public static int MARKDOWN_HARD_LINE_BREAK
```


导出为 Markdown 硬换行符 '\\\\'。

### NONE {#NONE}
```
public static int NONE
```


不要导出空段落。

### length {#length}
```
public static int length
```


### fromName(String markdownEmptyParagraphExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownEmptyParagraphExportModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownEmptyParagraphExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownEmptyParagraphExportMode) {#getName-int}
```
public static String getName(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownEmptyParagraphExportMode) {#toString-int}
```
public static String toString(int markdownEmptyParagraphExportMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| markdownEmptyParagraphExportMode | int |  |

**Returns:**
java.lang.String

---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中合并多个文档时格式如何合并。"
type: docs
weight: 464
url: /zh/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

指定在合并多个文档时格式如何合并。

 **Examples:** 

展示如何将文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | 表示源文档将保留其原始格式，例如字体样式、大小、颜色、缩进以及应用于其内容的任何其他格式元素。 |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | 在最终文档中保留原始文档的布局。 |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | 合并已合并文档的格式。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


表示源文档将保留其原始格式，例如字体样式、大小、颜色、缩进以及应用于其内容的任何其他格式元素。

 **Remarks:** 

使用此选项，可确保复制的内容与原始来源中的显示方式相同，而不受合并队列中第一份文档的格式设置影响。

当输入和输出格式均为 PDF 时，此选项不会产生任何影响。

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


在最终文档中保留原始文档的布局。

 **Remarks:** 

一般来说，这看起来像是您打印出原始文档，然后使用胶水手动将它们粘合在一起。

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


合并已合并文档的格式。

 **Remarks:** 

使用此选项时，Aspose.Words 会将第一份文档的格式调整为匹配第二份文档的结构和外观，但仍保留部分原始格式不变。此选项在您希望保持目标文档的整体外观和感觉，同时仍保留原始文档的某些格式方面时非常有用。

当输入和输出格式均为 PDF 时，此选项不会产生任何影响。

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String

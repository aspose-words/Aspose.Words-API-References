---
title: MarkdownExportAsHtml
linktitle: MarkdownExportAsHtml
second_title: Aspose.Words for Java
description: Allows to specify the elements to be exported to Markdown as raw HTML in Java.
type: docs
weight: 445
url: /java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Allows to specify the elements to be exported to Markdown as raw HTML.

 **Examples:** 

Shows how to export a table to Markdown as raw HTML.

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
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Export all elements using Markdown syntax without any raw HTML. |
| [TABLES](#TABLES) | Export tables as raw HTML. |
| [length](#length) |  |
## Methods

| Method | Description |
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


Export all elements using Markdown syntax without any raw HTML.

### TABLES {#TABLES}
```
public static int TABLES
```


Export tables as raw HTML.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String

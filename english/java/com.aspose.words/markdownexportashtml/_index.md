---
title: MarkdownExportAsHtml
linktitle: MarkdownExportAsHtml
second_title: Aspose.Words for Java
description: Allows to specify the elements to be exported to Markdown as raw HTML in Java.
type: docs
weight: 449
url: /java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Allows to specify the elements to be exported to Markdown as raw HTML.

 **Examples:** 

Shows how to export tables that cannot be correctly represented in pure Markdown as raw HTML.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```

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
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Export tables that cannot be correctly represented in pure Markdown as raw HTML. |
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

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Export tables that cannot be correctly represented in pure Markdown as raw HTML.

 **Remarks:** 

When this option is enabled, Aspose.Words will only export tables that have merged cells or nested tables as raw HTML. And all other tables will be exported in Markdown format. Also note, this option will not preserve all formatting of the table, but only preserves corresponding spans of the cells.

If related [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) flag is set, then this flag will be ignored.

### TABLES {#TABLES}
```
public static int TABLES
```


Export tables as raw HTML.

 **Remarks:** 

When this option is enabled, every table will be exported as raw HTML. Aspose.Words will try to preserve all formatting of the tables in this case.

If this flag is set, then related [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) flag will be ignored.

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

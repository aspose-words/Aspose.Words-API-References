---
title: MarkdownListExportMode
linktitle: MarkdownListExportMode
second_title: Aspose.Words for Java
description: Specifies how lists are exported into Markdown in Java.
type: docs
weight: 447
url: /java/com.aspose.words/markdownlistexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownListExportMode
```

Specifies how lists are exported into Markdown.

 **Examples:** 

Shows how to list items will be written to the markdown document.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [MARKDOWN_SYNTAX](#MARKDOWN-SYNTAX) | Export list items compatible with Markdown syntax. |
| [PLAIN_TEXT](#PLAIN-TEXT) | Export list items as plain text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String markdownListExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownListExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownListExportMode)](#toString-int) |  |
### MARKDOWN_SYNTAX {#MARKDOWN-SYNTAX}
```
public static int MARKDOWN_SYNTAX
```


Export list items compatible with Markdown syntax.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


Export list items as plain text.

### length {#length}
```
public static int length
```


### fromName(String markdownListExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownListExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownListExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownListExportMode) {#getName-int}
```
public static String getName(int markdownListExportMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| markdownListExportMode | int |  |

**Returns:**
java.lang.String

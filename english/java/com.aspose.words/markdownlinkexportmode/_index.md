---
title: MarkdownLinkExportMode
linktitle: MarkdownLinkExportMode
second_title: Aspose.Words for Java
description: Specifies how links are exported into Markdown in Java.
type: docs
weight: 427
url: /java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Specifies how links are exported into Markdown.

 **Examples:** 

Shows how to links will be written to the .md file.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Automatically detect export mode for each link. |
| [INLINE](#INLINE) | Export all links as inline blocks. |
| [REFERENCE](#REFERENCE) | Export all links as reference blocks. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Automatically detect export mode for each link.

### INLINE {#INLINE}
```
public static int INLINE
```


Export all links as inline blocks.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Export all links as reference blocks.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownLinkExportMode) {#toString-int}
```
public static String toString(int markdownLinkExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String

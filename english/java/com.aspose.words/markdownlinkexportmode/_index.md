---
title: MarkdownLinkExportMode
linktitle: MarkdownLinkExportMode
second_title: Aspose.Words for Java
description: The mode of exporting links to a target document in Java.
type: docs
weight: 413
url: /java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

The mode of exporting links to a target document.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | A link is exported as a reference block if it has roundtrip information or is mentioned more than once in a document. |
| [INLINE](#INLINE) | Links are exported as inline blocks. |
| [REFERENCE](#REFERENCE) | Links are exported as reference blocks. |
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


A link is exported as a reference block if it has roundtrip information or is mentioned more than once in a document. In all other cases a link is exported as an inline block.

### INLINE {#INLINE}
```
public static int INLINE
```


Links are exported as inline blocks.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Links are exported as reference blocks.

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

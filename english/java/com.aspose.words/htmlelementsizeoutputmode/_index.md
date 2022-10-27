---
title: HtmlElementSizeOutputMode
second_title: Aspose.Words for Java API Reference
description: Specifies how Aspose.Words exports element widths and heights to HTML MHTML and EPUB.
type: docs
weight: 324
url: /java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.
## Fields

| Field | Description |
| --- | --- |
| [ALL](#ALL) | All element sizes, both in absolute and relative units, specified in the document are exported. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Element sizes are exported only if they are specified in relative units in the document. |
| [NONE](#NONE) | Element sizes are not exported. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int htmlElementSizeOutputMode)](#getName-int-) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int-) |  |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### ALL {#ALL}
```
public static int ALL
```


All element sizes, both in absolute and relative units, specified in the document are exported.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Element sizes are exported only if they are specified in relative units in the document. Fixed sizes are not exported in this mode. Visual agents will calculate missing sizes to make document layout more natural.

### NONE {#NONE}
```
public static int NONE
```


Element sizes are not exported. Visual agents will build layout automatically according to relationship between elements.

### length {#length}
```
public static int length
```


### getName(int htmlElementSizeOutputMode) {#getName-int-}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
### toString(int htmlElementSizeOutputMode) {#toString-int-}
```
public static String toString(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

---
title: CssStyleSheetType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 97
url: /java/com.aspose.words/cssstylesheettype/
---

**Inheritance:**
java.lang.Object
```
public class CssStyleSheetType
```

A utility class providing constants. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML.
## Fields

| Field | Description |
| --- | --- |
| [INLINE](#INLINE) | CSS styles are written inline (as a value of the **style** attribute on every element). |
| [EMBEDDED](#EMBEDDED) | CSS styles are written separately from the content in a style sheet embedded in the HTML file. |
| [EXTERNAL](#EXTERNAL) | CSS styles are written separately from the content in a style sheet in an external file. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int cssStyleSheetType)](#getName-int-) |  |
| [toString(int cssStyleSheetType)](#toString-int-) |  |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


CSS styles are written inline (as a value of the **style** attribute on every element).

### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


CSS styles are written separately from the content in a style sheet embedded in the HTML file.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


CSS styles are written separately from the content in a style sheet in an external file. The HTML file links the style sheet.

### length {#length}
```
public static int length
```


### getName(int cssStyleSheetType) {#getName-int-}
```
public static String getName(int cssStyleSheetType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
### toString(int cssStyleSheetType) {#toString-int-}
```
public static String toString(int cssStyleSheetType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

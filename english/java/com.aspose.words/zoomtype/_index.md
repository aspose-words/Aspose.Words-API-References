---
title: ZoomType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 631
url: /java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

A utility class providing constants. Possible values for how large or small the document appears on the screen in Microsoft Word.
## Fields

| Field | Description |
| --- | --- |
| [CUSTOM](#CUSTOM) | Zoom percentage is set explicitly. |
| [NONE](#NONE) | Indicates to use the explicit zoom percentage. |
| [FULL_PAGE](#FULL-PAGE) | Zoom percentage is automatically recalculated to fit one full page. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Zoom percentage is automatically recalculated to fit page width. |
| [TEXT_FIT](#TEXT-FIT) | Zoom percentage is automatically recalculated to fit text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int zoomType)](#getName-int-) |  |
| [toString(int zoomType)](#toString-int-) |  |
| [fromName(String zoomTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Zoom percentage is set explicitly. It is not recalculated automatically when control size changes.

### NONE {#NONE}
```
public static int NONE
```


Indicates to use the explicit zoom percentage. Same as [CUSTOM](../../com.aspose.words/zoomtype\#CUSTOM).

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Zoom percentage is automatically recalculated to fit one full page.

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Zoom percentage is automatically recalculated to fit page width.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Zoom percentage is automatically recalculated to fit text.

### length {#length}
```
public static int length
```


### getName(int zoomType) {#getName-int-}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### toString(int zoomType) {#toString-int-}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### fromName(String zoomTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

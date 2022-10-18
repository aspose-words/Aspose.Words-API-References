---
title: ImlRenderingMode
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 345
url: /java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

A utility class providing constants. Specifies how ink (InkML) objects are rendered to fixed page formats.
## Fields

| Field | Description |
| --- | --- |
| [FALLBACK](#FALLBACK) | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int imlRenderingMode)](#getName-int-) |  |
| [toString(int imlRenderingMode)](#toString-int-) |  |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. Please note that after saving a document to a fixed page format with fall-back rendering mode, InkML objects in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if ImlRenderingMode is set to InkML.

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode.

### length {#length}
```
public static int length
```


### getName(int imlRenderingMode) {#getName-int-}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### toString(int imlRenderingMode) {#toString-int-}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### fromName(String imlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

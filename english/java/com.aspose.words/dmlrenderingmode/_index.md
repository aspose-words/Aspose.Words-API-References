---
title: DmlRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how DrawingML shapes are rendered to fixed page formats.
type: docs
weight: 118
url: /java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Specifies how DrawingML shapes are rendered to fixed page formats.
## Fields

| Field | Description |
| --- | --- |
| [FALLBACK](#FALLBACK) | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int dmlRenderingMode)](#getName-int-) |  |
| [toString(int dmlRenderingMode)](#toString-int-) |  |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. Please note that after saving a document to a fixed page format with fall-back DML rendering mode, DML shapes in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if DmlRenderingMode is set to DrawingML.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode.

### length {#length}
```
public static int length
```


### getName(int dmlRenderingMode) {#getName-int-}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### toString(int dmlRenderingMode) {#toString-int-}
```
public static String toString(int dmlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### fromName(String dmlRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

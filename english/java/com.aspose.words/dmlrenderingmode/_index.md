---
title: DmlRenderingMode
linktitle: DmlRenderingMode
second_title: Aspose.Words for Java
description: Specifies how DrawingML shapes are rendered to fixed page formats in Java.
type: docs
weight: 129
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
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. |
| [FALLBACK](#FALLBACK) | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML.

 **Remarks:** 

Please note that after saving a document to a fixed page format with fall-back DML rendering mode, DML shapes in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) is set to [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlRenderingMode) {#toString-int}
```
public static String toString(int dmlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String

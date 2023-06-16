---
title: MetafileRenderingMode
linktitle: MetafileRenderingMode
second_title: Aspose.Words for Java
description: Specifies how Aspose.Words should render WMF and EMF metafiles in Java.
type: docs
weight: 415
url: /java/com.aspose.words/metafilerenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingMode
```

Specifies how Aspose.Words should render WMF and EMF metafiles.
## Fields

| Field | Description |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document. |
| [VECTOR](#VECTOR) | Aspose.Words renders a metafile as vector graphics. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words tries to render a metafile as vector graphics. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words renders a metafile as vector graphics.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words tries to render a metafile as vector graphics. If Aspose.Words cannot correctly render some of the metafile records to vector graphics then Aspose.Words renders this metafile to a bitmap.

### length {#length}
```
public static int length
```


### fromName(String metafileRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int metafileRenderingMode) {#getName-int}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int metafileRenderingMode) {#toString-int}
```
public static String toString(int metafileRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String

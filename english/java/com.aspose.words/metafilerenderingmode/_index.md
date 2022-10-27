---
title: MetafileRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how Aspose.Words should render WMF and EMF metafiles.
type: docs
weight: 396
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
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words tries to render a metafile as vector graphics. |
| [VECTOR](#VECTOR) | Aspose.Words renders a metafile as vector graphics. |
| [BITMAP](#BITMAP) | Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int metafileRenderingMode)](#getName-int-) |  |
| [toString(int metafileRenderingMode)](#toString-int-) |  |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words tries to render a metafile as vector graphics. If Aspose.Words cannot correctly render some of the metafile records to vector graphics then Aspose.Words renders this metafile to a bitmap.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words renders a metafile as vector graphics.

### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document.

### length {#length}
```
public static int length
```


### getName(int metafileRenderingMode) {#getName-int-}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
### toString(int metafileRenderingMode) {#toString-int-}
```
public static String toString(int metafileRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
### fromName(String metafileRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

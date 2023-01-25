---
title: MetafileRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how Aspose.Words should render WMF and EMF metafiles.
type: docs
weight: 400
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |


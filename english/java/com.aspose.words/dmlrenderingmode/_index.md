---
title: DmlRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how DrawingML shapes are rendered to fixed page formats.
type: docs
weight: 119
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. Please note that after saving a document to a fixed page format with fall-back DML rendering mode, DML shapes in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) is set to [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode\#DRAWING-ML).

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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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


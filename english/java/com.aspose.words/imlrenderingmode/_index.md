---
title: ImlRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how ink InkML objects are rendered to fixed page formats.
type: docs
weight: 347
url: /java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Specifies how ink (InkML) objects are rendered to fixed page formats.
## Fields

| Field | Description |
| --- | --- |
| [FALLBACK](#FALLBACK) | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. Please note that after saving a document to a fixed page format with fall-back rendering mode, InkML objects in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if [ImlRenderingMode](../../com.aspose.words/imlrenderingmode) is set to [INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode.

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
### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingMode | int |  |

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
### toString(int imlRenderingMode) {#toString-int}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imlRenderingMode | int |  |

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


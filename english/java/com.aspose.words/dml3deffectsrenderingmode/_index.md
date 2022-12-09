---
title: Dml3DEffectsRenderingMode
second_title: Aspose.Words for Java API Reference
description: Specifies how 3D shape effects are rendered.
type: docs
weight: 117
url: /java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Specifies how 3D shape effects are rendered.
## Fields

| Field | Description |
| --- | --- |
| [ADVANCED](#ADVANCED) | Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. |
| [BASIC](#BASIC) | A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. The current implementation uses OpenGL. Please make sure that OpenGL library version 1.1 or higher is installed on your system before use. This mode is still under development, and some things may not be supported, so it's recommended to use the [BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC) mode if the rendering result is not acceptable. Please see documentation for details.

### BASIC {#BASIC}
```
public static int BASIC
```


A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. Please see documentation for details.

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
### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

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
### toString(int dml3DEffectsRenderingMode) {#toString-int}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

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


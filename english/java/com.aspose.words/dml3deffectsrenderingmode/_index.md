---
title: Dml3DEffectsRenderingMode
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 116
url: /java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

A utility class providing constants. Specifies how 3D shape effects are rendered.
## Fields

| Field | Description |
| --- | --- |
| [BASIC](#BASIC) | A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. |
| [ADVANCED](#ADVANCED) | Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int dml3DEffectsRenderingMode)](#getName-int-) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int-) |  |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### BASIC {#BASIC}
```
public static int BASIC
```


A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. Please see documentation for details.

### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. The current implementation uses OpenGL. Please make sure that OpenGL library version 1.1 or higher is installed on your system before use. This mode is still under development, and some things may not be supported, so it's recommended to use the [BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC) mode if the rendering result is not acceptable. Please see documentation for details.

### length {#length}
```
public static int length
```


### getName(int dml3DEffectsRenderingMode) {#getName-int-}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### toString(int dml3DEffectsRenderingMode) {#toString-int-}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

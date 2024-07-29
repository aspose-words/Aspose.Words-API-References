---
title: Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words for Java
description: Specifies how 3D shape effects are rendered in Java.
type: docs
weight: 144
url: /java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Specifies how 3D shape effects are rendered.

 **Examples:** 

Shows how 3D effects are rendered.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [ADVANCED](#ADVANCED) | Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. |
| [BASIC](#BASIC) | A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials.

 **Remarks:** 

The current implementation uses OpenGL. Please make sure that OpenGL library version 1.1 or higher is installed on your system before use. This mode is still under development, and some things may not be supported, so it's recommended to use the [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC) mode if the rendering result is not acceptable. Please see documentation for details.

### BASIC {#BASIC}
```
public static int BASIC
```


A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. Please see documentation for details.

### length {#length}
```
public static int length
```


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

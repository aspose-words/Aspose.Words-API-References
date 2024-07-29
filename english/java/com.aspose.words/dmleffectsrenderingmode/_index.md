---
title: DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
second_title: Aspose.Words for Java
description: Specifies how DrawingML effects are rendered to fixed page formats in Java.
type: docs
weight: 145
url: /java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

Specifies how DrawingML effects are rendered to fixed page formats.

 **Examples:** 

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [FINE](#FINE) | DrawingML effects are rendered in fine mode which involves advanced processing. |
| [NONE](#NONE) | No DrawingML effects are rendered. |
| [SIMPLIFIED](#SIMPLIFIED) | Rendering of DrawingML effects are simplified. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED) mode.

### NONE {#NONE}
```
public static int NONE
```


No DrawingML effects are rendered.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


Rendering of DrawingML effects are simplified.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlEffectsRenderingMode) {#toString-int}
```
public static String toString(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String

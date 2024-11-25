---
title: ImlRenderingMode
linktitle: ImlRenderingMode
second_title: Aspose.Words for Java
description: Specifies how ink InkML objects are rendered to fixed page formats in Java.
type: docs
weight: 386
url: /java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Specifies how ink (InkML) objects are rendered to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [FALLBACK](#FALLBACK) | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML.

 **Remarks:** 

Please note that after saving a document to a fixed page format with fall-back rendering mode, InkML objects in the AW document model are permanently replaced with their fall-back counterparts. As a result, saving the same document again will always use fall-back shapes, even if [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) is set to [INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode.

### length {#length}
```
public static int length
```


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

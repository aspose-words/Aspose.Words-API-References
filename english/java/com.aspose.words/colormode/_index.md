---
title: ColorMode
linktitle: ColorMode
second_title: Aspose.Words for Java
description: Specifies how colors are rendered in Java.
type: docs
weight: 91
url: /java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Specifies how colors are rendered.

 **Examples:** 

Shows how to change image color with saving options property.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Rendering with colors in a range of gray shades from white to black. |
| [NORMAL](#NORMAL) | Rendering with unmodified colors. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Rendering with colors in a range of gray shades from white to black.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Rendering with unmodified colors.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorMode) {#toString-int}
```
public static String toString(int colorMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String

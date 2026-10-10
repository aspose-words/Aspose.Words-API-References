---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Farben in Java gerendert werden."
type: docs
weight: 105
url: /de/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Gibt an, wie Farben gerendert werden.

 **Examples:** 

Zeigt, wie die Bildfarbe mit der Eigenschaft saving options geändert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Rendern mit Farben in einer Reihe von Graustufen von Weiß bis Schwarz. |
| [NORMAL](#NORMAL) | Rendern mit unveränderten Farben. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Rendern mit Farben in einer Reihe von Graustufen von Weiß bis Schwarz.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Rendern mit unveränderten Farben.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String

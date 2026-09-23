---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les couleurs sont rendues en Java."
type: docs
weight: 105
url: /fr/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Spécifie comment les couleurs sont rendues.

 **Examples:** 

Montre comment changer la couleur de l'image avec la propriété des options d'enregistrement.

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
## Champs

| Champ | Description |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Rendu avec des couleurs dans une gamme de nuances de gris du blanc au noir. |
| [NORMAL](#NORMAL) | Rendu avec des couleurs non modifiées. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Rendu avec des couleurs dans une gamme de nuances de gris du blanc au noir.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Rendu avec des couleurs non modifiées.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String

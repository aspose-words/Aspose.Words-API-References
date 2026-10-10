---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se renderizan los colores en Java."
type: docs
weight: 105
url: /es/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Especifica cómo se renderizan los colores.

 **Examples:** 

Muestra cómo cambiar el color de la imagen con la propiedad de opciones de guardado.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Renderizado con colores en una gama de tonos de gris desde blanco hasta negro. |
| [NORMAL](#NORMAL) | Renderizado con colores sin modificar. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Renderizado con colores en una gama de tonos de gris desde blanco hasta negro.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Renderizado con colores sin modificar.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String

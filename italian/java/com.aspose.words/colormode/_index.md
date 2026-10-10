---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words per Java"
description: "Specifica come i colori vengono renderizzati in Java."
type: docs
weight: 105
url: /it/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Specifica come vengono renderizzati i colori.

 **Examples:** 

Mostra come modificare il colore dell'immagine con la proprietà delle opzioni di salvataggio.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Rendering con colori in una gamma di tonalità di grigio dal bianco al nero. |
| [NORMAL](#NORMAL) | Rendering con colori non modificati. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Rendering con colori in una gamma di tonalità di grigio dal bianco al nero.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Rendering con colori non modificati.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String

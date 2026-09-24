---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de zoom aplicado a un documento PDF cuando se abre en un visor PDF en Java."
type: docs
weight: 544
url: /es/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Especifica el tipo de zoom aplicado a un documento PDF cuando se abre en un visor PDF.

 **Examples:** 

Muestra cómo establecer el zoom predeterminado que un lector aplica al abrir un documento PDF renderizado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
 // apply a percentage-based zoom factor when we open the document with it.
 // Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
 PdfSaveOptions options = new PdfSaveOptions();
 {
     options.setZoomBehavior(PdfZoomBehavior.ZOOM_FACTOR);
     options.setZoomFactor(25);
 }

 // When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
 doc.save(getArtifactsDir() + "PdfSaveOptions.ZoomBehaviour.pdf", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Ajusta el cuadro delimitador (rectángulo que contiene todos los elementos visibles en la página). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Ajusta la altura de la página. |
| [FIT_PAGE](#FIT-PAGE) | Muestra la página para que sea visible completamente. |
| [FIT_WIDTH](#FIT-WIDTH) | Ajusta el ancho de la página. |
| [NONE](#NONE) | Cómo se muestra el documento queda a cargo del visor PDF. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Muestra la página usando el factor de zoom especificado. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Ajusta el cuadro delimitador (rectángulo que contiene todos los elementos visibles en la página).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Ajusta la altura de la página.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Muestra la página para que sea visible completamente.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Ajusta el ancho de la página.

### NONE {#NONE}
```
public static int NONE
```


Cómo se muestra el documento queda a cargo del visor PDF. Normalmente el visor muestra el documento para ajustarse al ancho de la página.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Muestra la página usando el factor de zoom especificado.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfZoomBehavior) {#toString-int}
```
public static String toString(int pdfZoomBehavior)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String

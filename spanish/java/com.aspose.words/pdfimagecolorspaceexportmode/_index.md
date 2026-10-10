---
title: "PdfImageColorSpaceExportMode"
linktitle: "PdfImageColorSpaceExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se seleccionará el espacio de color para las imágenes en un documento PDF en Java."
type: docs
weight: 536
url: /es/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.

 **Examples:** 

Muestra cómo establecer un espacio de color diferente para las imágenes en un documento al exportarlo a PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jpeg image:");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertParagraph();
 builder.writeln("Png image:");
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
 // automatically select the color space for images in the document that it converts to PDF.
 // In most cases, the color space will be RGB.
 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
 // to use the CMYK color space for all images in the saved PDF.
 // Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
 pdfSaveOptions.setImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words selecciona automáticamente el espacio de color más apropiado para cada imagen. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words convierte imágenes RGB al espacio de color CMYK usando una fórmula simple. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words selecciona automáticamente el espacio de color más apropiado para cada imagen.

 **Remarks:** 

La mayoría de las imágenes se guardan en el espacio de color RGB. También pueden usarse los espacios de color Indexado y Escala de grises. El espacio de color CMYK nunca se usa.

Para algunas imágenes, el espacio de color puede ser diferente en distintas plataformas.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words convierte imágenes RGB al espacio de color CMYK usando una fórmula simple.

 **Remarks:** 

Las imágenes en espacio de color RGB se convierten a CMYK usando la fórmula: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). Los valores RGB se normalizan; están entre 0 y 1.0.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageColorSpaceExportMode) {#toString-int}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String

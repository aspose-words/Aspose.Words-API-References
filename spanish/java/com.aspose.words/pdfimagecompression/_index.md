---
title: "PdfImageCompression"
linktitle: "PdfImageCompression"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de compresión aplicado a las imágenes en el archivo PDF en Java."
type: docs
weight: 537
url: /es/java/com.aspose.words/pdfimagecompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageCompression
```

Especifica el tipo de compresión aplicado a las imágenes en el archivo PDF.

 **Examples:** 

Muestra cómo especificar un tipo de compresión para todas las imágenes en un documento que estamos convirtiendo a PDF.

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

 // Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
 // "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
 // Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
 // "ImageCompression" property to control the quality of all images that end up in the output PDF.
 pdfSaveOptions.setImageCompression(pdfImageCompression);

 // Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
 pdfSaveOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Selecciona automáticamente la compresión más adecuada para cada imagen. |
| [JPEG](#JPEG) | Compresión JPEG. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfImageCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageCompression)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Selecciona automáticamente la compresión más adecuada para cada imagen.

### JPEG {#JPEG}
```
public static int JPEG
```


Compresión JPEG. No admite transparencia.

### length {#length}
```
public static int length
```


### fromName(String pdfImageCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageCompressionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageCompression) {#getName-int}
```
public static String getName(int pdfImageCompression)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageCompression) {#toString-int}
```
public static String toString(int pdfImageCompression)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String

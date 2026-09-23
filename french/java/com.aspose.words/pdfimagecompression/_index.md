---
title: "PdfImageCompression"
linktitle: "PdfImageCompression"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de compression appliqué aux images du fichier PDF en Java."
type: docs
weight: 537
url: /fr/java/com.aspose.words/pdfimagecompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageCompression
```

Spécifie le type de compression appliqué aux images dans le fichier PDF.

 **Examples:** 

Montre comment spécifier un type de compression pour toutes les images d'un document que nous convertissons en PDF.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Sélectionne automatiquement la compression la plus appropriée pour chaque image. |
| [JPEG](#JPEG) | Compression JPEG. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfImageCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageCompression)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Sélectionne automatiquement la compression la plus appropriée pour chaque image.

### JPEG {#JPEG}
```
public static int JPEG
```


Compression JPEG. Ne prend pas en charge la transparence.

### length {#length}
```
public static int length
```


### fromName(String pdfImageCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageCompressionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfImageCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageCompression) {#getName-int}
```
public static String getName(int pdfImageCompression)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String

---
title: PdfImageCompression
linktitle: PdfImageCompression
second_title: Aspose.Words for Java
description: Specifies the type of compression applied to images in the PDF file in Java.
type: docs
weight: 495
url: /java/com.aspose.words/pdfimagecompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageCompression
```

Specifies the type of compression applied to images in the PDF file.

 **Examples:** 

Shows how to specify a compression type for all images in a document that we are converting to PDF.

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
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Automatically selects the most appropriate compression for each image. |
| [JPEG](#JPEG) | Jpeg compression. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfImageCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageCompression)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Automatically selects the most appropriate compression for each image.

### JPEG {#JPEG}
```
public static int JPEG
```


Jpeg compression. Does not support transparency.

### length {#length}
```
public static int length
```


### fromName(String pdfImageCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageCompressionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageCompression) {#getName-int}
```
public static String getName(int pdfImageCompression)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String

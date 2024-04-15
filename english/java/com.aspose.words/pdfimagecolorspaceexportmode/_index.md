---
title: PdfImageColorSpaceExportMode
linktitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words for Java
description: Specifies how the color space will be selected for the images in PDF document in Java.
type: docs
weight: 489
url: /java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Specifies how the color space will be selected for the images in PDF document.

 **Examples:** 

Shows how to set a different color space for images in a document as we export it to PDF.

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
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words automatically selects the most appropriate color space for each image. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words coverts RGB images to CMYK color space using simple formula. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words automatically selects the most appropriate color space for each image.

 **Remarks:** 

Most of the images are saved in RGB color space. Also Indexed and Grayscale color spaces may be used. CMYK color space is never used.

For some images the color space may be different on different platforms.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words coverts RGB images to CMYK color space using simple formula.

 **Remarks:** 

Images in RGB color space are converted to CMYK using formula: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). RGB values are normalized - they are between 0 and 1.0.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String

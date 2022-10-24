---
title: PdfImageColorSpaceExportMode
second_title: Aspose.Words for Java API Reference
description: Specifies how the color space will be selected for the images in PDF document.
type: docs
weight: 456
url: /java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Specifies how the color space will be selected for the images in PDF document.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words automatically selects the most appropriate color space for each image. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words coverts RGB images to CMYK color space using simple formula. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int-) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int-) |  |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words automatically selects the most appropriate color space for each image.

Most of the images are saved in RGB color space. Also Indexed and Grayscale color spaces may be used. CMYK color space is never used.

For some images the color space may be different on different platforms.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words coverts RGB images to CMYK color space using simple formula.

Images in RGB color space are converted to CMYK using formula: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). RGB values are normalized - they are between 0 and 1.0.

### length {#length}
```
public static int length
```


### getName(int pdfImageColorSpaceExportMode) {#getName-int-}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### toString(int pdfImageColorSpaceExportMode) {#toString-int-}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

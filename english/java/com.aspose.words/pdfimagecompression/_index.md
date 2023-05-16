---
title: PdfImageCompression
linktitle: PdfImageCompression
second_title: Aspose.Words for Java
description: Specifies the type of compression applied to images in the PDF file in Java.
type: docs
weight: 474
url: /java/com.aspose.words/pdfimagecompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageCompression
```

Specifies the type of compression applied to images in the PDF file.
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

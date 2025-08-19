---
title: TiffCompression
linktitle: TiffCompression
second_title: Aspose.Words for Java
description: Specifies what type of compression to apply when saving page images into a TIFF file in Java.
type: docs
weight: 681
url: /java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Specifies what type of compression to apply when saving page images into a TIFF file.

 **Examples:** 

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Tagged Image File Format.tiff");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 // Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
 // which may result in a very large output file.
 // Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
 // Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
 options.setTiffCompression(tiffCompression);

 doc.save(getArtifactsDir() + "ImageSaveOptions.TiffImageCompression.tiff", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [CCITT_3](#CCITT-3) | Specifies the CCITT3 compression scheme. |
| [CCITT_4](#CCITT-4) | Specifies the CCITT4 compression scheme. |
| [LZW](#LZW) | Specifies the LZW compression scheme. |
| [NONE](#NONE) | Specifies no compression. |
| [RLE](#RLE) | Specifies the RLE compression scheme. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Specifies the CCITT3 compression scheme.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Specifies the CCITT4 compression scheme.

### LZW {#LZW}
```
public static int LZW
```


Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression.

### NONE {#NONE}
```
public static int NONE
```


Specifies no compression.

### RLE {#RLE}
```
public static int RLE
```


Specifies the RLE compression scheme.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tiffCompression) {#toString-int}
```
public static String toString(int tiffCompression)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

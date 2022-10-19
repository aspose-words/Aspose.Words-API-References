---
title: TiffCompression
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 579
url: /java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

A utility class providing constants. Specifies what type of compression to apply when saving page images into a TIFF file.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Specifies no compression. |
| [RLE](#RLE) | Specifies the RLE compression scheme. |
| [LZW](#LZW) | Specifies the LZW compression scheme. |
| [CCITT_3](#CCITT-3) | Specifies the CCITT3 compression scheme. |
| [CCITT_4](#CCITT-4) | Specifies the CCITT4 compression scheme. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int tiffCompression)](#getName-int-) |  |
| [toString(int tiffCompression)](#toString-int-) |  |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
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

### LZW {#LZW}
```
public static int LZW
```


Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression.

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

### length {#length}
```
public static int length
```


### getName(int tiffCompression) {#getName-int-}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String
### toString(int tiffCompression) {#toString-int-}
```
public static String toString(int tiffCompression)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String
### fromName(String tiffCompressionName) {#fromName-java.lang.String-}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

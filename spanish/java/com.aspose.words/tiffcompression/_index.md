---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words para Java"
description: "Especifica qué tipo de compresión aplicar al guardar imágenes de página en un archivo TIFF en Java."
type: docs
weight: 688
url: /es/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Especifica qué tipo de compresión aplicar al guardar imágenes de página en un archivo TIFF.

 **Examples:** 

Muestra cómo seleccionar el esquema de compresión a aplicar a un documento que convertimos en una imagen TIFF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CCITT_3](#CCITT-3) | Especifica el esquema de compresión CCITT3. |
| [CCITT_4](#CCITT-4) | Especifica el esquema de compresión CCITT4. |
| [LZW](#LZW) | Especifica el esquema de compresión LZW. |
| [NONE](#NONE) | Especifica que no hay compresión. |
| [RLE](#RLE) | Especifica el esquema de compresión RLE. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Especifica el esquema de compresión CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Especifica el esquema de compresión CCITT4.

### LZW {#LZW}
```
public static int LZW
```


Especifica el esquema de compresión LZW. En Java se emula mediante compresión Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


Especifica que no hay compresión.

### RLE {#RLE}
```
public static int RLE
```


Especifica el esquema de compresión RLE.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words per Java"
description: "Specifica quale tipo di compressione applicare durante il salvataggio delle immagini delle pagine in un file TIFF in Java."
type: docs
weight: 688
url: /it/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Specifica quale tipo di compressione applicare quando si salvano le immagini delle pagine in un file TIFF.

 **Examples:** 

Mostra come selezionare lo schema di compressione da applicare a un documento che convertiamo in un'immagine TIFF.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CCITT_3](#CCITT-3) | Specifica lo schema di compressione CCITT3. |
| [CCITT_4](#CCITT-4) | Specifica lo schema di compressione CCITT4. |
| [LZW](#LZW) | Specifica lo schema di compressione LZW. |
| [NONE](#NONE) | Specifica nessuna compressione. |
| [RLE](#RLE) | Specifica lo schema di compressione RLE. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Specifica lo schema di compressione CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Specifica lo schema di compressione CCITT4.

### LZW {#LZW}
```
public static int LZW
```


Specifica lo schema di compressione LZW. In Java è emulato dalla compressione Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


Specifica nessuna compressione.

### RLE {#RLE}
```
public static int RLE
```


Specifica lo schema di compressione RLE.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

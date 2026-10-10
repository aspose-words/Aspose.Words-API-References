---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de compression à appliquer lors de l'enregistrement des images de page dans un fichier TIFF en Java."
type: docs
weight: 688
url: /fr/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Spécifie le type de compression à appliquer lors de l’enregistrement des images de pages dans un fichier TIFF.

 **Examples:** 

Montre comment sélectionner le schéma de compression à appliquer à un document que nous convertissons en image TIFF.

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
## Champs

| Champ | Description |
| --- | --- |
| [CCITT_3](#CCITT-3) | Spécifie le schéma de compression CCITT3. |
| [CCITT_4](#CCITT-4) | Spécifie le schéma de compression CCITT4. |
| [LZW](#LZW) | Spécifie le schéma de compression LZW. |
| [NONE](#NONE) | Spécifie aucune compression. |
| [RLE](#RLE) | Spécifie le schéma de compression RLE. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Spécifie le schéma de compression CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Spécifie le schéma de compression CCITT4.

### LZW {#LZW}
```
public static int LZW
```


Spécifie le schéma de compression LZW. En Java, il est émulé par la compression Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


Spécifie aucune compression.

### RLE {#RLE}
```
public static int RLE
```


Spécifie le schéma de compression RLE.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

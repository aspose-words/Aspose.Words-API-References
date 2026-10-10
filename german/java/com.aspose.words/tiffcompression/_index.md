---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words für Java"
description: "Gibt an, welchen Kompressionstyp beim Speichern von Seitenbildern in einer TIFF-Datei in Java angewendet werden soll."
type: docs
weight: 688
url: /de/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Gibt an, welche Art von Kompression beim Speichern von Seitenbildern in einer TIFF-Datei angewendet werden soll.

 **Examples:** 

Zeigt, wie das anzuwendende Kompressionsschema für ein Dokument ausgewählt wird, das wir in ein TIFF-Bild konvertieren.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CCITT_3](#CCITT-3) | Gibt das CCITT3-Kompressionsschema an. |
| [CCITT_4](#CCITT-4) | Gibt das CCITT4-Kompressionsschema an. |
| [LZW](#LZW) | Gibt das LZW-Kompressionsschema an. |
| [NONE](#NONE) | Gibt keine Kompression an. |
| [RLE](#RLE) | Gibt das RLE-Kompressionsverfahren an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Gibt das CCITT3-Kompressionsschema an.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Gibt das CCITT4-Kompressionsschema an.

### LZW {#LZW}
```
public static int LZW
```


Gibt das LZW-Kompressionsverfahren an. In Java wird es durch Deflate (Zip)-Kompression emuliert.

### NONE {#NONE}
```
public static int NONE
```


Gibt keine Kompression an.

### RLE {#RLE}
```
public static int RLE
```


Gibt das RLE-Kompressionsverfahren an.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa görüntülerini bir TIFF dosyasına kaydederken uygulanacak sıkıştırma türünü belirtir."
type: docs
weight: 688
url: /tr/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Sayfa görüntülerini bir TIFF dosyasına kaydederken uygulanacak sıkıştırma türünü belirtir.

 **Examples:** 

Bir belgeyi TIFF görüntüsüne dönüştürürken uygulanacak sıkıştırma şemasını nasıl seçeceğimizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CCITT_3](#CCITT-3) | CCITT3 sıkıştırma şemasını belirtir. |
| [CCITT_4](#CCITT-4) | CCITT4 sıkıştırma şemasını belirtir. |
| [LZW](#LZW) | LZW sıkıştırma şemasını belirtir. |
| [NONE](#NONE) | Sıkıştırma olmadığını belirtir. |
| [RLE](#RLE) | RLE sıkıştırma şemasını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


CCITT3 sıkıştırma şemasını belirtir.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


CCITT4 sıkıştırma şemasını belirtir.

### LZW {#LZW}
```
public static int LZW
```


LZW sıkıştırma şemasını belirtir. Java'da Deflate (Zip) sıkıştırmasıyla taklit edilir.

### NONE {#NONE}
```
public static int NONE
```


Sıkıştırma olmadığını belirtir.

### RLE {#RLE}
```
public static int RLE
```


RLE sıkıştırma şemasını belirtir.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

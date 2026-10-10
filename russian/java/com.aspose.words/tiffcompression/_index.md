---
title: "TiffCompression"
linktitle: "TiffCompression"
second_title: "Aspose.Words для Java"
description: "Указывает тип сжатия, применяемый при сохранении изображений страниц в файл TIFF в Java."
type: docs
weight: 688
url: /ru/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

Указывает тип сжатия, применяемый при сохранении изображений страниц в файл TIFF.

 **Examples:** 

Показывает, как выбрать схему сжатия, применяемую к документу, который мы преобразуем в изображение TIFF.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CCITT_3](#CCITT-3) | Указывает схему сжатия CCITT3. |
| [CCITT_4](#CCITT-4) | Указывает схему сжатия CCITT4. |
| [LZW](#LZW) | Указывает схему сжатия LZW. |
| [NONE](#NONE) | Указывает отсутствие сжатия. |
| [RLE](#RLE) | Указывает схему сжатия RLE. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Указывает схему сжатия CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Указывает схему сжатия CCITT4.

### LZW {#LZW}
```
public static int LZW
```


Указывает схему сжатия LZW. В Java эмулируется сжатием Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


Указывает отсутствие сжатия.

### RLE {#RLE}
```
public static int RLE
```


Указывает схему сжатия RLE.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

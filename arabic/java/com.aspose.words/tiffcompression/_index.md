---
title: "ضغط Tiff"
linktitle: "ضغط Tiff"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع الضغط الذي يتم تطبيقه عند حفظ صور الصفحات في ملف TIFF في Java."
type: docs
weight: 688
url: /ar/java/com.aspose.words/tiffcompression/
---

**Inheritance:**
java.lang.Object
```
public class TiffCompression
```

يحدد نوع الضغط الذي يُطبق عند حفظ صور الصفحات في ملف TIFF.

 **Examples:** 

يظهر كيفية اختيار مخطط الضغط لتطبيقه على مستند نقوم بتحويله إلى صورة TIFF.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CCITT_3](#CCITT-3) | يحدد مخطط الضغط CCITT3. |
| [CCITT_4](#CCITT-4) | يحدد مخطط الضغط CCITT4. |
| [LZW](#LZW) | يحدد مخطط الضغط LZW. |
| [NONE](#NONE) | يحدد عدم وجود ضغط. |
| [RLE](#RLE) | يحدد مخطط ضغط RLE. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String) |  |
| [getName(int tiffCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tiffCompression)](#toString-int) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


يحدد مخطط الضغط CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


يحدد مخطط الضغط CCITT4.

### LZW {#LZW}
```
public static int LZW
```


يحدد مخطط ضغط LZW. في Java يتم محاكاته بواسطة ضغط Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


يحدد عدم وجود ضغط.

### RLE {#RLE}
```
public static int RLE
```


يحدد مخطط ضغط RLE.

### length {#length}
```
public static int length
```


### fromName(String tiffCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String tiffCompressionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int tiffCompression) {#getName-int}
```
public static String getName(int tiffCompression)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| tiffCompression | int |  |

**Returns:**
java.lang.String

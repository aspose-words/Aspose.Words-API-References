---
title: "ImagePixelFormat"
linktitle: "ImagePixelFormat"
second_title: "Aspose.Words Java için"
description: "Java'da belge sayfalarının oluşturulan görüntüleri için piksel biçimini belirtir."
type: docs
weight: 393
url: /tr/java/com.aspose.words/imagepixelformat/
---

**Inheritance:**
java.lang.Object
```
public class ImagePixelFormat
```

Belge sayfalarının oluşturulan görüntüleri için piksel biçimini belirtir.

 **Examples:** 

Bir belgeyi görüntüye render etmek için bit-per-piksel oranının nasıl seçileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 21000);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a pixel format for the image that the saving operation will generate.
 // Various bit per pixel rates will affect the quality and file size of the generated image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPixelFormat(imagePixelFormat);

 // We can clone ImageSaveOptions instances.
 Assert.assertNotEquals(imageSaveOptions, imageSaveOptions.deepClone());

 doc.save(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FORMAT_16_BPP_ARGB_1555](#FORMAT-16-BPP-ARGB-1555) | 16 bit piksel başına, ARGB. |
| [FORMAT_16_BPP_RGB_555](#FORMAT-16-BPP-RGB-555) | 16 bit piksel başına, RGB. |
| [FORMAT_16_BPP_RGB_565](#FORMAT-16-BPP-RGB-565) | 16 bit piksel başına, RGB. |
| [FORMAT_1_BPP_INDEXED](#FORMAT-1-BPP-INDEXED) | 1 bit piksel başına, Indexed. |
| [FORMAT_24_BPP_RGB](#FORMAT-24-BPP-RGB) | 24 bit piksel başına, RGB. |
| [FORMAT_32_BPP_ARGB](#FORMAT-32-BPP-ARGB) | 32 bit piksel başına, ARGB. |
| [FORMAT_32_BPP_P_ARGB](#FORMAT-32-BPP-P-ARGB) | 32 bit piksel başına, ARGB, önceden çarpılmış alfa. |
| [FORMAT_32_BPP_RGB](#FORMAT-32-BPP-RGB) | 32 bit piksel başına, RGB. |
| [FORMAT_48_BPP_RGB](#FORMAT-48-BPP-RGB) | 48 bit piksel başına, RGB. |
| [FORMAT_64_BPP_ARGB](#FORMAT-64-BPP-ARGB) | 64 bit piksel başına, ARGB. |
| [FORMAT_64_BPP_P_ARGB](#FORMAT-64-BPP-P-ARGB) | 64 bit piksel başına, ARGB, önceden çarpılmış alfa. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String imagePixelFormatName)](#fromName-java.lang.String) |  |
| [getName(int imagePixelFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imagePixelFormat)](#toString-int) |  |
### FORMAT_16_BPP_ARGB_1555 {#FORMAT-16-BPP-ARGB-1555}
```
public static int FORMAT_16_BPP_ARGB_1555
```


16 bit piksel başına, ARGB.

### FORMAT_16_BPP_RGB_555 {#FORMAT-16-BPP-RGB-555}
```
public static int FORMAT_16_BPP_RGB_555
```


16 bit piksel başına, RGB.

### FORMAT_16_BPP_RGB_565 {#FORMAT-16-BPP-RGB-565}
```
public static int FORMAT_16_BPP_RGB_565
```


16 bit piksel başına, RGB.

### FORMAT_1_BPP_INDEXED {#FORMAT-1-BPP-INDEXED}
```
public static int FORMAT_1_BPP_INDEXED
```


1 bit piksel başına, Indexed.

### FORMAT_24_BPP_RGB {#FORMAT-24-BPP-RGB}
```
public static int FORMAT_24_BPP_RGB
```


24 bit piksel başına, RGB.

### FORMAT_32_BPP_ARGB {#FORMAT-32-BPP-ARGB}
```
public static int FORMAT_32_BPP_ARGB
```


32 bit piksel başına, ARGB.

### FORMAT_32_BPP_P_ARGB {#FORMAT-32-BPP-P-ARGB}
```
public static int FORMAT_32_BPP_P_ARGB
```


32 bit piksel başına, ARGB, önceden çarpılmış alfa.

### FORMAT_32_BPP_RGB {#FORMAT-32-BPP-RGB}
```
public static int FORMAT_32_BPP_RGB
```


32 bit piksel başına, RGB.

### FORMAT_48_BPP_RGB {#FORMAT-48-BPP-RGB}
```
public static int FORMAT_48_BPP_RGB
```


48 bit piksel başına, RGB.

### FORMAT_64_BPP_ARGB {#FORMAT-64-BPP-ARGB}
```
public static int FORMAT_64_BPP_ARGB
```


64 bit piksel başına, ARGB.

### FORMAT_64_BPP_P_ARGB {#FORMAT-64-BPP-P-ARGB}
```
public static int FORMAT_64_BPP_P_ARGB
```


64 bit piksel başına, ARGB, önceden çarpılmış alfa.

### length {#length}
```
public static int length
```


### fromName(String imagePixelFormatName) {#fromName-java.lang.String}
```
public static int fromName(String imagePixelFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imagePixelFormatName | java.lang.String |  |

**Returns:**
int
### getName(int imagePixelFormat) {#getName-int}
```
public static String getName(int imagePixelFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imagePixelFormat) {#toString-int}
```
public static String toString(int imagePixelFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String

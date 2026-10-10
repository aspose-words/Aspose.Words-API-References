---
title: "ImagePixelFormat"
linktitle: "ImagePixelFormat"
second_title: "Aspose.Words لـ Java"
description: "يحدد تنسيق البكسل للصور المولدة لصفحات المستند في Java."
type: docs
weight: 393
url: /ar/java/com.aspose.words/imagepixelformat/
---

**Inheritance:**
java.lang.Object
```
public class ImagePixelFormat
```

يحدد تنسيق البكسل للصور المولدة لصفحات المستند.

 **Examples:** 

يوضح كيفية اختيار معدل البت لكل بكسل الذي يتم به تحويل المستند إلى صورة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FORMAT_16_BPP_ARGB_1555](#FORMAT-16-BPP-ARGB-1555) | 16 بت لكل بكسل، ARGB. |
| [FORMAT_16_BPP_RGB_555](#FORMAT-16-BPP-RGB-555) | 16 بت لكل بكسل، RGB. |
| [FORMAT_16_BPP_RGB_565](#FORMAT-16-BPP-RGB-565) | 16 بت لكل بكسل، RGB. |
| [FORMAT_1_BPP_INDEXED](#FORMAT-1-BPP-INDEXED) | 1 بت لكل بكسل، Indexed. |
| [FORMAT_24_BPP_RGB](#FORMAT-24-BPP-RGB) | 24 بت لكل بكسل، RGB. |
| [FORMAT_32_BPP_ARGB](#FORMAT-32-BPP-ARGB) | 32 بت لكل بكسل، ARGB. |
| [FORMAT_32_BPP_P_ARGB](#FORMAT-32-BPP-P-ARGB) | 32 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا. |
| [FORMAT_32_BPP_RGB](#FORMAT-32-BPP-RGB) | 32 بت لكل بكسل، RGB. |
| [FORMAT_48_BPP_RGB](#FORMAT-48-BPP-RGB) | 48 بت لكل بكسل، RGB. |
| [FORMAT_64_BPP_ARGB](#FORMAT-64-BPP-ARGB) | 64 بت لكل بكسل، ARGB. |
| [FORMAT_64_BPP_P_ARGB](#FORMAT-64-BPP-P-ARGB) | 64 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String imagePixelFormatName)](#fromName-java.lang.String) |  |
| [getName(int imagePixelFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imagePixelFormat)](#toString-int) |  |
### FORMAT_16_BPP_ARGB_1555 {#FORMAT-16-BPP-ARGB-1555}
```
public static int FORMAT_16_BPP_ARGB_1555
```


16 بت لكل بكسل، ARGB.

### FORMAT_16_BPP_RGB_555 {#FORMAT-16-BPP-RGB-555}
```
public static int FORMAT_16_BPP_RGB_555
```


16 بت لكل بكسل، RGB.

### FORMAT_16_BPP_RGB_565 {#FORMAT-16-BPP-RGB-565}
```
public static int FORMAT_16_BPP_RGB_565
```


16 بت لكل بكسل، RGB.

### FORMAT_1_BPP_INDEXED {#FORMAT-1-BPP-INDEXED}
```
public static int FORMAT_1_BPP_INDEXED
```


1 بت لكل بكسل، Indexed.

### FORMAT_24_BPP_RGB {#FORMAT-24-BPP-RGB}
```
public static int FORMAT_24_BPP_RGB
```


24 بت لكل بكسل، RGB.

### FORMAT_32_BPP_ARGB {#FORMAT-32-BPP-ARGB}
```
public static int FORMAT_32_BPP_ARGB
```


32 بت لكل بكسل، ARGB.

### FORMAT_32_BPP_P_ARGB {#FORMAT-32-BPP-P-ARGB}
```
public static int FORMAT_32_BPP_P_ARGB
```


32 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا.

### FORMAT_32_BPP_RGB {#FORMAT-32-BPP-RGB}
```
public static int FORMAT_32_BPP_RGB
```


32 بت لكل بكسل، RGB.

### FORMAT_48_BPP_RGB {#FORMAT-48-BPP-RGB}
```
public static int FORMAT_48_BPP_RGB
```


48 بت لكل بكسل، RGB.

### FORMAT_64_BPP_ARGB {#FORMAT-64-BPP-ARGB}
```
public static int FORMAT_64_BPP_ARGB
```


64 بت لكل بكسل، ARGB.

### FORMAT_64_BPP_P_ARGB {#FORMAT-64-BPP-P-ARGB}
```
public static int FORMAT_64_BPP_P_ARGB
```


64 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا.

### length {#length}
```
public static int length
```


### fromName(String imagePixelFormatName) {#fromName-java.lang.String}
```
public static int fromName(String imagePixelFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imagePixelFormatName | java.lang.String |  |

**Returns:**
int
### getName(int imagePixelFormat) {#getName-int}
```
public static String getName(int imagePixelFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String

---
title: "ImageBinarizationMethod"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words لـ Java"
description: "يحدد الطريقة المستخدمة لتحويل الصورة إلى ثنائية في Java."
type: docs
weight: 389
url: /ar/java/com.aspose.words/imagebinarizationmethod/
---

**Inheritance:**
java.lang.Object
```
public class ImageBinarizationMethod
```

يحدد الطريقة المستخدمة لتحويل الصورة إلى ثنائية.

 **Examples:** 

يوضح كيفية تعيين عتبة خطأ التحويل الثنائي لتنسيق TIFF عند استخدام طريقة Floyd‑Steinberg لتصيير صورة TIFF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FLOYD_STEINBERG_DITHERING](#FLOYD-STEINBERG-DITHERING) | يحدد التمويه باستخدام طريقة انتشار الخطأ Floyd‑Steinberg. |
| [THRESHOLD](#THRESHOLD) | يحدد طريقة العتبة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String imageBinarizationMethodName)](#fromName-java.lang.String) |  |
| [getName(int imageBinarizationMethod)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageBinarizationMethod)](#toString-int) |  |
### FLOYD_STEINBERG_DITHERING {#FLOYD-STEINBERG-DITHERING}
```
public static int FLOYD_STEINBERG_DITHERING
```


يحدد التمويه باستخدام طريقة انتشار الخطأ Floyd‑Steinberg.

### THRESHOLD {#THRESHOLD}
```
public static int THRESHOLD
```


يحدد طريقة العتبة.

### length {#length}
```
public static int length
```


### fromName(String imageBinarizationMethodName) {#fromName-java.lang.String}
```
public static int fromName(String imageBinarizationMethodName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBinarizationMethodName | java.lang.String |  |

**Returns:**
int
### getName(int imageBinarizationMethod) {#getName-int}
```
public static String getName(int imageBinarizationMethod)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imageBinarizationMethod) {#toString-int}
```
public static String toString(int imageBinarizationMethod)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String

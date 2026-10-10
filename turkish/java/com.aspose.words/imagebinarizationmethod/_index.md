---
title: "ImageBinarizationMethod"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words Java için"
description: "Java'da görüntüyü ikili hale getirmek için kullanılan yöntemi belirtir."
type: docs
weight: 389
url: /tr/java/com.aspose.words/imagebinarizationmethod/
---

**Inheritance:**
java.lang.Object
```
public class ImageBinarizationMethod
```

Görüntüyü ikili hale getirmek için kullanılan yöntemi belirtir.

 **Examples:** 

Floyd‑Steinberg yöntemi kullanılarak bir TIFF görüntüsü oluşturulurken TIFF ikilileştirme hata eşiğinin nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FLOYD_STEINBERG_DITHERING](#FLOYD-STEINBERG-DITHERING) | Floyd‑Steinberg hata yayılım yöntemi kullanılarak titreme (dithering) yapılmasını belirtir. |
| [THRESHOLD](#THRESHOLD) | Eşik yöntemini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String imageBinarizationMethodName)](#fromName-java.lang.String) |  |
| [getName(int imageBinarizationMethod)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageBinarizationMethod)](#toString-int) |  |
### FLOYD_STEINBERG_DITHERING {#FLOYD-STEINBERG-DITHERING}
```
public static int FLOYD_STEINBERG_DITHERING
```


Floyd‑Steinberg hata yayılım yöntemi kullanılarak titreme (dithering) yapılmasını belirtir.

### THRESHOLD {#THRESHOLD}
```
public static int THRESHOLD
```


Eşik yöntemini belirtir.

### length {#length}
```
public static int length
```


### fromName(String imageBinarizationMethodName) {#fromName-java.lang.String}
```
public static int fromName(String imageBinarizationMethodName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBinarizationMethodName | java.lang.String |  |

**Returns:**
int
### getName(int imageBinarizationMethod) {#getName-int}
```
public static String getName(int imageBinarizationMethod)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String

---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words Java için"
description: "Java'da belge sayfalarının oluşturulan görüntüleri için renk modunu belirtir."
type: docs
weight: 390
url: /tr/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Belge sayfalarının oluşturulan görüntüleri için renk modunu belirtir.

 **Examples:** 

Belgeleri işlerken renk modunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 20200);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a color mode for the image that the saving operation will generate.
 // If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
 // the saving operation will apply grayscale color reduction while rendering the document.
 // If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
 // the saving operation will render the document into a monochrome image.
 // If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
 // and preserve all the document's colors in the output image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setImageColorMode(imageColorMode);

 doc.save(getArtifactsDir() + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | Belgenin sayfaları siyah beyaz görüntüler olarak işlenecek. |
| [GRAYSCALE](#GRAYSCALE) | Belgenin sayfaları gri tonlamalı görüntüler olarak işlenecek. |
| [NONE](#NONE) | Belgenin sayfaları renkli görüntüler olarak işlenecek. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


Belgenin sayfaları siyah beyaz görüntüler olarak işlenecek.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Belgenin sayfaları gri tonlamalı görüntüler olarak işlenecek.

### NONE {#NONE}
```
public static int NONE
```


Belgenin sayfaları renkli görüntüler olarak işlenecek.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imageColorMode) {#toString-int}
```
public static String toString(int imageColorMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String

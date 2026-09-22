---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد وضع اللون للصور المولدة لصفحات المستند في جافا."
type: docs
weight: 390
url: /ar/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

يحدد وضع اللون للصور المولدة لصفحات المستند.

 **Examples:** 

يعرض كيفية تعيين وضع اللون عند عرض المستندات.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | ستُعرض صفحات المستند كصور بالأبيض والأسود. |
| [GRAYSCALE](#GRAYSCALE) | ستُعرض صفحات المستند كصور بتدرج الرمادي. |
| [NONE](#NONE) | ستُعرض صفحات المستند كصور ملونة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


ستُعرض صفحات المستند كصور بالأبيض والأسود.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


ستُعرض صفحات المستند كصور بتدرج الرمادي.

### NONE {#NONE}
```
public static int NONE
```


ستُعرض صفحات المستند كصور ملونة.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String

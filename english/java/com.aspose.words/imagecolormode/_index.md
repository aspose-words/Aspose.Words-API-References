---
title: ImageColorMode
linktitle: ImageColorMode
second_title: Aspose.Words for Java
description: Specifies the color mode for the generated images of document pages in Java.
type: docs
weight: 351
url: /java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Specifies the color mode for the generated images of document pages.

 **Examples:** 

Shows how to set a color mode when rendering documents.

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
## Fields

| Field | Description |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | The pages of the document will be rendered as black and white images. |
| [GRAYSCALE](#GRAYSCALE) | The pages of the document will be rendered as grayscale images. |
| [NONE](#NONE) | The pages of the document will be rendered as color images. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


The pages of the document will be rendered as black and white images.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


The pages of the document will be rendered as grayscale images.

### NONE {#NONE}
```
public static int NONE
```


The pages of the document will be rendered as color images.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String

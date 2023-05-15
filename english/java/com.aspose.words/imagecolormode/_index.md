---
title: ImageColorMode
linktitle: ImageColorMode
second_title: Aspose.Words for Java
description: Specifies the color mode for the generated images of document pages in Java.
type: docs
weight: 348
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

 switch (imageColorMode) {
     case ImageColorMode.NONE:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.ColorMode.png").length() < 156000);
         break;
     case ImageColorMode.GRAYSCALE:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.ColorMode.png").length() < 85000);
         break;
     case ImageColorMode.BLACK_AND_WHITE:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.ColorMode.png").length() <= 20000);
         break;
 }
 
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int imageColorMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |


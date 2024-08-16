---
title: ImageBinarizationMethod
linktitle: ImageBinarizationMethod
second_title: Aspose.Words for Java
description: Specifies the method used to binarize image in Java.
type: docs
weight: 368
url: /java/com.aspose.words/imagebinarizationmethod/
---

**Inheritance:**
java.lang.Object
```
public class ImageBinarizationMethod
```

Specifies the method used to binarize image.

 **Examples:** 

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

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
## Fields

| Field | Description |
| --- | --- |
| [FLOYD_STEINBERG_DITHERING](#FLOYD-STEINBERG-DITHERING) | Specifies dithering using Floyd-Steinberg error diffusion method. |
| [THRESHOLD](#THRESHOLD) | Specifies threshold method. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String imageBinarizationMethodName)](#fromName-java.lang.String) |  |
| [getName(int imageBinarizationMethod)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageBinarizationMethod)](#toString-int) |  |
### FLOYD_STEINBERG_DITHERING {#FLOYD-STEINBERG-DITHERING}
```
public static int FLOYD_STEINBERG_DITHERING
```


Specifies dithering using Floyd-Steinberg error diffusion method.

### THRESHOLD {#THRESHOLD}
```
public static int THRESHOLD
```


Specifies threshold method.

### length {#length}
```
public static int length
```


### fromName(String imageBinarizationMethodName) {#fromName-java.lang.String}
```
public static int fromName(String imageBinarizationMethodName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBinarizationMethodName | java.lang.String |  |

**Returns:**
int
### getName(int imageBinarizationMethod) {#getName-int}
```
public static String getName(int imageBinarizationMethod)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String

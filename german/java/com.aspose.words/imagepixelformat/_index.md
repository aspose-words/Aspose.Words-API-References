---
title: "ImagePixelFormat"
linktitle: "ImagePixelFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Pixelformat für die erzeugten Bilder von Dokumentseiten in Java an."
type: docs
weight: 393
url: /de/java/com.aspose.words/imagepixelformat/
---

**Inheritance:**
java.lang.Object
```
public class ImagePixelFormat
```

Gibt das Pixel-Format für die erzeugten Bilder der Dokumentseiten an.

 **Examples:** 

Zeigt, wie man eine Bit-pro-Pixel-Rate auswählt, mit der ein Dokument in ein Bild gerendert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FORMAT_16_BPP_ARGB_1555](#FORMAT-16-BPP-ARGB-1555) | 16 Bits pro Pixel, ARGB. |
| [FORMAT_16_BPP_RGB_555](#FORMAT-16-BPP-RGB-555) | 16 Bits pro Pixel, RGB. |
| [FORMAT_16_BPP_RGB_565](#FORMAT-16-BPP-RGB-565) | 16 Bits pro Pixel, RGB. |
| [FORMAT_1_BPP_INDEXED](#FORMAT-1-BPP-INDEXED) | 1 Bit pro Pixel, indiziert. |
| [FORMAT_24_BPP_RGB](#FORMAT-24-BPP-RGB) | 24 Bits pro Pixel, RGB. |
| [FORMAT_32_BPP_ARGB](#FORMAT-32-BPP-ARGB) | 32 Bits pro Pixel, ARGB. |
| [FORMAT_32_BPP_P_ARGB](#FORMAT-32-BPP-P-ARGB) | 32 Bits pro Pixel, ARGB, vormultiplizierter Alpha. |
| [FORMAT_32_BPP_RGB](#FORMAT-32-BPP-RGB) | 32 Bits pro Pixel, RGB. |
| [FORMAT_48_BPP_RGB](#FORMAT-48-BPP-RGB) | 48 Bits pro Pixel, RGB. |
| [FORMAT_64_BPP_ARGB](#FORMAT-64-BPP-ARGB) | 64 Bits pro Pixel, ARGB. |
| [FORMAT_64_BPP_P_ARGB](#FORMAT-64-BPP-P-ARGB) | 64 Bits pro Pixel, ARGB, vormultiplizierter Alpha. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String imagePixelFormatName)](#fromName-java.lang.String) |  |
| [getName(int imagePixelFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imagePixelFormat)](#toString-int) |  |
### FORMAT_16_BPP_ARGB_1555 {#FORMAT-16-BPP-ARGB-1555}
```
public static int FORMAT_16_BPP_ARGB_1555
```


16 Bits pro Pixel, ARGB.

### FORMAT_16_BPP_RGB_555 {#FORMAT-16-BPP-RGB-555}
```
public static int FORMAT_16_BPP_RGB_555
```


16 Bits pro Pixel, RGB.

### FORMAT_16_BPP_RGB_565 {#FORMAT-16-BPP-RGB-565}
```
public static int FORMAT_16_BPP_RGB_565
```


16 Bits pro Pixel, RGB.

### FORMAT_1_BPP_INDEXED {#FORMAT-1-BPP-INDEXED}
```
public static int FORMAT_1_BPP_INDEXED
```


1 Bit pro Pixel, indiziert.

### FORMAT_24_BPP_RGB {#FORMAT-24-BPP-RGB}
```
public static int FORMAT_24_BPP_RGB
```


24 Bits pro Pixel, RGB.

### FORMAT_32_BPP_ARGB {#FORMAT-32-BPP-ARGB}
```
public static int FORMAT_32_BPP_ARGB
```


32 Bits pro Pixel, ARGB.

### FORMAT_32_BPP_P_ARGB {#FORMAT-32-BPP-P-ARGB}
```
public static int FORMAT_32_BPP_P_ARGB
```


32 Bits pro Pixel, ARGB, vormultiplizierter Alpha.

### FORMAT_32_BPP_RGB {#FORMAT-32-BPP-RGB}
```
public static int FORMAT_32_BPP_RGB
```


32 Bits pro Pixel, RGB.

### FORMAT_48_BPP_RGB {#FORMAT-48-BPP-RGB}
```
public static int FORMAT_48_BPP_RGB
```


48 Bits pro Pixel, RGB.

### FORMAT_64_BPP_ARGB {#FORMAT-64-BPP-ARGB}
```
public static int FORMAT_64_BPP_ARGB
```


64 Bits pro Pixel, ARGB.

### FORMAT_64_BPP_P_ARGB {#FORMAT-64-BPP-P-ARGB}
```
public static int FORMAT_64_BPP_P_ARGB
```


64 Bits pro Pixel, ARGB, vormultiplizierter Alpha.

### length {#length}
```
public static int length
```


### fromName(String imagePixelFormatName) {#fromName-java.lang.String}
```
public static int fromName(String imagePixelFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imagePixelFormatName | java.lang.String |  |

**Returns:**
int
### getName(int imagePixelFormat) {#getName-int}
```
public static String getName(int imagePixelFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String

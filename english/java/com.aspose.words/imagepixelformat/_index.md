---
title: ImagePixelFormat
linktitle: ImagePixelFormat
second_title: Aspose.Words for Java API Reference
description: Specifies the pixel format for the generated images of document pages in Java.
type: docs
weight: 342
url: /java/com.aspose.words/imagepixelformat/
---

**Inheritance:**
java.lang.Object
```
public class ImagePixelFormat
```

Specifies the pixel format for the generated images of document pages.

 **Examples:** 

Shows how to select a bit-per-pixel rate with which to render a document to an image.

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

 switch (imagePixelFormat) {
     case ImagePixelFormat.FORMAT_1_BPP_INDEXED:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png").length() <= 10000);
         break;
     case ImagePixelFormat.FORMAT_16_BPP_RGB_555:
     case ImagePixelFormat.FORMAT_32_BPP_RGB:
     case ImagePixelFormat.FORMAT_48_BPP_RGB:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png").length() < 156000);
         break;
     case ImagePixelFormat.FORMAT_24_BPP_RGB:
         Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png").length() < 146000);
         break;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [FORMAT_16_BPP_ARGB_1555](#FORMAT-16-BPP-ARGB-1555) | 16 bits per pixel, ARGB. |
| [FORMAT_16_BPP_RGB_555](#FORMAT-16-BPP-RGB-555) | 16 bits per pixel, RGB. |
| [FORMAT_16_BPP_RGB_565](#FORMAT-16-BPP-RGB-565) | 16 bits per pixel, RGB. |
| [FORMAT_1_BPP_INDEXED](#FORMAT-1-BPP-INDEXED) | 1 bit per pixel, Indexed. |
| [FORMAT_24_BPP_RGB](#FORMAT-24-BPP-RGB) | 24 bits per pixel, RGB. |
| [FORMAT_32_BPP_ARGB](#FORMAT-32-BPP-ARGB) | 32 bits per pixel, ARGB. |
| [FORMAT_32_BPP_P_ARGB](#FORMAT-32-BPP-P-ARGB) | 32 bits per pixel, ARGB, premultiplied alpha. |
| [FORMAT_32_BPP_RGB](#FORMAT-32-BPP-RGB) | 32 bits per pixel, RGB. |
| [FORMAT_48_BPP_RGB](#FORMAT-48-BPP-RGB) | 48 bits per pixel, RGB. |
| [FORMAT_64_BPP_ARGB](#FORMAT-64-BPP-ARGB) | 64 bits per pixel, ARGB. |
| [FORMAT_64_BPP_P_ARGB](#FORMAT-64-BPP-P-ARGB) | 64 bits per pixel, ARGB, premultiplied alpha. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String imagePixelFormatName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int imagePixelFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int imagePixelFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FORMAT_16_BPP_ARGB_1555 {#FORMAT-16-BPP-ARGB-1555}
```
public static int FORMAT_16_BPP_ARGB_1555
```


16 bits per pixel, ARGB.

### FORMAT_16_BPP_RGB_555 {#FORMAT-16-BPP-RGB-555}
```
public static int FORMAT_16_BPP_RGB_555
```


16 bits per pixel, RGB.

### FORMAT_16_BPP_RGB_565 {#FORMAT-16-BPP-RGB-565}
```
public static int FORMAT_16_BPP_RGB_565
```


16 bits per pixel, RGB.

### FORMAT_1_BPP_INDEXED {#FORMAT-1-BPP-INDEXED}
```
public static int FORMAT_1_BPP_INDEXED
```


1 bit per pixel, Indexed.

### FORMAT_24_BPP_RGB {#FORMAT-24-BPP-RGB}
```
public static int FORMAT_24_BPP_RGB
```


24 bits per pixel, RGB.

### FORMAT_32_BPP_ARGB {#FORMAT-32-BPP-ARGB}
```
public static int FORMAT_32_BPP_ARGB
```


32 bits per pixel, ARGB.

### FORMAT_32_BPP_P_ARGB {#FORMAT-32-BPP-P-ARGB}
```
public static int FORMAT_32_BPP_P_ARGB
```


32 bits per pixel, ARGB, premultiplied alpha.

### FORMAT_32_BPP_RGB {#FORMAT-32-BPP-RGB}
```
public static int FORMAT_32_BPP_RGB
```


32 bits per pixel, RGB.

### FORMAT_48_BPP_RGB {#FORMAT-48-BPP-RGB}
```
public static int FORMAT_48_BPP_RGB
```


48 bits per pixel, RGB.

### FORMAT_64_BPP_ARGB {#FORMAT-64-BPP-ARGB}
```
public static int FORMAT_64_BPP_ARGB
```


64 bits per pixel, ARGB.

### FORMAT_64_BPP_P_ARGB {#FORMAT-64-BPP-P-ARGB}
```
public static int FORMAT_64_BPP_P_ARGB
```


64 bits per pixel, ARGB, premultiplied alpha.

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
### fromName(String imagePixelFormatName) {#fromName-java.lang.String}
```
public static int fromName(String imagePixelFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imagePixelFormatName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int imagePixelFormat) {#getName-int}
```
public static String getName(int imagePixelFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
### toString(int imagePixelFormat) {#toString-int}
```
public static String toString(int imagePixelFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imagePixelFormat | int |  |

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


---
title: ImageType
second_title: Aspose.Words for Java API Reference
description: Specifies the type format of an image in a Microsoft Word document.
type: docs
weight: 343
url: /java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Specifies the type (format) of an image in a Microsoft Word document.
## Fields

| Field | Description |
| --- | --- |
| [NO_IMAGE](#NO-IMAGE) | The is no image data. |
| [UNKNOWN](#UNKNOWN) | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [WMF](#WMF) | Windows Metafile. |
| [PICT](#PICT) | Macintosh PICT. |
| [JPEG](#JPEG) | JPEG JFIF. |
| [PNG](#PNG) | Portable Network Graphics. |
| [BMP](#BMP) | Windows Bitmap. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int imageType)](#getName-int-) |  |
| [toString(int imageType)](#toString-int-) |  |
| [fromName(String imageTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NO_IMAGE {#NO-IMAGE}
```
public static int NO_IMAGE
```


The is no image data.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


An unknown image type or image type that cannot be directly stored inside a Microsoft Word document.

### EMF {#EMF}
```
public static int EMF
```


Windows Enhanced Metafile.

### WMF {#WMF}
```
public static int WMF
```


Windows Metafile.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported.

### JPEG {#JPEG}
```
public static int JPEG
```


JPEG JFIF.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### BMP {#BMP}
```
public static int BMP
```


Windows Bitmap.

### length {#length}
```
public static int length
```


### getName(int imageType) {#getName-int-}
```
public static String getName(int imageType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### toString(int imageType) {#toString-int-}
```
public static String toString(int imageType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### fromName(String imageTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String imageTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]

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
| [BMP](#BMP) | Windows Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | The is no image data. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String imageTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int imageType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int imageType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BMP {#BMP}
```
public static int BMP
```


Windows Bitmap.

### EMF {#EMF}
```
public static int EMF
```


Windows Enhanced Metafile.

### JPEG {#JPEG}
```
public static int JPEG
```


JPEG JFIF.

### NO_IMAGE {#NO-IMAGE}
```
public static int NO_IMAGE
```


The is no image data.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


An unknown image type or image type that cannot be directly stored inside a Microsoft Word document.

### WMF {#WMF}
```
public static int WMF
```


Windows Metafile.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




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
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |


---
title: DownsampleOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify downsample options.
type: docs
weight: 133
url: /java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Allows to specify downsample options.

To learn more, visit the **Save a Document** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDownsampleImages()](#getDownsampleImages--) | Specifies whether images should be downsampled. |
| [getResolution()](#getResolution--) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [getResolutionThreshold()](#getResolutionThreshold--) | Specifies the threshold resolution in pixels per inch. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean-) | Specifies whether images should be downsampled. |
| [setResolution(int value)](#setResolution-int-) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int-) | Specifies the threshold resolution in pixels per inch. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDownsampleImages() {#getDownsampleImages--}
```
public boolean getDownsampleImages()
```


Specifies whether images should be downsampled. The default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getResolution() {#getResolution--}
```
public int getResolution()
```


Specifies the resolution in pixels per inch which the images should be downsampled to. The default value is 220 ppi.

**Returns:**
int - The corresponding  int  value.
### getResolutionThreshold() {#getResolutionThreshold--}
```
public int getResolutionThreshold()
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. The default value is 0.

**Returns:**
int - The corresponding  int  value.
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




### setDownsampleImages(boolean value) {#setDownsampleImages-boolean-}
```
public void setDownsampleImages(boolean value)
```


Specifies whether images should be downsampled. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResolution(int value) {#setResolution-int-}
```
public void setResolution(int value)
```


Specifies the resolution in pixels per inch which the images should be downsampled to. The default value is 220 ppi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int-}
```
public void setResolutionThreshold(int value)
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### toString() {#toString--}
```
public String toString()
```




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


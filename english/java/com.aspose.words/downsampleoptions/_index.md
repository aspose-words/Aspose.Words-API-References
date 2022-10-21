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
| [getDownsampleImages()](#getDownsampleImages--) | Specifies whether images should be downsampled. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean-) | Specifies whether images should be downsampled. |
| [getResolution()](#getResolution--) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [setResolution(int value)](#setResolution-int-) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [getResolutionThreshold()](#getResolutionThreshold--) | Specifies the threshold resolution in pixels per inch. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int-) | Specifies the threshold resolution in pixels per inch. |
### getDownsampleImages() {#getDownsampleImages--}
```
public boolean getDownsampleImages()
```


Specifies whether images should be downsampled. The default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean-}
```
public void setDownsampleImages(boolean value)
```


Specifies whether images should be downsampled. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getResolution() {#getResolution--}
```
public int getResolution()
```


Specifies the resolution in pixels per inch which the images should be downsampled to. The default value is 220 ppi.

**Returns:**
int - The corresponding  int  value.
### setResolution(int value) {#setResolution-int-}
```
public void setResolution(int value)
```


Specifies the resolution in pixels per inch which the images should be downsampled to. The default value is 220 ppi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getResolutionThreshold() {#getResolutionThreshold--}
```
public int getResolutionThreshold()
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### setResolutionThreshold(int value) {#setResolutionThreshold-int-}
```
public void setResolutionThreshold(int value)
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |


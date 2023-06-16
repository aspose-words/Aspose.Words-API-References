---
title: DownsampleOptions
linktitle: DownsampleOptions
second_title: Aspose.Words for Java
description: Allows to specify downsample options in Java.
type: docs
weight: 145
url: /java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Allows to specify downsample options.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | Specifies whether images should be downsampled. |
| [getResolution()](#getResolution) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [getResolutionThreshold()](#getResolutionThreshold) | Specifies the threshold resolution in pixels per inch. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | Specifies whether images should be downsampled. |
| [setResolution(int value)](#setResolution-int) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | Specifies the threshold resolution in pixels per inch. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


Specifies whether images should be downsampled.

 **Remarks:** 

The default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getResolution() {#getResolution}
```
public int getResolution()
```


Specifies the resolution in pixels per inch which the images should be downsampled to.

 **Remarks:** 

The default value is 220 ppi.

**Returns:**
int - The corresponding  int  value.
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.

 **Remarks:** 

The default value is 0.

**Returns:**
int - The corresponding  int  value.
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


Specifies whether images should be downsampled.

 **Remarks:** 

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


Specifies the resolution in pixels per inch which the images should be downsampled to.

 **Remarks:** 

The default value is 220 ppi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.

 **Remarks:** 

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |


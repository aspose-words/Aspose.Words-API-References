---
title: Watermark
second_title: Aspose.Words for Java API Reference
description: Represents class to work with document watermark.
type: docs
weight: 608
url: /java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Represents class to work with document watermark.

To learn more, visit the **Working with Watermark** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getType()](#getType--) | Gets the watermark type. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the watermark. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | Adds Image watermark into the document. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-) | Adds Image watermark into the document. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-) | Adds Image watermark into the document. |
| [setText(String text)](#setText-java.lang.String-) | Adds Text watermark into the document. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-) | Adds Text watermark into the document. |
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
### getType() {#getType--}
```
public int getType()
```


Gets the watermark type.

**Returns:**
int - The watermark type. The returned value is one of [WatermarkType](../../com.aspose.words/watermarktype) constants.
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




### remove() {#remove--}
```
public void remove()
```


Removes the watermark.

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image that is displayed as a watermark. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | Defines additional options for the image watermark. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | java.lang.String | Path to the image file that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | Defines additional options for the image watermark. |

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


Adds Text watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Text that is displayed as a watermark. The text length must be in the range from 1 to 200 inclusive. The text cannot be null or contain only whitespaces. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-}
```
public void setText(String text, TextWatermarkOptions options)
```


Adds Text watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions) | Defines additional options for the text watermark. The text length must be in the range from 1 to 200 inclusive. The text cannot be null or contain only whitespaces. |

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


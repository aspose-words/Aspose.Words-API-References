---
title: ImageWatermarkOptions
linktitle: ImageWatermarkOptions
second_title: Aspose.Words for Java API Reference
description: Contains options that can be specified when adding a watermark with image in Java.
type: docs
weight: 347
url: /java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contains options that can be specified when adding a watermark with image.

To learn more, visit the [ Working with Watermark ][Working with Watermark] documentation article.


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getScale()](#getScale) | Gets the scale factor expressed as a fraction of the image. |
| [hashCode()](#hashCode) |  |
| [isWashout()](#isWashout) | Gets a boolean value which is responsible for washout effect of the watermark. |
| [isWashout(boolean value)](#isWashout-boolean) | Sets a boolean value which is responsible for washout effect of the watermark. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setScale(double value)](#setScale-double) | Sets the scale factor expressed as a fraction of the image. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getScale() {#getScale}
```
public double getScale()
```


Gets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

 **Remarks:** 

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

**Returns:**
double - The scale factor expressed as a fraction of the image.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Gets a boolean value which is responsible for washout effect of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a watermark from an image in the local file system.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Returns:**
boolean - A boolean value which is responsible for washout effect of the watermark.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Sets a boolean value which is responsible for washout effect of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a watermark from an image in the local file system.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for washout effect of the watermark. |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

 **Remarks:** 

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The scale factor expressed as a fraction of the image. |

### toString() {#toString}
```
public String toString()
```




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


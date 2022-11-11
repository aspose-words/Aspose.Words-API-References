---
title: ImageData
second_title: Aspose.Words for Java API Reference
description: Defines an image for a shape.
type: docs
weight: 337
url: /java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

Defines an image for a shape.

To learn more, visit the **Working with Images** documentation article.

Use the [Shape.getImageData()](../../com.aspose.words/shape\#getImageData--) property to access and modify the image inside a shape. You do not create instances of the [ImageData](../../com.aspose.words/imagedata) class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual image using the [toByteArray()](../../com.aspose.words/imagedata\#toByteArray--), [toImage()](../../com.aspose.words/imagedata\#toImage--) or [save(java.lang.String)](../../com.aspose.words/imagedata\#save-java.lang.String-) methods. If the image is stored inside the shape, you can also directly access it using the [getImageBytes()](../../com.aspose.words/imagedata\#getImageBytes--) / [setImageBytes(byte[])](../../com.aspose.words/imagedata\#setImageBytes-byte---) property.

To store an image inside a shape use the [setImage(java.lang.String)](../../com.aspose.words/imagedata\#setImage-java.lang.String-) method. To link an image to a shape, set the [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) property.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getBiLevel()](#getBiLevel--) | Determines whether an image will be displayed in black and white. |
| [getBorders()](#getBorders--) | Gets the collection of borders of the image. |
| [getBrightness()](#getBrightness--) | Gets the brightness of the picture. |
| [getChromaKey()](#getChromaKey--) | Defines the color value of the image that will be treated as transparent. |
| [getClass()](#getClass--) |  |
| [getContrast()](#getContrast--) | Gets the contrast for the specified picture. |
| [getCropBottom()](#getCropBottom--) | Defines the fraction of picture removal from the bottom side. |
| [getCropLeft()](#getCropLeft--) | Defines the fraction of picture removal from the left side. |
| [getCropRight()](#getCropRight--) | Defines the fraction of picture removal from the right side. |
| [getCropTop()](#getCropTop--) | Defines the fraction of picture removal from the top side. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getGrayScale()](#getGrayScale--) | Determines whether a picture will display in grayscale mode. |
| [getImageBytes()](#getImageBytes--) | Gets the raw bytes of the image stored in the shape. |
| [getImageSize()](#getImageSize--) | Gets the information about image size and resolution. |
| [getImageType()](#getImageType--) | Gets the type of the image. |
| [getSourceFullName()](#getSourceFullName--) | Gets the path and name of the source file for the linked image. |
| [getTitle()](#getTitle--) | Defines the title of an image. |
| [hasImage()](#hasImage--) | Returns true if the shape has image bytes or links an image. |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) | Returns true if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) is specified). |
| [isLinkOnly()](#isLinkOnly--) | Returns true if the image is linked and not stored in the document. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Saves the image into a file. |
| [setBiLevel(boolean value)](#setBiLevel-boolean-) | Determines whether an image will be displayed in black and white. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBrightness(double value)](#setBrightness-double-) | Sets the brightness of the picture. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color-) | Defines the color value of the image that will be treated as transparent. |
| [setContrast(double value)](#setContrast-double-) | Sets the contrast for the specified picture. |
| [setCropBottom(double value)](#setCropBottom-double-) | Defines the fraction of picture removal from the bottom side. |
| [setCropLeft(double value)](#setCropLeft-double-) | Defines the fraction of picture removal from the left side. |
| [setCropRight(double value)](#setCropRight-double-) | Defines the fraction of picture removal from the right side. |
| [setCropTop(double value)](#setCropTop-double-) | Defines the fraction of picture removal from the top side. |
| [setGrayScale(boolean value)](#setGrayScale-boolean-) | Determines whether a picture will display in grayscale mode. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | Sets the image that the shape displays. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream-) |  |
| [setImage(String fileName)](#setImage-java.lang.String-) | Sets the image that the shape displays. |
| [setImageBytes(byte[] value)](#setImageBytes-byte---) | Sets the raw bytes of the image stored in the shape. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | Sets the path and name of the source file for the linked image. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Defines the title of an image. |
| [toByteArray()](#toByteArray--) | Returns image bytes for any image regardless whether the image is stored or linked. |
| [toImage()](#toImage--) | Gets the image stored in the shape as a java  BufferedImage  object. |
| [toStream()](#toStream--) | Creates and returns a stream that contains the image bytes. |
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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBiLevel() {#getBiLevel--}
```
public boolean getBiLevel()
```


Determines whether an image will be displayed in black and white.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Gets the collection of borders of the image. Borders only have effect for inline images.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection) - The collection of borders of the image.
### getBrightness() {#getBrightness--}
```
public double getBrightness()
```


Gets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest).

The default value is 0.5.

**Returns:**
double - The brightness of the picture.
### getChromaKey() {#getChromaKey--}
```
public Color getChromaKey()
```


Defines the color value of the image that will be treated as transparent.

The default value is 0.

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContrast() {#getContrast--}
```
public double getContrast()
```


Gets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast).

The default value is 0.5.

**Returns:**
double - The contrast for the specified picture.
### getCropBottom() {#getCropBottom--}
```
public double getCropBottom()
```


Defines the fraction of picture removal from the bottom side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### getCropLeft() {#getCropLeft--}
```
public double getCropLeft()
```


Defines the fraction of picture removal from the left side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### getCropRight() {#getCropRight--}
```
public double getCropRight()
```


Defines the fraction of picture removal from the right side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### getCropTop() {#getCropTop--}
```
public double getCropTop()
```


Defines the fraction of picture removal from the top side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale--}
```
public boolean getGrayScale()
```


Determines whether a picture will display in grayscale mode.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


Gets the raw bytes of the image stored in the shape.

Setting the value to  null  or an empty array will remove the image from the shape.

Returns  null  if the image is not stored in the document (e.g the image is probably linked in this case).

**Returns:**
byte[] - The raw bytes of the image stored in the shape.
### getImageSize() {#getImageSize--}
```
public ImageSize getImageSize()
```


Gets the information about image size and resolution. (4661,6)

If the image is linked only and not stored in the document, returns zero size.

**Returns:**
[ImageSize](../../com.aspose.words/imagesize) - The information about image size and resolution.
### getImageType() {#getImageType--}
```
public int getImageType()
```


Gets the type of the image. (4671,6)

**Returns:**
int - The type of the image. The returned value is one of [ImageType](../../com.aspose.words/imagetype) constants.
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


Gets the path and name of the source file for the linked image.

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) is not an empty string, the image is linked.

**Returns:**
java.lang.String - The path and name of the source file for the linked image.
### getTitle() {#getTitle--}
```
public String getTitle()
```


Defines the title of an image.

The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### hasImage() {#hasImage--}
```
public boolean hasImage()
```


Returns true if the shape has image bytes or links an image. (4654,6)

**Returns:**
boolean - True if the shape has image bytes or links an image.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isLink() {#isLink--}
```
public boolean isLink()
```


Returns true if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) is specified). (4678,6)

**Returns:**
boolean - True if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) is specified).
### isLinkOnly() {#isLinkOnly--}
```
public boolean isLinkOnly()
```


Returns true if the image is linked and not stored in the document. (4685,6)

**Returns:**
boolean - True if the image is linked and not stored in the document.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Saves the image into a file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file name where to save the image. |

### setBiLevel(boolean value) {#setBiLevel-boolean-}
```
public void setBiLevel(boolean value)
```


Determines whether an image will be displayed in black and white.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double-}
```
public void setBrightness(double value)
```


Sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest).

The default value is 0.5.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The brightness of the picture. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color-}
```
public void setChromaKey(Color value)
```


Defines the color value of the image that will be treated as transparent.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setContrast(double value) {#setContrast-double-}
```
public void setContrast(double value)
```


Sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast).

The default value is 0.5.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The contrast for the specified picture. |

### setCropBottom(double value) {#setCropBottom-double-}
```
public void setCropBottom(double value)
```


Defines the fraction of picture removal from the bottom side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropLeft(double value) {#setCropLeft-double-}
```
public void setCropLeft(double value)
```


Defines the fraction of picture removal from the left side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropRight(double value) {#setCropRight-double-}
```
public void setCropRight(double value)
```


Defines the fraction of picture removal from the right side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropTop(double value) {#setCropTop-double-}
```
public void setCropTop(double value)
```


Defines the fraction of picture removal from the top side.

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setGrayScale(boolean value) {#setGrayScale-boolean-}
```
public void setGrayScale(boolean value)
```


Determines whether a picture will display in grayscale mode.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


Sets the image that the shape displays.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image object. |

### setImage(InputStream stream) {#setImage-java.io.InputStream-}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String-}
```
public void setImage(String fileName)
```


Sets the image that the shape displays.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The image file. Can be a file name or a URL. |

### setImageBytes(byte[] value) {#setImageBytes-byte---}
```
public void setImageBytes(byte[] value)
```


Sets the raw bytes of the image stored in the shape.

Setting the value to  null  or an empty array will remove the image from the shape.

Returns  null  if the image is not stored in the document (e.g the image is probably linked in this case).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The raw bytes of the image stored in the shape. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


Sets the path and name of the source file for the linked image.

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) is not an empty string, the image is linked.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The path and name of the source file for the linked image. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Defines the title of an image.

The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### toByteArray() {#toByteArray--}
```
public byte[] toByteArray()
```


Returns image bytes for any image regardless whether the image is stored or linked.

**Returns:**
byte[] - If the image is linked, downloads the image every time it is called.
### toImage() {#toImage--}
```
public BufferedImage toImage()
```


Gets the image stored in the shape as a java  BufferedImage  object.

**Returns:**
java.awt.image.BufferedImage - Tries to create a new  java.awt.image.BufferedImage  object from image bytes every time this method is called. If  javax.imageio.ImageReader  can't read image bytes (emf, wmf, tiff, etc.) the method returns null.

It is the responsibility of the caller to dispose the image object.
### toStream() {#toStream--}
```
public InputStream toStream()
```


Creates and returns a stream that contains the image bytes.

If the image bytes are stored in the shape, creates and returns a  object.

If the image is linked and stored in a file, opens the file and returns a  object.

If the image is linked and stored in an external URL, opens the URL and returns a  object.

Is it the responsibility of the caller to dispose the stream object.

This is not ported to Java yet.

**Returns:**
java.io.InputStream
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


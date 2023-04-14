---
title: ImageSize
linktitle: ImageSize
second_title: Aspose.Words for Java API Reference
description: Contains information about image size and resolution in Java.
type: docs
weight: 345
url: /java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

Contains information about image size and resolution.

To learn more, visit the [ Working with Images ][Working with Images] documentation article.

 **Examples:** 

Shows how to resize a shape with an image.

```

 BufferedImage image = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 Assert.assertEquals(400, image.getWidth());
 Assert.assertEquals(400, image.getHeight());

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```


[Working with Images]: https://docs.aspose.com/words/java/working-with-images/
## Constructors

| Constructor | Description |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int) | Initializes width and height to the given values in pixels. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double) | Initializes width, height and resolution to the given values. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getHeightPixels()](#getHeightPixels) | Gets the height of the image in pixels. |
| [getHeightPoints()](#getHeightPoints) | Gets the height of the image in points. |
| [getHorizontalResolution()](#getHorizontalResolution) | Gets the horizontal resolution in DPI. |
| [getVerticalResolution()](#getVerticalResolution) | Gets the vertical resolution in DPI. |
| [getWidthPixels()](#getWidthPixels) | Gets the width of the image in pixels. |
| [getWidthPoints()](#getWidthPoints) | Gets the width of the image in points. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int}
```
public ImageSize(int widthPixels, int heightPixels)
```


Initializes width and height to the given values in pixels. Initializes resolution to 96 dpi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| widthPixels | int | Width in pixels. |
| heightPixels | int | Height in pixels. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Initializes width, height and resolution to the given values.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| widthPixels | int | Width in pixels. |
| heightPixels | int | Height in pixels. |
| horizontalResolution | double | Horizontal resolution in DPI. |
| verticalResolution | double | Vertical resolution in DPI. |

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
### getHeightPixels() {#getHeightPixels}
```
public int getHeightPixels()
```


Gets the height of the image in pixels.

 **Examples:** 

Shows how to read the properties of an image in a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape into the document which contains an image taken from our local file system.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // If the shape contains an image, its ImageData property will be valid,
 // and it will contain an ImageSize object.
 ImageSize imageSize = shape.getImageData().getImageSize();

 // The ImageSize object contains read-only information about the image within the shape.
 Assert.assertEquals(imageSize.getHeightPixels(), 400);
 Assert.assertEquals(imageSize.getWidthPixels(), 400);

 final double delta = 0.05;
 Assert.assertEquals(imageSize.getHorizontalResolution(), 95.98d, delta);
 Assert.assertEquals(imageSize.getVerticalResolution(), 95.98d, delta);

 // We can base the size of the shape on the size of its image to avoid stretching the image.
 shape.setWidth(imageSize.getWidthPoints() * 2.0);
 shape.setHeight(imageSize.getHeightPoints() * 2.0);

 doc.save(getArtifactsDir() + "Drawing.ImageSize.docx");
 
```

**Returns:**
int - The height of the image in pixels.
### getHeightPoints() {#getHeightPoints}
```
public double getHeightPoints()
```


Gets the height of the image in points. 1 point is 1/72 inch.

 **Examples:** 

Shows how to resize a shape with an image.

```

 BufferedImage image = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 Assert.assertEquals(400, image.getWidth());
 Assert.assertEquals(400, image.getHeight());

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Returns:**
double - The height of the image in points.
### getHorizontalResolution() {#getHorizontalResolution}
```
public double getHorizontalResolution()
```


Gets the horizontal resolution in DPI.

 **Examples:** 

Shows how to read the properties of an image in a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape into the document which contains an image taken from our local file system.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // If the shape contains an image, its ImageData property will be valid,
 // and it will contain an ImageSize object.
 ImageSize imageSize = shape.getImageData().getImageSize();

 // The ImageSize object contains read-only information about the image within the shape.
 Assert.assertEquals(imageSize.getHeightPixels(), 400);
 Assert.assertEquals(imageSize.getWidthPixels(), 400);

 final double delta = 0.05;
 Assert.assertEquals(imageSize.getHorizontalResolution(), 95.98d, delta);
 Assert.assertEquals(imageSize.getVerticalResolution(), 95.98d, delta);

 // We can base the size of the shape on the size of its image to avoid stretching the image.
 shape.setWidth(imageSize.getWidthPoints() * 2.0);
 shape.setHeight(imageSize.getHeightPoints() * 2.0);

 doc.save(getArtifactsDir() + "Drawing.ImageSize.docx");
 
```

**Returns:**
double - The horizontal resolution in DPI.
### getVerticalResolution() {#getVerticalResolution}
```
public double getVerticalResolution()
```


Gets the vertical resolution in DPI.

 **Examples:** 

Shows how to read the properties of an image in a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape into the document which contains an image taken from our local file system.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // If the shape contains an image, its ImageData property will be valid,
 // and it will contain an ImageSize object.
 ImageSize imageSize = shape.getImageData().getImageSize();

 // The ImageSize object contains read-only information about the image within the shape.
 Assert.assertEquals(imageSize.getHeightPixels(), 400);
 Assert.assertEquals(imageSize.getWidthPixels(), 400);

 final double delta = 0.05;
 Assert.assertEquals(imageSize.getHorizontalResolution(), 95.98d, delta);
 Assert.assertEquals(imageSize.getVerticalResolution(), 95.98d, delta);

 // We can base the size of the shape on the size of its image to avoid stretching the image.
 shape.setWidth(imageSize.getWidthPoints() * 2.0);
 shape.setHeight(imageSize.getHeightPoints() * 2.0);

 doc.save(getArtifactsDir() + "Drawing.ImageSize.docx");
 
```

**Returns:**
double - The vertical resolution in DPI.
### getWidthPixels() {#getWidthPixels}
```
public int getWidthPixels()
```


Gets the width of the image in pixels.

 **Examples:** 

Shows how to read the properties of an image in a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape into the document which contains an image taken from our local file system.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // If the shape contains an image, its ImageData property will be valid,
 // and it will contain an ImageSize object.
 ImageSize imageSize = shape.getImageData().getImageSize();

 // The ImageSize object contains read-only information about the image within the shape.
 Assert.assertEquals(imageSize.getHeightPixels(), 400);
 Assert.assertEquals(imageSize.getWidthPixels(), 400);

 final double delta = 0.05;
 Assert.assertEquals(imageSize.getHorizontalResolution(), 95.98d, delta);
 Assert.assertEquals(imageSize.getVerticalResolution(), 95.98d, delta);

 // We can base the size of the shape on the size of its image to avoid stretching the image.
 shape.setWidth(imageSize.getWidthPoints() * 2.0);
 shape.setHeight(imageSize.getHeightPoints() * 2.0);

 doc.save(getArtifactsDir() + "Drawing.ImageSize.docx");
 
```

**Returns:**
int - The width of the image in pixels.
### getWidthPoints() {#getWidthPoints}
```
public double getWidthPoints()
```


Gets the width of the image in points. 1 point is 1/72 inch.

 **Examples:** 

Shows how to resize a shape with an image.

```

 BufferedImage image = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 Assert.assertEquals(400, image.getWidth());
 Assert.assertEquals(400, image.getHeight());

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Returns:**
double - The width of the image in points.
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


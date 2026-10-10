---
title: "ImageSize"
linktitle: "ImageSize"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على معلومات حول حجم الصورة ودقتها في Java."
type: docs
weight: 396
url: /ar/java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

يحتوي على معلومات حول حجم الصورة ودقتها.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Images ][Working with Images].

 **Examples:** 

يعرض كيفية تغيير حجم شكل باستخدام صورة.

```

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int) | يُهيئ العرض والارتفاع إلى القيم المعطاة بالبكسل. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double) | يُهيئ العرض والارتفاع والدقة إلى القيم المعطاة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getHeightPixels()](#getHeightPixels) | يحصل على ارتفاع الصورة بالبكسل. |
| [getHeightPoints()](#getHeightPoints) | يحصل على ارتفاع الصورة بالنقاط. |
| [getHorizontalResolution()](#getHorizontalResolution) | يحصل على الدقة الأفقية بوحدة DPI. |
| [getVerticalResolution()](#getVerticalResolution) | يحصل على الدقة العمودية بوحدة DPI. |
| [getWidthPixels()](#getWidthPixels) | يحصل على عرض الصورة بالبكسل. |
| [getWidthPoints()](#getWidthPoints) | يحصل على عرض الصورة بالنقاط. |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int}
```
public ImageSize(int widthPixels, int heightPixels)
```


يُهيئ العرض والارتفاع إلى القيم المعطاة بالبكسل. يُهيئ الدقة إلى 96 dpi.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| widthPixels | int | العرض بالبكسل. |
| heightPixels | int | الارتفاع بالبكسل. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


يُهيئ العرض والارتفاع والدقة إلى القيم المعطاة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| widthPixels | int | العرض بالبكسل. |
| heightPixels | int | الارتفاع بالبكسل. |
| horizontalResolution | double | الدقة الأفقية بوحدة DPI. |
| verticalResolution | double | الدقة العمودية بوحدة DPI. |

### getHeightPixels() {#getHeightPixels}
```
public int getHeightPixels()
```


يحصل على ارتفاع الصورة بالبكسل.

 **Examples:** 

يعرض كيفية قراءة خصائص صورة داخل شكل.

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
int - ارتفاع الصورة بالبكسل.
### getHeightPoints() {#getHeightPoints}
```
public double getHeightPoints()
```


يحصل على ارتفاع الصورة بالنقاط. 1 نقطة تساوي 1/72 بوصة.

 **Examples:** 

يعرض كيفية تغيير حجم شكل باستخدام صورة.

```

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
double - ارتفاع الصورة بالنقاط.
### getHorizontalResolution() {#getHorizontalResolution}
```
public double getHorizontalResolution()
```


يحصل على الدقة الأفقية بوحدة DPI.

 **Examples:** 

يعرض كيفية قراءة خصائص صورة داخل شكل.

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
double - الدقة الأفقية بوحدة DPI.
### getVerticalResolution() {#getVerticalResolution}
```
public double getVerticalResolution()
```


يحصل على الدقة العمودية بوحدة DPI.

 **Examples:** 

يعرض كيفية قراءة خصائص صورة داخل شكل.

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
double - الدقة العمودية بوحدة DPI.
### getWidthPixels() {#getWidthPixels}
```
public int getWidthPixels()
```


يحصل على عرض الصورة بالبكسل.

 **Examples:** 

يعرض كيفية قراءة خصائص صورة داخل شكل.

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
int - عرض الصورة بالبكسل.
### getWidthPoints() {#getWidthPoints}
```
public double getWidthPoints()
```


يحصل على عرض الصورة بالنقاط. 1 نقطة تساوي 1/72 بوصة.

 **Examples:** 

يعرض كيفية تغيير حجم شكل باستخدام صورة.

```

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
double - عرض الصورة بالنقاط.

---
title: "ImageSize"
linktitle: "ImageSize"
second_title: "Aspose.Words Java için"
description: "Java'da görüntü boyutu ve çözünürlüğü hakkında bilgi içerir."
type: docs
weight: 396
url: /tr/java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir.

Daha fazla bilgi için, [ Working with Images ][Working with Images] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir şekli görüntü ile yeniden boyutlandırmanın nasıl yapılacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int) | Genişlik ve yüksekliği piksel cinsinden verilen değerlere başlatır. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double) | Genişlik, yükseklik ve çözünürlüğü verilen değerlere başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getHeightPixels()](#getHeightPixels) | Görüntünün yüksekliğini piksel cinsinden alır. |
| [getHeightPoints()](#getHeightPoints) | Görüntünün yüksekliğini nokta cinsinden alır. |
| [getHorizontalResolution()](#getHorizontalResolution) | Yatay çözünürlüğü DPI cinsinden alır. |
| [getVerticalResolution()](#getVerticalResolution) | Dikey çözünürlüğü DPI cinsinden alır. |
| [getWidthPixels()](#getWidthPixels) | Görüntünün genişliğini piksel cinsinden alır. |
| [getWidthPoints()](#getWidthPoints) | Görüntünün genişliğini nokta cinsinden alır. |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int}
```
public ImageSize(int widthPixels, int heightPixels)
```


Genişlik ve yüksekliği verilen değerlerle piksel cinsinden başlatır. Çözünürlüğü 96 DPI olarak başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| widthPixels | int | Piksel cinsinden genişlik. |
| heightPixels | int | Piksel cinsinden yükseklik. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Genişlik, yükseklik ve çözünürlüğü verilen değerlere başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| widthPixels | int | Piksel cinsinden genişlik. |
| heightPixels | int | Piksel cinsinden yükseklik. |
| horizontalResolution | double | DPI cinsinden yatay çözünürlük. |
| verticalResolution | double | DPI cinsinden dikey çözünürlük. |

### getHeightPixels() {#getHeightPixels}
```
public int getHeightPixels()
```


Görüntünün yüksekliğini piksel cinsinden alır.

 **Examples:** 

Bir şekildeki görüntünün özelliklerini nasıl okuyacağınızı gösterir.

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
int - Görüntünün piksel cinsinden yüksekliği.
### getHeightPoints() {#getHeightPoints}
```
public double getHeightPoints()
```


Görüntünün yüksekliğini nokta cinsinden alır. 1 nokta 1/72 inçtir.

 **Examples:** 

Bir şekli görüntü ile yeniden boyutlandırmanın nasıl yapılacağını gösterir.

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
double - Görüntünün nokta cinsinden yüksekliği.
### getHorizontalResolution() {#getHorizontalResolution}
```
public double getHorizontalResolution()
```


Yatay çözünürlüğü DPI cinsinden alır.

 **Examples:** 

Bir şekildeki görüntünün özelliklerini nasıl okuyacağınızı gösterir.

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
double - DPI cinsinden yatay çözünürlük.
### getVerticalResolution() {#getVerticalResolution}
```
public double getVerticalResolution()
```


Dikey çözünürlüğü DPI cinsinden alır.

 **Examples:** 

Bir şekildeki görüntünün özelliklerini nasıl okuyacağınızı gösterir.

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
double - DPI cinsinden dikey çözünürlük.
### getWidthPixels() {#getWidthPixels}
```
public int getWidthPixels()
```


Görüntünün genişliğini piksel cinsinden alır.

 **Examples:** 

Bir şekildeki görüntünün özelliklerini nasıl okuyacağınızı gösterir.

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
int - Görüntünün piksel cinsinden genişliği.
### getWidthPoints() {#getWidthPoints}
```
public double getWidthPoints()
```


Görüntünün genişliğini nokta cinsinden alır. 1 nokta 1/72 inçtir.

 **Examples:** 

Bir şekli görüntü ile yeniden boyutlandırmanın nasıl yapılacağını gösterir.

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
double - Nokta cinsinden genişlik.

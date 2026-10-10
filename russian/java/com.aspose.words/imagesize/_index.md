---
title: "ImageSize"
linktitle: "ImageSize"
second_title: "Aspose.Words для Java"
description: "Содержит информацию о размере изображения и разрешении в Java."
type: docs
weight: 396
url: /ru/java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

Содержит информацию о размере изображения и разрешении.

Чтобы узнать больше, посетите статью документации [ Working with Images ][Working with Images].

 **Examples:** 

Показывает, как изменить размер фигуры с изображением.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int) | Инициализирует ширину и высоту заданными значениями в пикселях. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double) | Инициализирует ширину, высоту и разрешение заданными значениями. |
## Методы

| Метод | Описание |
| --- | --- |
| [getHeightPixels()](#getHeightPixels) | Возвращает высоту изображения в пикселях. |
| [getHeightPoints()](#getHeightPoints) | Получает высоту изображения в пунктах. |
| [getHorizontalResolution()](#getHorizontalResolution) | Получает горизонтальное разрешение в DPI. |
| [getVerticalResolution()](#getVerticalResolution) | Получает вертикальное разрешение в DPI. |
| [getWidthPixels()](#getWidthPixels) | Получает ширину изображения в пикселях. |
| [getWidthPoints()](#getWidthPoints) | Получает ширину изображения в пунктах. |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int}
```
public ImageSize(int widthPixels, int heightPixels)
```


Инициализирует ширину и высоту заданными значениями в пикселях. Инициализирует разрешение до 96 dpi.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| widthPixels | int | Ширина в пикселях. |
| heightPixels | int | Высота в пикселях. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Инициализирует ширину, высоту и разрешение заданными значениями.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| widthPixels | int | Ширина в пикселях. |
| heightPixels | int | Высота в пикселях. |
| horizontalResolution | double | Горизонтальное разрешение в DPI. |
| verticalResolution | double | Вертикальное разрешение в DPI. |

### getHeightPixels() {#getHeightPixels}
```
public int getHeightPixels()
```


Возвращает высоту изображения в пикселях.

 **Examples:** 

Показывает, как прочитать свойства изображения в фигуре.

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
int - Высота изображения в пикселях.
### getHeightPoints() {#getHeightPoints}
```
public double getHeightPoints()
```


Получает высоту изображения в пунктах. 1 пункт = 1/72 дюйма.

 **Examples:** 

Показывает, как изменить размер фигуры с изображением.

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
double - Высота изображения в пунктах.
### getHorizontalResolution() {#getHorizontalResolution}
```
public double getHorizontalResolution()
```


Получает горизонтальное разрешение в DPI.

 **Examples:** 

Показывает, как прочитать свойства изображения в фигуре.

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
double - Горизонтальное разрешение в DPI.
### getVerticalResolution() {#getVerticalResolution}
```
public double getVerticalResolution()
```


Получает вертикальное разрешение в DPI.

 **Examples:** 

Показывает, как прочитать свойства изображения в фигуре.

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
double - Вертикальное разрешение в DPI.
### getWidthPixels() {#getWidthPixels}
```
public int getWidthPixels()
```


Получает ширину изображения в пикселях.

 **Examples:** 

Показывает, как прочитать свойства изображения в фигуре.

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
int - Ширина изображения в пикселях.
### getWidthPoints() {#getWidthPoints}
```
public double getWidthPoints()
```


Получает ширину изображения в пунктах. 1 пункт = 1/72 дюйма.

 **Examples:** 

Показывает, как изменить размер фигуры с изображением.

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
double - Ширина изображения в пунктах.

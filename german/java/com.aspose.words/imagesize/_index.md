---
title: "ImageSize"
linktitle: "ImageSize"
second_title: "Aspose.Words für Java"
description: "Enthält Informationen über Bildgröße und Auflösung in Java."
type: docs
weight: 396
url: /de/java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

Enthält Informationen über Bildgröße und Auflösung.

Um mehr zu erfahren, besuchen Sie den [ Working with Images ][Working with Images] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man eine Form mit einem Bild skaliert.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int) | Initialisiert Breite und Höhe mit den angegebenen Werten in Pixeln. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double) | Initialisiert Breite, Höhe und Auflösung mit den angegebenen Werten. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getHeightPixels()](#getHeightPixels) | Liefert die Höhe des Bildes in Pixeln. |
| [getHeightPoints()](#getHeightPoints) | Liefert die Höhe des Bildes in Punkten. |
| [getHorizontalResolution()](#getHorizontalResolution) | Ruft die horizontale Auflösung in DPI ab. |
| [getVerticalResolution()](#getVerticalResolution) | Ruft die vertikale Auflösung in DPI ab. |
| [getWidthPixels()](#getWidthPixels) | Ruft die Breite des Bildes in Pixeln ab. |
| [getWidthPoints()](#getWidthPoints) | Ruft die Breite des Bildes in Punkten ab. |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int}
```
public ImageSize(int widthPixels, int heightPixels)
```


Initialisiert Breite und Höhe mit den angegebenen Werten in Pixeln. Initialisiert die Auflösung auf 96 DPI.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| widthPixels | int | Breite in Pixeln. |
| heightPixels | int | Höhe in Pixeln. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Initialisiert Breite, Höhe und Auflösung mit den angegebenen Werten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| widthPixels | int | Breite in Pixeln. |
| heightPixels | int | Höhe in Pixeln. |
| horizontalResolution | double | Horizontale Auflösung in DPI. |
| verticalResolution | double | Vertikale Auflösung in DPI. |

### getHeightPixels() {#getHeightPixels}
```
public int getHeightPixels()
```


Liefert die Höhe des Bildes in Pixeln.

 **Examples:** 

Zeigt, wie man die Eigenschaften eines Bildes in einer Form ausliest.

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
int - Die Höhe des Bildes in Pixeln.
### getHeightPoints() {#getHeightPoints}
```
public double getHeightPoints()
```


Ruft die Höhe des Bildes in Punkten ab. 1 Punkt entspricht 1/72 Zoll.

 **Examples:** 

Zeigt, wie man eine Form mit einem Bild skaliert.

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
double - Die Höhe des Bildes in Punkten.
### getHorizontalResolution() {#getHorizontalResolution}
```
public double getHorizontalResolution()
```


Ruft die horizontale Auflösung in DPI ab.

 **Examples:** 

Zeigt, wie man die Eigenschaften eines Bildes in einer Form ausliest.

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
double - Die horizontale Auflösung in DPI.
### getVerticalResolution() {#getVerticalResolution}
```
public double getVerticalResolution()
```


Ruft die vertikale Auflösung in DPI ab.

 **Examples:** 

Zeigt, wie man die Eigenschaften eines Bildes in einer Form ausliest.

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
double - Die vertikale Auflösung in DPI.
### getWidthPixels() {#getWidthPixels}
```
public int getWidthPixels()
```


Ruft die Breite des Bildes in Pixeln ab.

 **Examples:** 

Zeigt, wie man die Eigenschaften eines Bildes in einer Form ausliest.

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
int - Die Breite des Bildes in Pixeln.
### getWidthPoints() {#getWidthPoints}
```
public double getWidthPoints()
```


Ruft die Breite des Bildes in Punkten ab. 1 Punkt entspricht 1/72 Zoll.

 **Examples:** 

Zeigt, wie man eine Form mit einem Bild skaliert.

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
double - Die Breite des Bildes in Punkten.

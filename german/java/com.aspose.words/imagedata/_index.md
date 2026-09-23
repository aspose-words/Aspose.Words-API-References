---
title: "ImageData"
linktitle: "ImageData"
second_title: "Aspose.Words für Java"
description: "Definiert ein Bild für ein Shape in Java."
type: docs
weight: 391
url: /de/java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

Definiert ein Bild für eine Form.

Um mehr zu erfahren, besuchen Sie den [ Working with Images ][Working with Images] Dokumentationsartikel.

 **Remarks:** 

Verwenden Sie die Eigenschaft [Shape.getImageData()](../../com.aspose.words/shape/\#getImageData), um auf das Bild in einem Shape zuzugreifen und es zu ändern. Sie erstellen keine Instanzen der Klasse [ImageData](../../com.aspose.words/imagedata/) direkt.

Ein Bild kann in einem Shape gespeichert, mit einer externen Datei verknüpft oder beides (verknüpft und im Dokument gespeichert) sein.

Unabhängig davon, ob das Bild im Shape gespeichert oder verknüpft ist, können Sie stets auf das tatsächliche Bild über die Methoden [toByteArray()](../../com.aspose.words/imagedata/\#toByteArray), [toImage()](../../com.aspose.words/imagedata/\#toImage) oder [save(java.lang.String)](../../com.aspose.words/imagedata/\#save-java.lang.String) zugreifen. Wenn das Bild im Shape gespeichert ist, können Sie es auch direkt über die Eigenschaft [getImageBytes()](../../com.aspose.words/imagedata/\#getImageBytes) / [setImageBytes(byte[])](../../com.aspose.words/imagedata/\#setImageBytes-byte) abrufen.

Um ein Bild in einem Shape zu speichern, verwenden Sie die Methode [setImage(java.lang.String)](../../com.aspose.words/imagedata/\#setImage-java.lang.String). Um ein Bild mit einem Shape zu verknüpfen, setzen Sie die Eigenschaft [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String).

 **Examples:** 

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```


[Working with Images]: https://docs.aspose.com/words/java/working-with-images/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fitImageToShape()](#fitImageToShape) | Passt die Bilddaten an den Shape-Rahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des Shape-Rahmens entspricht. |
| [getBiLevel()](#getBiLevel) | Bestimmt, ob ein Bild in Schwarzweiß angezeigt wird. |
| [getBorders()](#getBorders) | Ruft die Sammlung der Bildränder ab. |
| [getBrightness()](#getBrightness) | Ruft die Helligkeit des Bildes ab. |
| [getChromaKey()](#getChromaKey) | Definiert den Farbwert des Bildes, der als transparent behandelt wird. |
| [getContrast()](#getContrast) | Ruft den Kontrast für das angegebene Bild ab. |
| [getCropBottom()](#getCropBottom) | Definiert den Anteil der Bildentfernung von der Unterseite. |
| [getCropLeft()](#getCropLeft) | Definiert den Anteil der Bildentfernung von der linken Seite. |
| [getCropRight()](#getCropRight) | Definiert den Anteil der Bildentfernung von der rechten Seite. |
| [getCropTop()](#getCropTop) | Definiert den Anteil der Bildentfernung von der Oberseite. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getGrayScale()](#getGrayScale) | Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird. |
| [getImageBytes()](#getImageBytes) | Ruft die Rohbytes des im Shape gespeicherten Bildes ab. |
| [getImageSize()](#getImageSize) | Ruft die Informationen zur Bildgröße und Auflösung ab. |
| [getImageType()](#getImageType) | Ruft den Typ des Bildes ab. |
| [getSourceFullName()](#getSourceFullName) | Ruft den Pfad und den Namen der Quelldatei für das verknüpfte Bild ab. |
| [getTitle()](#getTitle) | Definiert den Titel eines Bildes. |
| [hasImage()](#hasImage) | Gibt  true  zurück, wenn das Shape Bildbytes enthält oder ein Bild verknüpft. |
| [isLink()](#isLink) | Gibt  true  zurück, wenn das Bild mit dem Shape verknüpft ist (wenn [getSourceFullName()](../../com.aspose.words/imagedata/#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/#setSourceFullName-java.lang.String) angegeben ist). |
| [isLinkOnly()](#isLinkOnly) | Gibt  true  zurück, wenn das Bild verknüpft und nicht im Dokument gespeichert ist. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Speichert das Bild in einer Datei. |
| [setBiLevel(boolean value)](#setBiLevel-boolean) | Bestimmt, ob ein Bild in Schwarzweiß angezeigt wird. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBrightness(double value)](#setBrightness-double) | Setzt die Helligkeit des Bildes. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color) | Definiert den Farbwert des Bildes, der als transparent behandelt wird. |
| [setContrast(double value)](#setContrast-double) | Setzt den Kontrast für das angegebene Bild. |
| [setCropBottom(double value)](#setCropBottom-double) | Definiert den Anteil der Bildentfernung von der Unterseite. |
| [setCropLeft(double value)](#setCropLeft-double) | Definiert den Anteil der Bildentfernung von der linken Seite. |
| [setCropRight(double value)](#setCropRight-double) | Definiert den Anteil der Bildentfernung von der rechten Seite. |
| [setCropTop(double value)](#setCropTop-double) | Definiert den Anteil der Bildentfernung von der Oberseite. |
| [setGrayScale(boolean value)](#setGrayScale-boolean) | Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Setzt das Bild, das das Shape anzeigt. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Setzt das Bild, das das Shape anzeigt. |
| [setImageBytes(byte[] value)](#setImageBytes-byte) | Setzt die Rohbytes des im Shape gespeicherten Bildes. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Setzt den Pfad und den Namen der Quelldatei für das verknüpfte Bild. |
| [setTitle(String value)](#setTitle-java.lang.String) | Definiert den Titel eines Bildes. |
| [toByteArray()](#toByteArray) | Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist. |
| [toImage()](#toImage) | Ruft das im Shape gespeicherte Bild als java  BufferedImage  Objekt ab. |
| [toStream()](#toStream) | Erstellt und gibt einen Stream zurück, der die Bildbytes enthält. |
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fitImageToShape() {#fitImageToShape}
```
public void fitImageToShape()
```


Passt die Bilddaten an den Shape-Rahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des Shape-Rahmens entspricht.

 **Examples:** 

Zeigt, wie man die Bilddaten an den Shape‑Rahmen anpasst.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert an image shape and leave its orientation in its default state.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 300.0, 450.0);
 shape.getImageData().setImage(getImageDir() + "Barcode.png");
 shape.getImageData().fitImageToShape();

 doc.save(getArtifactsDir() + "Shape.FitImageToShape.docx");
 
```

### getBiLevel() {#getBiLevel}
```
public boolean getBiLevel()
```


Bestimmt, ob ein Bild in Schwarzweiß angezeigt wird.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Ruft die Sammlung der Rahmen des Bildes ab. Rahmen wirken nur bei Inline‑Bildern.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of borders of the image.
### getBrightness() {#getBrightness}
```
public double getBrightness()
```


Ruft die Helligkeit des Bildes ab. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0.0 (dimmste) und 1.0 (hellste) sein.

 **Remarks:** 

Der Standardwert ist 0,5.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Die Helligkeit des Bildes.
### getChromaKey() {#getChromaKey}
```
public Color getChromaKey()
```


Definiert den Farbwert des Bildes, der als transparent behandelt wird.

 **Remarks:** 

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
java.awt.Color - Der entsprechende java.awt.Color‑Wert.
### getContrast() {#getContrast}
```
public double getContrast()
```


Ruft den Kontrast für das angegebene Bild ab. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0.0 (geringster Kontrast) und 1.0 (höchster Kontrast) sein.

 **Remarks:** 

Der Standardwert ist 0,5.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Der Kontrast für das angegebene Bild.
### getCropBottom() {#getCropBottom}
```
public double getCropBottom()
```


Definiert den Anteil der Bildentfernung von der Unterseite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Der entsprechende  double  Wert.
### getCropLeft() {#getCropLeft}
```
public double getCropLeft()
```


Definiert den Anteil der Bildentfernung von der linken Seite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Der entsprechende  double  Wert.
### getCropRight() {#getCropRight}
```
public double getCropRight()
```


Definiert den Anteil der Bildentfernung von der rechten Seite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Der entsprechende  double  Wert.
### getCropTop() {#getCropTop}
```
public double getCropTop()
```


Definiert den Anteil der Bildentfernung von der Oberseite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
double - Der entsprechende  double  Wert.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale}
```
public boolean getGrayScale()
```


Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Ruft die Rohbytes des im Shape gespeicherten Bildes ab.

 **Remarks:** 

Das Setzen des Wertes auf  null  oder ein leeres Array entfernt das Bild aus der Form.

Gibt  null  zurück, wenn das Bild nicht im Dokument gespeichert ist (z. B. ist das Bild in diesem Fall wahrscheinlich verlinkt).

 **Examples:** 

Zeigt, wie man eine Bilddatei aus den Rohbilddaten einer Form erstellt.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");
 Shape imgShape = (Shape) imgSourceDoc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertTrue(imgShape.hasImage());

 // ToByteArray() returns the array stored in the ImageBytes property.
 Assert.assertEquals(imgShape.getImageData().getImageBytes(), imgShape.getImageData().toByteArray());

 // Save the shape's image data to an image file in the local file system.
 InputStream imgStream = imgShape.getImageData().toStream();

 try {
     File imageFile = new File(getArtifactsDir() + "Drawing.GetDataFromImage.png");
     imageFile.createNewFile();
     copyInputStreamToFile(imgStream, imageFile);
 } finally {
     if (imgStream != null) imgStream.close();
 }
 
```

**Returns:**
byte[] - Die Rohbytes des im Shape gespeicherten Bildes.
### getImageSize() {#getImageSize}
```
public ImageSize getImageSize()
```


Liest die Informationen zur Bildgröße und Auflösung aus. (97679,6)

 **Remarks:** 

Wenn das Bild nur verlinkt und nicht im Dokument gespeichert ist, wird die Größe 0 zurückgegeben.

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
[ImageSize](../../com.aspose.words/imagesize/) - The information about image size and resolution.
### getImageType() {#getImageType}
```
public int getImageType()
```


Liest den Typ des Bildes aus. (97725,6)

 **Examples:** 

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

**Returns:**
int - Der Typ des Bildes. Der zurückgegebene Wert ist einer der Konstanten von [ImageType](../../com.aspose.words/imagetype/).
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Ruft den Pfad und den Namen der Quelldatei für das verknüpfte Bild ab.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Wenn [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) kein leerer String ist, ist das Bild verlinkt.

 **Examples:** 

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Returns:**
java.lang.String - Der Pfad und Name der Quelldatei für das verlinkte Bild.
### getTitle() {#getTitle}
```
public String getTitle()
```


Definiert den Titel eines Bildes.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


Gibt  true  zurück, wenn die Form Bildbytes enthält oder ein Bild verlinkt. (97641,6)

 **Examples:** 

Zeigt, wie man alle Bilder aus einem Dokument im Dateisystem speichert.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 // Shapes with the "HasImage" flag set store and display all the document's images.
 NodeCollection shapes = imgSourceDoc.getChildNodes(NodeType.SHAPE, true);
 Assert.assertEquals(shapes.getCount(), 10);

 // Go through each shape and save its image.
 for (int i = 0; i < shapes.getCount(); i++) {
     Shape shape = (Shape) shapes.get(i);
     ImageData imageData = shape.getImageData();

     if (imageData.hasImage()) {
         InputStream format = imageData.toStream();

         ImageInputStream iis = ImageIO.createImageInputStream(format);
         Iterator imageReaders = ImageIO.getImageReaders(iis);

         while (imageReaders.hasNext()) {
             ImageReader reader = imageReaders.next();
             String fileExtension = reader.getFormatName();

             OutputStream fileStream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("Drawing.SaveAllImages.{0}.{1}", i, fileExtension));
             try {
                 imageData.save(fileStream);
             } finally {
                 if (fileStream != null) fileStream.close();
             }
         }
     }
 }
 
```

**Returns:**
boolean -  true  wenn die Form Bildbytes enthält oder ein Bild verlinkt.
### isLink() {#isLink}
```
public boolean isLink()
```


Gibt  true  zurück, wenn das Bild mit der Form verlinkt ist (wenn [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) angegeben ist). (97749,6)

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
boolean -  true  wenn das Bild mit der Form verlinkt ist (wenn [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) angegeben ist).
### isLinkOnly() {#isLinkOnly}
```
public boolean isLinkOnly()
```


Gibt  true  zurück, wenn das Bild verlinkt und nicht im Dokument gespeichert ist. (97811,6)

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Returns:**
boolean -  true  wenn das Bild verlinkt und nicht im Dokument gespeichert ist.
### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Speichert das Bild in einer Datei.

 **Examples:** 

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Dateiname, unter dem das Bild gespeichert werden soll. |

### setBiLevel(boolean value) {#setBiLevel-boolean}
```
public void setBiLevel(boolean value)
```


Bestimmt, ob ein Bild in Schwarzweiß angezeigt wird.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double}
```
public void setBrightness(double value)
```


Setzt die Helligkeit des Bildes. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0.0 (dunkelste) und 1.0 (hellste) sein.

 **Remarks:** 

Der Standardwert ist 0,5.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Helligkeit des Bildes. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color}
```
public void setChromaKey(Color value)
```


Definiert den Farbwert des Bildes, der als transparent behandelt wird.

 **Remarks:** 

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Der entsprechende java.awt.Color-Wert. |

### setContrast(double value) {#setContrast-double}
```
public void setContrast(double value)
```


Setzt den Kontrast für das angegebene Bild. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0.0 (geringster Kontrast) und 1.0 (höchster Kontrast) sein.

 **Remarks:** 

Der Standardwert ist 0,5.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Kontrast für das angegebene Bild. |

### setCropBottom(double value) {#setCropBottom-double}
```
public void setCropBottom(double value)
```


Definiert den Anteil der Bildentfernung von der Unterseite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setCropLeft(double value) {#setCropLeft-double}
```
public void setCropLeft(double value)
```


Definiert den Anteil der Bildentfernung von der linken Seite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setCropRight(double value) {#setCropRight-double}
```
public void setCropRight(double value)
```


Definiert den Anteil der Bildentfernung von der rechten Seite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setCropTop(double value) {#setCropTop-double}
```
public void setCropTop(double value)
```


Definiert den Anteil der Bildentfernung von der Oberseite.

 **Remarks:** 

Der Betrag des Zuschneidens kann von -1.0 bis 1.0 reichen. Der Standardwert ist 0. Beachten Sie, dass ein Wert von 1 kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der beschnittenen Kante nach innen gedrückt wird (der leere Raum zwischen dem Bild und der beschnittenen Kante wird mit der Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gedehnt wird, um in die Form zu passen.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setGrayScale(boolean value) {#setGrayScale-boolean}
```
public void setGrayScale(boolean value)
```


Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Setzt das Bild, das das Shape anzeigt.

 **Examples:** 

Zeigt, wie man Bilder aus dem lokalen Dateisystem in einem Dokument anzeigt.

```

 Document doc = new Document();

 // Below are two ways of getting an image from a file in the local file system.
 // 1 -  Create an image object from an image file:
 BufferedImage srcImage = ImageIO.read(new File(getImageDir() + "Logo.jpg"));

 // To display an image in a document, we will need to create a shape
 // which will contain an image, and then append it to the document's body.
 Shape imgShape = new Shape(doc, ShapeType.IMAGE);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(imgShape);
 imgShape.getImageData().setImage(srcImage);
 srcImage.flush();

 // 2 -  Open an image file from the local file system using a stream:
 InputStream stream = new FileInputStream(getImageDir() + "Logo.jpg");
 try {
     imgShape = new Shape(doc, ShapeType.IMAGE);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(imgShape);
     imgShape.getImageData().setImage(stream);
     imgShape.setLeft(150.0f);
 } finally {
     if (stream != null) stream.close();
 }

 doc.save(getArtifactsDir() + "Drawing.ImportImage.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | java.awt.image.BufferedImage | Das Bildobjekt. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Setzt das Bild, das das Shape anzeigt.

 **Examples:** 

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Die Bilddatei. Kann ein Dateiname oder eine URL sein. |

### setImageBytes(byte[] value) {#setImageBytes-byte}
```
public void setImageBytes(byte[] value)
```


Setzt die Rohbytes des im Shape gespeicherten Bildes.

 **Remarks:** 

Das Setzen des Wertes auf  null  oder ein leeres Array entfernt das Bild aus der Form.

Gibt  null  zurück, wenn das Bild nicht im Dokument gespeichert ist (z. B. ist das Bild in diesem Fall wahrscheinlich verlinkt).

 **Examples:** 

Zeigt, wie man eine Bilddatei aus den Rohbilddaten einer Form erstellt.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");
 Shape imgShape = (Shape) imgSourceDoc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertTrue(imgShape.hasImage());

 // ToByteArray() returns the array stored in the ImageBytes property.
 Assert.assertEquals(imgShape.getImageData().getImageBytes(), imgShape.getImageData().toByteArray());

 // Save the shape's image data to an image file in the local file system.
 InputStream imgStream = imgShape.getImageData().toStream();

 try {
     File imageFile = new File(getArtifactsDir() + "Drawing.GetDataFromImage.png");
     imageFile.createNewFile();
     copyInputStreamToFile(imgStream, imageFile);
 } finally {
     if (imgStream != null) imgStream.close();
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | byte[] | Die Rohbytes des Bildes, die in der Form gespeichert sind. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Setzt den Pfad und den Namen der Quelldatei für das verknüpfte Bild.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Wenn [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) kein leerer String ist, ist das Bild verlinkt.

 **Examples:** 

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Pfad und Name der Quelldatei für das verknüpfte Bild. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Definiert den Titel eines Bildes.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie man die Bilddaten eines Shapes bearbeitet.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 Shape sourceShape = (Shape) imgSourceDoc.getChildNodes(NodeType.SHAPE, true).get(0);

 Document dstDoc = new Document();

 // Import a shape from the source document and append it to the first paragraph.
 Shape importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 // The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
 ImageData imageData = importedShape.getImageData();
 imageData.setTitle("Imported Image");

 Assert.assertTrue(imageData.hasImage());

 // If an image has no borders, its ImageData object will define the border color as empty.
 Assert.assertEquals(imageData.getBorders().getCount(), 4);
 Assert.assertEquals(imageData.getBorders().get(0).getColor(), new Color(0, true));

 // This image does not link to another shape or image file in the local file system.
 Assert.assertFalse(imageData.isLink());
 Assert.assertFalse(imageData.isLinkOnly());

 // The "Brightness" and "Contrast" properties define image brightness and contrast
 // on a 0-1 scale, with the default value at 0.5.
 imageData.setBrightness(0.8d);
 imageData.setContrast(1.0d);

 // The above brightness and contrast values have created an image with a lot of white.
 // We can select a color with the ChromaKey property to replace with transparency, such as white.
 imageData.setChromaKey(Color.WHITE);

 // Import the source shape again and set the image to monochrome.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setGrayScale(true);

 // Import the source shape again to create a third image and set it to BiLevel.
 // BiLevel sets every pixel to either black or white, whichever is closer to the original color.
 importedShape = (Shape) dstDoc.importNode(sourceShape, true);
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(importedShape);

 importedShape.getImageData().setBiLevel(true);

 // Cropping is determined on a 0-1 scale. Cropping a side by 0.3
 // will crop 30% of the image out at the cropped side.
 importedShape.getImageData().setCropBottom(0.3d);
 importedShape.getImageData().setCropLeft(0.3d);
 importedShape.getImageData().setCropTop(0.3d);
 importedShape.getImageData().setCropRight(0.3d);

 dstDoc.save(getArtifactsDir() + "Drawing.ImageData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist.

 **Remarks:** 

Wenn das Bild verknüpft ist, wird das Bild jedes Mal heruntergeladen, wenn es aufgerufen wird.

 **Examples:** 

Zeigt, wie man eine Bilddatei aus den Rohbilddaten einer Form erstellt.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");
 Shape imgShape = (Shape) imgSourceDoc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertTrue(imgShape.hasImage());

 // ToByteArray() returns the array stored in the ImageBytes property.
 Assert.assertEquals(imgShape.getImageData().getImageBytes(), imgShape.getImageData().toByteArray());

 // Save the shape's image data to an image file in the local file system.
 InputStream imgStream = imgShape.getImageData().toStream();

 try {
     File imageFile = new File(getArtifactsDir() + "Drawing.GetDataFromImage.png");
     imageFile.createNewFile();
     copyInputStreamToFile(imgStream, imageFile);
 } finally {
     if (imgStream != null) imgStream.close();
 }
 
```

**Returns:**
byte[] -
### toImage() {#toImage}
```
public BufferedImage toImage()
```


Ruft das im Shape gespeicherte Bild als java  BufferedImage  Objekt ab.

 **Remarks:** 

Versucht, jedes Mal, wenn diese Methode aufgerufen wird, ein neues  java.awt.image.BufferedImage  Objekt aus Bildbytes zu erstellen. Wenn  javax.imageio.ImageReader  die Bildbytes (emf, wmf, tiff usw.) nicht lesen kann, gibt die Methode  null  zurück.

Es liegt in der Verantwortung des Aufrufers, das Bildobjekt zu entsorgen.

 **Examples:** 

Zeigt, wie man alle Bilder aus einem Dokument im Dateisystem speichert.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");

 // Shapes with the "HasImage" flag set store and display all the document's images.
 NodeCollection shapes = imgSourceDoc.getChildNodes(NodeType.SHAPE, true);
 Assert.assertEquals(shapes.getCount(), 10);

 // Go through each shape and save its image.
 for (int i = 0; i < shapes.getCount(); i++) {
     Shape shape = (Shape) shapes.get(i);
     ImageData imageData = shape.getImageData();

     if (imageData.hasImage()) {
         InputStream format = imageData.toStream();

         ImageInputStream iis = ImageIO.createImageInputStream(format);
         Iterator imageReaders = ImageIO.getImageReaders(iis);

         while (imageReaders.hasNext()) {
             ImageReader reader = imageReaders.next();
             String fileExtension = reader.getFormatName();

             OutputStream fileStream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("Drawing.SaveAllImages.{0}.{1}", i, fileExtension));
             try {
                 imageData.save(fileStream);
             } finally {
                 if (fileStream != null) fileStream.close();
             }
         }
     }
 }
 
```

**Returns:**
java.awt.image.BufferedImage -
### toStream() {#toStream}
```
public InputStream toStream()
```


Erstellt und gibt einen Stream zurück, der die Bildbytes enthält.  Dies ist noch nicht nach Java portiert.

 **Remarks:** 

Wenn die Bildbytes in der Form gespeichert sind, wird ein  Objekt erstellt und zurückgegeben.

Wenn das Bild verknüpft ist und in einer Datei gespeichert ist, wird die Datei geöffnet und ein  Objekt zurückgegeben.

Wenn das Bild verknüpft ist und in einer externen URL gespeichert ist, wird die URL geöffnet und ein  Objekt zurückgegeben.

Liegt es in der Verantwortung des Aufrufers, das Stream-Objekt zu entsorgen.

 **Examples:** 

Zeigt, wie man eine Bilddatei aus den Rohbilddaten einer Form erstellt.

```

 Document imgSourceDoc = new Document(getMyDir() + "Images.docx");
 Shape imgShape = (Shape) imgSourceDoc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertTrue(imgShape.hasImage());

 // ToByteArray() returns the array stored in the ImageBytes property.
 Assert.assertEquals(imgShape.getImageData().getImageBytes(), imgShape.getImageData().toByteArray());

 // Save the shape's image data to an image file in the local file system.
 InputStream imgStream = imgShape.getImageData().toStream();

 try {
     File imageFile = new File(getArtifactsDir() + "Drawing.GetDataFromImage.png");
     imageFile.createNewFile();
     copyInputStreamToFile(imgStream, imageFile);
 } finally {
     if (imgStream != null) imgStream.close();
 }
 
```

**Returns:**
java.io.InputStream

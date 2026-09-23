---
title: "ImageData"
linktitle: "ImageData"
second_title: "Aspose.Words per Java"
description: "Definisce un'immagine per una shape in Java."
type: docs
weight: 391
url: /it/java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

Definisce un'immagine per una forma.

Per saperne di più, visita l'articolo di documentazione [ Working with Images ][Working with Images].

 **Remarks:** 

Utilizza la proprietà [Shape.getImageData()](../../com.aspose.words/shape/\#getImageData) per accedere e modificare l'immagine all'interno di una shape. Non crei istanze della classe [ImageData](../../com.aspose.words/imagedata/) direttamente.

Un'immagine può essere memorizzata all'interno di una shape, collegata a un file esterno o entrambe le cose (collegata e memorizzata nel documento).

Indipendentemente dal fatto che l'immagine sia memorizzata all'interno della shape o collegata, puoi sempre accedere all'immagine reale utilizzando i metodi [toByteArray()](../../com.aspose.words/imagedata/\#toByteArray), [toImage()](../../com.aspose.words/imagedata/\#toImage) o [save(java.lang.String)](../../com.aspose.words/imagedata/\#save-java.lang.String). Se l'immagine è memorizzata all'interno della shape, puoi anche accedervi direttamente tramite la proprietà [getImageBytes()](../../com.aspose.words/imagedata/\#getImageBytes) / [setImageBytes(byte[])](../../com.aspose.words/imagedata/\#setImageBytes-byte).

Per memorizzare un'immagine all'interno di una shape utilizza il metodo [setImage(java.lang.String)](../../com.aspose.words/imagedata/\#setImage-java.lang.String). Per collegare un'immagine a una shape, imposta la proprietà [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String).

 **Examples:** 

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file individuali.

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

Mostra come inserire un'immagine collegata in un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fitImageToShape()](#fitImageToShape) | Adatta i dati dell'immagine al riquadro della Shape in modo che il rapporto d'aspetto dei dati dell'immagine corrisponda al rapporto d'aspetto del riquadro della Shape. |
| [getBiLevel()](#getBiLevel) | Determina se un'immagine verrà visualizzata in bianco e nero. |
| [getBorders()](#getBorders) | Ottiene la collezione dei bordi dell'immagine. |
| [getBrightness()](#getBrightness) | Ottiene la luminosità dell'immagine. |
| [getChromaKey()](#getChromaKey) | Definisce il valore di colore dell'immagine che sarà trattato come trasparente. |
| [getContrast()](#getContrast) | Ottiene il contrasto per l'immagine specificata. |
| [getCropBottom()](#getCropBottom) | Definisce la frazione di rimozione dell'immagine dal lato inferiore. |
| [getCropLeft()](#getCropLeft) | Definisce la frazione di rimozione dell'immagine dal lato sinistro. |
| [getCropRight()](#getCropRight) | Definisce la frazione di rimozione dell'immagine dal lato destro. |
| [getCropTop()](#getCropTop) | Definisce la frazione di rimozione dell'immagine dal lato superiore. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getGrayScale()](#getGrayScale) | Determina se un'immagine verrà visualizzata in modalità scala di grigi. |
| [getImageBytes()](#getImageBytes) | Ottiene i byte grezzi dell'immagine memorizzata nella forma. |
| [getImageSize()](#getImageSize) | Ottiene le informazioni sulle dimensioni e sulla risoluzione dell'immagine. |
| [getImageType()](#getImageType) | Ottiene il tipo dell'immagine. |
| [getSourceFullName()](#getSourceFullName) | Ottiene il percorso e il nome del file sorgente per l'immagine collegata. |
| [getTitle()](#getTitle) | Definisce il titolo di un'immagine. |
| [hasImage()](#hasImage) | Restituisce  true  se la forma ha byte dell'immagine o collega un'immagine. |
| [isLink()](#isLink) | Restituisce  true  se l'immagine è collegata alla forma (quando [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) è specificato). |
| [isLinkOnly()](#isLinkOnly) | Restituisce  true  se l'immagine è collegata e non è memorizzata nel documento. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Salva l'immagine in un file. |
| [setBiLevel(boolean value)](#setBiLevel-boolean) | Determina se un'immagine verrà visualizzata in bianco e nero. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBrightness(double value)](#setBrightness-double) | Imposta la luminosità dell'immagine. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color) | Definisce il valore di colore dell'immagine che sarà trattato come trasparente. |
| [setContrast(double value)](#setContrast-double) | Imposta il contrasto per l'immagine specificata. |
| [setCropBottom(double value)](#setCropBottom-double) | Definisce la frazione di rimozione dell'immagine dal lato inferiore. |
| [setCropLeft(double value)](#setCropLeft-double) | Definisce la frazione di rimozione dell'immagine dal lato sinistro. |
| [setCropRight(double value)](#setCropRight-double) | Definisce la frazione di rimozione dell'immagine dal lato destro. |
| [setCropTop(double value)](#setCropTop-double) | Definisce la frazione di rimozione dell'immagine dal lato superiore. |
| [setGrayScale(boolean value)](#setGrayScale-boolean) | Determina se un'immagine verrà visualizzata in modalità scala di grigi. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Imposta l'immagine che la forma visualizza. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Imposta l'immagine che la forma visualizza. |
| [setImageBytes(byte[] value)](#setImageBytes-byte) | Imposta i byte grezzi dell'immagine memorizzata nella forma. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Imposta il percorso e il nome del file sorgente per l'immagine collegata. |
| [setTitle(String value)](#setTitle-java.lang.String) | Definisce il titolo di un'immagine. |
| [toByteArray()](#toByteArray) | Restituisce i byte dell'immagine per qualsiasi immagine indipendentemente dal fatto che l'immagine sia memorizzata o collegata. |
| [toImage()](#toImage) | Ottiene l'immagine memorizzata nella forma come oggetto java  BufferedImage . |
| [toStream()](#toStream) | Crea e restituisce un flusso che contiene i byte dell'immagine. |
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fitImageToShape() {#fitImageToShape}
```
public void fitImageToShape()
```


Adatta i dati dell'immagine al riquadro della Shape in modo che il rapporto d'aspetto dei dati dell'immagine corrisponda al rapporto d'aspetto del riquadro della Shape.

 **Examples:** 

Mostra come adattare i dati dell'immagine al riquadro della Forma.

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


Determina se un'immagine verrà visualizzata in bianco e nero.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
boolean - Il valore booleano corrispondente.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Ottiene la collezione dei bordi dell'immagine. I bordi hanno effetto solo per le immagini in linea.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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


Ottiene la luminosità dell'immagine. Il valore per questa proprietà deve essere un numero da 0.0 (più scuro) a 1.0 (più luminoso).

 **Remarks:** 

Il valore predefinito è 0.5.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - La luminosità dell'immagine.
### getChromaKey() {#getChromaKey}
```
public Color getChromaKey()
```


Definisce il valore di colore dell'immagine che sarà trattato come trasparente.

 **Remarks:** 

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
java.awt.Color - Il valore java.awt.Color corrispondente.
### getContrast() {#getContrast}
```
public double getContrast()
```


Restituisce il contrasto per l'immagine specificata. Il valore di questa proprietà deve essere un numero da 0.0 (il contrasto più basso) a 1.0 (il contrasto più alto).

 **Remarks:** 

Il valore predefinito è 0.5.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - Il contrasto per l'immagine specificata.
### getCropBottom() {#getCropBottom}
```
public double getCropBottom()
```


Definisce la frazione di rimozione dell'immagine dal lato inferiore.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - Il valore double corrispondente.
### getCropLeft() {#getCropLeft}
```
public double getCropLeft()
```


Definisce la frazione di rimozione dell'immagine dal lato sinistro.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - Il valore double corrispondente.
### getCropRight() {#getCropRight}
```
public double getCropRight()
```


Definisce la frazione di rimozione dell'immagine dal lato destro.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - Il valore double corrispondente.
### getCropTop() {#getCropTop}
```
public double getCropTop()
```


Definisce la frazione di rimozione dell'immagine dal lato superiore.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
double - Il valore double corrispondente.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale}
```
public boolean getGrayScale()
```


Determina se un'immagine verrà visualizzata in modalità scala di grigi.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
boolean - Il valore booleano corrispondente.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Ottiene i byte grezzi dell'immagine memorizzata nella forma.

 **Remarks:** 

Impostare il valore a null o a un array vuoto rimuoverà l'immagine dalla forma.

Restituisce null se l'immagine non è memorizzata nel documento (ad es. l'immagine è probabilmente collegata in questo caso).

 **Examples:** 

Mostra come creare un file immagine dai dati grezzi dell'immagine di una forma.

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
byte[] - I byte grezzi dell'immagine memorizzata nella forma.
### getImageSize() {#getImageSize}
```
public ImageSize getImageSize()
```


Restituisce le informazioni sulla dimensione e sulla risoluzione dell'immagine. (97679,6)

 **Remarks:** 

Se l'immagine è solo collegata e non memorizzata nel documento, restituisce dimensione zero.

 **Examples:** 

Mostra come ridimensionare una forma con un'immagine.

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


Restituisce il tipo dell'immagine. (97725,6)

 **Examples:** 

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file individuali.

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
int - Il tipo dell'immagine. Il valore restituito è una delle costanti [ImageType](../../com.aspose.words/imagetype/).
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Ottiene il percorso e il nome del file sorgente per l'immagine collegata.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Se [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) non è una stringa vuota, l'immagine è collegata.

 **Examples:** 

Mostra come inserire un'immagine collegata in un documento.

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
java.lang.String - Il percorso e il nome del file sorgente per l'immagine collegata.
### getTitle() {#getTitle}
```
public String getTitle()
```


Definisce il titolo di un'immagine.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
java.lang.String - Il valore java.lang.String corrispondente.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


Restituisce true se la forma contiene byte dell'immagine o collega un'immagine. (97641,6)

 **Examples:** 

Mostra come salvare tutte le immagini da un documento nel file system.

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
boolean - true se la forma contiene byte dell'immagine o collega un'immagine.
### isLink() {#isLink}
```
public boolean isLink()
```


Restituisce true se l'immagine è collegata alla forma (quando [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) è specificato). (97749,6)

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
boolean - true se l'immagine è collegata alla forma (quando [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) è specificato).
### isLinkOnly() {#isLinkOnly}
```
public boolean isLinkOnly()
```


Restituisce true se l'immagine è collegata e non è memorizzata nel documento. (97811,6)

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
boolean - true se l'immagine è collegata e non è memorizzata nel documento.
### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Salva l'immagine in un file.

 **Examples:** 

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file individuali.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String | Il nome del file in cui salvare l'immagine. |

### setBiLevel(boolean value) {#setBiLevel-boolean}
```
public void setBiLevel(boolean value)
```


Determina se un'immagine verrà visualizzata in bianco e nero.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |
| valore | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double}
```
public void setBrightness(double value)
```


Imposta la luminosità dell'immagine. Il valore di questa proprietà deve essere un numero da 0.0 (la più scura) a 1.0 (la più luminosa).

 **Remarks:** 

Il valore predefinito è 0.5.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La luminosità dell'immagine. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color}
```
public void setChromaKey(Color value)
```


Definisce il valore di colore dell'immagine che sarà trattato come trasparente.

 **Remarks:** 

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il valore java.awt.Color corrispondente. |

### setContrast(double value) {#setContrast-double}
```
public void setContrast(double value)
```


Imposta il contrasto per l'immagine specificata. Il valore di questa proprietà deve essere un numero da 0.0 (il contrasto più basso) a 1.0 (il contrasto più alto).

 **Remarks:** 

Il valore predefinito è 0.5.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il contrasto per l'immagine specificata. |

### setCropBottom(double value) {#setCropBottom-double}
```
public void setCropBottom(double value)
```


Definisce la frazione di rimozione dell'immagine dal lato inferiore.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setCropLeft(double value) {#setCropLeft-double}
```
public void setCropLeft(double value)
```


Definisce la frazione di rimozione dell'immagine dal lato sinistro.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setCropRight(double value) {#setCropRight-double}
```
public void setCropRight(double value)
```


Definisce la frazione di rimozione dell'immagine dal lato destro.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setCropTop(double value) {#setCropTop-double}
```
public void setCropTop(double value)
```


Definisce la frazione di rimozione dell'immagine dal lato superiore.

 **Remarks:** 

La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setGrayScale(boolean value) {#setGrayScale-boolean}
```
public void setGrayScale(boolean value)
```


Determina se un'immagine verrà visualizzata in modalità scala di grigi.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Imposta l'immagine che la forma visualizza.

 **Examples:** 

Mostra come visualizzare le immagini dal file system locale in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| immagine | java.awt.image.BufferedImage | L'oggetto immagine. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Imposta l'immagine che la forma visualizza.

 **Examples:** 

Mostra come inserire un'immagine collegata in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String | Il file immagine. Può essere un nome file o un URL. |

### setImageBytes(byte[] value) {#setImageBytes-byte}
```
public void setImageBytes(byte[] value)
```


Imposta i byte grezzi dell'immagine memorizzata nella forma.

 **Remarks:** 

Impostare il valore a null o a un array vuoto rimuoverà l'immagine dalla forma.

Restituisce null se l'immagine non è memorizzata nel documento (ad es. l'immagine è probabilmente collegata in questo caso).

 **Examples:** 

Mostra come creare un file immagine dai dati grezzi dell'immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | I byte grezzi dell'immagine memorizzati nella forma. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Imposta il percorso e il nome del file sorgente per l'immagine collegata.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Se [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) non è una stringa vuota, l'immagine è collegata.

 **Examples:** 

Mostra come inserire un'immagine collegata in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il percorso e il nome del file sorgente per l'immagine collegata. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Definisce il titolo di un'immagine.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come modificare i dati immagine di una forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


Restituisce i byte dell'immagine per qualsiasi immagine indipendentemente dal fatto che l'immagine sia memorizzata o collegata.

 **Remarks:** 

Se l'immagine è collegata, scarica l'immagine ogni volta che viene chiamata.

 **Examples:** 

Mostra come creare un file immagine dai dati grezzi dell'immagine di una forma.

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


Ottiene l'immagine memorizzata nella forma come oggetto java  BufferedImage .

 **Remarks:** 

Cerca di creare un nuovo  java.awt.image.BufferedImage  oggetto dai byte dell'immagine ogni volta che questo metodo viene chiamato. Se  javax.imageio.ImageReader  non può leggere i byte dell'immagine (emf, wmf, tiff, ecc.) il metodo restituisce  null .

È responsabilità del chiamante rilasciare l'oggetto immagine.

 **Examples:** 

Mostra come salvare tutte le immagini da un documento nel file system.

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


Crea e restituisce uno stream che contiene i byte dell'immagine.  Questo non è ancora stato portato su Java.

 **Remarks:** 

Se i byte dell'immagine sono memorizzati nella forma, crea e restituisce un  oggetto.

Se l'immagine è collegata e memorizzata in un file, apre il file e restituisce un  oggetto.

Se l'immagine è collegata e memorizzata in un URL esterno, apre l'URL e restituisce un  oggetto.

È responsabilità del chiamante rilasciare l'oggetto stream.

 **Examples:** 

Mostra come creare un file immagine dai dati grezzi dell'immagine di una forma.

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

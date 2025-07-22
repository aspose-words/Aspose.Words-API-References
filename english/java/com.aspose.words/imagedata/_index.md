---
title: ImageData
linktitle: ImageData
second_title: Aspose.Words for Java
description: Defines an image for a shape in Java.
type: docs
weight: 386
url: /java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

Defines an image for a shape.

To learn more, visit the [ Working with Images ][Working with Images] documentation article.

 **Remarks:** 

Use the [Shape.getImageData()](../../com.aspose.words/shape/\#getImageData) property to access and modify the image inside a shape. You do not create instances of the [ImageData](../../com.aspose.words/imagedata/) class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual image using the [toByteArray()](../../com.aspose.words/imagedata/\#toByteArray), [toImage()](../../com.aspose.words/imagedata/\#toImage) or [save(java.lang.String)](../../com.aspose.words/imagedata/\#save-java.lang.String) methods. If the image is stored inside the shape, you can also directly access it using the [getImageBytes()](../../com.aspose.words/imagedata/\#getImageBytes) / [setImageBytes(byte[])](../../com.aspose.words/imagedata/\#setImageBytes-byte) property.

To store an image inside a shape use the [setImage(java.lang.String)](../../com.aspose.words/imagedata/\#setImage-java.lang.String) method. To link an image to a shape, set the [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) property.

 **Examples:** 

Shows how to extract images from a document, and save them to the local file system as individual files.

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

Shows how to insert a linked image into a document.

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
## Methods

| Method | Description |
| --- | --- |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fitImageToShape()](#fitImageToShape) | Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame. |
| [getBiLevel()](#getBiLevel) | Determines whether an image will be displayed in black and white. |
| [getBorders()](#getBorders) | Gets the collection of borders of the image. |
| [getBrightness()](#getBrightness) | Gets the brightness of the picture. |
| [getChromaKey()](#getChromaKey) | Defines the color value of the image that will be treated as transparent. |
| [getContrast()](#getContrast) | Gets the contrast for the specified picture. |
| [getCropBottom()](#getCropBottom) | Defines the fraction of picture removal from the bottom side. |
| [getCropLeft()](#getCropLeft) | Defines the fraction of picture removal from the left side. |
| [getCropRight()](#getCropRight) | Defines the fraction of picture removal from the right side. |
| [getCropTop()](#getCropTop) | Defines the fraction of picture removal from the top side. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getGrayScale()](#getGrayScale) | Determines whether a picture will display in grayscale mode. |
| [getImageBytes()](#getImageBytes) | Gets the raw bytes of the image stored in the shape. |
| [getImageSize()](#getImageSize) | Gets the information about image size and resolution. |
| [getImageType()](#getImageType) | Gets the type of the image. |
| [getSourceFullName()](#getSourceFullName) | Gets the path and name of the source file for the linked image. |
| [getTitle()](#getTitle) | Defines the title of an image. |
| [hasImage()](#hasImage) | Returns  true  if the shape has image bytes or links an image. |
| [isLink()](#isLink) | Returns  true  if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) is specified). |
| [isLinkOnly()](#isLinkOnly) | Returns  true  if the image is linked and not stored in the document. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the image into a file. |
| [setBiLevel(boolean value)](#setBiLevel-boolean) | Determines whether an image will be displayed in black and white. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBrightness(double value)](#setBrightness-double) | Sets the brightness of the picture. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color) | Defines the color value of the image that will be treated as transparent. |
| [setContrast(double value)](#setContrast-double) | Sets the contrast for the specified picture. |
| [setCropBottom(double value)](#setCropBottom-double) | Defines the fraction of picture removal from the bottom side. |
| [setCropLeft(double value)](#setCropLeft-double) | Defines the fraction of picture removal from the left side. |
| [setCropRight(double value)](#setCropRight-double) | Defines the fraction of picture removal from the right side. |
| [setCropTop(double value)](#setCropTop-double) | Defines the fraction of picture removal from the top side. |
| [setGrayScale(boolean value)](#setGrayScale-boolean) | Determines whether a picture will display in grayscale mode. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Sets the image that the shape displays. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Sets the image that the shape displays. |
| [setImageBytes(byte[] value)](#setImageBytes-byte) | Sets the raw bytes of the image stored in the shape. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Sets the path and name of the source file for the linked image. |
| [setTitle(String value)](#setTitle-java.lang.String) | Defines the title of an image. |
| [toByteArray()](#toByteArray) | Returns image bytes for any image regardless whether the image is stored or linked. |
| [toImage()](#toImage) | Gets the image stored in the shape as a java  BufferedImage  object. |
| [toStream()](#toStream) | Creates and returns a stream that contains the image bytes. |
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fitImageToShape() {#fitImageToShape}
```
public void fitImageToShape()
```


Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame.

 **Examples:** 

Shows hot to fit the image data to Shape frame.

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


Determines whether an image will be displayed in black and white.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to edit a shape's image data.

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
boolean - The corresponding  boolean  value.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gets the collection of borders of the image. Borders only have effect for inline images.

 **Examples:** 

Shows how to edit a shape's image data.

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


Gets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest).

 **Remarks:** 

The default value is 0.5.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The brightness of the picture.
### getChromaKey() {#getChromaKey}
```
public Color getChromaKey()
```


Defines the color value of the image that will be treated as transparent.

 **Remarks:** 

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
java.awt.Color - The corresponding java.awt.Color value.
### getContrast() {#getContrast}
```
public double getContrast()
```


Gets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast).

 **Remarks:** 

The default value is 0.5.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The contrast for the specified picture.
### getCropBottom() {#getCropBottom}
```
public double getCropBottom()
```


Defines the fraction of picture removal from the bottom side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The corresponding  double  value.
### getCropLeft() {#getCropLeft}
```
public double getCropLeft()
```


Defines the fraction of picture removal from the left side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The corresponding  double  value.
### getCropRight() {#getCropRight}
```
public double getCropRight()
```


Defines the fraction of picture removal from the right side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The corresponding  double  value.
### getCropTop() {#getCropTop}
```
public double getCropTop()
```


Defines the fraction of picture removal from the top side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
double - The corresponding  double  value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale}
```
public boolean getGrayScale()
```


Determines whether a picture will display in grayscale mode.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to edit a shape's image data.

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
boolean - The corresponding  boolean  value.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Gets the raw bytes of the image stored in the shape.

 **Remarks:** 

Setting the value to  null  or an empty array will remove the image from the shape.

Returns  null  if the image is not stored in the document (e.g the image is probably linked in this case).

 **Examples:** 

Shows how to create an image file from a shape's raw image data.

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
byte[] - The raw bytes of the image stored in the shape.
### getImageSize() {#getImageSize}
```
public ImageSize getImageSize()
```


Gets the information about image size and resolution. (46591,6)

 **Remarks:** 

If the image is linked only and not stored in the document, returns zero size.

 **Examples:** 

Shows how to resize a shape with an image.

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


Gets the type of the image. (46637,6)

 **Examples:** 

Shows how to extract images from a document, and save them to the local file system as individual files.

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
int - The type of the image. The returned value is one of [ImageType](../../com.aspose.words/imagetype/) constants.
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Gets the path and name of the source file for the linked image.

 **Remarks:** 

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) is not an empty string, the image is linked.

 **Examples:** 

Shows how to insert a linked image into a document.

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
java.lang.String - The path and name of the source file for the linked image.
### getTitle() {#getTitle}
```
public String getTitle()
```


Defines the title of an image.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to edit a shape's image data.

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
java.lang.String - The corresponding java.lang.String value.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


Returns  true  if the shape has image bytes or links an image. (46553,6)

 **Examples:** 

Shows how to save all images from a document to the file system.

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
boolean -  true  if the shape has image bytes or links an image.
### isLink() {#isLink}
```
public boolean isLink()
```


Returns  true  if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) is specified). (46661,6)

 **Examples:** 

Shows how to edit a shape's image data.

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
boolean -  true  if the image is linked to the shape (when [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) is specified).
### isLinkOnly() {#isLinkOnly}
```
public boolean isLinkOnly()
```


Returns  true  if the image is linked and not stored in the document. (46723,6)

 **Examples:** 

Shows how to edit a shape's image data.

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
boolean -  true  if the image is linked and not stored in the document.
### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Saves the image into a file.

 **Examples:** 

Shows how to extract images from a document, and save them to the local file system as individual files.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file name where to save the image. |

### setBiLevel(boolean value) {#setBiLevel-boolean}
```
public void setBiLevel(boolean value)
```


Determines whether an image will be displayed in black and white.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double}
```
public void setBrightness(double value)
```


Sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest).

 **Remarks:** 

The default value is 0.5.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The brightness of the picture. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color}
```
public void setChromaKey(Color value)
```


Defines the color value of the image that will be treated as transparent.

 **Remarks:** 

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setContrast(double value) {#setContrast-double}
```
public void setContrast(double value)
```


Sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast).

 **Remarks:** 

The default value is 0.5.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The contrast for the specified picture. |

### setCropBottom(double value) {#setCropBottom-double}
```
public void setCropBottom(double value)
```


Defines the fraction of picture removal from the bottom side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropLeft(double value) {#setCropLeft-double}
```
public void setCropLeft(double value)
```


Defines the fraction of picture removal from the left side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropRight(double value) {#setCropRight-double}
```
public void setCropRight(double value)
```


Defines the fraction of picture removal from the right side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setCropTop(double value) {#setCropTop-double}
```
public void setCropTop(double value)
```


Defines the fraction of picture removal from the top side.

 **Remarks:** 

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setGrayScale(boolean value) {#setGrayScale-boolean}
```
public void setGrayScale(boolean value)
```


Determines whether a picture will display in grayscale mode.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Sets the image that the shape displays.

 **Examples:** 

Shows how to display images from the local file system in a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | The image object. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Sets the image that the shape displays.

 **Examples:** 

Shows how to insert a linked image into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The image file. Can be a file name or a URL. |

### setImageBytes(byte[] value) {#setImageBytes-byte}
```
public void setImageBytes(byte[] value)
```


Sets the raw bytes of the image stored in the shape.

 **Remarks:** 

Setting the value to  null  or an empty array will remove the image from the shape.

Returns  null  if the image is not stored in the document (e.g the image is probably linked in this case).

 **Examples:** 

Shows how to create an image file from a shape's raw image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The raw bytes of the image stored in the shape. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Sets the path and name of the source file for the linked image.

 **Remarks:** 

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) is not an empty string, the image is linked.

 **Examples:** 

Shows how to insert a linked image into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The path and name of the source file for the linked image. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Defines the title of an image.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to edit a shape's image data.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


Returns image bytes for any image regardless whether the image is stored or linked.

 **Remarks:** 

If the image is linked, downloads the image every time it is called.

 **Examples:** 

Shows how to create an image file from a shape's raw image data.

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


Gets the image stored in the shape as a java  BufferedImage  object.

 **Remarks:** 

Tries to create a new  java.awt.image.BufferedImage  object from image bytes every time this method is called. If  javax.imageio.ImageReader  can't read image bytes (emf, wmf, tiff, etc.) the method returns  null .

It is the responsibility of the caller to dispose the image object.

 **Examples:** 

Shows how to save all images from a document to the file system.

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


Creates and returns a stream that contains the image bytes.  This is not ported to Java yet.

 **Remarks:** 

If the image bytes are stored in the shape, creates and returns a  object.

If the image is linked and stored in a file, opens the file and returns a  object.

If the image is linked and stored in an external URL, opens the URL and returns a  object.

Is it the responsibility of the caller to dispose the stream object.

 **Examples:** 

Shows how to create an image file from a shape's raw image data.

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

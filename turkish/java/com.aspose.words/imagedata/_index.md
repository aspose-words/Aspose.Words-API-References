---
title: "ImageData"
linktitle: "ImageData"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekil için bir görüntüyü tanımlar."
type: docs
weight: 391
url: /tr/java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

Bir şekil için bir görüntü tanımlar.

Daha fazla bilgi için, [ Working with Images ][Working with Images] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir şeklin içindeki görüntüye erişmek ve değiştirmek için [Shape.getImageData()](../../com.aspose.words/shape/\#getImageData) özelliğini kullanın. [ImageData](../../com.aspose.words/imagedata/) sınıfının örneklerini doğrudan oluşturmazsınız.

Bir görüntü bir şekil içinde depolanabilir, harici bir dosyaya bağlanabilir veya her ikisi (bağlantılı ve belgede depolanmış) olabilir.

Görüntünün şekil içinde depolanmış veya bağlanmış olmasına bakılmaksızın, gerçek görüntüye her zaman [toByteArray()](../../com.aspose.words/imagedata/\#toByteArray), [toImage()](../../com.aspose.words/imagedata/\#toImage) veya [save(java.lang.String)](../../com.aspose.words/imagedata/\#save-java.lang.String) yöntemlerini kullanarak erişebilirsiniz. Görüntü şekil içinde depolanmışsa, ayrıca [getImageBytes()](../../com.aspose.words/imagedata/\#getImageBytes) / [setImageBytes(byte[])](../../com.aspose.words/imagedata/\#setImageBytes-byte) özelliğini kullanarak doğrudan erişebilirsiniz.

Bir görüntüyü şekil içinde depolamak için [setImage(java.lang.String)](../../com.aspose.words/imagedata/\#setImage-java.lang.String) yöntemini kullanın. Bir görüntüyü şekle bağlamak için [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) özelliğini ayarlayın.

 **Examples:** 

Bir belgeden görüntüleri nasıl çıkaracağınızı ve bunları yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedeceğinizi gösterir.

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

Bir belgeye bağlı bir görüntünün nasıl ekleneceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fitImageToShape()](#fitImageToShape) | Görüntü verisini Shape çerçevesine uyarlar, böylece görüntü verisinin en‑boy oranı Shape çerçevesinin en‑boy oranına eşleşir. |
| [getBiLevel()](#getBiLevel) | Bir görüntünün siyah beyaz olarak gösterilip gösterilmeyeceğini belirler. |
| [getBorders()](#getBorders) | Görüntünün kenarlık koleksiyonunu alır. |
| [getBrightness()](#getBrightness) | Resmin parlaklığını alır. |
| [getChromaKey()](#getChromaKey) | Şeffaf olarak işlenecek görüntünün renk değerini tanımlar. |
| [getContrast()](#getContrast) | Belirtilen resim için kontrastı alır. |
| [getCropBottom()](#getCropBottom) | Resmin alt tarafından kaldırılma oranını tanımlar. |
| [getCropLeft()](#getCropLeft) | Resmin sol tarafından kaldırılma oranını tanımlar. |
| [getCropRight()](#getCropRight) | Resmin sağ tarafından kaldırılma oranını tanımlar. |
| [getCropTop()](#getCropTop) | Resmin üst tarafından kaldırılma oranını tanımlar. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getGrayScale()](#getGrayScale) | Belirler bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini. |
| [getImageBytes()](#getImageBytes) | Şekilde depolanan görüntünün ham baytlarını alır. |
| [getImageSize()](#getImageSize) | Görüntü boyutu ve çözünürlüğü hakkında bilgileri alır. |
| [getImageType()](#getImageType) | Görüntünün türünü alır. |
| [getSourceFullName()](#getSourceFullName) | Bağlantılı görüntü için kaynak dosyanın yolunu ve adını alır. |
| [getTitle()](#getTitle) | Bir görüntünün başlığını tanımlar. |
| [hasImage()](#hasImage) | Şeklin görüntü baytları varsa veya bir görüntüye bağlanıyorsa  true  döndürür. |
| [isLink()](#isLink) | Görüntünün şekle bağlandığı durumlarda ( [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) belirtildiğinde)  true  döndürür. |
| [isLinkOnly()](#isLinkOnly) | Görüntünün bağlandığı ve belgede depolanmadığı durumlarda  true  döndürür. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Görüntüyü bir dosyaya kaydeder. |
| [setBiLevel(boolean value)](#setBiLevel-boolean) | Bir görüntünün siyah beyaz olarak gösterilip gösterilmeyeceğini belirler. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBrightness(double value)](#setBrightness-double) | Resmin parlaklığını ayarlar. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color) | Şeffaf olarak işlenecek görüntünün renk değerini tanımlar. |
| [setContrast(double value)](#setContrast-double) | Belirtilen resim için kontrastı ayarlar. |
| [setCropBottom(double value)](#setCropBottom-double) | Resmin alt tarafından kaldırılma oranını tanımlar. |
| [setCropLeft(double value)](#setCropLeft-double) | Resmin sol tarafından kaldırılma oranını tanımlar. |
| [setCropRight(double value)](#setCropRight-double) | Resmin sağ tarafından kaldırılma oranını tanımlar. |
| [setCropTop(double value)](#setCropTop-double) | Resmin üst tarafından kaldırılma oranını tanımlar. |
| [setGrayScale(boolean value)](#setGrayScale-boolean) | Belirler bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Şeklin görüntülediği resmi ayarlar. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Şeklin görüntülediği resmi ayarlar. |
| [setImageBytes(byte[] value)](#setImageBytes-byte) | Şekilde depolanan görüntünün ham baytlarını ayarlar. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Bağlantılı görüntü için kaynak dosyanın yolunu ve adını ayarlar. |
| [setTitle(String value)](#setTitle-java.lang.String) | Bir görüntünün başlığını tanımlar. |
| [toByteArray()](#toByteArray) | Görüntünün depolanmış veya bağlantılı olup olmadığına bakılmaksızın görüntü baytlarını döndürür. |
| [toImage()](#toImage) | Şekilde depolanan görüntüyü bir java  BufferedImage  nesnesi olarak alır. |
| [toStream()](#toStream) | Görüntü baytlarını içeren bir akış oluşturur ve döndürür. |
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fitImageToShape() {#fitImageToShape}
```
public void fitImageToShape()
```


Görüntü verisini Shape çerçevesine uyarlar, böylece görüntü verisinin en‑boy oranı Shape çerçevesinin en‑boy oranına eşleşir.

 **Examples:** 

Görüntü verilerini Shape çerçevesine nasıl sığdırılacağını gösterir.

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


Bir görüntünün siyah beyaz olarak gösterilip gösterilmeyeceğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Görüntünün kenarlık koleksiyonunu alır. Kenarlıklar yalnızca satır içi görüntülerde etkilidir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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


Resmin parlaklığını alır. Bu özelliğin değeri 0.0 (en karanlık) ile 1.0 (en parlak) arasında bir sayı olmalıdır.

 **Remarks:** 

Varsayılan değer 0.5'tir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - Resmin parlaklığı.
### getChromaKey() {#getChromaKey}
```
public Color getChromaKey()
```


Şeffaf olarak işlenecek görüntünün renk değerini tanımlar.

 **Remarks:** 

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getContrast() {#getContrast}
```
public double getContrast()
```


Belirtilen resim için kontrastı alır. Bu özelliğin değeri 0.0 (en düşük kontrast) ile 1.0 (en yüksek kontrast) arasında bir sayı olmalıdır.

 **Remarks:** 

Varsayılan değer 0.5'tir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - Belirtilen resim için kontrast.
### getCropBottom() {#getCropBottom}
```
public double getCropBottom()
```


Resmin alt tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - İlgili  double  değeri.
### getCropLeft() {#getCropLeft}
```
public double getCropLeft()
```


Resmin sol tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - İlgili  double  değeri.
### getCropRight() {#getCropRight}
```
public double getCropRight()
```


Resmin sağ tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - İlgili  double  değeri.
### getCropTop() {#getCropTop}
```
public double getCropTop()
```


Resmin üst tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
double - İlgili  double  değeri.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale}
```
public boolean getGrayScale()
```


Belirler bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Şekilde depolanan görüntünün ham baytlarını alır.

 **Remarks:** 

Değeri  null  veya boş bir dizi olarak ayarlamak, resmi şekilden kaldıracaktır.

Resim belgeye kaydedilmemişse  null  döndürür (ör. bu durumda resim muhtemelen bağlantılıdır).

 **Examples:** 

Bir şeklin ham resim verilerinden bir resim dosyası oluşturmanın nasıl yapılacağını gösterir.

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
byte[] - Şekilde depolanan resmin ham baytları.
### getImageSize() {#getImageSize}
```
public ImageSize getImageSize()
```


Resim boyutu ve çözünürlüğü hakkında bilgi alır. (97679,6)

 **Remarks:** 

Resim yalnızca bağlantılı ve belgede depolanmamışsa, sıfır boyut döndürür.

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
[ImageSize](../../com.aspose.words/imagesize/) - The information about image size and resolution.
### getImageType() {#getImageType}
```
public int getImageType()
```


Resmin tipini alır. (97725,6)

 **Examples:** 

Bir belgeden görüntüleri nasıl çıkaracağınızı ve bunları yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedeceğinizi gösterir.

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
int - Resmin tipi. Döndürülen değer, [ImageType](../../com.aspose.words/imagetype/) sabitlerinden biridir.
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Bağlantılı görüntü için kaynak dosyanın yolunu ve adını alır.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Eğer [getSourceFullName()](../../com.aspose.words/imagedata/\\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\\#setSourceFullName-java.lang.String) boş bir dize değilse, resim bağlantılıdır.

 **Examples:** 

Bir belgeye bağlı bir görüntünün nasıl ekleneceğini gösterir.

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
java.lang.String - Bağlantılı resim için kaynak dosyanın yolu ve adı.
### getTitle() {#getTitle}
```
public String getTitle()
```


Bir görüntünün başlığını tanımlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


Şeklin resim baytları varsa veya bir resmi bağlarsa  true  döndürür. (97641,6)

 **Examples:** 

Bir belgedeki tüm resimleri dosya sistemine kaydetmenin nasıl yapılacağını gösterir.

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
boolean -  true  şeklin resim baytları varsa veya bir resmi bağlarsa.
### isLink() {#isLink}
```
public boolean isLink()
```


Resim şekle bağlanmışsa ( [getSourceFullName()](../../com.aspose.words/imagedata/\\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\\#setSourceFullName-java.lang.String) belirtildiğinde)  true  döndürür. (97749,6)

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
boolean -  true  resim şekle bağlanmışsa ( [getSourceFullName()](../../com.aspose.words/imagedata/\\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\\#setSourceFullName-java.lang.String) belirtildiğinde).
### isLinkOnly() {#isLinkOnly}
```
public boolean isLinkOnly()
```


Resim bağlantılı ve belgede depolanmamışsa  true  döndürür. (97811,6)

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
boolean -  true  resim bağlantılı ve belgede depolanmamışsa.
### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Görüntüyü bir dosyaya kaydeder.

 **Examples:** 

Bir belgeden görüntüleri nasıl çıkaracağınızı ve bunları yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Resmin kaydedileceği dosya adı. |

### setBiLevel(boolean value) {#setBiLevel-boolean}
```
public void setBiLevel(boolean value)
```


Bir görüntünün siyah beyaz olarak gösterilip gösterilmeyeceğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double}
```
public void setBrightness(double value)
```


Resmin parlaklığını ayarlar. Bu özelliğin değeri 0.0 (en karanlık) ile 1.0 (en parlak) arasında bir sayı olmalıdır.

 **Remarks:** 

Varsayılan değer 0.5'tir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Resmin parlaklığı. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color}
```
public void setChromaKey(Color value)
```


Şeffaf olarak işlenecek görüntünün renk değerini tanımlar.

 **Remarks:** 

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setContrast(double value) {#setContrast-double}
```
public void setContrast(double value)
```


Belirtilen resim için kontrastı ayarlar. Bu özelliğin değeri 0.0 (en düşük kontrast) ile 1.0 (en yüksek kontrast) arasında bir sayı olmalıdır.

 **Remarks:** 

Varsayılan değer 0.5'tir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Belirtilen resim için kontrast. |

### setCropBottom(double value) {#setCropBottom-double}
```
public void setCropBottom(double value)
```


Resmin alt tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setCropLeft(double value) {#setCropLeft-double}
```
public void setCropLeft(double value)
```


Resmin sol tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setCropRight(double value) {#setCropRight-double}
```
public void setCropRight(double value)
```


Resmin sağ tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setCropTop(double value) {#setCropTop-double}
```
public void setCropTop(double value)
```


Resmin üst tarafından kaldırılma oranını tanımlar.

 **Remarks:** 

Kırpma miktarı -1.0 ile 1.0 arasında olabilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan içeriye doğru resmin sıkıştırılmasına yol açar (resim ile kırpılan kenar arasındaki boşluk şeklin doldurma rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine neden olur.

Varsayılan değer 0.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setGrayScale(boolean value) {#setGrayScale-boolean}
```
public void setGrayScale(boolean value)
```


Belirler bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Şeklin görüntülediği resmi ayarlar.

 **Examples:** 

Bir belgede yerel dosya sisteminden görüntülerin nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage | Görüntü nesnesi. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Şeklin görüntülediği resmi ayarlar.

 **Examples:** 

Bir belgeye bağlı bir görüntünün nasıl ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Görüntü dosyası. Bir dosya adı veya URL olabilir. |

### setImageBytes(byte[] value) {#setImageBytes-byte}
```
public void setImageBytes(byte[] value)
```


Şekilde depolanan görüntünün ham baytlarını ayarlar.

 **Remarks:** 

Değeri  null  veya boş bir dizi olarak ayarlamak, resmi şekilden kaldıracaktır.

Resim belgeye kaydedilmemişse  null  döndürür (ör. bu durumda resim muhtemelen bağlantılıdır).

 **Examples:** 

Bir şeklin ham resim verilerinden bir resim dosyası oluşturmanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | byte[] | Şekilde depolanan görüntünün ham baytları. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Bağlantılı görüntü için kaynak dosyanın yolunu ve adını ayarlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Eğer [getSourceFullName()](../../com.aspose.words/imagedata/\\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\\#setSourceFullName-java.lang.String) boş bir dize değilse, resim bağlantılıdır.

 **Examples:** 

Bir belgeye bağlı bir görüntünün nasıl ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bağlantılı görüntünün kaynak dosyasının yolu ve adı. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Bir görüntünün başlığını tanımlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

 **Examples:** 

Bir şeklin görüntü verilerini nasıl düzenleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


Görüntünün depolanmış veya bağlantılı olup olmadığına bakılmaksızın görüntü baytlarını döndürür.

 **Remarks:** 

Görüntü bağlantılıysa, her çağrıldığında görüntüyü indirir.

 **Examples:** 

Bir şeklin ham resim verilerinden bir resim dosyası oluşturmanın nasıl yapılacağını gösterir.

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


Şekilde depolanan görüntüyü bir java  BufferedImage  nesnesi olarak alır.

 **Remarks:** 

Bu yöntem her çağrıldığında görüntü baytlarından yeni bir java.awt.image.BufferedImage nesnesi oluşturmaya çalışır. Eğer javax.imageio.ImageReader görüntü baytlarını (emf, wmf, tiff, vb.) okuyamazsa yöntem null döndürür.

Görüntü nesnesini serbest bırakmak çağıranın sorumluluğundadır.

 **Examples:** 

Bir belgedeki tüm resimleri dosya sistemine kaydetmenin nasıl yapılacağını gösterir.

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


Görüntü baytlarını içeren bir akış oluşturur ve döndürür. Bu henüz Java'ya aktarılmadı.

 **Remarks:** 

Görüntü baytları şekle depolanmışsa, bir nesne oluşturur ve döndürür.

Görüntü bağlantılı ve bir dosyada depolanmışsa, dosyayı açar ve bir nesne döndürür.

Görüntü bağlantılı ve harici bir URL'de depolanmışsa, URL'yi açar ve bir nesne döndürür.

Akış nesnesini serbest bırakmak çağıranın sorumluluğu mudur.

 **Examples:** 

Bir şeklin ham resim verilerinden bir resim dosyası oluşturmanın nasıl yapılacağını gösterir.

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

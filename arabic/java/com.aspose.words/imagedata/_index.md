---
title: "ImageData"
linktitle: "ImageData"
second_title: "Aspose.Words لـ Java"
description: "يحدد صورة لشكل في Java."
type: docs
weight: 391
url: /ar/java/com.aspose.words/imagedata/
---

**Inheritance:**
java.lang.Object
```
public class ImageData
```

يحدد صورة لشكل.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Images ][Working with Images].

 **Remarks:** 

استخدم الخاصية [Shape.getImageData()](../../com.aspose.words/shape/\#getImageData) للوصول إلى الصورة داخل الشكل وتعديلها. لا تقوم بإنشاء مثيلات من الفئة [ImageData](../../com.aspose.words/imagedata/) مباشرةً.

يمكن تخزين صورة داخل شكل، أو ربطها بملف خارجي أو كلاهما (مربوطة ومخزنة في المستند).

بغض النظر عما إذا كانت الصورة مخزنة داخل الشكل أو مربوطة، يمكنك دائمًا الوصول إلى الصورة الفعلية باستخدام طرق [toByteArray()](../../com.aspose.words/imagedata/\#toByteArray)، [toImage()](../../com.aspose.words/imagedata/\#toImage) أو [save(java.lang.String)](../../com.aspose.words/imagedata/\#save-java.lang.String). إذا كانت الصورة مخزنة داخل الشكل، يمكنك أيضًا الوصول إليها مباشرةً باستخدام الخاصية [getImageBytes()](../../com.aspose.words/imagedata/\#getImageBytes) / [setImageBytes(byte[])](../../com.aspose.words/imagedata/\#setImageBytes-byte).

لتخزين صورة داخل شكل استخدم الطريقة [setImage(java.lang.String)](../../com.aspose.words/imagedata/\#setImage-java.lang.String). لربط صورة بشكل، اضبط الخاصية [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String).

 **Examples:** 

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات منفصلة.

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

يوضح كيفية إدراج صورة مربوطة في مستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fitImageToShape()](#fitImageToShape) | يضبط بيانات الصورة لتتناسب مع إطار Shape بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة الإطار. |
| [getBiLevel()](#getBiLevel) | يحدد ما إذا كانت الصورة ستُعرض بالأبيض والأسود. |
| [getBorders()](#getBorders) | يحصل على مجموعة حدود الصورة. |
| [getBrightness()](#getBrightness) | يحصل على سطوع الصورة. |
| [getChromaKey()](#getChromaKey) | يحدد قيمة اللون للصورة التي ستُعامل كشفافة. |
| [getContrast()](#getContrast) | يحصل على التباين للصورة المحددة. |
| [getCropBottom()](#getCropBottom) | يحدد نسبة إزالة الصورة من الجانب السفلي. |
| [getCropLeft()](#getCropLeft) | يحدد نسبة إزالة الصورة من الجانب الأيسر. |
| [getCropRight()](#getCropRight) | يحدد نسبة إزالة الصورة من الجانب الأيمن. |
| [getCropTop()](#getCropTop) | يحدد نسبة إزالة الصورة من الجانب العلوي. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getGrayScale()](#getGrayScale) | يحدد ما إذا كانت الصورة ستُعرض بوضع التدرج الرمادي. |
| [getImageBytes()](#getImageBytes) | يحصل على البايتات الخام للصورة المخزنة في الشكل. |
| [getImageSize()](#getImageSize) | يحصل على المعلومات حول حجم الصورة ودقتها. |
| [getImageType()](#getImageType) | يحصل على نوع الصورة. |
| [getSourceFullName()](#getSourceFullName) | يحصل على المسار واسم ملف المصدر للصورة المرتبطة. |
| [getTitle()](#getTitle) | يحدد عنوان الصورة. |
| [hasImage()](#hasImage) | يرجع  true  إذا كان الشكل يحتوي على بايتات الصورة أو يربط صورة. |
| [isLink()](#isLink) | يرجع  true  إذا كانت الصورة مرتبطة بالشكل (عند تحديد [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String)). |
| [isLinkOnly()](#isLinkOnly) | يرجع  true  إذا كانت الصورة مرتبطة ولم تُخزن في المستند. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | يحفظ الصورة في ملف. |
| [setBiLevel(boolean value)](#setBiLevel-boolean) | يحدد ما إذا كانت الصورة ستُعرض بالأبيض والأسود. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBrightness(double value)](#setBrightness-double) | يضبط سطوع الصورة. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color) | يحدد قيمة اللون للصورة التي ستُعامل كشفافة. |
| [setContrast(double value)](#setContrast-double) | يضبط التباين للصورة المحددة. |
| [setCropBottom(double value)](#setCropBottom-double) | يحدد نسبة إزالة الصورة من الجانب السفلي. |
| [setCropLeft(double value)](#setCropLeft-double) | يحدد نسبة إزالة الصورة من الجانب الأيسر. |
| [setCropRight(double value)](#setCropRight-double) | يحدد نسبة إزالة الصورة من الجانب الأيمن. |
| [setCropTop(double value)](#setCropTop-double) | يحدد نسبة إزالة الصورة من الجانب العلوي. |
| [setGrayScale(boolean value)](#setGrayScale-boolean) | يحدد ما إذا كانت الصورة ستُعرض بوضع التدرج الرمادي. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | يضبط الصورة التي يعرضها الشكل. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | يضبط الصورة التي يعرضها الشكل. |
| [setImageBytes(byte[] value)](#setImageBytes-byte) | يضبط البايتات الخام للصورة المخزنة في الشكل. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | يضبط المسار واسم ملف المصدر للصورة المرتبطة. |
| [setTitle(String value)](#setTitle-java.lang.String) | يحدد عنوان الصورة. |
| [toByteArray()](#toByteArray) | يرجع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة. |
| [toImage()](#toImage) | يحصل على الصورة المخزنة في الشكل ككائن java  BufferedImage . |
| [toStream()](#toStream) | ينشئ ويرجع تدفقًا يحتوي على بايتات الصورة. |
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fitImageToShape() {#fitImageToShape}
```
public void fitImageToShape()
```


يضبط بيانات الصورة لتتناسب مع إطار Shape بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة الإطار.

 **Examples:** 

يعرض كيفية ملاءمة بيانات الصورة لإطار الشكل.

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


يحدد ما إذا كانت الصورة ستُعرض بالأبيض والأسود.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
boolean - القيمة المنطقية المقابلة.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


يحصل على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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


يحصل على سطوع الصورة. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (أكثر قتامة) إلى 1.0 (أكثر سطوعًا).

 **Remarks:** 

القيمة الافتراضية هي 0.5.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - سطوع الصورة.
### getChromaKey() {#getChromaKey}
```
public Color getChromaKey()
```


يحدد قيمة اللون للصورة التي ستُعامل كشفافة.

 **Remarks:** 

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getContrast() {#getContrast}
```
public double getContrast()
```


يحصل على التباين للصورة المحددة. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (أقل تباين) إلى 1.0 (أعلى تباين).

 **Remarks:** 

القيمة الافتراضية هي 0.5.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - التباين للصورة المحددة.
### getCropBottom() {#getCropBottom}
```
public double getCropBottom()
```


يحدد نسبة إزالة الصورة من الجانب السفلي.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - القيمة المقابلة للـ double.
### getCropLeft() {#getCropLeft}
```
public double getCropLeft()
```


يحدد نسبة إزالة الصورة من الجانب الأيسر.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - القيمة المقابلة للـ double.
### getCropRight() {#getCropRight}
```
public double getCropRight()
```


يحدد نسبة إزالة الصورة من الجانب الأيمن.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - القيمة المقابلة للـ double.
### getCropTop() {#getCropTop}
```
public double getCropTop()
```


يحدد نسبة إزالة الصورة من الجانب العلوي.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
double - القيمة المقابلة للـ double.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getGrayScale() {#getGrayScale}
```
public boolean getGrayScale()
```


يحدد ما إذا كانت الصورة ستُعرض بوضع التدرج الرمادي.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
boolean - القيمة المنطقية المقابلة.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


يحصل على البايتات الخام للصورة المخزنة في الشكل.

 **Remarks:** 

ضبط القيمة إلى  null  أو مصفوفة فارغة سيؤدي إلى إزالة الصورة من الشكل.

يعيد  null  إذا لم يتم تخزين الصورة في المستند (مثلاً قد تكون الصورة مرتبطة في هذه الحالة).

 **Examples:** 

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.

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
byte[] - البايتات الخام للصورة المخزنة في الشكل.
### getImageSize() {#getImageSize}
```
public ImageSize getImageSize()
```


يحصل على معلومات حول حجم الصورة ودقتها. (97679,6)

 **Remarks:** 

إذا كانت الصورة مرتبطة فقط ولم تُخزن في المستند، يعيد حجمًا صفرًا.

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
[ImageSize](../../com.aspose.words/imagesize/) - The information about image size and resolution.
### getImageType() {#getImageType}
```
public int getImageType()
```


يحصل على نوع الصورة. (97725,6)

 **Examples:** 

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات منفصلة.

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
int - نوع الصورة. القيمة المرجعة هي واحدة من ثوابت [ImageType](../../com.aspose.words/imagetype/).
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


يحصل على المسار واسم ملف المصدر للصورة المرتبطة.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

إذا لم يكن [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) سلسلةً فارغة، تكون الصورة مرتبطة.

 **Examples:** 

يوضح كيفية إدراج صورة مربوطة في مستند.

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
java.lang.String - المسار والاسم لملف المصدر للصورة المرتبطة.
### getTitle() {#getTitle}
```
public String getTitle()
```


يحدد عنوان الصورة.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


يعيد  true  إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة. (97641,6)

 **Examples:** 

يوضح كيفية حفظ جميع الصور من مستند إلى نظام الملفات.

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
boolean -  true  إذا كان الشكل يحتوي على بايتات صورة أو يربط صورة.
### isLink() {#isLink}
```
public boolean isLink()
```


يعيد  true  إذا كانت الصورة مرتبطة بالشكل (عند تحديد [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String)). (97749,6)

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
boolean -  true  إذا كانت الصورة مرتبطة بالشكل (عند تحديد [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String)).
### isLinkOnly() {#isLinkOnly}
```
public boolean isLinkOnly()
```


يعيد  true  إذا كانت الصورة مرتبطة ولم تُخزن في المستند. (97811,6)

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
boolean -  true  إذا كانت الصورة مرتبطة ولم تُخزن في المستند.
### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


يحفظ الصورة في ملف.

 **Examples:** 

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات منفصلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف حيث يتم حفظ الصورة. |

### setBiLevel(boolean value) {#setBiLevel-boolean}
```
public void setBiLevel(boolean value)
```


يحدد ما إذا كانت الصورة ستُعرض بالأبيض والأسود.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double}
```
public void setBrightness(double value)
```


يضبط سطوع الصورة. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (أكثر تعتيمًا) إلى 1.0 (أكثر سطوعًا).

 **Remarks:** 

القيمة الافتراضية هي 0.5.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | سطوع الصورة. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color}
```
public void setChromaKey(Color value)
```


يحدد قيمة اللون للصورة التي ستُعامل كشفافة.

 **Remarks:** 

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setContrast(double value) {#setContrast-double}
```
public void setContrast(double value)
```


يضبط التباين للصورة المحددة. يجب أن تكون قيمة هذه الخاصية رقمًا من 0.0 (أقل تباين) إلى 1.0 (أعلى تباين).

 **Remarks:** 

القيمة الافتراضية هي 0.5.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | التباين للصورة المحددة. |

### setCropBottom(double value) {#setCropBottom-double}
```
public void setCropBottom(double value)
```


يحدد نسبة إزالة الصورة من الجانب السفلي.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setCropLeft(double value) {#setCropLeft-double}
```
public void setCropLeft(double value)
```


يحدد نسبة إزالة الصورة من الجانب الأيسر.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setCropRight(double value) {#setCropRight-double}
```
public void setCropRight(double value)
```


يحدد نسبة إزالة الصورة من الجانب الأيمن.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setCropTop(double value) {#setCropTop-double}
```
public void setCropTop(double value)
```


يحدد نسبة إزالة الصورة من الجانب العلوي.

 **Remarks:** 

يمكن أن يتراوح مقدار القص من -1.0 إلى 1.0. القيمة الافتراضية هي 0. لاحظ أن القيمة 1 ستؤدي إلى عدم عرض أي صورة على الإطلاق. القيم السالبة ستؤدي إلى ضغط الصورة نحو الداخل من الحافة التي يتم قصها (سيتم ملء الفراغ بين الصورة والحافة المقصوصة بلون تعبئة الشكل). القيم الموجبة الأقل من 1 ستؤدي إلى تمديد الصورة المتبقية لتناسب الشكل.

القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setGrayScale(boolean value) {#setGrayScale-boolean}
```
public void setGrayScale(boolean value)
```


يحدد ما إذا كانت الصورة ستُعرض بوضع التدرج الرمادي.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


يضبط الصورة التي يعرضها الشكل.

 **Examples:** 

يظهر كيفية عرض الصور من نظام الملفات المحلي في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage | كائن الصورة. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


يضبط الصورة التي يعرضها الشكل.

 **Examples:** 

يوضح كيفية إدراج صورة مربوطة في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | ملف الصورة. يمكن أن يكون اسم ملف أو عنوان URL. |

### setImageBytes(byte[] value) {#setImageBytes-byte}
```
public void setImageBytes(byte[] value)
```


يضبط البايتات الخام للصورة المخزنة في الشكل.

 **Remarks:** 

ضبط القيمة إلى  null  أو مصفوفة فارغة سيؤدي إلى إزالة الصورة من الشكل.

يعيد  null  إذا لم يتم تخزين الصورة في المستند (مثلاً قد تكون الصورة مرتبطة في هذه الحالة).

 **Examples:** 

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | البايتات الخام للصورة المخزنة في الشكل. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


يضبط المسار واسم ملف المصدر للصورة المرتبطة.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

إذا لم يكن [getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) سلسلةً فارغة، تكون الصورة مرتبطة.

 **Examples:** 

يوضح كيفية إدراج صورة مربوطة في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | المسار واسم ملف المصدر للصورة المرتبطة. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


يحدد عنوان الصورة.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية تحرير بيانات صورة الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


يرجع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة.

 **Remarks:** 

إذا كانت الصورة مرتبطة، يتم تنزيل الصورة في كل مرة يتم استدعاؤها.

 **Examples:** 

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.

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


يحصل على الصورة المخزنة في الشكل ككائن java  BufferedImage .

 **Remarks:** 

يحاول إنشاء كائن  java.awt.image.BufferedImage  جديد من بايتات الصورة في كل مرة يتم استدعاء هذه الطريقة. إذا كان  javax.imageio.ImageReader  لا يستطيع قراءة بايتات الصورة (emf, wmf, tiff, إلخ) فإن الطريقة تُعيد  null .

إنها مسؤولية المتصل التخلص من كائن الصورة.

 **Examples:** 

يوضح كيفية حفظ جميع الصور من مستند إلى نظام الملفات.

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


ينشئ ويُعيد دفقًا يحتوي على بايتات الصورة.  هذا لم يُحوَّل إلى Java بعد.

 **Remarks:** 

إذا كانت بايتات الصورة مخزنة في الشكل، ينشئ ويُعيد كائنًا.

إذا كانت الصورة مرتبطة ومخزنة في ملف، يفتح الملف ويُعيد كائنًا.

إذا كانت الصورة مرتبطة ومخزنة في عنوان URL خارجي، يفتح عنوان URL ويُعيد كائنًا.

هل هي مسؤولية المتصل التخلص من كائن الدفق.

 **Examples:** 

يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.

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

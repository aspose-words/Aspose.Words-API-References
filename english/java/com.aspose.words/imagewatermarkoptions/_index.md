---
title: ImageWatermarkOptions
linktitle: ImageWatermarkOptions
second_title: Aspose.Words for Java
description: Contains options that can be specified when adding a watermark with image in Java.
type: docs
weight: 392
url: /java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contains options that can be specified when adding a watermark with image.

To learn more, visit the [ Working with Watermark ][Working with Watermark] documentation article.

 **Examples:** 

Shows how to create a watermark from an image in the local file system.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Methods

| Method | Description |
| --- | --- |
| [getScale()](#getScale) | Gets the scale factor expressed as a fraction of the image. |
| [isWashout()](#isWashout) | Gets a boolean value which is responsible for washout effect of the watermark. |
| [isWashout(boolean value)](#isWashout-boolean) | Sets a boolean value which is responsible for washout effect of the watermark. |
| [setScale(double value)](#setScale-double) | Sets the scale factor expressed as a fraction of the image. |
### getScale() {#getScale}
```
public double getScale()
```


Gets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

**Returns:**
double - The scale factor expressed as a fraction of the image.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Gets a boolean value which is responsible for washout effect of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a watermark from an image in the local file system.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Returns:**
boolean - A boolean value which is responsible for washout effect of the watermark.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Sets a boolean value which is responsible for washout effect of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a watermark from an image in the local file system.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for washout effect of the watermark. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The scale factor expressed as a fraction of the image. |


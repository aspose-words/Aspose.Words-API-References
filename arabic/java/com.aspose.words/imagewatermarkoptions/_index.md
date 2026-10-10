---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بصورة في Java."
type: docs
weight: 398
url: /ar/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بصورة.

لمزيد من المعلومات، زر [ Working with Watermark ][Working with Watermark] مقالة الوثائق.

 **Examples:** 

يظهر كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getScale()](#getScale) | يحصل على معامل القياس معبرًا عنه ككسر من الصورة. |
| [isWashout()](#isWashout) | يحصل على قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية. |
| [isWashout(boolean value)](#isWashout-boolean) | يضبط قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية. |
| [setScale(double value)](#setScale-double) | يضبط معامل القياس معبرًا عنه ككسر من الصورة. |
### getScale() {#getScale}
```
public double getScale()
```


يحصل على معامل القياس معبرًا عنه ككسر من الصورة. القيمة الافتراضية هي 0 - تلقائي.

**Returns:**
double - معامل القياس معبرًا عنه ككسر من الصورة.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


يحصل على قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية. القيمة الافتراضية هي true.

 **Examples:** 

يظهر كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

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
boolean - قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


يضبط قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية. القيمة الافتراضية هي true.

 **Examples:** 

يظهر كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية مسؤولة عن تأثير الغسلة للعلامة المائية. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


يضبط معامل القياس معبرًا عنه ككسر من الصورة. القيمة الافتراضية هي 0 - تلقائي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | معامل القياس معبرًا عنه ككسر من الصورة. |


---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words для Java"
description: "Содержит параметры, которые можно указать при добавлении водяного знака с изображением в Java."
type: docs
weight: 398
url: /ru/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Содержит параметры, которые можно указать при добавлении водяного знака с изображением.

Чтобы узнать больше, посетите статью документации [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Показывает, как создать водяной знак из изображения в локальной файловой системе.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getScale()](#getScale) | Получает коэффициент масштабирования, выраженный в виде доли изображения. |
| [isWashout()](#isWashout) | Получает булево значение, отвечающее за эффект выцветания водяного знака. |
| [isWashout(boolean value)](#isWashout-boolean) | Устанавливает булево значение, отвечающее за эффект выцветания водяного знака. |
| [setScale(double value)](#setScale-double) | Устанавливает коэффициент масштабирования, выраженный в виде доли изображения. |
### getScale() {#getScale}
```
public double getScale()
```


Получает коэффициент масштабирования, выраженный в виде доли изображения. Значение по умолчанию — 0 — авто.

**Returns:**
double - Коэффициент масштабирования, выраженный в виде доли изображения.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Получает булево значение, отвечающее за эффект выцветания водяного знака. Значение по умолчанию — true.

 **Examples:** 

Показывает, как создать водяной знак из изображения в локальной файловой системе.

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
boolean - Булево значение, отвечающее за эффект выцветания водяного знака.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Устанавливает булево значение, отвечающее за эффект выцветания водяного знака. Значение по умолчанию — true.

 **Examples:** 

Показывает, как создать водяной знак из изображения в локальной файловой системе.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Булево значение, отвечающее за эффект выцветания водяного знака. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Устанавливает коэффициент масштабирования, выраженный в виде доли изображения. Значение по умолчанию — 0 — авто.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Коэффициент масштабирования, выраженный в виде доли изображения. |


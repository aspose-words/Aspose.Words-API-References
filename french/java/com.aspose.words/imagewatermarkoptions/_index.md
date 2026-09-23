---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words pour Java"
description: "Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec image en Java."
type: docs
weight: 398
url: /fr/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contient les options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec une image.

Pour en savoir plus, consultez l'article de documentation [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getScale()](#getScale) | Obtient le facteur d'échelle exprimé en fraction de l'image. |
| [isWashout()](#isWashout) | Obtient une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. |
| [isWashout(boolean value)](#isWashout-boolean) | Définit une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. |
| [setScale(double value)](#setScale-double) | Définit le facteur d'échelle exprimé en fraction de l'image. |
### getScale() {#getScale}
```
public double getScale()
```


Obtient le facteur d'échelle exprimé en fraction de l'image. La valeur par défaut est 0 - auto.

**Returns:**
double - Le facteur d'échelle exprimé en fraction de l'image.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Obtient une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. La valeur par défaut est true.

 **Examples:** 

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

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
boolean - Une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Définit une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. La valeur par défaut est true.

 **Examples:** 

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Définit le facteur d'échelle exprimé en fraction de l'image. La valeur par défaut est 0 - auto.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Le facteur d'échelle exprimé en fraction de l'image. |


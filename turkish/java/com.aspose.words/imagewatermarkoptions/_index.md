---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words Java için"
description: "Java'da görüntü ile bir filigran eklerken belirtilebilecek seçenekleri içerir."
type: docs
weight: 398
url: /tr/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Görüntü ile filigran eklerken belirtilebilecek seçenekleri içerir.

Daha fazla bilgi için, [ Working with Watermark ][Working with Watermark] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Yerel dosya sistemindeki bir görüntüden filigran oluşturmanın nasıl yapılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getScale()](#getScale) | Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır. |
| [isWashout()](#isWashout) | Filigranın solma etkisinden sorumlu bir boolean değerini alır. |
| [isWashout(boolean value)](#isWashout-boolean) | Filigranın solma etkisinden sorumlu bir boolean değerini ayarlar. |
| [setScale(double value)](#setScale-double) | Görüntünün bir kesri olarak ifade edilen ölçek faktörünü ayarlar. |
### getScale() {#getScale}
```
public double getScale()
```


Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır. Varsayılan değer 0 - otomatik'tir.

**Returns:**
double - Görüntünün bir kesri olarak ifade edilen ölçek faktörü.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Filigranın solma etkisinden sorumlu bir boolean değerini alır. Varsayılan değer true'dur.

 **Examples:** 

Yerel dosya sistemindeki bir görüntüden filigran oluşturmanın nasıl yapılacağını gösterir.

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
boolean - Filigranın solma etkisinden sorumlu bir boolean değeri.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Filigranın solma etkisinden sorumlu bir boolean değerini ayarlar. Varsayılan değer true'dur.

 **Examples:** 

Yerel dosya sistemindeki bir görüntüden filigran oluşturmanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Filigranın solma etkisinden sorumlu bir boolean değeri. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Görüntünün bir kesri olarak ifade edilen ölçek faktörünü ayarlar. Varsayılan değer 0 - otomatik'tir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Görüntünün bir kesri olarak ifade edilen ölçek faktörü. |


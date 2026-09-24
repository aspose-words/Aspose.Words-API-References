---
title: "Filigran"
linktitle: "Filigran"
second_title: "Aspose.Words Java için"
description: "Java'da belge filigranı ile çalışmak için sınıfı temsil eder."
type: docs
weight: 721
url: /tr/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Belge filigranı ile çalışmak için sınıfı temsil eder.

Daha fazla bilgi için, [ Working with Watermark ][Working with Watermark] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Metin filigranı oluşturmayı gösterir.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getType()](#getType) | Filigran türünü alır. |
| [remove()](#remove) | Filigranı kaldırır. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Belgeye Görüntü filigranı ekler. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Belgeye Görüntü filigranı ekler. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Belgeye Görüntü filigranı ekler. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Belgeye Görüntü filigranı ekler. |
| [setText(String text)](#setText-java.lang.String) | Belgeye Metin filigranı ekler. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Belgeye Metin filigranı ekler. |
### getType() {#getType}
```
public int getType()
```


Filigran türünü alır.

 **Examples:** 

Metin filigranı oluşturmayı gösterir.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```

**Returns:**
int - Filigran türü. Döndürülen değer, [WatermarkType](../../com.aspose.words/watermarktype/) sabitlerinden biridir.
### remove() {#remove}
```
public void remove()
```


Filigranı kaldırır.

 **Examples:** 

Metin filigranı oluşturmayı gösterir.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Belgeye Görüntü filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage | Filigran olarak görüntülenen resim. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Belgeye Görüntü filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage | Filigran olarak görüntülenen resim. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Resim filigranı için ek seçenekleri tanımlar. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Belgeye Görüntü filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageStream | java.io.InputStream | Filigran olarak görüntülenen görüntü verilerini içeren akış. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Resim filigranı için ek seçenekleri tanımlar. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Belgeye Görüntü filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imagePath | java.lang.String | Filigran olarak görüntülenen görüntü dosyasının yolu. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Resim filigranı için ek seçenekleri tanımlar. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Belgeye Metin filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | java.lang.String | Filigran olarak görüntülenen metin. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Belgeye Metin filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | java.lang.String | Filigran olarak görüntülenen metin. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Metin filigranı için ek seçenekleri tanımlar. |


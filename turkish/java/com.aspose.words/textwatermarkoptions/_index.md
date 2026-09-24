---
title: "TextWatermarkOptions"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words Java için"
description: "Java'da metinle bir filigran eklerken belirtilebilecek seçenekleri içerir."
type: docs
weight: 678
url: /tr/java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Metin içeren bir filigran eklerken belirtilebilecek seçenekleri içerir.

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
| [getColor()](#getColor) | Yazı tipi rengini alır. |
| [getFontFamily()](#getFontFamily) | Yazı tipi ailesi adını alır. |
| [getFontSize()](#getFontSize) | Yazı tipi boyutunu alır. |
| [getLayout()](#getLayout) | Filigranın düzenini alır. |
| [isSemitrasparent()](#isSemitrasparent) | Filigranın opaklığından sorumlu bir boolean değer alır. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | Filigranın opaklığından sorumlu bir boolean değer ayarlar. |
| [setColor(Color value)](#setColor-java.awt.Color) | Yazı tipi rengini ayarlar. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Yazı tipi ailesi adını ayarlar. |
| [setFontSize(float value)](#setFontSize-float) | Yazı tipi boyutunu ayarlar. |
| [setLayout(int value)](#setLayout-int) | Filigranın düzenini ayarlar. |
### getColor() {#getColor}
```
public Color getColor()
```


Yazı tipi rengini alır. Varsayılan değer java.awt.Color\#getSilver().getSilver().

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
java.awt.Color - Yazı tipi rengi.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Yazı tipi ailesi adını alır. Varsayılan değer "Calibri".

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
java.lang.String - Yazı tipi ailesi adı.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


Bir yazı tipi boyutu alır. Varsayılan değer 0 - otomatik.

**Returns:**
float - Bir yazı tipi boyutu.
### getLayout() {#getLayout}
```
public int getLayout()
```


Filigranın düzenini alır. Varsayılan değer [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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
int - Filigranın düzeni. Döndürülen değer [WatermarkLayout](../../com.aspose.words/watermarklayout/) sabitlerinden biridir.
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


Filigranın opaklığından sorumlu bir boolean değer alır. Varsayılan değer  true .

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
boolean - Filigranın opaklığından sorumlu bir boolean değer.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


Filigranın opaklığından sorumlu bir boolean değer ayarlar. Varsayılan değer  true .

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Filigranın opaklığından sorumlu bir boolean değer. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Yazı tipi rengini ayarlar. Varsayılan değer java.awt.Color\#getSilver().getSilver().

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yazı tipi rengi. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Yazı tipi ailesi adını ayarlar. Varsayılan değer "Calibri".

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Yazı tipi ailesi adı. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


Bir yazı tipi boyutu ayarlar. Varsayılan değer 0 - otomatik.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | float | Bir yazı tipi boyutu. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


Filigranın düzenini ayarlar. Varsayılan değer [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Filigranın düzeni. Değer [WatermarkLayout](../../com.aspose.words/watermarklayout/) sabitlerinden biri olmalıdır. |


---
title: "FrameFormat"
linktitle: "FrameFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir paragraf için çerçeveyle ilgili biçimlendirmeyi temsil eder."
type: docs
weight: 352
url: /tr/java/com.aspose.words/frameformat/
---

**Inheritance:**
java.lang.Object
```
public class FrameFormat
```

Bir paragraf için çerçeveyle ilgili biçimlendirmeyi temsil eder.

 **Remarks:** 

Bu nesne her zaman oluşturulur. Bir paragraf bir çerçeve ise, tüm özellikler ilgili değerleri içerir, aksi takdirde tüm özellikler varsayılanlarına ayarlanır.

Paragrafın bir çerçeve olup olmadığını kontrol etmek için [isFrame()](../../com.aspose.words/frameformat/\#isFrame) kullanın.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getHeight()](#getHeight) | Belirtilen çerçevenin yüksekliğini alır. |
| [getHeightRule()](#getHeightRule) | Belirtilen çerçevenin yüksekliğini belirleme kuralını alır. |
| [getHorizontalAlignment()](#getHorizontalAlignment) | Belirtilen çerçevenin yatay hizalamasını alır. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText) | Bir çerçeve ile çevresindeki metin arasındaki yatay mesafeyi, nokta cinsinden alır. |
| [getHorizontalPosition()](#getHorizontalPosition) | Çerçevenin kenarı ile [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition) özelliğiyle belirtilen öğe arasındaki yatay mesafeyi alır. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition) | Bir çerçevenin göreli yatay konumunu alır. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition) | Bir çerçevenin göreli dikey konumunu alır. |
| [getVerticalAlignment()](#getVerticalAlignment) | Belirtilen çerçevenin dikey hizalamasını alır. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText) | Bir çerçeve ile çevresindeki metin arasındaki dikey mesafeyi (nokta cinsinden) belirtir. |
| [getVerticalPosition()](#getVerticalPosition) | Çerçevenin kenarı ile [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) özelliğiyle belirtilen öğe arasındaki dikey mesafeyi alır. |
| [getWidth()](#getWidth) | Belirtilen çerçevenin genişliğini, nokta cinsinden alır. |
| [isFrame()](#isFrame) | Paragraf bir çerçeve ise  true  döndürür. |
### getHeight() {#getHeight}
```
public double getHeight()
```


Belirtilen çerçevenin yüksekliğini alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Belirtilen çerçevenin yüksekliği.
### getHeightRule() {#getHeightRule}
```
public int getHeightRule()
```


Belirtilen çerçevenin yüksekliğini belirleme kuralını alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Belirtilen çerçevenin yüksekliğini belirleme kuralı. Döndürülen değer, [HeightRule](../../com.aspose.words/heightrule/) sabitlerinden biridir.
### getHorizontalAlignment() {#getHorizontalAlignment}
```
public int getHorizontalAlignment()
```


Belirtilen çerçevenin yatay hizalamasını alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Belirtilen çerçevenin yatay hizalaması. Döndürülen değer, [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) sabitlerinden biridir.
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText}
```
public double getHorizontalDistanceFromText()
```


Bir çerçeve ile çevresindeki metin arasındaki yatay mesafeyi, nokta cinsinden alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Bir çerçeve ile çevresindeki metin arasındaki yatay mesafe, puan cinsinden.
### getHorizontalPosition() {#getHorizontalPosition}
```
public double getHorizontalPosition()
```


Çerçevenin kenarı ile [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition) özelliğiyle belirtilen öğe arasındaki yatay mesafeyi alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Çerçevenin kenarı ile [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition) özelliğiyle belirtilen öğe arasındaki yatay mesafe.
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition}
```
public int getRelativeHorizontalPosition()
```


Bir çerçevenin göreli yatay konumunu alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Bir çerçevenin göreli yatay konumu. Döndürülen değer, [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/) sabitlerinden biridir.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition}
```
public int getRelativeVerticalPosition()
```


Bir çerçevenin göreli dikey konumunu alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Bir çerçevenin göreli dikey konumu. Döndürülen değer, [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/) sabitlerinden biridir.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Belirtilen çerçevenin dikey hizalamasını alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Belirtilen çerçevenin dikey hizalaması. Döndürülen değer, [VerticalAlignment](../../com.aspose.words/verticalalignment/) sabitlerinden biridir.
### getVerticalDistanceFromText() {#getVerticalDistanceFromText}
```
public double getVerticalDistanceFromText()
```


Bir çerçeve ile çevresindeki metin arasındaki dikey mesafeyi (nokta cinsinden) belirtir.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - İlgili  double  değeri.
### getVerticalPosition() {#getVerticalPosition}
```
public double getVerticalPosition()
```


Çerçevenin kenarı ile [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) özelliğiyle belirtilen öğe arasındaki dikey mesafeyi alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Çerçevenin kenarı ile [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) özelliğiyle belirtilen öğe arasındaki dikey mesafe.
### getWidth() {#getWidth}
```
public double getWidth()
```


Belirtilen çerçevenin genişliğini, nokta cinsinden alır.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Belirtilen çerçevenin genişliği, puan cinsinden.
### isFrame() {#isFrame}
```
public boolean isFrame()
```


Paragraf bir çerçeve ise  true  döndürür.

 **Examples:** 

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
boolean -  true  eğer paragraf bir çerçeve ise.

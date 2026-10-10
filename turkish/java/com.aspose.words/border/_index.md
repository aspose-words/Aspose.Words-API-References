---
title: "Kenarlık"
linktitle: "Kenarlık"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesnenin kenarlığını temsil eder."
type: docs
weight: 46
url: /tr/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Bir nesnenin kenarlığını temsil eder.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Kenarlıklar, paragraf, paragraf içindeki metin yürütmesi veya tablo hücresi gibi çeşitli belge öğelerine uygulanabilir.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Üst kenarlı bir paragraf eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Kenarlık özelliklerini varsayılan değerlere sıfırlar. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Belirtilen kenarlığın mevcut kenarlığa değer olarak eşit olup olmadığını belirler. |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [getColor()](#getColor) | Kenarlık rengini alır. |
| [getDistanceFromText()](#getDistanceFromText) | Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığını alır. |
| [getLineStyle()](#getLineStyle) | Kenarlık stilini alır. |
| [getLineWidth()](#getLineWidth) | Kenarlık genişliğini nokta cinsinden alır. |
| [getShadow()](#getShadow) | Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri alır. |
| [getThemeColor()](#getThemeColor) | Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır. |
| [getTintAndShade()](#getTintAndShade) | Bir rengi açan veya karartan double değerini alır. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Eğer [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) değilse  true  döndürür. |
| [setColor(Color value)](#setColor-java.awt.Color) | Kenarlık rengini ayarlar. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığını ayarlar. |
| [setLineStyle(int value)](#setLineStyle-int) | Kenarlık stilini ayarlar. |
| [setLineWidth(double value)](#setLineWidth-double) | Kenarlık genişliğini nokta cinsinden ayarlar. |
| [setShadow(boolean value)](#setShadow-boolean) | Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri ayarlar. |
| [setThemeColor(int value)](#setThemeColor-int) | Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini ayarlar. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Bir rengi açan veya karartan double değerini ayarlar. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Kenarlık özelliklerini varsayılan değerlere sıfırlar.

 **Remarks:** 

Kenarlık özellikleri varsayılan değerlere sıfırlandığında, kenarlık görünmez olur.

 **Examples:** 

Bir paragraftan kenarlıkların nasıl kaldırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

### equals(Border rhs) {#equals-com.aspose.words.Border}
```
public boolean equals(Border rhs)
```


Belirtilen kenarlığın mevcut kenarlığa değer olarak eşit olup olmadığını belirler.

 **Examples:** 

Kenarlık koleksiyonlarının öğeleri nasıl paylaşabileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler.

 **Examples:** 

Kenarlık koleksiyonlarının öğeleri nasıl paylaşabileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Kenarlık rengini alır.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
java.awt.Color - Kenarlık rengi.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığını alır.

 **Remarks:** 

Hiçbir etkisi yoktur ve tablo hücrelerinin kenarlıkları için otomatik olarak sıfıra sıfırlanır.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
double - Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığı.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Kenarlık stilini alır.

 **Remarks:** 

Çizgi stilini none olarak ayarlarsanız, çizgi genişliği otomatik olarak sıfıra ayarlanır.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
int - Kenarlık stili. Döndürülen değer, [LineStyle](../../com.aspose.words/linestyle/) sabitlerinden biridir.
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Kenarlık genişliğini nokta cinsinden alır.

 **Remarks:** 

Çizgi stili none iken çizgi genişliğini sıfırdan büyük bir değere ayarlarsanız, çizgi stili otomatik olarak tek çizgiye değiştirilir.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
double - Kenarlık genişliği nokta cinsinden.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri alır.

 **Remarks:** 

Microsoft Word'de bir kenarlığın gölgesi olabilmesi için, dört tarafındaki (sol, üst, sağ ve alt) kenarlıkların aynı tip, genişlik ve renkte olması ve tümünün Shadow özelliğinin  true  olarak ayarlanmış olması gerekir.

 **Examples:** 

Gölge ile yeşil dalgalı sayfa kenarlığı nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
boolean - Kenarlığın gölgesi olup olmadığını gösteren bir değer.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır.

 **Examples:** 

Üst kenarlı bir paragraf eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Returns:**
int - Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengi. Döndürülen değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biridir.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Bir rengi açan veya karartan double değerini alır.

**Returns:**
double - Bir rengi açan veya karartan double değeri.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Eğer [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) değilse  true  döndürür.

 **Examples:** 

Bir paragraftan kenarlıkların nasıl kaldırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

**Returns:**
boolean -  true  eğer [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) değilse.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Kenarlık rengini ayarlar.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Kenarlık rengi. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığını ayarlar.

 **Remarks:** 

Hiçbir etkisi yoktur ve tablo hücrelerinin kenarlıkları için otomatik olarak sıfıra sıfırlanır.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Kenarlığın metinden veya sayfa kenarından nokta cinsinden uzaklığı. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Kenarlık stilini ayarlar.

 **Remarks:** 

Çizgi stilini none olarak ayarlarsanız, çizgi genişliği otomatik olarak sıfıra ayarlanır.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Kenarlık stili. Değer, [LineStyle](../../com.aspose.words/linestyle/) sabitlerinden biri olmalıdır. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Kenarlık genişliğini nokta cinsinden ayarlar.

 **Remarks:** 

Çizgi stili none iken çizgi genişliğini sıfırdan büyük bir değere ayarlarsanız, çizgi stili otomatik olarak tek çizgiye değiştirilir.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Kenarlık genişliği nokta cinsinden. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri ayarlar.

 **Remarks:** 

Microsoft Word'de bir kenarlığın gölgesi olabilmesi için, dört tarafındaki (sol, üst, sağ ve alt) kenarlıkların aynı tip, genişlik ve renkte olması ve tümünün Shadow özelliğinin  true  olarak ayarlanmış olması gerekir.

 **Examples:** 

Gölge ile yeşil dalgalı sayfa kenarlığı nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Kenarlığın gölgesi olup olmadığını gösteren bir değer. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini ayarlar.

 **Examples:** 

Üst kenarlı bir paragraf eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengi. Değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biri olmalıdır. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Bir rengi açan veya karartan double değerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Bir rengi açan veya karartan double değer. |


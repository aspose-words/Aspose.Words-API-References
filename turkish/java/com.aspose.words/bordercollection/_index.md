---
title: "BorderCollection"
linktitle: "BorderCollection"
second_title: "Aspose.Words Java için"
description: "Java'da Border nesnelerinden oluşan bir koleksiyon."
type: docs
weight: 47
url: /tr/java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

Bir [Border](../../com.aspose.words/border/) nesnelerinden oluşan koleksiyon.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Farklı belge öğeleri farklı kenarlara sahiptir. Örneğin, [ParagraphFormat](../../com.aspose.words/paragraphformat/) içinde [getBottom()](../../com.aspose.words/bordercollection/\#getBottom), [getLeft()](../../com.aspose.words/bordercollection/\#getLeft), [getRight()](../../com.aspose.words/bordercollection/\#getRight) ve [getTop()](../../com.aspose.words/bordercollection/\#getTop) kenarları bulunur. Her kenar için farklı biçimlendirme belirtebilir veya tüm kenarları döngüyle gezerek aynı biçimlendirmeyi uygulayabilirsiniz.

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


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Bir nesnenin tüm kenarlarını kaldırır. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | Kenarlık koleksiyonlarını karşılaştırır. |
| [get(int index)](#get-int) | İndexe göre bir [Border](../../com.aspose.words/border/) nesnesini alır. |
| [getBottom()](#getBottom) | Alt kenarı alır. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getColor()](#getColor) | Kenarlık rengini alır. |
| [getCount()](#getCount) | Koleksiyondaki kenarlık sayısını alır. |
| [getDistanceFromText()](#getDistanceFromText) | Kenarlığın metinden nokta cinsinden uzaklığını alır. |
| [getHorizontal()](#getHorizontal) | Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır. |
| [getLeft()](#getLeft) | Sol kenarlığı alır. |
| [getLineStyle()](#getLineStyle) | Kenarlık stilini alır. |
| [getLineWidth()](#getLineWidth) | Kenarlık genişliğini nokta cinsinden alır. |
| [getRight()](#getRight) | Sağ kenarlığı alır. |
| [getShadow()](#getShadow) | Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri alır. |
| [getTop()](#getTop) | Üst kenarlığı alır. |
| [getVertical()](#getVertical) | Hücreler arasında kullanılan dikey kenarlığı alır. |
| [iterator()](#iterator) | Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [setColor(Color value)](#setColor-java.awt.Color) | Kenarlık rengini ayarlar. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Kenarlığın metinden nokta cinsinden uzaklığını ayarlar. |
| [setLineStyle(int value)](#setLineStyle-int) | Kenarlık stilini ayarlar. |
| [setLineWidth(double value)](#setLineWidth-double) | Kenarlık genişliğini nokta cinsinden ayarlar. |
| [setShadow(boolean value)](#setShadow-boolean) | Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri ayarlar. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Bir nesnenin tüm kenarlarını kaldırır.

 **Examples:** 

Bir belgede tüm paragraflardan tüm kenarlıkları nasıl kaldıracağını gösterir.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // The first paragraph of this document has visible borders with these settings.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), firstParagraphBorders.getColor().getRGB());
 Assert.assertEquals(LineStyle.SINGLE, firstParagraphBorders.getLineStyle());
 Assert.assertEquals(3.0d, firstParagraphBorders.getLineWidth());

 // Use the "ClearFormatting" method on each paragraph to remove all borders.
 for (Paragraph paragraph : doc.getFirstSection().getBody().getParagraphs()) {
     paragraph.getParagraphFormat().getBorders().clearFormatting();

     for (Border border : paragraph.getParagraphFormat().getBorders()) {
         Assert.assertEquals(0, border.getColor().getRGB());
         Assert.assertEquals(LineStyle.NONE, border.getLineStyle());
         Assert.assertEquals(0.0d, border.getLineWidth());
     }
 }

 doc.save(getArtifactsDir() + "BorderCollection.RemoveAllBorders.docx");
 
```

### equals(BorderCollection brColl) {#equals-com.aspose.words.BorderCollection}
```
public boolean equals(BorderCollection brColl)
```


Kenarlık koleksiyonlarını karşılaştırır.

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
| brColl | [BorderCollection](../../com.aspose.words/bordercollection/) |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Border get(int index)
```


İndexe göre bir [Border](../../com.aspose.words/border/) nesnesini alır.

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
| indeks | int | Alınacak kenarlığın sıfır tabanlı dizini. |

**Returns:**
[Border](../../com.aspose.words/border/) - The corresponding [Border](../../com.aspose.words/border/) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


Alt kenarı alır.

 **Examples:** 

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The bottom border.
### getByBorderType(int borderType) {#getByBorderType-int}
```
public Border getByBorderType(int borderType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border/)
### getColor() {#getColor}
```
public Color getColor()
```


Kenarlık rengini alır.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın rengini döndürür.

Koleksiyondaki diyagonal kenarlıklar hariç tüm kenarlıkların rengini ayarlar.

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
java.awt.Color - Kenarlık rengi.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki kenarlık sayısını alır.

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

**Returns:**
int - Koleksiyondaki kenarlık sayısı.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Kenarlığın metinden nokta cinsinden uzaklığını alır.

 **Remarks:** 

İlk kenarlık için metinden olan mesafeyi alır.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların metinden olan mesafesini ayarlar.

Hiçbir etkisi yoktur ve tablo hücrelerinin kenarlıkları için otomatik olarak sıfıra sıfırlanır.

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
double - Kenarlığın metinden nokta cinsinden mesafesi.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır.

 **Examples:** 

Bir paragraf biçimine yatay kenarlıklara ayarların nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a red horizontal border for the paragraph. Any paragraphs created afterwards will inherit these border settings.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 borders.getHorizontal().setColor(Color.RED);
 borders.getHorizontal().setLineStyle(LineStyle.DASH_SMALL_GAP);
 borders.getHorizontal().setLineWidth(3.0);

 // Write text to the document without creating a new paragraph afterward.
 // Since there is no paragraph underneath, the horizontal border will not be visible.
 builder.write("Paragraph above horizontal border.");

 // Once we add a second paragraph, the border of the first paragraph will become visible.
 builder.insertParagraph();
 builder.write("Paragraph below horizontal border.");

 doc.save(getArtifactsDir() + "Border.HorizontalBorders.docx");
 
```

Bir tablo satırı biçimine dikey kenarlıklara ayarların nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with red and blue inner borders.
 Table table = builder.startTable();

 for (int i = 0; i < 3; i++) {
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, Column 1", i + 1));
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, Column 2", i + 1));

     Row row = builder.endRow();
     BorderCollection borders = row.getRowFormat().getBorders();

     // Adjust the appearance of borders that will appear between rows.
     borders.getHorizontal().setColor(Color.RED);
     borders.getHorizontal().setLineStyle(LineStyle.DOT);
     borders.getHorizontal().setLineWidth(2.0d);

     // Adjust the appearance of borders that will appear between cells.
     borders.getVertical().setColor(Color.BLUE);
     borders.getVertical().setLineStyle(LineStyle.DOT);
     borders.getVertical().setLineWidth(2.0d);
 }

 // A row format, and a cell's inner paragraph use different border settings.
 Border border = table.getFirstRow().getFirstCell().getLastParagraph().getParagraphFormat().getBorders().getVertical();

 Assert.assertEquals(0, border.getColor().getRGB());
 Assert.assertEquals(0.0d, border.getLineWidth());
 Assert.assertEquals(LineStyle.NONE, border.getLineStyle());

 doc.save(getArtifactsDir() + "Border.VerticalBorders.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The horizontal border that is used between cells or conforming paragraphs.
### getLeft() {#getLeft}
```
public Border getLeft()
```


Sol kenarlığı alır.

 **Examples:** 

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The left border.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Kenarlık stilini alır.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın stilini döndürür.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların stilini ayarlar.

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
int - Kenarlık stili. Döndürülen değer, [LineStyle](../../com.aspose.words/linestyle/) sabitlerinden biridir.
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Kenarlık genişliğini nokta cinsinden alır.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın genişliğini döndürür.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların genişliğini ayarlar.

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
double - Kenarlık genişliği nokta cinsinden.
### getRight() {#getRight}
```
public Border getRight()
```


Sağ kenarlığı alır.

 **Examples:** 

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The right border.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri alır.

 **Remarks:** 

Koleksiyondaki ilk kenarlıktan değeri alır.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların değerini ayarlar.

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
### getTop() {#getTop}
```
public Border getTop()
```


Üst kenarlığı alır.

 **Examples:** 

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The top border.
### getVertical() {#getVertical}
```
public Border getVertical()
```


Hücreler arasında kullanılan dikey kenarlığı alır.

 **Examples:** 

Bir tablo satırı biçimine dikey kenarlıklara ayarların nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with red and blue inner borders.
 Table table = builder.startTable();

 for (int i = 0; i < 3; i++) {
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, Column 1", i + 1));
     builder.insertCell();
     builder.write(MessageFormat.format("Row {0}, Column 2", i + 1));

     Row row = builder.endRow();
     BorderCollection borders = row.getRowFormat().getBorders();

     // Adjust the appearance of borders that will appear between rows.
     borders.getHorizontal().setColor(Color.RED);
     borders.getHorizontal().setLineStyle(LineStyle.DOT);
     borders.getHorizontal().setLineWidth(2.0d);

     // Adjust the appearance of borders that will appear between cells.
     borders.getVertical().setColor(Color.BLUE);
     borders.getVertical().setLineStyle(LineStyle.DOT);
     borders.getVertical().setLineWidth(2.0d);
 }

 // A row format, and a cell's inner paragraph use different border settings.
 Border border = table.getFirstRow().getFirstCell().getLastParagraph().getParagraphFormat().getBorders().getVertical();

 Assert.assertEquals(0, border.getColor().getRGB());
 Assert.assertEquals(0.0d, border.getLineWidth());
 Assert.assertEquals(LineStyle.NONE, border.getLineStyle());

 doc.save(getArtifactsDir() + "Border.VerticalBorders.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - The vertical border that is used between cells.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür.

 **Examples:** 

Bir paragraf biçim nesnesindeki tüm kenarlıklar üzerinde yineleme yapmayı ve düzenlemeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the builder's paragraph format settings to create a green wave border on all sides.
 BorderCollection borders = builder.getParagraphFormat().getBorders();

 Iterator enumerator = borders.iterator();
 while (enumerator.hasNext()) {
     Border border = enumerator.next();
     border.setColor(Color.green);
     border.setLineStyle(LineStyle.WAVE);
     border.setLineWidth(3.0);
 }

 // Insert a paragraph. Our border settings will determine the appearance of its border.
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "BorderCollection.GetBordersEnumerator.docx");
 
```

**Returns:**
java.util.Iterator
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Kenarlık rengini ayarlar.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın rengini döndürür.

Koleksiyondaki diyagonal kenarlıklar hariç tüm kenarlıkların rengini ayarlar.

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
| değer | java.awt.Color | Kenarlık rengi. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Kenarlığın metinden nokta cinsinden uzaklığını ayarlar.

 **Remarks:** 

İlk kenarlık için metinden olan mesafeyi alır.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların metinden olan mesafesini ayarlar.

Hiçbir etkisi yoktur ve tablo hücrelerinin kenarlıkları için otomatik olarak sıfıra sıfırlanır.

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
| değer | double | Kenarlığın metinden nokta cinsinden mesafesi. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Kenarlık stilini ayarlar.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın stilini döndürür.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların stilini ayarlar.

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
| value | int | Kenarlık stili. Değer, [LineStyle](../../com.aspose.words/linestyle/) sabitlerinden biri olmalıdır. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Kenarlık genişliğini nokta cinsinden ayarlar.

 **Remarks:** 

Koleksiyondaki ilk kenarlığın genişliğini döndürür.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların genişliğini ayarlar.

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
| değer | double | Kenarlık genişliği nokta cinsinden. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Kenarlığın gölgeye sahip olup olmadığını gösteren bir değeri ayarlar.

 **Remarks:** 

Koleksiyondaki ilk kenarlıktan değeri alır.

Köşegen kenarlıklar hariç, koleksiyondaki tüm kenarlıkların değerini ayarlar.

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


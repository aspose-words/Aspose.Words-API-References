---
title: "BorderCollection"
linktitle: "BorderCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من كائنات Border في Java."
type: docs
weight: 47
url: /ar/java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

مجموعة من كائنات [Border](../../com.aspose.words/border/).

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

تحتوي عناصر المستند المختلفة على حدود مختلفة. على سبيل المثال، يحتوي [ParagraphFormat](../../com.aspose.words/paragraphformat/) على حدود [getBottom()](../../com.aspose.words/bordercollection/\#getBottom)، [getLeft()](../../com.aspose.words/bordercollection/\#getLeft)، [getRight()](../../com.aspose.words/bordercollection/\#getRight) و [getTop()](../../com.aspose.words/bordercollection/\#getTop). يمكنك تحديد تنسيق مختلف لكل حد بشكل مستقل أو التكرار عبر جميع الحدود وتطبيق نفس التنسيق.

 **Examples:** 

يظهر كيفية إدراج فقرة بحد أعلى.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يزيل جميع حدود كائن. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | يقارن مجموعات الحدود. |
| [get(int index)](#get-int) | يسترجع كائن [Border](../../com.aspose.words/border/) حسب الفهرس. |
| [getBottom()](#getBottom) | يحصل على الحد السفلي. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getColor()](#getColor) | يحصل على لون الحد. |
| [getCount()](#getCount) | يحصل على عدد الحدود في المجموعة. |
| [getDistanceFromText()](#getDistanceFromText) | يحصل على مسافة الحد من النص بالنقاط. |
| [getHorizontal()](#getHorizontal) | يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المتطابقة. |
| [getLeft()](#getLeft) | يحصل على الحد الأيسر. |
| [getLineStyle()](#getLineStyle) | يحصل على نمط الحد. |
| [getLineWidth()](#getLineWidth) | يحصل على عرض الحد بالنقاط. |
| [getRight()](#getRight) | يحصل على الحد الأيمن. |
| [getShadow()](#getShadow) | يحصل على قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
| [getTop()](#getTop) | يحصل على الحد العلوي. |
| [getVertical()](#getVertical) | يحصل على الحد الرأسي المستخدم بين الخلايا. |
| [iterator()](#iterator) | يعيد كائن عداد يمكن استخدامه للتنقل عبر جميع الحدود في المجموعة. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون الحد. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | يضبط مسافة الحد من النص بالنقاط. |
| [setLineStyle(int value)](#setLineStyle-int) | يضبط نمط الحد. |
| [setLineWidth(double value)](#setLineWidth-double) | يضبط عرض الحد بالنقاط. |
| [setShadow(boolean value)](#setShadow-boolean) | يضبط قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يزيل جميع حدود كائن.

 **Examples:** 

يوضح كيفية إزالة جميع الحدود من جميع الفقرات في المستند.

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


يقارن مجموعات الحدود.

 **Examples:** 

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection/) |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Border get(int index)
```


يسترجع كائن [Border](../../com.aspose.words/border/) حسب الفهرس.

 **Examples:** 

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للحد المراد استرجاعه. |

**Returns:**
[Border](../../com.aspose.words/border/) - The corresponding [Border](../../com.aspose.words/border/) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


يحصل على الحد السفلي.

 **Examples:** 

يوضح كيفية تطبيق لون الحد والظل أثناء بناء جدول.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border/)
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على لون الحد.

 **Remarks:** 

يعيد لون أول حد في المجموعة.

يضبط لون جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
java.awt.Color - لون الحد.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد الحدود في المجموعة.

 **Examples:** 

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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
int - عدد الحدود في المجموعة.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


يحصل على مسافة الحد من النص بالنقاط.

 **Remarks:** 

يحصل على المسافة من النص للحد الأول.

يضبط المسافة من النص لجميع الحدود في المجموعة باستثناء الحدود القطرية.

ليس له أي تأثير وسيتم إعادة ضبطه تلقائيًا إلى الصفر للحدود في خلايا الجدول.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
double - مسافة الحد من النص بالنقاط.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المتطابقة.

 **Examples:** 

يوضح كيفية تطبيق الإعدادات على الحدود الأفقية لتنسيق الفقرة.

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

يوضح كيفية تطبيق الإعدادات على الحدود العمودية لتنسيق صف الجدول.

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


يحصل على الحد الأيسر.

 **Examples:** 

يوضح كيفية تطبيق لون الحد والظل أثناء بناء جدول.

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


يحصل على نمط الحد.

 **Remarks:** 

يعيد نمط الحد الأول في المجموعة.

يضبط نمط جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
int - نمط الحد. القيمة المرجعة هي واحدة من ثوابت [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


يحصل على عرض الحد بالنقاط.

 **Remarks:** 

يعيد عرض الحد الأول في المجموعة.

يضبط عرض جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
double - عرض الحد بالنقاط.
### getRight() {#getRight}
```
public Border getRight()
```


يحصل على الحد الأيمن.

 **Examples:** 

يوضح كيفية تطبيق لون الحد والظل أثناء بناء جدول.

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


يحصل على قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

 **Remarks:** 

يحصل على القيمة من الحد الأول في المجموعة.

يضبط القيمة لجميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
boolean - قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.
### getTop() {#getTop}
```
public Border getTop()
```


يحصل على الحد العلوي.

 **Examples:** 

يوضح كيفية تطبيق لون الحد والظل أثناء بناء جدول.

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


يحصل على الحد الرأسي المستخدم بين الخلايا.

 **Examples:** 

يوضح كيفية تطبيق الإعدادات على الحدود العمودية لتنسيق صف الجدول.

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


يعيد كائن عداد يمكن استخدامه للتنقل عبر جميع الحدود في المجموعة.

 **Examples:** 

يوضح كيفية التكرار وتعديل جميع الحدود في كائن تنسيق الفقرة.

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


يضبط لون الحد.

 **Remarks:** 

يعيد لون أول حد في المجموعة.

يضبط لون جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الحد. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


يضبط مسافة الحد من النص بالنقاط.

 **Remarks:** 

يحصل على المسافة من النص للحد الأول.

يضبط المسافة من النص لجميع الحدود في المجموعة باستثناء الحدود القطرية.

ليس له أي تأثير وسيتم إعادة ضبطه تلقائيًا إلى الصفر للحدود في خلايا الجدول.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | مسافة الحد من النص بالنقاط. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


يضبط نمط الحد.

 **Remarks:** 

يعيد نمط الحد الأول في المجموعة.

يضبط نمط جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نمط الحد. يجب أن تكون القيمة واحدة من ثوابت [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


يضبط عرض الحد بالنقاط.

 **Remarks:** 

يعيد عرض الحد الأول في المجموعة.

يضبط عرض جميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | عرض الحد بالنقاط. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

 **Remarks:** 

يحصل على القيمة من الحد الأول في المجموعة.

يضبط القيمة لجميع الحدود في المجموعة باستثناء الحدود القطرية.

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |


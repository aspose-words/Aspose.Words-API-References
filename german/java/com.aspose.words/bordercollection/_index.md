---
title: "BorderCollection"
linktitle: "BorderCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von Border-Objekten in Java."
type: docs
weight: 47
url: /de/java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

Eine Sammlung von [Border](../../com.aspose.words/border/) Objekten.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Verschiedene Dokumentelemente haben unterschiedliche Rahmen. Zum Beispiel hat [ParagraphFormat](../../com.aspose.words/paragraphformat/) die Rahmen [getBottom()](../../com.aspose.words/bordercollection/\#getBottom), [getLeft()](../../com.aspose.words/bordercollection/\#getLeft), [getRight()](../../com.aspose.words/bordercollection/\#getRight) und [getTop()](../../com.aspose.words/bordercollection/\#getTop). Sie können für jeden Rahmen unabhängig unterschiedliche Formatierungen festlegen oder alle Rahmen durchlaufen und dieselbe Formatierung anwenden.

 **Examples:** 

Zeigt, wie ein Absatz mit einem oberen Rahmen eingefügt wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Entfernt alle Rahmen eines Objekts. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | Vergleicht Sammlungen von Rahmen. |
| [get(int index)](#get-int) | Ruft ein [Border](../../com.aspose.words/border/) Objekt anhand des Index ab. |
| [getBottom()](#getBottom) | Liefert den unteren Rahmen. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getColor()](#getColor) | Liefert die Rahmenfarbe. |
| [getCount()](#getCount) | Liefert die Anzahl der Rahmen in der Sammlung. |
| [getDistanceFromText()](#getDistanceFromText) | Liefert den Abstand des Rahmens vom Text in Punkten. |
| [getHorizontal()](#getHorizontal) | Liefert den horizontalen Rahmen, der zwischen Zellen oder zusammengehörigen Absätzen verwendet wird. |
| [getLeft()](#getLeft) | Liefert den linken Rahmen. |
| [getLineStyle()](#getLineStyle) | Liefert den Rahmenstil. |
| [getLineWidth()](#getLineWidth) | Liefert die Rahmenbreite in Punkten. |
| [getRight()](#getRight) | Liefert den rechten Rahmen. |
| [getShadow()](#getShadow) | Liefert einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
| [getTop()](#getTop) | Liefert den oberen Rahmen. |
| [getVertical()](#getVertical) | Liefert den vertikalen Rahmen, der zwischen Zellen verwendet wird. |
| [iterator()](#iterator) | Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle Rahmen in der Sammlung zu iterieren. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt die Rahmenfarbe. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Setzt den Abstand des Rahmens vom Text in Punkten. |
| [setLineStyle(int value)](#setLineStyle-int) | Setzt den Rahmenstil. |
| [setLineWidth(double value)](#setLineWidth-double) | Setzt die Rahmenbreite in Punkten. |
| [setShadow(boolean value)](#setShadow-boolean) | Setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Entfernt alle Rahmen eines Objekts.

 **Examples:** 

Zeigt, wie man alle Rahmen aus allen Absätzen in einem Dokument entfernt.

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


Vergleicht Sammlungen von Rahmen.

 **Examples:** 

Zeigt, wie Rahmenkollektionen Elemente teilen können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection/) |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Border get(int index)
```


Ruft ein [Border](../../com.aspose.words/border/) Objekt anhand des Index ab.

 **Examples:** 

Zeigt, wie Rahmenkollektionen Elemente teilen können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des abzurufenden Rahmens. |

**Returns:**
[Border](../../com.aspose.words/border/) - The corresponding [Border](../../com.aspose.words/border/) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


Liefert den unteren Rahmen.

 **Examples:** 

Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border/)
### getColor() {#getColor}
```
public Color getColor()
```


Liefert die Rahmenfarbe.

 **Remarks:** 

Gibt die Farbe des ersten Rands in der Sammlung zurück.

Setzt die Farbe aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
java.awt.Color - Die Randfarbe.
### getCount() {#getCount}
```
public int getCount()
```


Liefert die Anzahl der Rahmen in der Sammlung.

 **Examples:** 

Zeigt, wie Rahmenkollektionen Elemente teilen können.

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
int - Die Anzahl der Ränder in der Sammlung.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Liefert den Abstand des Rahmens vom Text in Punkten.

 **Remarks:** 

Ermittelt den Abstand vom Text für den ersten Rand.

Setzt den Abstand vom Text für alle Ränder in der Sammlung, ausgenommen diagonale Ränder.

Hat keine Wirkung und wird für Tabellenzellenränder automatisch auf Null zurückgesetzt.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
double - Abstand des Rands vom Text in Punkten.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


Liefert den horizontalen Rahmen, der zwischen Zellen oder zusammengehörigen Absätzen verwendet wird.

 **Examples:** 

Zeigt, wie man Einstellungen auf horizontale Ränder eines Absatzformats anwendet.

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

Zeigt, wie man Einstellungen auf vertikale Ränder eines Tabellenzeilenformats anwendet.

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


Liefert den linken Rahmen.

 **Examples:** 

Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.

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


Liefert den Rahmenstil.

 **Remarks:** 

Gibt den Stil des ersten Rands in der Sammlung zurück.

Setzt den Stil aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
int - Der Randstil. Der zurückgegebene Wert ist einer der Konstanten von [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Liefert die Rahmenbreite in Punkten.

 **Remarks:** 

Gibt die Breite des ersten Rands in der Sammlung zurück.

Setzt die Breite aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
double - Die Randbreite in Punkten.
### getRight() {#getRight}
```
public Border getRight()
```


Liefert den rechten Rahmen.

 **Examples:** 

Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.

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


Liefert einen Wert, der angibt, ob der Rahmen einen Schatten hat.

 **Remarks:** 

Ermittelt den Wert des ersten Rands in der Sammlung.

Setzt den Wert für alle Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
boolean - Ein Wert, der angibt, ob der Rand einen Schatten hat.
### getTop() {#getTop}
```
public Border getTop()
```


Liefert den oberen Rahmen.

 **Examples:** 

Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.

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


Liefert den vertikalen Rahmen, der zwischen Zellen verwendet wird.

 **Examples:** 

Zeigt, wie man Einstellungen auf vertikale Ränder eines Tabellenzeilenformats anwendet.

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


Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle Rahmen in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man über alle Ränder in einem Absatzformatobjekt iteriert und sie bearbeitet.

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


Setzt die Rahmenfarbe.

 **Remarks:** 

Gibt die Farbe des ersten Rands in der Sammlung zurück.

Setzt die Farbe aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Randfarbe. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Setzt den Abstand des Rahmens vom Text in Punkten.

 **Remarks:** 

Ermittelt den Abstand vom Text für den ersten Rand.

Setzt den Abstand vom Text für alle Ränder in der Sammlung, ausgenommen diagonale Ränder.

Hat keine Wirkung und wird für Tabellenzellenränder automatisch auf Null zurückgesetzt.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Abstand des Rands vom Text in Punkten. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Setzt den Rahmenstil.

 **Remarks:** 

Gibt den Stil des ersten Rands in der Sammlung zurück.

Setzt den Stil aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Randstil. Der Wert muss einer der Konstanten von [LineStyle](../../com.aspose.words/linestyle/) sein. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Setzt die Rahmenbreite in Punkten.

 **Remarks:** 

Gibt die Breite des ersten Rands in der Sammlung zurück.

Setzt die Breite aller Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Randbreite in Punkten. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat.

 **Remarks:** 

Ermittelt den Wert des ersten Rands in der Sammlung.

Setzt den Wert für alle Ränder in der Sammlung, ausgenommen diagonale Ränder.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob der Rand einen Schatten hat. |


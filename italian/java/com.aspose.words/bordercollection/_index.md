---
title: "BorderCollection"
linktitle: "BorderCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti Border in Java."
type: docs
weight: 47
url: /it/java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

Una raccolta di oggetti [Border](../../com.aspose.words/border/).

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Remarks:** 

Diversi elementi del documento hanno bordi diversi. Ad esempio, [ParagraphFormat](../../com.aspose.words/paragraphformat/) ha i bordi [getBottom()](../../com.aspose.words/bordercollection/\#getBottom), [getLeft()](../../com.aspose.words/bordercollection/\#getLeft), [getRight()](../../com.aspose.words/bordercollection/\#getRight) e [getTop()](../../com.aspose.words/bordercollection/\#getTop). È possibile specificare una formattazione diversa per ciascun bordo in modo indipendente o enumerare tutti i bordi e applicare la stessa formattazione.

 **Examples:** 

Mostra come inserire un paragrafo con un bordo superiore.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Rimuove tutti i bordi di un oggetto. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | Confronta le raccolte di bordi. |
| [get(int index)](#get-int) | Recupera un oggetto [Border](../../com.aspose.words/border/) per indice. |
| [getBottom()](#getBottom) | Ottiene il bordo inferiore. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getColor()](#getColor) | Ottiene il colore del bordo. |
| [getCount()](#getCount) | Ottiene il numero di bordi nella collezione. |
| [getDistanceFromText()](#getDistanceFromText) | Ottiene la distanza del bordo dal testo in punti. |
| [getHorizontal()](#getHorizontal) | Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi corrispondenti. |
| [getLeft()](#getLeft) | Ottiene il bordo sinistro. |
| [getLineStyle()](#getLineStyle) | Ottiene lo stile del bordo. |
| [getLineWidth()](#getLineWidth) | Ottiene la larghezza del bordo in punti. |
| [getRight()](#getRight) | Ottiene il bordo destro. |
| [getShadow()](#getShadow) | Ottiene un valore che indica se il bordo ha un'ombra. |
| [getTop()](#getTop) | Ottiene il bordo superiore. |
| [getVertical()](#getVertical) | Ottiene il bordo verticale utilizzato tra le celle. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti i bordi nella collezione. |
| [setColor(Color value)](#setColor-java.awt.Color) | Imposta il colore del bordo. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Imposta la distanza del bordo dal testo in punti. |
| [setLineStyle(int value)](#setLineStyle-int) | Imposta lo stile del bordo. |
| [setLineWidth(double value)](#setLineWidth-double) | Imposta la larghezza del bordo in punti. |
| [setShadow(boolean value)](#setShadow-boolean) | Imposta un valore che indica se il bordo ha un'ombra. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Rimuove tutti i bordi di un oggetto.

 **Examples:** 

Mostra come rimuovere tutti i bordi da tutti i paragrafi in un documento.

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


Confronta le raccolte di bordi.

 **Examples:** 

Mostra come le collezioni di bordi possono condividere elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection/) |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Border get(int index)
```


Recupera un oggetto [Border](../../com.aspose.words/border/) per indice.

 **Examples:** 

Mostra come le collezioni di bordi possono condividere elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero del bordo da recuperare. |

**Returns:**
[Border](../../com.aspose.words/border/) - The corresponding [Border](../../com.aspose.words/border/) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


Ottiene il bordo inferiore.

 **Examples:** 

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border/)
### getColor() {#getColor}
```
public Color getColor()
```


Ottiene il colore del bordo.

 **Remarks:** 

Restituisce il colore del primo bordo nella collezione.

Imposta il colore di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
java.awt.Color - Il colore del bordo.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di bordi nella collezione.

 **Examples:** 

Mostra come le collezioni di bordi possono condividere elementi.

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
int - Il numero di bordi nella collezione.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Ottiene la distanza del bordo dal testo in punti.

 **Remarks:** 

Ottiene la distanza dal testo per il primo bordo.

Imposta la distanza dal testo per tutti i bordi nella collezione escludendo i bordi diagonali.

Non ha effetto e verrà automaticamente reimpostato a zero per i bordi delle celle della tabella.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
double - Distanza del bordo dal testo in punti.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi corrispondenti.

 **Examples:** 

Mostra come applicare le impostazioni ai bordi orizzontali nel formato di un paragrafo.

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

Mostra come applicare le impostazioni ai bordi verticali nel formato di una riga di tabella.

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


Ottiene il bordo sinistro.

 **Examples:** 

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

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


Ottiene lo stile del bordo.

 **Remarks:** 

Restituisce lo stile del primo bordo nella collezione.

Imposta lo stile di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
int - Lo stile del bordo. Il valore restituito è una delle costanti [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Ottiene la larghezza del bordo in punti.

 **Remarks:** 

Restituisce la larghezza del primo bordo nella collezione.

Imposta la larghezza di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
double - La larghezza del bordo in punti.
### getRight() {#getRight}
```
public Border getRight()
```


Ottiene il bordo destro.

 **Examples:** 

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

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


Ottiene un valore che indica se il bordo ha un'ombra.

 **Remarks:** 

Ottiene il valore dal primo bordo nella collezione.

Imposta il valore per tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
boolean - Un valore che indica se il bordo ha un'ombra.
### getTop() {#getTop}
```
public Border getTop()
```


Ottiene il bordo superiore.

 **Examples:** 

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

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


Ottiene il bordo verticale utilizzato tra le celle.

 **Examples:** 

Mostra come applicare le impostazioni ai bordi verticali nel formato di una riga di tabella.

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


Restituisce un oggetto enumeratore che può essere usato per iterare su tutti i bordi nella collezione.

 **Examples:** 

Mostra come iterare e modificare tutti i bordi in un oggetto di formato del paragrafo.

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


Imposta il colore del bordo.

 **Remarks:** 

Restituisce il colore del primo bordo nella collezione.

Imposta il colore di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il colore del bordo. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Imposta la distanza del bordo dal testo in punti.

 **Remarks:** 

Ottiene la distanza dal testo per il primo bordo.

Imposta la distanza dal testo per tutti i bordi nella collezione escludendo i bordi diagonali.

Non ha effetto e verrà automaticamente reimpostato a zero per i bordi delle celle della tabella.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Distanza del bordo dal testo in punti. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Imposta lo stile del bordo.

 **Remarks:** 

Restituisce lo stile del primo bordo nella collezione.

Imposta lo stile di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Lo stile del bordo. Il valore deve essere una delle costanti [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Imposta la larghezza del bordo in punti.

 **Remarks:** 

Restituisce la larghezza del primo bordo nella collezione.

Imposta la larghezza di tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La larghezza del bordo in punti. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Imposta un valore che indica se il bordo ha un'ombra.

 **Remarks:** 

Ottiene il valore dal primo bordo nella collezione.

Imposta il valore per tutti i bordi nella collezione escludendo i bordi diagonali.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che indica se il bordo ha un'ombra. |


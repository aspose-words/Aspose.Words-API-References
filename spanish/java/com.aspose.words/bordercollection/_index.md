---
title: "BorderCollection"
linktitle: "BorderCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos Border en Java."
type: docs
weight: 47
url: /es/java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

Una colección de objetos [Border](../../com.aspose.words/border/).

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Los diferentes elementos del documento tienen bordes diferentes. Por ejemplo, [ParagraphFormat](../../com.aspose.words/paragraphformat/) tiene los bordes [getBottom()](../../com.aspose.words/bordercollection/\#getBottom), [getLeft()](../../com.aspose.words/bordercollection/\#getLeft), [getRight()](../../com.aspose.words/bordercollection/\#getRight) y [getTop()](../../com.aspose.words/bordercollection/\#getTop). Puede especificar un formato diferente para cada borde de forma independiente o recorrer todos los bordes y aplicar el mismo formato.

 **Examples:** 

Muestra cómo insertar un párrafo con un borde superior.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Elimina todos los bordes de un objeto. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | Compara colecciones de bordes. |
| [get(int index)](#get-int) | Recupera un objeto [Border](../../com.aspose.words/border/) por índice. |
| [getBottom()](#getBottom) | Obtiene el borde inferior. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getColor()](#getColor) | Obtiene el color del borde. |
| [getCount()](#getCount) | Obtiene el número de bordes en la colección. |
| [getDistanceFromText()](#getDistanceFromText) | Obtiene la distancia del borde al texto en puntos. |
| [getHorizontal()](#getHorizontal) | Obtiene el borde horizontal que se usa entre celdas o párrafos conformes. |
| [getLeft()](#getLeft) | Obtiene el borde izquierdo. |
| [getLineStyle()](#getLineStyle) | Obtiene el estilo del borde. |
| [getLineWidth()](#getLineWidth) | Obtiene el ancho del borde en puntos. |
| [getRight()](#getRight) | Obtiene el borde derecho. |
| [getShadow()](#getShadow) | Obtiene un valor que indica si el borde tiene sombra. |
| [getTop()](#getTop) | Obtiene el borde superior. |
| [getVertical()](#getVertical) | Obtiene el borde vertical que se usa entre celdas. |
| [iterator()](#iterator) | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los bordes de la colección. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color del borde. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Establece la distancia del borde al texto en puntos. |
| [setLineStyle(int value)](#setLineStyle-int) | Establece el estilo del borde. |
| [setLineWidth(double value)](#setLineWidth-double) | Establece el ancho del borde en puntos. |
| [setShadow(boolean value)](#setShadow-boolean) | Establece un valor que indica si el borde tiene sombra. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Elimina todos los bordes de un objeto.

 **Examples:** 

Muestra cómo eliminar todos los bordes de todos los párrafos en un documento.

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


Compara colecciones de bordes.

 **Examples:** 

Muestra cómo las colecciones de bordes pueden compartir elementos.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection/) |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Border get(int index)
```


Recupera un objeto [Border](../../com.aspose.words/border/) por índice.

 **Examples:** 

Muestra cómo las colecciones de bordes pueden compartir elementos.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero del borde a recuperar. |

**Returns:**
[Border](../../com.aspose.words/border/) - The corresponding [Border](../../com.aspose.words/border/) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


Obtiene el borde inferior.

 **Examples:** 

Muestra cómo aplicar el color del borde y de sombreado al crear una tabla.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border/)
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color del borde.

 **Remarks:** 

Devuelve el color del primer borde en la colección.

Establece el color de todos los bordes de la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
java.awt.Color - El color del borde.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de bordes en la colección.

 **Examples:** 

Muestra cómo las colecciones de bordes pueden compartir elementos.

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
int - El número de bordes en la colección.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Obtiene la distancia del borde al texto en puntos.

 **Remarks:** 

Obtiene la distancia del texto para el primer borde.

Establece la distancia del texto para todos los bordes de la colección excluyendo los bordes diagonales.

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de tabla.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
double - Distancia del borde al texto en puntos.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


Obtiene el borde horizontal que se usa entre celdas o párrafos conformes.

 **Examples:** 

Muestra cómo aplicar configuraciones a los bordes horizontales al formato de un párrafo.

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

Muestra cómo aplicar configuraciones a los bordes verticales al formato de una fila de tabla.

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


Obtiene el borde izquierdo.

 **Examples:** 

Muestra cómo aplicar el color del borde y de sombreado al crear una tabla.

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


Obtiene el estilo del borde.

 **Remarks:** 

Devuelve el estilo del primer borde en la colección.

Establece el estilo de todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
int - El estilo del borde. El valor devuelto es una de las constantes [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Obtiene el ancho del borde en puntos.

 **Remarks:** 

Devuelve el ancho del primer borde en la colección.

Establece el ancho de todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
double - El ancho del borde en puntos.
### getRight() {#getRight}
```
public Border getRight()
```


Obtiene el borde derecho.

 **Examples:** 

Muestra cómo aplicar el color del borde y de sombreado al crear una tabla.

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


Obtiene un valor que indica si el borde tiene sombra.

 **Remarks:** 

Obtiene el valor del primer borde en la colección.

Establece el valor para todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
boolean - Un valor que indica si el borde tiene sombra.
### getTop() {#getTop}
```
public Border getTop()
```


Obtiene el borde superior.

 **Examples:** 

Muestra cómo aplicar el color del borde y de sombreado al crear una tabla.

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


Obtiene el borde vertical que se usa entre celdas.

 **Examples:** 

Muestra cómo aplicar configuraciones a los bordes verticales al formato de una fila de tabla.

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


Devuelve un objeto enumerador que puede usarse para iterar sobre todos los bordes de la colección.

 **Examples:** 

Muestra cómo iterar y editar todos los bordes en un objeto de formato de párrafo.

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


Establece el color del borde.

 **Remarks:** 

Devuelve el color del primer borde en la colección.

Establece el color de todos los bordes de la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color del borde. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Establece la distancia del borde al texto en puntos.

 **Remarks:** 

Obtiene la distancia del texto para el primer borde.

Establece la distancia del texto para todos los bordes de la colección excluyendo los bordes diagonales.

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de tabla.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Distancia del borde al texto en puntos. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Establece el estilo del borde.

 **Remarks:** 

Devuelve el estilo del primer borde en la colección.

Establece el estilo de todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El estilo del borde. El valor debe ser una de las constantes [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Establece el ancho del borde en puntos.

 **Remarks:** 

Devuelve el ancho del primer borde en la colección.

Establece el ancho de todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El ancho del borde en puntos. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Establece un valor que indica si el borde tiene sombra.

 **Remarks:** 

Obtiene el valor del primer borde en la colección.

Establece el valor para todos los bordes en la colección excluyendo los bordes diagonales.

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si el borde tiene sombra. |


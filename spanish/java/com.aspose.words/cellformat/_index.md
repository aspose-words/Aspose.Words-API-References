---
title: "CellFormat"
linktitle: "CellFormat"
second_title: "Aspose.Words para Java"
description: "Representa todo el formato de una celda de tabla en Java."
type: docs
weight: 61
url: /es/java/com.aspose.words/cellformat/
---

**Inheritance:**
java.lang.Object
```
public class CellFormat
```

Representa todo el formato de una celda de tabla.

Para obtener más información, visite el artículo de documentación [ Working with Tables ][Working with Tables].

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo modificar el formato de filas y celdas en una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("City");
 builder.insertCell();
 builder.write("Country");
 builder.endRow();
 builder.insertCell();
 builder.write("London");
 builder.insertCell();
 builder.write("U.K.");
 builder.endTable();

 // Use the first row's "RowFormat" property to modify the formatting
 // of the contents of all cells in this row.
 RowFormat rowFormat = table.getFirstRow().getRowFormat();
 rowFormat.setHeight(25.0);
 rowFormat.getBorders().getByBorderType(BorderType.BOTTOM).setColor(Color.RED);

 // Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
 CellFormat cellFormat = table.getLastRow().getFirstCell().getCellFormat();
 cellFormat.setWidth(100.0);
 cellFormat.getShading().setBackgroundPatternColor(Color.ORANGE);

 doc.save(getArtifactsDir() + "Table.RowCellFormat.docx");
 
```

Muestra cómo modificar el formato de una celda de tabla.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 // Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
 firstCell.getCellFormat().setWidth(30.0);
 firstCell.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 firstCell.getCellFormat().getShading().setForegroundPatternColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Table.CellFormat.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Restablece el formato predeterminado de la celda. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getBorders()](#getBorders) | Obtiene la colección de bordes de la celda. |
| [getBottomPadding()](#getBottomPadding) | Obtiene la cantidad de espacio (en puntos) para agregar debajo del contenido de la celda. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getFitText()](#getFitText) | Si  true , ajusta el texto en la celda, comprimiendo cada párrafo al ancho de la celda. |
| [getHideMark()](#getHideMark) | Obtiene la visibilidad de la marca de celda. |
| [getHorizontalMerge()](#getHorizontalMerge) | Especifica cómo se combina la celda horizontalmente con otras celdas en la fila. |
| [getLeftPadding()](#getLeftPadding) | Obtiene la cantidad de espacio (en puntos) que se añadirá a la izquierda del contenido de la celda. |
| [getOrientation()](#getOrientation) | Obtiene la orientación del texto en una celda de tabla. |
| [getPreferredWidth()](#getPreferredWidth) | Obtiene el ancho preferido de la celda. |
| [getRightPadding()](#getRightPadding) | Obtiene la cantidad de espacio (en puntos) que se añadirá a la derecha del contenido de la celda. |
| [getShading()](#getShading) | Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado de la celda. |
| [getTopPadding()](#getTopPadding) | Obtiene la cantidad de espacio (en puntos) que se añadirá encima del contenido de la celda. |
| [getVerticalAlignment()](#getVerticalAlignment) | Obtiene la alineación vertical del texto en la celda. |
| [getVerticalMerge()](#getVerticalMerge) | Especifica cómo se combina la celda con otras celdas verticalmente. |
| [getWidth()](#getWidth) | Obtiene el ancho de la celda en puntos. |
| [getWrapText()](#getWrapText) | Si true, ajusta el texto para la celda. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Establece la cantidad de espacio (en puntos) que se añadirá debajo del contenido de la celda. |
| [setFitText(boolean value)](#setFitText-boolean) | Si  true , ajusta el texto en la celda, comprimiendo cada párrafo al ancho de la celda. |
| [setHideMark(boolean value)](#setHideMark-boolean) | Establece la visibilidad de la marca de celda. |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int) | Especifica cómo se combina la celda horizontalmente con otras celdas en la fila. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Establece la cantidad de espacio (en puntos) que se añadirá a la izquierda del contenido de la celda. |
| [setOrientation(int value)](#setOrientation-int) | Establece la orientación del texto en una celda de tabla. |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double) | Establece la cantidad de espacio (en puntos) que se añadirá a la izquierda/arriba/derecha/abajo del contenido de la celda. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth) | Establece el ancho preferido de la celda. |
| [setRightPadding(double value)](#setRightPadding-double) | Establece la cantidad de espacio (en puntos) que se añadirá a la derecha del contenido de la celda. |
| [setTopPadding(double value)](#setTopPadding-double) | Establece la cantidad de espacio (en puntos) que se añadirá encima del contenido de la celda. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Establece la alineación vertical del texto en la celda. |
| [setVerticalMerge(int value)](#setVerticalMerge-int) | Especifica cómo se combina la celda con otras celdas verticalmente. |
| [setWidth(double value)](#setWidth-double) | Obtiene el ancho de la celda en puntos. |
| [setWrapText(boolean value)](#setWrapText-boolean) | Si true, ajusta el texto para la celda. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Restablece el formato de celda predeterminado. No cambia el ancho de la celda.

 **Examples:** 

Muestra cómo combinar las filas de dos tablas en una sola.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtiene la colección de bordes de la celda.

 **Examples:** 

Muestra cómo combinar las filas de dos tablas en una sola.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - Collection of borders of the cell.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Obtiene la cantidad de espacio (en puntos) para agregar debajo del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se añadirá debajo del contenido de la celda.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getFitText() {#getFitText}
```
public boolean getFitText()
```


Si  true , ajusta el texto en la celda, comprimiendo cada párrafo al ancho de la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getHideMark() {#getHideMark}
```
public boolean getHideMark()
```


Obtiene la visibilidad de la marca de celda.

 **Remarks:** 

Especifica que el contenido de la celda de tabla se renderiza sin altura si todas las celdas de la fila están vacías; sin embargo, las celdas tienen una altura visible si poseen bordes de celda, márgenes de celda o espaciado de celda diferentes de cero.

**Returns:**
boolean - Visibilidad de la marca de celda.
### getHorizontalMerge() {#getHorizontalMerge}
```
public int getHorizontalMerge()
```


Especifica cómo se combina la celda horizontalmente con otras celdas en la fila.

 **Examples:** 

Muestra cómo combinar celdas de tabla horizontalmente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of horizontally merged cells.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row. Instead of adding text contents,
 // we will merge this cell with the first cell that we added directly to the left.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.PREVIOUS);
 builder.endRow();

 // Insert two more unmerged cells to the second row.
 builder.getCellFormat().setHorizontalMerge(CellMerge.NONE);
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.HorizontalMerge.docx");
 
```

Imprime el tipo de combinación horizontal y vertical de una celda.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es una de las constantes de [CellMerge](../../com.aspose.words/cellmerge/).
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añadirá a la izquierda del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se debe añadir a la izquierda del contenido de la celda.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Obtiene la orientación del texto en una celda de tabla.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
int - La orientación del texto en una celda de tabla. El valor devuelto es una de las constantes de [TextOrientation](../../com.aspose.words/textorientation/).
### getPreferredWidth() {#getPreferredWidth}
```
public PreferredWidth getPreferredWidth()
```


Obtiene el ancho preferido de la celda.

 **Remarks:** 

El ancho preferido (junto con la opción Auto Fit de la tabla) determina cómo se calcula el ancho real de la celda mediante el algoritmo de diseño de tabla. El diseño de tabla puede ser realizado por Aspose.Words al guardar el documento o por Microsoft Word al mostrar el documento.

El ancho preferido puede especificarse en puntos o en porcentaje. El ancho preferido también puede especificarse como "auto", lo que significa que no se especifica un ancho preferido.

El valor predeterminado es [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Muestra cómo establecer un ancho preferido para las celdas de la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/) - The preferred width of the cell.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añadirá a la derecha del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se debe añadir a la derecha del contenido de la celda.
### getShading() {#getShading}
```
public Shading getShading()
```


Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado de la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo modificar el formato de filas y celdas en una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("City");
 builder.insertCell();
 builder.write("Country");
 builder.endRow();
 builder.insertCell();
 builder.write("London");
 builder.insertCell();
 builder.write("U.K.");
 builder.endTable();

 // Use the first row's "RowFormat" property to modify the formatting
 // of the contents of all cells in this row.
 RowFormat rowFormat = table.getFirstRow().getRowFormat();
 rowFormat.setHeight(25.0);
 rowFormat.getBorders().getByBorderType(BorderType.BOTTOM).setColor(Color.RED);

 // Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
 CellFormat cellFormat = table.getLastRow().getFirstCell().getCellFormat();
 cellFormat.setWidth(100.0);
 cellFormat.getShading().setBackgroundPatternColor(Color.ORANGE);

 doc.save(getArtifactsDir() + "Table.RowCellFormat.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the cell.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Obtiene la cantidad de espacio (en puntos) que se añadirá encima del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - La cantidad de espacio (en puntos) que se debe añadir por encima del contenido de la celda.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Obtiene la alineación vertical del texto en la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Returns:**
int - La alineación vertical del texto en la celda. El valor devuelto es una de las constantes de [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/).
### getVerticalMerge() {#getVerticalMerge}
```
public int getVerticalMerge()
```


Especifica cómo se combina la celda con otras celdas verticalmente.

 **Remarks:** 

Las celdas solo pueden combinarse verticalmente si sus límites izquierdo y derecho son idénticos.

Cuando las celdas se combinan verticalmente, las áreas de visualización de las celdas combinadas se consolidan. El área consolidada se utiliza para mostrar el contenido de la primera celda combinada verticalmente y todas las demás celdas combinadas verticalmente deben estar vacías.

 **Examples:** 

Muestra cómo combinar celdas de tabla verticalmente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Imprime el tipo de combinación horizontal y vertical de una celda.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es una de las constantes de [CellMerge](../../com.aspose.words/cellmerge/).
### getWidth() {#getWidth}
```
public double getWidth()
```


Obtiene el ancho de la celda en puntos.

 **Remarks:** 

El ancho es calculado por Aspose.Words al cargar y guardar el documento. Actualmente, no se admite todas las combinaciones de propiedades de tabla, celda y documento. El valor devuelto puede no ser preciso para algunos documentos. Puede no coincidir exactamente con el ancho de la celda calculado por MS Word cuando el documento se abre en MS Word.

Configurar esta propiedad no es recomendable. No hay garantía de que la celda tenga realmente el ancho establecido. El ancho puede ajustarse para acomodar el contenido de la celda en un diseño de tabla auto-ajustable. Las celdas en otras filas pueden tener configuraciones de ancho conflictivas. La tabla puede redimensionarse para ajustarse al contenedor o para cumplir con las configuraciones de ancho de tabla. Considere usar [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) para establecer el ancho de la celda. Configurar esta propiedad establece [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) implícitamente desde la versión 15.8.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
double - El ancho de la celda en puntos.
### getWrapText() {#getWrapText}
```
public boolean getWrapText()
```


Si true, ajusta el texto para la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añadirá debajo del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir debajo del contenido de la celda. |

### setFitText(boolean value) {#setFitText-boolean}
```
public void setFitText(boolean value)
```


Si  true , ajusta el texto en la celda, comprimiendo cada párrafo al ancho de la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setHideMark(boolean value) {#setHideMark-boolean}
```
public void setHideMark(boolean value)
```


Establece la visibilidad de la marca de celda.

 **Remarks:** 

Especifica que el contenido de la celda de tabla se renderiza sin altura si todas las celdas de la fila están vacías; sin embargo, las celdas tienen una altura visible si poseen bordes de celda, márgenes de celda o espaciado de celda diferentes de cero.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Visibilidad de la marca de celda. |

### setHorizontalMerge(int value) {#setHorizontalMerge-int}
```
public void setHorizontalMerge(int value)
```


Especifica cómo se combina la celda horizontalmente con otras celdas en la fila.

 **Examples:** 

Muestra cómo combinar celdas de tabla horizontalmente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of horizontally merged cells.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row. Instead of adding text contents,
 // we will merge this cell with the first cell that we added directly to the left.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.PREVIOUS);
 builder.endRow();

 // Insert two more unmerged cells to the second row.
 builder.getCellFormat().setHorizontalMerge(CellMerge.NONE);
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.HorizontalMerge.docx");
 
```

Imprime el tipo de combinación horizontal y vertical de una celda.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [CellMerge](../../com.aspose.words/cellmerge/). |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añadirá a la izquierda del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir a la izquierda del contenido de la celda. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Establece la orientación del texto en una celda de tabla.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La orientación del texto en una celda de tabla. El valor debe ser una de las constantes de [TextOrientation](../../com.aspose.words/textorientation/). |

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


Establece la cantidad de espacio (en puntos) que se añadirá a la izquierda/arriba/derecha/abajo del contenido de la celda.

 **Examples:** 

Muestra cómo rellenar el contenido de una celda con espacios en blanco.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a padding distance (in points) between the border and the text contents
 // of each table cell we create with the document builder.
 builder.getCellFormat().setPaddings(5.0, 10.0, 40.0, 50.0);

 // Create a table with one cell whose contents will have whitespace padding.
 builder.startTable();
 builder.insertCell();
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "CellFormat.Padding.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth}
```
public void setPreferredWidth(PreferredWidth value)
```


Establece el ancho preferido de la celda.

 **Remarks:** 

El ancho preferido (junto con la opción Auto Fit de la tabla) determina cómo se calcula el ancho real de la celda mediante el algoritmo de diseño de tabla. El diseño de tabla puede ser realizado por Aspose.Words al guardar el documento o por Microsoft Word al mostrar el documento.

El ancho preferido puede especificarse en puntos o en porcentaje. El ancho preferido también puede especificarse como "auto", lo que significa que no se especifica un ancho preferido.

El valor predeterminado es [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Muestra cómo establecer un ancho preferido para las celdas de la tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth/) | El ancho preferido de la celda. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añadirá a la derecha del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir a la derecha del contenido de la celda. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Establece la cantidad de espacio (en puntos) que se añadirá encima del contenido de la celda.

 **Examples:** 

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio (en puntos) que se debe añadir encima del contenido de la celda. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Establece la alineación vertical del texto en la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La alineación vertical del texto en la celda. El valor debe ser una de las constantes de [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/). |

### setVerticalMerge(int value) {#setVerticalMerge-int}
```
public void setVerticalMerge(int value)
```


Especifica cómo se combina la celda con otras celdas verticalmente.

 **Remarks:** 

Las celdas solo pueden combinarse verticalmente si sus límites izquierdo y derecho son idénticos.

Cuando las celdas se combinan verticalmente, las áreas de visualización de las celdas combinadas se consolidan. El área consolidada se utiliza para mostrar el contenido de la primera celda combinada verticalmente y todas las demás celdas combinadas verticalmente deben estar vacías.

 **Examples:** 

Muestra cómo combinar celdas de tabla verticalmente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Imprime el tipo de combinación horizontal y vertical de una celda.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [CellMerge](../../com.aspose.words/cellmerge/). |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Obtiene el ancho de la celda en puntos.

 **Remarks:** 

El ancho es calculado por Aspose.Words al cargar y guardar el documento. Actualmente, no se admite todas las combinaciones de propiedades de tabla, celda y documento. El valor devuelto puede no ser preciso para algunos documentos. Puede no coincidir exactamente con el ancho de la celda calculado por MS Word cuando el documento se abre en MS Word.

Configurar esta propiedad no es recomendable. No hay garantía de que la celda tenga realmente el ancho establecido. El ancho puede ajustarse para acomodar el contenido de la celda en un diseño de tabla auto-ajustable. Las celdas en otras filas pueden tener configuraciones de ancho conflictivas. La tabla puede redimensionarse para ajustarse al contenedor o para cumplir con las configuraciones de ancho de tabla. Considere usar [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) para establecer el ancho de la celda. Configurar esta propiedad establece [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) implícitamente desde la versión 15.8.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El ancho de la celda en puntos. |

### setWrapText(boolean value) {#setWrapText-boolean}
```
public void setWrapText(boolean value)
```


Si true, ajusta el texto para la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |


---
title: CellFormat
linktitle: CellFormat
second_title: Aspose.Words for Java
description: Represents all formatting for a table cell in Java.
type: docs
weight: 54
url: /java/com.aspose.words/cellformat/
---

**Inheritance:**
java.lang.Object
```
public class CellFormat
```

Represents all formatting for a table cell.

To learn more, visit the [ Working with Tables ][Working with Tables] documentation article.

 **Examples:** 

Shows how to modify formatting of a table cell.

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

Shows how to modify the format of rows and cells in a table.

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

Shows how to build a table with custom borders.

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


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets to default cell formatting. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getBorders()](#getBorders) | Gets collection of borders of the cell. |
| [getBottomPadding()](#getBottomPadding) | Gets the amount of space (in points) to add below the contents of cell. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getFitText()](#getFitText) | If  true , fits text in the cell, compressing each paragraph to the width of the cell. |
| [getHideMark()](#getHideMark) | Gets visibility of cell mark. |
| [getHorizontalMerge()](#getHorizontalMerge) | Specifies how the cell is merged horizontally with other cells in the row. |
| [getLeftPadding()](#getLeftPadding) | Gets the amount of space (in points) to add to the left of the contents of cell. |
| [getOrientation()](#getOrientation) | Gets the orientation of text in a table cell. |
| [getPreferredWidth()](#getPreferredWidth) | Gets the preferred width of the cell. |
| [getRightPadding()](#getRightPadding) | Gets the amount of space (in points) to add to the right of the contents of cell. |
| [getShading()](#getShading) | Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the cell. |
| [getTopPadding()](#getTopPadding) | Gets the amount of space (in points) to add above the contents of cell. |
| [getVerticalAlignment()](#getVerticalAlignment) | Gets the vertical alignment of text in the cell. |
| [getVerticalMerge()](#getVerticalMerge) | Specifies how the cell is merged with other cells vertically. |
| [getWidth()](#getWidth) | Gets the width of the cell in points. |
| [getWrapText()](#getWrapText) | If  true , wrap text for the cell. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Sets the amount of space (in points) to add below the contents of cell. |
| [setFitText(boolean value)](#setFitText-boolean) | If  true , fits text in the cell, compressing each paragraph to the width of the cell. |
| [setHideMark(boolean value)](#setHideMark-boolean) | Sets visibility of cell mark. |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int) | Specifies how the cell is merged horizontally with other cells in the row. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Sets the amount of space (in points) to add to the left of the contents of cell. |
| [setOrientation(int value)](#setOrientation-int) | Sets the orientation of text in a table cell. |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth) | Sets the preferred width of the cell. |
| [setRightPadding(double value)](#setRightPadding-double) | Sets the amount of space (in points) to add to the right of the contents of cell. |
| [setTopPadding(double value)](#setTopPadding-double) | Sets the amount of space (in points) to add above the contents of cell. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Sets the vertical alignment of text in the cell. |
| [setVerticalMerge(int value)](#setVerticalMerge-int) | Specifies how the cell is merged with other cells vertically. |
| [setWidth(double value)](#setWidth-double) | Gets the width of the cell in points. |
| [setWrapText(boolean value)](#setWrapText-boolean) | If  true , wrap text for the cell. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets to default cell formatting. Does not change the width of the cell.

 **Examples:** 

Shows how to combine the rows from two tables into one.

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
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gets collection of borders of the cell.

 **Examples:** 

Shows how to combine the rows from two tables into one.

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


Gets the amount of space (in points) to add below the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
double - The amount of space (in points) to add below the contents of cell.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getFitText() {#getFitText}
```
public boolean getFitText()
```


If  true , fits text in the cell, compressing each paragraph to the width of the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
boolean - The corresponding  boolean  value.
### getHideMark() {#getHideMark}
```
public boolean getHideMark()
```


Gets visibility of cell mark.

 **Remarks:** 

Specifies that table cell content is rendered with no height if all cells in the row are empty; however, cells have a visible height if they have nonzero cell borders, cell margins, or cell spacing.

**Returns:**
boolean - Visibility of cell mark.
### getHorizontalMerge() {#getHorizontalMerge}
```
public int getHorizontalMerge()
```


Specifies how the cell is merged horizontally with other cells in the row.

 **Examples:** 

Shows how to merge table cells horizontally.

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

Prints the horizontal and vertical merge type of a cell.

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
int - The corresponding  int  value. The returned value is one of [CellMerge](../../com.aspose.words/cellmerge/) constants.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
double - The amount of space (in points) to add to the left of the contents of cell.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Gets the orientation of text in a table cell.

 **Examples:** 

Shows how to build a table with custom borders.

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

Shows how to build a formatted 2x2 table.

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
int - The orientation of text in a table cell. The returned value is one of [TextOrientation](../../com.aspose.words/textorientation/) constants.
### getPreferredWidth() {#getPreferredWidth}
```
public PreferredWidth getPreferredWidth()
```


Gets the preferred width of the cell.

 **Remarks:** 

The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. Table layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Shows how to set a preferred width for table cells.

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


Gets the amount of space (in points) to add to the right of the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
double - The amount of space (in points) to add to the right of the contents of cell.
### getShading() {#getShading}
```
public Shading getShading()
```


Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the cell.

 **Examples:** 

Shows how to modify the format of rows and cells in a table.

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

Shows how to build a table with custom borders.

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
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the cell.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
double - The amount of space (in points) to add above the contents of cell.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Gets the vertical alignment of text in the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
int - The vertical alignment of text in the cell. The returned value is one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) constants.
### getVerticalMerge() {#getVerticalMerge}
```
public int getVerticalMerge()
```


Specifies how the cell is merged with other cells vertically.

 **Remarks:** 

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated. The consolidated area is used to display the contents of the first vertically merged cell and all other vertically merged cells must be empty.

 **Examples:** 

Shows how to merge table cells vertically.

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

Prints the horizontal and vertical merge type of a cell.

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
int - The corresponding  int  value. The returned value is one of [CellMerge](../../com.aspose.words/cellmerge/) constants.
### getWidth() {#getWidth}
```
public double getWidth()
```


Gets the width of the cell in points.

 **Remarks:** 

The width is calculated by Aspose.Words on document loading and saving. Currently, not every combination of table, cell and document properties is supported. The returned value may not be accurate for some documents. It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended. There is no guarantee that the cell will actually have the set width. The width may be adjusted to accommodate cell contents in an auto-fit table layout. Cells in other rows may have conflicting width settings. The table may be resized to fit into the container or to meet table width settings. Consider using [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) for setting the cell width. Setting this property sets [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) implicitly since version 15.8.

 **Examples:** 

Shows how to build a table with custom borders.

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

Shows how to format cells with a document builder.

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
double - The width of the cell in points.
### getWrapText() {#getWrapText}
```
public boolean getWrapText()
```


If  true , wrap text for the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
boolean - The corresponding  boolean  value.
### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of cell. |

### setFitText(boolean value) {#setFitText-boolean}
```
public void setFitText(boolean value)
```


If  true , fits text in the cell, compressing each paragraph to the width of the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setHideMark(boolean value) {#setHideMark-boolean}
```
public void setHideMark(boolean value)
```


Sets visibility of cell mark.

 **Remarks:** 

Specifies that table cell content is rendered with no height if all cells in the row are empty; however, cells have a visible height if they have nonzero cell borders, cell margins, or cell spacing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Visibility of cell mark. |

### setHorizontalMerge(int value) {#setHorizontalMerge-int}
```
public void setHorizontalMerge(int value)
```


Specifies how the cell is merged horizontally with other cells in the row.

 **Examples:** 

Shows how to merge table cells horizontally.

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

Prints the horizontal and vertical merge type of a cell.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CellMerge](../../com.aspose.words/cellmerge/) constants. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of cell. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Sets the orientation of text in a table cell.

 **Examples:** 

Shows how to build a table with custom borders.

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

Shows how to build a formatted 2x2 table.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The orientation of text in a table cell. The value must be one of [TextOrientation](../../com.aspose.words/textorientation/) constants. |

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.

 **Examples:** 

Shows how to pad the contents of a cell with whitespace.

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
| Parameter | Type | Description |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth}
```
public void setPreferredWidth(PreferredWidth value)
```


Sets the preferred width of the cell.

 **Remarks:** 

The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. Table layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Shows how to set a preferred width for table cells.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth/) | The preferred width of the cell. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of cell. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of cell.

 **Examples:** 

Shows how to format cells with a document builder.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of cell. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Sets the vertical alignment of text in the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The vertical alignment of text in the cell. The value must be one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) constants. |

### setVerticalMerge(int value) {#setVerticalMerge-int}
```
public void setVerticalMerge(int value)
```


Specifies how the cell is merged with other cells vertically.

 **Remarks:** 

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated. The consolidated area is used to display the contents of the first vertically merged cell and all other vertically merged cells must be empty.

 **Examples:** 

Shows how to merge table cells vertically.

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

Prints the horizontal and vertical merge type of a cell.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CellMerge](../../com.aspose.words/cellmerge/) constants. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Gets the width of the cell in points.

 **Remarks:** 

The width is calculated by Aspose.Words on document loading and saving. Currently, not every combination of table, cell and document properties is supported. The returned value may not be accurate for some documents. It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended. There is no guarantee that the cell will actually have the set width. The width may be adjusted to accommodate cell contents in an auto-fit table layout. Cells in other rows may have conflicting width settings. The table may be resized to fit into the container or to meet table width settings. Consider using [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) for setting the cell width. Setting this property sets [getPreferredWidth()](../../com.aspose.words/cellformat/\#getPreferredWidth) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat/\#setPreferredWidth-com.aspose.words.PreferredWidth) implicitly since version 15.8.

 **Examples:** 

Shows how to build a table with custom borders.

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

Shows how to format cells with a document builder.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the cell in points. |

### setWrapText(boolean value) {#setWrapText-boolean}
```
public void setWrapText(boolean value)
```


If  true , wrap text for the cell.

 **Examples:** 

Shows how to build a table with custom borders.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |


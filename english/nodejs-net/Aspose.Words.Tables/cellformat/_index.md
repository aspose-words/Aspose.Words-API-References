---
title: CellFormat class
linktitle: CellFormat class
articleTitle: CellFormat class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.CellFormat class. Represents all formatting for a table cell"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Tables/cellformat/
---

## CellFormat class

Represents all formatting for a table cell.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [borders](./borders/) | Gets collection of borders of the cell. |
| [bottomPadding](./bottomPadding/) | Returns or sets the amount of space (in points) to add below the contents of cell. |
| [fitText](./fitText/) | If ``True``, fits text in the cell, compressing each paragraph to the width of the cell. |
| [hideMark](./hideMark/) | Returns or sets visibility of cell mark. |
| [horizontalMerge](./horizontalMerge/) | Specifies how the cell is merged horizontally with other cells in the row. |
| [leftPadding](./leftPadding/) | Returns or sets the amount of space (in points) to add to the left of the contents of cell. |
| [orientation](./orientation/) | Returns or sets the orientation of text in a table cell. |
| [preferredWidth](./preferredWidth/) | Returns or sets the preferred width of the cell. |
| [rightPadding](./rightPadding/) | Returns or sets the amount of space (in points) to add to the right of the contents of cell. |
| [shading](./shading/) | Returns a [Shading](../../aspose.words/shading/) object that refers to the shading formatting for the cell. |
| [topPadding](./topPadding/) | Returns or sets the amount of space (in points) to add above the contents of cell. |
| [verticalAlignment](./verticalAlignment/) | Returns or sets the vertical alignment of text in the cell. |
| [verticalMerge](./verticalMerge/) | Specifies how the cell is merged with other cells vertically. |
| [width](./width/) | Gets the width of the cell in points. |
| [wrapText](./wrapText/) | If ``True``, wrap text for the cell. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets to default cell formatting. Does not change the width of the cell. |
|[ setPaddings(leftPadding, topPadding, rightPadding, bottomPadding)](./setPaddings/#number_number_number_number) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |

### Examples

Shows how to modify the format of rows and cells in a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
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
let rowFormat = table.firstRow.rowFormat;
rowFormat.height = 25;
rowFormat.borders.at(aw.BorderType.Bottom).color = "#FF0000";

// Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
let cellFormat = table.lastRow.firstCell.cellFormat;
cellFormat.width = 100;
cellFormat.shading.backgroundPatternColor = "#FFA500";

doc.save(base.artifactsDir + "Table.RowCellFormat.docx");
```

Shows how to modify formatting of a table cell.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);
let firstCell = table.firstRow.firstCell;

// Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
firstCell.cellFormat.width = 30;
firstCell.cellFormat.orientation = aw.TextOrientation.Downward;
firstCell.cellFormat.shading.foregroundPatternColor = "#90EE90";

doc.save(base.artifactsDir + "Table.cellFormat.docx");
```

Shows how to build a table with custom borders.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

builder.cellFormat.clearFormatting();
builder.cellFormat.width = 150;
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.cellFormat.shading.backgroundPatternColor = "#ADFF2F";
builder.cellFormat.wrapText = false;
builder.cellFormat.fitText = true;

builder.rowFormat.clearFormatting();
builder.rowFormat.heightRule = aw.HeightRule.Exactly;
builder.rowFormat.height = 50;
builder.rowFormat.borders.lineStyle = aw.LineStyle.Engrave3D;
builder.rowFormat.borders.color = "#FFA500";

builder.insertCell();
builder.write("Row 1, Col 1");

builder.insertCell();
builder.write("Row 1, Col 2");
builder.endRow();

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder.cellFormat.shading.clearFormatting();

builder.insertCell();
builder.write("Row 2, Col 1");

builder.insertCell();
builder.write("Row 2, Col 2");

builder.endRow();

// Increase row height to fit the vertical text.
builder.insertCell();
builder.rowFormat.height = 150;
builder.cellFormat.orientation = aw.TextOrientation.Upward;
builder.write("Row 3, Col 1");

builder.insertCell();
builder.cellFormat.orientation = aw.TextOrientation.Downward;
builder.write("Row 3, Col 2");

builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "DocumentBuilder.InsertTable.docx");
```

### See Also

* module [Aspose.Words.Tables](../)


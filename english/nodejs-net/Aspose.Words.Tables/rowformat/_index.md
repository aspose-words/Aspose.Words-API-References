---
title: RowFormat class
linktitle: RowFormat class
articleTitle: RowFormat class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.RowFormat class. Represents all formatting for a table row"
type: docs
weight: 110
url: /nodejs-net/Aspose.Words.Tables/rowformat/
---

## RowFormat class

Represents all formatting for a table row.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [allowBreakAcrossPages](./allowBreakAcrossPages/) | True if the text in a table row is allowed to split across a page break. |
| [borders](./borders/) | Gets the collection of default cell borders for the row. |
| [headingFormat](./headingFormat/) | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [height](./height/) | Gets or sets the height of the table row in points. |
| [heightRule](./heightRule/) | Gets or sets the rule for determining the height of the table row. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets to default row formatting. |

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

Shows how to modify formatting of a table row.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);

// Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
let firstRow = table.firstRow;
firstRow.rowFormat.borders.lineStyle = aw.LineStyle.None;
firstRow.rowFormat.heightRule = aw.HeightRule.Auto;
firstRow.rowFormat.allowBreakAcrossPages = true;

doc.save(base.artifactsDir + "Table.rowFormat.docx");
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


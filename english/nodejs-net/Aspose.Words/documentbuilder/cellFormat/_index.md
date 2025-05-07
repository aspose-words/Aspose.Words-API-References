---
title: DocumentBuilder.cellFormat property
linktitle: cellFormat property
articleTitle: cellFormat property
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.cellFormat property. Returns an object that represents current table cell formatting properties."
type: docs
weight: 30
url: /nodejs-net/aspose.words/documentbuilder/cellFormat/
---

## DocumentBuilder.cellFormat property

Returns an object that represents current table cell formatting properties.


```js
get cellFormat(): Aspose.Words.Tables.CellFormat
```

### Examples

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

Shows how to build a formatted 2x2 table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.write("Row 1, cell 1.");
builder.insertCell();
builder.write("Row 1, cell 2.");
builder.endRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
expect(table.rows.at(0).cells.at(0).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);
expect(table.rows.at(0).cells.at(1).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);

builder.insertCell();
builder.rowFormat.height = 100;
builder.rowFormat.heightRule = aw.HeightRule.Exactly;
builder.cellFormat.orientation = aw.TextOrientation.Upward;
builder.write("Row 2, cell 1.");
builder.insertCell();
builder.cellFormat.orientation = aw.TextOrientation.Downward;
builder.write("Row 2, cell 2.");
builder.endRow();
builder.endTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
expect(table.rows.at(0).rowFormat.height).toEqual(0);
expect(table.rows.at(0).rowFormat.heightRule).toEqual(aw.HeightRule.Auto);
expect(table.rows.at(1).rowFormat.height).toEqual(100);
expect(table.rows.at(1).rowFormat.heightRule).toEqual(aw.HeightRule.Exactly);
expect(table.rows.at(1).cells.at(0).cellFormat.orientation).toEqual(aw.TextOrientation.Upward);
expect(table.rows.at(1).cells.at(1).cellFormat.orientation).toEqual(aw.TextOrientation.Downward);

doc.save(base.artifactsDir + "DocumentBuilder.BuildTable.docx");
```

Shows how to format cells with a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1.");

// Insert a second cell, and then configure cell text padding options.
// The builder will apply these settings at its current cell, and any new cells creates afterwards.
builder.insertCell();

let cellFormat = builder.cellFormat;
cellFormat.width = 250;
cellFormat.leftPadding = 30;
cellFormat.rightPadding = 30;
cellFormat.topPadding = 30;
cellFormat.bottomPadding = 30;

builder.write("Row 1, cell 2.");
builder.endRow();
builder.endTable();

let cells = table.firstRow.cells.toArray();
// The first cell was unaffected by the padding reconfiguration, and still holds the default values.
expect(cells.at(0).cellFormat.width).toEqual(0.0);
expect(cells.at(0).cellFormat.leftPadding).toEqual(5.4);
expect(cells.at(0).cellFormat.rightPadding).toEqual(5.4);
expect(cells.at(0).cellFormat.topPadding).toEqual(0.0);
expect(cells.at(0).cellFormat.bottomPadding).toEqual(0.0);

expect(cells.at(1).cellFormat.width).toEqual(250.0);
expect(cells.at(1).cellFormat.leftPadding).toEqual(30.0);
expect(cells.at(1).cellFormat.rightPadding).toEqual(30.0);
expect(cells.at(1).cellFormat.topPadding).toEqual(30.0);
expect(cells.at(1).cellFormat.bottomPadding).toEqual(30.0);

// The first cell will still grow in the output document to match the size of its neighboring cell.
doc.save(base.artifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)


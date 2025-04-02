---
title: CellFormat.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for NodeJs
description: "CellFormat.width property. Gets the width of the cell in points."
type: docs
weight: 140
url: /nodejs-net/Aspose.Words.Tables/cellformat/width/
---

## CellFormat.width property

Gets the width of the cell in points.


```js
get width(): number
```

### Remarks

The width is calculated by Aspose.Words on document loading and saving.
Currently, not every combination of table, cell and document properties is supported.
The returned value may not be accurate for some documents.
It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended.
There is no guarantee that the cell will actually have the set width.
The width may be adjusted to accommodate cell contents in an auto-fit table layout.
Cells in other rows may have conflicting width settings.
The table may be resized to fit into the container or to meet table width settings.
Consider using [CellFormat.preferredWidth](../preferredWidth/) for setting the cell width.
Setting this property sets [CellFormat.preferredWidth](../preferredWidth/) implicitly since version 15.8.





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

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)
* property [CellFormat.preferredWidth](../preferredWidth/)


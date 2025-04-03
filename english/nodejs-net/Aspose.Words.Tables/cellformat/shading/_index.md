---
title: CellFormat.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for NodeJs
description: "CellFormat.shading property. Returns a [Shading](../../../aspose.words/shading/) object that refers to the shading formatting for the cell."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Tables/cellformat/shading/
---

## CellFormat.shading property

Returns a [Shading](../../../aspose.words/shading/) object that refers to the shading formatting for the cell.



```js
get shading(): Aspose.Words.Shading
```

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

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)


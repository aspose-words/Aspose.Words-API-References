---
title: DocumentBuilder.write method
linktitle: write method
articleTitle: write method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.write method. Inserts a string into the document at the current insert position."
type: docs
weight: 690
url: /nodejs-net/Aspose.Words/documentbuilder/write/
---

## write(text) {#string}

Inserts a string into the document at the current insert position.


```js
write(text: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | The string to insert into the document. |

### Remarks

Current font formatting specified by the [DocumentBuilder.font](../font/) property is used.



### Examples

Shows how to insert a string surrounded by a border into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.write("Text surrounded by green border.");

doc.save(base.artifactsDir + "Border.FontBorder.docx");
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

Shows how to use a document builder to create a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Start the table, then populate the first row with two cells.
builder.startTable();
builder.insertCell();
builder.write("Row 1, Cell 1.");
builder.insertCell();
builder.write("Row 1, Cell 2.");

// Call the builder's "EndRow" method to start a new row.
builder.endRow();
builder.insertCell();
builder.write("Row 2, Cell 1.");
builder.insertCell();
builder.write("Row 2, Cell 2.");
builder.endTable();

doc.save(base.artifactsDir + "DocumentBuilder.CreateTable.docx");
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

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)


---
title: RowFormat.heightRule property
linktitle: heightRule property
articleTitle: heightRule property
second_title: Aspose.Words for Node.js
description: "RowFormat.heightRule property. Gets or sets the rule for determining the height of the table row."
type: docs
weight: 50
url: /nodejs-net/aspose.words.tables/rowformat/heightRule/
---

## RowFormat.heightRule property

Gets or sets the rule for determining the height of the table row.


```js
get heightRule(): Aspose.Words.HeightRule
```

### Examples

Shows how to create a formatted table using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
table.leftIndent = 20;

// Set some formatting options for text and table appearance.
builder.rowFormat.height = 40;
builder.rowFormat.heightRule = aw.HeightRule.AtLeast;
builder.cellFormat.shading.backgroundPatternColor = "#C6D9F1";

builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.font.size = 16;
builder.font.name = "Arial";
builder.font.bold = true;

// Configuring the formatting options in a document builder will apply them
// to the current cell/row its cursor is in,
// as well as any new cells and rows created using that builder.
builder.write("Header Row,\n Cell 1");
builder.insertCell();
builder.write("Header Row,\n Cell 2");
builder.insertCell();
builder.write("Header Row,\n Cell 3");
builder.endRow();

// Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
// The builder will not apply these to the first row already created so that it will stand out as a header row.
builder.cellFormat.shading.backgroundPatternColor = "#FFFFFF";
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.rowFormat.height = 30;
builder.rowFormat.heightRule = aw.HeightRule.Auto;
builder.insertCell();
builder.font.size = 12;
builder.font.bold = false;

builder.write("Row 1, Cell 1.");
builder.insertCell();
builder.write("Row 1, Cell 2.");
builder.insertCell();
builder.write("Row 1, Cell 3.");
builder.endRow();
builder.insertCell();
builder.write("Row 2, Cell 1.");
builder.insertCell();
builder.write("Row 2, Cell 2.");
builder.insertCell();
builder.write("Row 2, Cell 3.");
builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

Shows how to format rows with a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1.");

// Start a second row, and then configure its height. The builder will apply these settings to
// its current row, as well as any new rows it creates afterwards.
builder.endRow();

let rowFormat = builder.rowFormat;
rowFormat.height = 100;
rowFormat.heightRule = aw.HeightRule.Exactly;

builder.insertCell();
builder.write("Row 2, cell 1.");
builder.endTable();

// The first row was unaffected by the padding reconfiguration and still holds the default values.
expect(table.rows.at(0).rowFormat.height).toEqual(0.0);
expect(table.rows.at(0).rowFormat.heightRule).toEqual(aw.HeightRule.Auto);

expect(table.rows.at(1).rowFormat.height).toEqual(100.0);
expect(table.rows.at(1).rowFormat.heightRule).toEqual(aw.HeightRule.Exactly);

doc.save(base.artifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [RowFormat](../)


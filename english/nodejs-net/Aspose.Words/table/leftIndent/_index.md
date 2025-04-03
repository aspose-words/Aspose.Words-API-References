---
title: Table.leftIndent property
linktitle: leftIndent property
articleTitle: leftIndent property
second_title: Aspose.Words for NodeJs
description: "Table.leftIndent property. Gets or sets the value that represents the left indent of the table."
type: docs
weight: 190
url: /nodejs-net/aspose.words/table/leftIndent/
---

## Table.leftIndent property

Gets or sets the value that represents the left indent of the table.


```js
get leftIndent(): number
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

### See Also

* module [Aspose.Words](../../)
* class [Table](../)


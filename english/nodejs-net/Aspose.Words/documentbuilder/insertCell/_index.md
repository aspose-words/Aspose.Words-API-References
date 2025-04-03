---
title: DocumentBuilder.insertCell method
linktitle: insertCell method
articleTitle: insertCell method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.insertCell method. Inserts a table cell into the document."
type: docs
weight: 270
url: /nodejs-net/aspose.words/documentbuilder/insertCell/
---

## insertCell() {#default}

Inserts a table cell into the document.


```js
insertCell()
```

### Remarks

To start a table, just call [DocumentBuilder.insertCell()](./#default). After this, any content you add using
other methods of the [DocumentBuilder](../) class will be added to the current cell.

To start a new cell in the same row, call [DocumentBuilder.insertCell()](./#default) again.

To end a table row call [DocumentBuilder.endRow()](../endRow/#default).

Use the [DocumentBuilder.cellFormat](../cellFormat/) property to specify cell formatting.




### Returns

The cell node that was just inserted.


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

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)


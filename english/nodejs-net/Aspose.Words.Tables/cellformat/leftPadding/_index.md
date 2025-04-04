---
title: CellFormat.leftPadding property
linktitle: leftPadding property
articleTitle: leftPadding property
second_title: Aspose.Words for Node.js
description: "CellFormat.leftPadding property. Returns or sets the amount of space (in points) to add to the left of the contents of cell."
type: docs
weight: 60
url: /nodejs-net/aspose.words.tables/cellformat/leftPadding/
---

## CellFormat.leftPadding property

Returns or sets the amount of space (in points) to add to the left of the contents of cell.


```js
get leftPadding(): number
```

### Examples

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


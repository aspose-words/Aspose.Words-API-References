---
title: Row.rowFormat property
linktitle: rowFormat property
articleTitle: rowFormat property
second_title: Aspose.Words for Node.js
description: "Row.rowFormat property. Provides access to the formatting properties of the row."
type: docs
weight: 110
url: /nodejs-net/aspose.words.tables/row/rowFormat/
---

## Row.rowFormat property

Provides access to the formatting properties of the row.


```js
get rowFormat(): Aspose.Words.Tables.RowFormat
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

### See Also

* module [Aspose.Words.Tables](../../)
* class [Row](../)


---
title: Cell.cellFormat property
linktitle: cellFormat property
articleTitle: cellFormat property
second_title: Aspose.Words for NodeJs
description: "Cell.cellFormat property. Provides access to the formatting properties of the cell."
type: docs
weight: 20
url: /nodejs-net/aspose.words.tables/cell/cellFormat/
---

## Cell.cellFormat property

Provides access to the formatting properties of the cell.


```js
get cellFormat(): Aspose.Words.Tables.CellFormat
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

Shows how to modify formatting of a table cell.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);
let firstCell = table.firstRow.firstCell;

// Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
firstCell.cellFormat.width = 30;
firstCell.cellFormat.orientation = aw.TextOrientation.Downward;
firstCell.cellFormat.shading.foregroundPatternColor = "#90EE90";

doc.save(base.artifactsDir + "Table.cellFormat.docx");
```

Shows how to combine the rows from two tables into one.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
let firstTable = doc.firstSection.body.tables.at(0);

// 2 -  Using the "GetChild" method:
let secondTable = doc.getTable(1, true);

// Append all rows from the current table to the next.
while (secondTable.hasChildNodes)
  firstTable.rows.add(secondTable.firstRow);

// Remove the empty table container.
secondTable.remove();

doc.save(base.artifactsDir + "Table.CombineTables.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [Cell](../)


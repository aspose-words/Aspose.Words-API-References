---
title: AutoFitBehavior enumeration
linktitle: AutoFitBehavior enumeration
articleTitle: AutoFitBehavior enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Tables.AutoFitBehavior enumeration. Determines how Aspose.Words resizes the table when you invoke the [Table.autoFit()](../../aspose.words/table/autoFit/#autofitbehavior) method."
type: docs
weight: 10
url: /nodejs-net/aspose.words.tables/autofitbehavior/
---

## AutoFitBehavior enumeration

Determines how Aspose.Words resizes the table when you invoke the [Table.autoFit()](../../aspose.words/table/autoFit/#autofitbehavior) method.



### Members

| Name | Description |
| --- | --- |
| AutoFitToContents | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout. |
| AutoFitToWindow | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%,  removes preferred widths from all cells and then updates the table layout. |
| FixedColumnWidths | Aspose.Words disables the AutoFit option and removes the preferred with from the table. |

### Examples

Shows how to build a new table while applying a style.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let table = builder.startTable();

// We must insert at least one row before setting any table formatting.
builder.insertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table.styleIdentifier = aw.StyleIdentifier.MediumShading1Accent1;

// Partially apply the style to features of the table based on predicates, then build the table.
table.styleOptions =
  aw.Tables.TableStyleOptions.FirstColumn | aw.Tables.TableStyleOptions.RowBands | aw.Tables.TableStyleOptions.FirstRow;
table.autoFit(aw.Tables.AutoFitBehavior.AutoFitToContents);

builder.writeln("Item");
builder.cellFormat.rightPadding = 40;
builder.insertCell();
builder.writeln("Quantity (kg)");
builder.endRow();

builder.insertCell();
builder.writeln("Apples");
builder.insertCell();
builder.writeln("20");
builder.endRow();

builder.insertCell();
builder.writeln("Bananas");
builder.insertCell();
builder.writeln("40");
builder.endRow();

builder.insertCell();
builder.writeln("Carrots");
builder.insertCell();
builder.writeln("50");
builder.endRow();

doc.save(base.artifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
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

* module [Aspose.Words.Tables](../)

